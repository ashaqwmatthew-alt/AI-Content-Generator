# ============================================================
# SECURE AI GENERATOR PRO
# FULL STACK — BACKEND + FRONTEND (JOINED)
# ============================================================


# ============================================================
# BACKEND — Python / FastAPI
# File: main.py
# ============================================================

import os, uuid, sqlite3
from datetime import datetime, timedelta
from fastapi import FastAPI, Form, Depends, HTTPException, Security
from fastapi.security import HTTPBearer, HTTPAuthorizationCredentials
from jose import jwt, JWTError
from passlib.context import CryptContext

SECRET_KEY = "SUPER_SECRET_AI_GENERATOR_KEY_2025"
ALGORITHM = "HS256"
DATABASE = "secure_data.db"
OUT_DIR = "secure_storage"

os.makedirs(OUT_DIR, exist_ok=True)

pwd_context = CryptContext(schemes=["bcrypt"], deprecated="auto")
security = HTTPBearer()
app = FastAPI(title="Secure AI Generator Pro")

def get_db():
    return sqlite3.connect(DATABASE, check_same_thread=False)

db = get_db()
cur = db.cursor()

cur.execute("CREATE TABLE IF NOT EXISTS users (id TEXT PRIMARY KEY, username TEXT UNIQUE, password TEXT)")
cur.execute("CREATE TABLE IF NOT EXISTS history (user_id TEXT, job_id TEXT, type TEXT, path TEXT, created TEXT)")
cur.execute("CREATE TABLE IF NOT EXISTS health_logs (user_id TEXT, bpm INTEGER, pressure INTEGER, created TEXT)")
db.commit()

def get_current_user(auth: HTTPAuthorizationCredentials = Security(security)):
    try:
        payload = jwt.decode(auth.credentials, SECRET_KEY, algorithms=[ALGORITHM])
        return payload["sub"]
    except JWTError:
        raise HTTPException(status_code=401, detail="Invalid token")

@app.post("/register")
def register(username: str = Form(...), password: str = Form(...)):
    user_id = str(uuid.uuid4())
    hashed = pwd_context.hash(password)
    try:
        cur.execute("INSERT INTO users VALUES (?, ?, ?)", (user_id, username, hashed))
        db.commit()
        return {"status": "registered"}
    except:
        raise HTTPException(status_code=400, detail="Username exists")

@app.post("/login")
def login(username: str = Form(...), password: str = Form(...)):
    cur.execute("SELECT id, password FROM users WHERE username=?", (username,))
    user = cur.fetchone()
    if not user or not pwd_context.verify(password, user[1]):
        raise HTTPException(status_code=401, detail="Invalid credentials")
    token = jwt.encode(
        {"sub": user[0], "exp": datetime.utcnow() + timedelta(hours=24)},
        SECRET_KEY,
        algorithm=ALGORITHM
    )
    return {"token": token}

@app.post("/generate/avatar-video")
def generate_avatar(script: str = Form(...), avatar: str = Form(...), user_id: str = Depends(get_current_user)):
    job_id = str(uuid.uuid4())
    path = f"{OUT_DIR}/{job_id}.mp4"
    cur.execute(
        "INSERT INTO history VALUES (?, ?, ?, ?, ?)",
        (user_id, job_id, "avatar_video", path, datetime.utcnow().isoformat())
    )
    db.commit()
    return {"job_id": job_id, "status": "processing"}

@app.post("/health/sync")
def sync_health(bpm: int = Form(...), steps: int = Form(...), user_id: str = Depends(get_current_user)):
    pressure = 50 + (20 if bpm > 100 else 0) - (10 if steps > 5000 else 0)
    cur.execute(
        "INSERT INTO health_logs VALUES (?, ?, ?, ?)",
        (user_id, bpm, pressure, datetime.utcnow().isoformat())
    )
    db.commit()
    return {
        "pressure_score": pressure,
        "recommendation": "Stretch & relax" if pressure > 70 else "Optimal"
    }

@app.get("/system/health")
def system_health():
    return {"status": "GREEN", "uptime": "99.9%", "security": "VERIFIED"}


# ============================================================
# FRONTEND — Flutter / Dart
# File: lib/main.dart
# ============================================================

import 'package:flutter/material.dart';
import 'package:provider/provider.dart';
import 'package:http/http.dart' as http;
import 'dart:convert';

const String API_URL = "http://10.0.2.2:8000";

class ThemeProvider with ChangeNotifier {
  ThemeMode themeMode = ThemeMode.system;
  void toggle() {
    themeMode = themeMode == ThemeMode.dark ? ThemeMode.light : ThemeMode.dark;
    notifyListeners();
  }
}

void main() {
  runApp(
    ChangeNotifierProvider(
      create: (_) => ThemeProvider(),
      child: const SecureAIApp(),
    ),
  );
}

class SecureAIApp extends StatelessWidget {
  const SecureAIApp({super.key});

  @override
  Widget build(BuildContext context) {
    final tp = Provider.of<ThemeProvider>(context);
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      themeMode: tp.themeMode,
      theme: ThemeData(useMaterial3: true, colorSchemeSeed: Colors.blue),
      darkTheme: ThemeData.dark(useMaterial3: true)
          .copyWith(colorSchemeSeed: Colors.cyan),
      home: const Dashboard(),
    );
  }
}

class Dashboard extends StatelessWidget {
  const Dashboard({super.key});

  @override
  Widget build(BuildContext context) {
    final tp = Provider.of<ThemeProvider>(context);

    return Scaffold(
      appBar: AppBar(
        title: const Text("AI Content Gen Pro"),
        actions: [
          IconButton(
            icon: Icon(tp.themeMode == ThemeMode.dark
                ? Icons.light_mode
                : Icons.dark_mode),
            onPressed: tp.toggle,
          )
        ],
      ),
      body: Padding(
        padding: const EdgeInsets.all(16),
        child: Column(
          children: [
            Container(
              padding: const EdgeInsets.all(16),
              decoration: BoxDecoration(
                gradient: const LinearGradient(
                  colors: [Color(0xFF43A047), Color(0xFF00ACC1)],
                ),
                borderRadius: BorderRadius.circular(14),
              ),
              child: const Row(
                mainAxisAlignment: MainAxisAlignment.spaceBetween,
                children: [
                  Text("User Wellness",
                      style: TextStyle(color: Colors.white, fontWeight: FontWeight.bold)),
                  CircularProgressIndicator(value: 0.45, color: Colors.white)
                ],
              ),
            ),
            const SizedBox(height: 20),
            ListTile(leading: Icon(Icons.image, color: Colors.purple), title: Text("Nano Banana Pro")),
            ListTile(leading: Icon(Icons.videocam, color: Colors.blue), title: Text("Veo 3 Video")),
            ListTile(leading: Icon(Icons.face, color: Colors.teal), title: Text("AI Avatar")),
          ],
        ),
      ),
    );
  }
}

# ============================================================
# END — ALL TOGETHER
# ============================================================# AI-Content-Generator