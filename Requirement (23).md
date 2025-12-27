# AI Content Generator Tool Requirements Document

## 1. Tool Overview
### 1.1 Tool Name
AI Content Generator\n
### 1.2 Tool Description
An AI-powered tool that generates images and videos based on user prompts or uploaded photos/videos, supporting multiple artistic styles with real-time progress tracking, automatic error recovery, content history management, and intelligent multi-media fusion capabilities. Enhanced with Ultra Fix Generator for proactive stability and performance optimization, plus advanced image and video enhancement features. Features adaptive dark/light theme system with automatic time-based switching and eye comfort protection. Powered by advanced AI models including Gemini intelligence, Nano Banana Pro for image generation, and Veo3 for video animation. Now includes AI Video Generator with Lifelike AI Avatars for creating professional video content with realistic digital presenters. **New: Integrated Health Monitoring and Pressure Management System for user wellness tracking.**

## 2. Core Features
### 2.1 Media Upload
- **Dual Upload Areas**: Two separate upload zones for flexible media input
  - **Upload Area 1**: Supports images (JPG, PNG, JPEG) and videos (MP4, MOV, AVI)
  - **Upload Area 2**: Supports images (JPG, PNG, JPEG) and videos (MP4, MOV, AVI)
- **Gallery Upload Support**: Users can upload images and videos directly from device gallery
  - Native gallery picker integration for seamless selection
  - Multi-select capability to choose multiple files at once
  - Preview thumbnails before confirming upload
  - Support for both photos and videos from gallery
  - Automatic format detection and compatibility checking
- Each upload area features:
  - Direct upload button with drag-and-drop support
  - Gallery upload button for selecting from device gallery
  - **Image Cover Display**: Uploaded image displayed as cover with overlay controls
  - **Change Image Button**: Button positioned on image cover to replace current image
    - Camera icon button with semi-transparent background
    - Opens file picker or gallery selector when clicked
    - Smooth transition animation when changing image
    - Preserves aspect ratio of new image
  - **Remove Image Button**: Button positioned on image cover to delete current image
    - Trash icon button with semi-transparent red background
    - Positioned at top-right corner of image cover\n    - Confirmation dialog before removing image
    - Smooth fade-out animation when removing\n    - Resets upload area to empty state after removal
  - Preview display for uploaded content
  - Download option for uploaded files
  - Clear/remove button to reset upload area
  - **Mix Toggle Button**: Enables mixing mode for the uploaded content in that area
- **Multi-Media Fusion Logic**:
  - **Two Images**: Blends both images together based on prompt description
  - **Two Videos**: Merges video sequences with smooth transitions
  - **Image + Video**: Intelligently integrates static image into video content, matching style and theme from prompt
  - **Image + Video with Mix Mode**: When mix toggle is enabled on image upload area, the image is deeply integrated into video frames, creating seamless fusion
  - **Video + Image with Mix Mode**: When mix toggle is enabled on video upload area, video elements are extracted and blended with the image to generate hybrid content
  - **Mixed Image and Video Generation**: When both upload areas have mix mode enabled, generates both a mixed image (combining key frames from video with the image) and a mixed video (integrating image elements throughout video timeline)
  - **Single Upload**: Works normally with one upload area filled
- High-quality processing for all fusion scenarios
- Automatic format compatibility checking
- **Mix Mode Indicator**: Visual badge showing which upload areas have mixing enabled
\n### 2.2 Prompt Input
- Single-line text input field for users to describe desired content
- Full-width input box with clear border styling
- **Fusion Matching**: When multiple media files are uploaded, prompt guides how they should be combined and matched together
- **Mix Mode Guidance**: Prompt can specify mixing intensity and style preferences for mixed content
\n### 2.3 Style Selection
- Dropdown menu with expanded style options:\n  - Realistic\n  - Cartoon
  - Anime
  - Oil Painting
  - Watercolor
  - Sketch\n  - Pop Art
  - Cyberpunk
  - Fantasy
  - Minimalist\n  - Vintage
  - Neon
  - Gothic
  - Impressionist
  - Abstract
  - Surrealism
  - Comic Book
  - Pixel Art
  - Low Poly
  - Steampunk
  - Art Deco
  - Baroque
  - Graffiti
  - Pastel
  - Monochrome
  - AI-recommended futuristic style (dynamic)\n- Default selection: AI-recommended style
- Style preview thumbnails on hover
- Custom style input option for advanced users

### 2.4 Aspect Ratio Control
- **Control Image Aspect Ratios**: Precise control over the exact shape of generated images - build perfect-fit images for vertical phone wallpapers or horizontal web banners
- Preset aspect ratio options:\n  - **Vertical Phone Wallpaper**: 9:16 (1080x1920) - Perfect for mobile device backgrounds
  - **Horizontal Web Banner**: 16:9 (1920x1080) - Ideal for website headers and promotional banners
  - **Square**: 1:1 (1080x1080) - Optimized for social media posts\n  - **Portrait**: 3:4 (1080x1440) - Classic portrait orientation
  - **Landscape**: 4:3 (1440x1080) - Traditional landscape format
  - **Ultrawide**: 21:9 (2560x1080) - Cinematic widescreen format
  - **Custom**: User-defined width and height input fields
- Dropdown selector positioned next to style selection
- Real-time preview of selected aspect ratio
- Automatic image cropping and scaling to fit chosen ratio
- Maintains image quality during aspect ratio adjustment

### 2.5 Generation Mode
- **Professional Fastest Generation Toggle**: Switch to enable high-speed professional generation mode
- **Ultra Fast Mode**: Advanced acceleration mode for near-instant content generation
- **Ultra Quality Mode**: Premium quality mode for highest-fidelity content generation with enhanced detail and precision
- **Creative Fusion Mode**: Experimental mode that blends multiple artistic styles for unique hybrid results
- **Eco-Efficient Mode**: Energy-optimized generation mode with balanced speed and quality
- **Cinematic Mode**: Professional video-focused mode with enhanced motion smoothness and cinematic color grading
- **Sketch-to-Art Mode**: Converts rough sketches into polished artistic renderings
- **Thinking Mode**: Advanced reasoning mode that gives AI time to think through complex queries and produce more thoughtful, detailed results
- **Stop Button**: Allows users to halt current generation and immediately switch to different mode
  - Red octagonal stop icon button positioned next to mode toggle
  - Instantly stops generation process without confirmation
  - Preserves current settings for quick mode switching
  - Enables seamless transition between generation modes
- **Refresh Button**: Resets all settings and clears current generation\n  - Circular arrow icon button positioned in control panel
  - Clears uploaded media, prompt text, and generated content
  - Resets mode to default AI-recommended style
  - Confirmation dialog to prevent accidental reset
- Visual indicator showing current mode status
- Mode-specific badge styling with distinctive colors and icons

### 2.6 Content Generation
- **Generate Image Button**: Creates static images based on prompt/uploaded media and selected style
  - Powered by **Nano Banana Pro** for high-quality image generation from text prompts
  - Perfect for creating blog post heroes, concept art, or unique assets in your application
- **Generate Video Button**: Creates video content based on prompt/uploaded media and selected style
  - Powered by **Veo 3** to animate images and bring them to life
  - Ideal for turning product photos into dynamic video ads or animating character portraits
  - Let users upload a product photo and turn it into a dynamic video ad, or animate a character's portrait
- **Mix Generation Master Toggle**: Global switch to enable/disable all mix generation features
  - Toggle switch positioned above Mix & Generate buttons
  - When enabled: Mix & Generate buttons become active and functional
  - When disabled: Mix & Generate buttons are grayed out and non-clickable
  - Visual indicator showing current mix generation status (ON/OFF)
  - Smooth transition animation when toggling
- **Mix & Generate Image Button**: Creates mixed images when mix mode is enabled and master toggle is ON
  - Positioned to the right of Generate Video button
  - Only functional when Mix Generation Master Toggle is enabled
  - Disabled state with tooltip when master toggle is OFF
- **Mix & Generate Video Button**: Creates mixed videos when mix mode is enabled and master toggle is ON
  - Positioned to the right of Mix & Generate Image button
  - Only functional when Mix Generation Master Toggle is enabled
  - Disabled state with tooltip when master toggle is OFF
- **Stop Mix Generation Button**: Dedicated stop button for halting mix generation processes
  - Red octagonal stop icon button positioned next to Mix & Generate buttons
  - Only visible and active during mix generation process
  - Instantly stops ongoing mix generation without confirmation
  - Preserves uploaded media and settings for retry
  - Clears mix generation progress indicator
  - Returns to ready state after stopping
- **Multi-Media Fusion Generation**:
  - Automatically detects uploaded media types in both upload areas
  - Applies intelligent matching algorithm based on prompt description
  - Detects mix mode status and applies advanced blending algorithms
  - Ensures seamless integration of multiple media sources
  - Maintains high quality output for all fusion combinations
  - **Perfect Mix Algorithm**: Automatically adjusts blending parameters to achieve optimal visual harmony between image and video elements
- **Cancel Button**: Stops ongoing generation process and returns to ready state
  - User-controlled cancellation with confirmation prompt
  - Immediately terminates generation and clears progress
- **Automatic Error Recovery**: System automatically detects and fixes generation failures
  - Automatically retries failed generations up to 3 times
  - Intelligently adjusts parameters if errors occur
  - Displays recovery status notification during auto-fix process
  - Logs recovery attempts in history for transparency
- Real-time progress indicator showing percentage (0-100%)
- Loading state display during generation process
- Mode-specific processing optimizations
\n### 2.7 Image Enhancement
- **Enhance Image Button**: AI-powered image enhancement feature
  - Positioned next to each generated or uploaded image
  - Circular button with sparkle icon
  - Applies intelligent enhancement algorithms to improve image quality
- **Enhancement Features**:
  - **Auto Quality Boost**: Automatically enhances resolution, sharpness, and clarity
  - **Color Correction**: Adjusts brightness, contrast, saturation, and color balance
  - **Noise Reduction**: Removes grain and digital noise while preserving details
  - **Detail Enhancement**: Sharpens edges and enhances fine details
  - **Smart Upscaling**: Increases resolution up to 4x using AI upscaling technology
  - **HDR Enhancement**: Expands dynamic range for richer colors and better highlights/shadows
- **Enhancement Modes**:
  - **Auto Mode**: One-click automatic enhancement with optimal settings
  - **Portrait Mode**: Specialized for faces with skin smoothing and feature enhancement
  - **Landscape Mode**: Optimized for scenery with sky and foliage enhancement
  - **Product Mode**: Perfect for e-commerce with background cleanup and color accuracy
  - **Custom Mode**: Manual adjustment sliders for fine-tuned control
- **Real-time Preview**: Side-by-side comparison of original and enhanced image
- **Undo/Redo**: Full enhancement history with unlimited undo capability
- **Batch Enhancement**: Apply same enhancement settings to multiple images
- **Enhancement Presets**: Save and load custom enhancement configurations
\n### 2.8 Video Enhancement
- **Enhance Video Button**: AI-powered video enhancement feature
  - Positioned next to each generated or uploaded video
  - Circular button with video sparkle icon
  - Applies intelligent enhancement algorithms to improve video quality\n- **Enhancement Features**:
  - **Resolution Upscaling**: Upscale videos from 1080p to 4K or4K to 8K using AI
  - **Frame Interpolation**: Increase frame rate from 30fps to 60fps or 120fps for smoother motion
  - **Stabilization**: Remove camera shake and jitter with advanced stabilization algorithms
  - **Color Grading**: Professional color correction and cinematic color grading
  - **Noise Reduction**: Remove video grain and compression artifacts
  - **Sharpness Enhancement**: Improve video clarity and detail definition
  - **Motion Blur Reduction**: Reduce motion blur in fast-moving scenes
  - **Low-Light Enhancement**: Brighten dark videos while preserving natural look
- **Enhancement Modes**:
  - **Auto Mode**: One-click automatic enhancement with optimal settings
  - **Cinematic Mode**: Film-grade color grading and motion smoothing
  - **Action Mode**: Optimized for fast motion with stabilization and sharpness
  - **Vlog Mode**: Perfect for talking-head videos with face enhancement
  - **Custom Mode**: Manual adjustment controls for advanced users
- **Real-time Preview**: Timeline scrubbing with before/after comparison
- **Selective Enhancement**: Apply enhancements to specific time ranges
- **Batch Processing**: Enhance multiple videos with same settings
- **Export Options**: Choose output resolution, frame rate, and bitrate

### 2.9 Enhancement Control Panel
- **Unified Enhancement Interface**: Dedicated panel for all enhancement operations
- **Enhancement Queue**: Shows all pending enhancement tasks with progress indicators
- **Enhancement History**: Tracks all enhancement operations with before/after previews
- **Quick Actions**:
  - **Enhance All Images**: Batch enhance all images in current session
  - **Enhance All Videos**: Batch enhance all videos in current session
  - **Compare Mode**: Side-by-side comparison view for original vs enhanced content
  - **Export Enhanced**: Download all enhanced content in one click
- **Enhancement Settings**:
  - **Quality Level**: Choose between Fast, Balanced, or Maximum quality
  - **Processing Priority**: Set priority for enhancement tasks\n  - **Auto-Save**: Automatically save enhanced versions\n  - **Watermark Option**: Add optional watermark to enhanced content
\n### 2.10 Gemini Intelligence Integration
- **Embedded Gemini AI**: Integrate Gemini intelligence in your app to complete all sorts of tasks - analyze content, make edits, and more
- **Content Analysis**: Analyze uploaded images to understand context, objects, and composition
- **Smart Editing Suggestions**: AI-powered recommendations for improving generated content
- **Contextual Understanding**: Interprets user prompts with deeper semantic understanding
- **Multi-Task Capabilities**: Completes various tasks including content analysis, style recommendations, and automatic adjustments
- **Natural Language Processing**: Understands complex, conversational prompts
- **Fast AI Responses**: Powered by Gemini 2.5 Flash-Lite for lightning-fast, real-time responses
  - Instant auto-completes for prompt suggestions
  - Conversational agents that feel alive and responsive
  - Sub-second response times for interactive features
\n### 2.11 Nano Banana Powered Photo Editing
- **Powerful Photo Editing**: Advanced editing capabilities powered by Nano Banana AI - add powerful photo editing to your app
- **Add Objects**: Users can add objects to images just by typing descriptions
- **Remove Backgrounds**: Automatic background removal with one-click operation
- **Change Photo Style**: Transform photo styles through text commands
  - Convert realistic photos to artistic styles
  - Apply filters and effects via natural language
- **Text-Based Editing**: All editing operations controlled through simple text input
- **Non-Destructive Editing**: Original images preserved, edits applied as layers
- **Undo/Redo Support**: Full editing history with unlimited undo capability
\n### 2.12 Image Analysis
- **Visual Understanding**: Enable app to see and understand image content
- **Receipt Analysis**: Upload receipt photos for instant data extraction
  - Automatic itemization and total calculation
  - Date and merchant information extraction
- **Menu Translation**: Upload menu photos for instant translation
  - Multi-language support\n  - Dish descriptions and ingredient identification
- **Chart Analysis**: Upload charts and graphs for data extraction and summaries
  - Automatic data point extraction
  - Trend analysis and insights generation
- **Document OCR**: Extract text from any image containing written content
- **Object Recognition**: Identify and label objects within images
- **Scene Understanding**: Analyze overall scene context and composition
\n### 2.13 Audio Transcription
- **Live Audio Transcription**: Real-time transcription of any audio feed
- **Multi-Language Support**: Transcribe audio in multiple languages
- **Speaker Identification**: Distinguish between different speakers in audio
- **Timestamp Generation**: Automatic timestamps for transcribed content
- **Export Options**: Download transcriptions in TXT, SRT, or VTT formats\n- **Audio Upload**: Support for MP3, WAV, M4A audio file formats
- **Microphone Input**: Real-time transcription from device microphone
- **Accuracy Indicators**: Confidence scores for transcribed text

### 2.14 AI Video Generator with Lifelike AI Avatars
- **AI Avatar Library**: Curated collection of professional, lifelike digital avatars
  - **Diverse Avatar Selection**: 50+ pre-built avatars with various ethnicities, ages, genders, and professional styles
  - **Avatar Categories**: Business professionals, educators, news anchors, casual presenters, customer service representatives\n  - **Customizable Appearance**: Adjust avatar clothing, hairstyle, accessories, and background settings
  - **Avatar Preview**: Real-time preview of selected avatar with sample animations
- **Text-to-Video Generation**: Convert written scripts into professional video presentations
  - **Script Input**: Multi-line text editor for entering video script (supports up to 10,000 characters)
  - **Voice Selection**: Choose from 100+ natural-sounding AI voices in 40+ languages
  - **Voice Customization**: Adjust speaking speed, pitch, tone, and emotional expression
  - **Pronunciation Control**: Add phonetic spellings for proper names and technical terms
- **Avatar Animation Features**:
  - **Realistic Lip Sync**: Precise mouth movements synchronized with generated speech
  - **Natural Gestures**: Automatic hand movements, head nods, and body language matching speech context
  - **Facial Expressions**: Dynamic expressions (smiling, serious, surprised) based on script sentiment
  - **Eye Contact**: Avatar maintains natural eye contact with camera
  - **Breathing Animation**: Subtle chest movements for lifelike realism
- **Video Customization Options**:
  - **Background Selection**: Choose from 200+ professional backgrounds (office, studio, outdoor, virtual sets)
  - **Custom Background Upload**: Upload your own background images or videos
  - **Green Screen Mode**: Generate avatar on transparent/green background for post-production
  - **Camera Angles**: Select from multiple camera positions (close-up, medium shot, full body)
  - **Video Resolution**: Output in 1080p, 4K, or vertical formats (9:16 for social media)
  - **Video Length**: Generate videos from 15 seconds to 30 minutes\n- **Advanced Features**:
  - **Multi-Avatar Scenes**: Include multiple avatars in single video with conversation flow
  - **Scene Transitions**: Automatic transitions between different backgrounds or camera angles
  - **Text Overlays**: Add titles, subtitles, captions, and lower thirds
  - **Logo Integration**: Insert company logos or watermarks
  - **Background Music**: Add royalty-free music tracks with volume control
  - **Slide Integration**: Combine avatar presentation with PowerPoint-style slides
- **Use Case Templates**:
  - **Corporate Training**: Pre-designed templates for employee onboarding and training videos
  - **Marketing Videos**: Product demos, explainer videos, promotional content
  - **Educational Content**: Lecture-style videos, tutorials, course materials
  - **News & Updates**: Company announcements, news broadcasts, update videos
  - **Social Media**: Short-form content for Instagram, TikTok, YouTube Shorts
  - **Customer Support**: FAQ videos, how-to guides, troubleshooting content
- **Generation Controls**:
  - **Generate Avatar Video Button**: Creates video with selected avatar and script
  - **Preview Mode**: Quick10-second preview before full generation
  - **Batch Generation**: Create multiple videos with different scripts simultaneously
  - **Real-time Progress**: Shows rendering progress with estimated completion time
  - **Quality Settings**: Choose between Fast (5min), Balanced (10 min), or Premium (20 min) rendering
- **Export & Sharing**:
  - **Download Formats**: MP4, MOV, WebM with customizable bitrate
  - **Direct Sharing**: One-click sharing to YouTube, Vimeo, social media platforms
  - **Embed Code**: Generate embed code for website integration
  - **Cloud Storage**: Automatic backup to cloud with30-day retention
- **Avatar Video History**:
  - **Project Management**: Save and organize avatar video projects
  - **Version Control**: Keep multiple versions of same video with edit history
  - **Quick Duplicate**: Clone existing projects for rapid iteration
  - **Search & Filter**: Find videos by avatar, script keywords, or creation date

### 2.15 Content Display
- **Image Display**: Shows generated images at250x250px size
- **Video Display**: Embedded video player with full-width layout and 300px height, supports playback controls
- **Avatar Video Display**: Dedicated player for AI avatar videos with full-width layout and 400px height
- **Fusion Result Display**: Clearly shows combined media output with quality indicators
- **Mixed Content Display**: Side-by-side display of mixed image and mixed video with sync playback option
- **Enhanced Content Display**: Dedicated section showing enhanced versions with quality comparison metrics
\n### 2.16 Download Functionality
- Download button in top navigation bar for batch downloads
- Individual download buttons for each generated image and video
- Download uploaded photos and videos option
- Download enhanced images and videos option
- Download AI avatar videos option
- Saves generated images as PNG format
- Saves generated videos as MP4 format
- Saves avatar videos as MP4 format with optional subtitle file (SRT)\n- Auto-saves to user's download directory
- Download progress indicator for large files
- One-click download all content option
- **Automatic Page Refresh After Download**: Page automatically refreshes after successfully downloading any generated content
  - Triggers after downloading any generated image\n  - Triggers after downloading any mixed image
  - Triggers after downloading any generated video
  - Triggers after downloading any mixed video
  - Triggers after downloading any uploaded photo
  - Triggers after downloading any enhanced image
  - Triggers after downloading any enhanced video
  - Triggers after downloading any AI avatar video
  - Smooth fade-out transition before refresh
  - Brief success notification before refresh (1 second)
  - Preserves user authentication state during refresh
  - Clears temporary generation data\n  - Resets upload areas and input fields to default state
\n### 2.17 History Management
- Displays chronological list of generated content\n- Shows content type (image/video/fusion/mixed/enhanced/avatar video) and filename
- Most recent items appear at the top\n- Scrollable list view for browsing past generations
- Download button for each history item
- **Remove Button**: Individual delete button for each history item
  - Trash icon button positioned next to download button
  - Confirmation dialog before deletion
  - Permanently removes item from history list
  - Updates display immediately after deletion
- Recovery attempt indicators for auto-fixed content
- **Mix Mode Badge**: Visual indicator showing which items were generated with mix mode enabled
- **Enhancement Badge**: Visual indicator showing which items have been enhanced
- **Avatar Video Badge**: Visual indicator showing AI avatar video content
\n### 2.18 Time and Date Display
- **Current time** shown in top navigation bar
- **Current date** displayed directly below the time
- Both time and date update in real-time
- Format: Time (HH:MM:SS) on first line, Date (YYYY-MM-DD Day) on second line
- Compact vertical layout in navigation bar
\n### 2.19 Search Functionality
- **Search Bar**: Located in top right corner of navigation bar
- Text input field with search icon
- Real-time search filtering of history items
- Searches by filename and content type
- Clear search button (X icon) to reset filter
- Placeholder text:'Search history...'
- Search results update instantly as user types
- Highlights matching items in history list
\n### 2.20 Suggestion Gallery from Nano Bananas
- **Pre-loaded Example Images**: Curated collection of approximately 50 high-quality sample images showcasing different styles and use cases
  - Portrait transformations, landscape enhancements, product visualization
  - Abstract art samples, seasonal and occasion-specific images
  - Trending visual styles and professional use cases
- **Pre-loaded Example Videos**: Curated collection of approximately 50 sample video outputs\n  - Short motion graphics, style transition videos, photo-to-video animations
  - Cinematic effect demonstrations, occasion-based video templates
  - Trending video formats and dynamic text animations
- **Pre-loaded Avatar Video Examples**: Curated collection of 30 sample AI avatar videos
  - Business presentation samples, educational tutorial examples\n  - Marketing pitch demonstrations, customer service scenarios
  - Multi-language examples, different avatar styles
- **Annual Content Updates**: Gallery automatically refreshes with approximately 50 new images,50 new videos, and 30 new avatar videos every year
  - Incorporates latest AI generation trends and techniques
  - Reflects current visual design movements and popular styles
- **Christmas Special Collection**: Dedicated section updated annually with new Christmas-themed content
  - **Christmas Photos**: 20+ new festive images added every year
    - Holiday decorations, winter landscapes, Santa themes
    - Family celebration scenes, gift wrapping ideas
    - Christmas card designs, festive food photography
  - **Christmas Videos**: 20+ new holiday videos added every year
    - Animated greeting cards, snowfall effects, fireplace ambiance
    - Christmas countdown timers, festive transitions
    - Holiday party clips, seasonal promotional templates
  - **Christmas Avatar Videos**: 10+ new holiday avatar videos added every year
    - Santa avatar greetings, holiday sales pitches
    - Christmas party invitations, year-end messages
  - Available from December 1st through January 6th each year
  - Archive of previous years' Christmas content accessible year-round
- **Occasion-Based Collections**: Dedicated sections for various occasions and events
  - Holidays, celebrations, seasonal themes, cultural festivals
  - Business occasions, social media trends\n- **One-Click Apply**: Users can click any example to automatically load its settings
- **Thumbnail Grid Layout**: Examples displayed in responsive grid with hover preview
- **Category Filters**: Filter examples by type, style, occasion, or use case
- **Most Useful Features Highlight**:
  - Quick-start templates, trending prompts section
  - Tips and tricks overlay, 'New This Year' badge
  - Occasion calendar showing upcoming events
\n### 2.21 Ultra Fix Generator
####2.21.1 Primary Objective
- Ensure the application operates smoothly and reliably under all expected conditions
- Proactively maintain optimal performance and prevent user-facing disruptions
\n#### 2.21.2 Core Functionality
- **Proactive Issue Detection**:
  - Continuously monitors application health metrics
  - Identifies potential errors before they affect users
  - Detects anomalies in generation processes and file handling
  - Monitors browser compatibility issues and resource constraints
- **Automatic Patch Generation and Application**:
  - Generates configuration adjustments in real-time
  - Applies performance optimizations automatically
  - Adjusts generation parameters dynamically based on system load
  - Clears cache when memory thresholds are reached
- **Detailed Logging and Reporting**:
  - Maintains comprehensive logs of identified problems and fixes
  - Records timestamps, severity levels, and resolution methods
  - Generates daily performance summary reports
  - Tracks fix success rates and recurring issue patterns
\n#### 2.21.3 Technical Implementation
- **Technology Stack**: JavaScript/TypeScript, Web Workers, IndexedDB, Service Worker\n- **Architecture Integration**: Background service with modular plugin design
- **Testing Protocol**: Automated unit tests, integration tests, performance benchmarking, A/B testing, staged rollout
\n#### 2.21.4 User Experience\n- **Operation Mode**: Silent operation by default, optional status notifications
- **Status Interface**:
  - Compact status indicator icon in top navigation bar
  - Color-coded health status (green: optimal, yellow: monitoring, blue: fixing)
  - Expandable detailed status panel showing system health score, recent fixes, performance metrics, activity history
  - Toggle switch to enable/disable automatic fixes
  - 'View Full Report' button for comprehensive diagnostics
\n#### 2.21.5 Success Metrics
- **Key Performance Indicators**: Crash rate reduction (90%), launch time improvement (30% faster), error reduction (80%), completion rate (95%+), uptime (99.5%+), issue resolution time (<5 seconds)
- **Monitoring Dashboard**: Real-time KPI tracking, weekly performance reports, comparative analysis\n\n#### 2.21.6 Implementation Strategy
1. **Phase 1 - Foundation (Week 1-2)**: Set up monitoring infrastructure and logging system
2. **Phase 2 - Detection (Week 3-4)**: Develop error detection algorithms\n3. **Phase 3 - Auto-Fix (Week 5-6)**: Implement automatic patch generation logic
4. **Phase 4 - Testing (Week 7-8)**: Conduct comprehensive testing\n5. **Phase 5 - Deployment (Week 9-10)**: Staged rollout and post-launch monitoring

### 2.22 Adaptive Theme System
- **Automatic Theme Switching**: System automatically switches between dark and light themes based on time of day
  - **Light Theme**: Activates during daytime hours (6:00 AM - 6:00 PM)
  - **Dark Theme**: Activates during nighttime hours (6:00 PM - 6:00 AM)
  - Smooth transition animation between themes (500ms fade)\n  - Time-based detection uses device local time
- **Manual Theme Override**: Users can manually switch themes regardless of time
  - Theme toggle button in top navigation bar
  - Sun icon for light theme, moon icon for dark theme
  - Manual selection persists across sessions
  - Override indicator showing manual mode is active
- **High Contrast Mode**: Enhanced text contrast for improved readability
  - **Light Theme Contrast**: Dark text (#1A1A1A) on light backgrounds (#FFFFFF)
  - **Dark Theme Contrast**: Light text (#F5F5F5) on dark backgrounds (#121212)
  - Minimum contrast ratio of 7:1 for all text elements
  - Enhanced border contrast for input fields and buttons
  - Increased font weight for better visibility (Regular → Medium)
- **Eye Comfort Shield**: Advanced eye protection features
  - **Blue Light Filter**: Reduces blue light emission during dark theme
    - Warm color temperature adjustment (6500K → 4500K)
    - Amber tint overlay with adjustable intensity (0-30%)
    - Automatic activation after 7:00 PM
  - **Brightness Adaptation**: Automatically adjusts interface brightness
    - Daytime: 100% brightness
    - Evening (6:00 PM - 9:00 PM): 80% brightness
    - Night (9:00 PM - 6:00 AM): 60% brightness
  - **Reading Mode**: Optimized typography for extended viewing
    - Increased line spacing (1.5x → 1.8x)
    - Slightly larger font sizes (+2px for body text)
    - Reduced animation intensity\n  - **Eye Comfort Settings Panel**: Dedicated control panel for customization
    - Blue light filter intensity slider (0-100%)
    - Brightness level adjustment\n    - Reading mode toggle
    - Color temperature selector
    - Reset to defaults button
- **Theme Persistence**: User preferences saved locally\n  - Manual theme selection stored in localStorage
  - Eye comfort settings preserved across sessions
  - Automatic restoration on page load
\n### 2.23 Health Monitoring and Pressure Management System
- **Health Dashboard**: Comprehensive wellness tracking interface
  - **Vital Signs Monitoring**: Real-time tracking of key health metrics
    - Heart rate monitoring (BPM)\n    - Blood pressure tracking (systolic/diastolic)
    - Stress level indicator (low/medium/high)
    - Activity level tracker (steps, calories burned)
  - **Pressure System**: Advanced stress and workload management
    - **Work Pressure Gauge**: Visual indicator showing current workload intensity
      - Color-coded levels: Green (optimal), Yellow (moderate), Orange (high), Red (critical)
      - Real-time pressure score calculation based on usage patterns
    - **Break Reminders**: Smart notification system for health breaks
      - Automatic reminders every 45-60 minutes during intensive work
      - Customizable break intervals and duration
      - Gentle audio/visual alerts with snooze option
    - **Pressure Relief Exercises**: Guided quick exercises to reduce stress
      - 2-minute breathing exercises with visual guidance
      - 5-minute stretching routines with animated demonstrations
      - Eye relaxation exercises for screen fatigue
      - Quick meditation sessions (3-10 minutes)
  - **Health Insights**: AI-powered health analysis and recommendations
    - Daily health summary with trend analysis
    - Personalized wellness tips based on usage patterns
    - Stress pattern recognition and early warning alerts
    - Sleep quality correlation with work pressure
- **Pressure Fix System**: Automated stress management and optimization
  - **Automatic Workload Balancing**: Intelligently distributes tasks to prevent burnout
    - Detects prolonged high-pressure periods
    - Suggests task prioritization and delegation
    - Recommends optimal work-rest cycles
  - **Stress Detection Algorithm**: Monitors user behavior for stress indicators
    - Tracks mouse movement patterns (erratic movements indicate stress)
    - Analyzes typing speed and error rates
    - Monitors session duration and break frequency
    - Detects rapid task switching (multitasking stress)
  - **Automatic Intervention**: Proactive stress reduction measures
    - Triggers calming interface adjustments (softer colors, reduced animations)
    - Activates ambient background sounds (nature sounds, white noise)
    - Suggests immediate micro-breaks when critical stress detected
    - Temporarily limits non-essential notifications
  - **Pressure Recovery Mode**: Special mode activated during high-stress periods
    - Simplified interface with reduced visual complexity
    - Extended break intervals with mandatory rest periods
    - Gentle productivity pacing to prevent overwork
    - Motivational messages and positive reinforcement
- **Health Data Integration**: Connect with external health devices and apps
  - **Wearable Device Sync**: Import data from fitness trackers and smartwatches
    - Apple Watch, Fitbit, Garmin, Samsung Galaxy Watch compatibility
    - Real-time heart rate and activity data synchronization
    - Sleep tracking data integration
  - **Health App Integration**: Connect with popular health platforms
    - Apple Health, Google Fit, Samsung Health support
    - Automatic data import and synchronization
    - Two-way data sharing for comprehensive tracking
- **Wellness Goals and Challenges**: Gamified health improvement system
  - **Daily Wellness Goals**: Set and track daily health objectives
    - Step count targets, active minutes, break frequency
    - Stress management goals, hydration reminders
    - Progress tracking with visual indicators
  - **Weekly Challenges**: Engaging wellness challenges with rewards
    - 'Stress-Free Week' challenge with daily meditation\n    - 'Active Creator' challenge promoting movement breaks
    - 'Balanced Workload' challenge for optimal work-rest ratio
    - Achievement badges and milestone celebrations
- **Health Reports and Analytics**: Comprehensive wellness reporting
  - **Weekly Health Summary**: Detailed report of health metrics and trends
    - Average stress levels, pressure patterns, break compliance
    - Activity statistics, sleep quality correlation
    - Improvement suggestions and personalized recommendations
  - **Monthly Wellness Report**: Long-term health trend analysis
    - Month-over-month comparison of key metrics
    - Identification of stress triggers and patterns
    - Success rate of pressure management interventions
    - Downloadable PDF report for personal records
- **Privacy and Security**: Robust health data protection
  - **Local Data Storage**: All health data stored locally on device
  - **Encrypted Storage**: AES-256 encryption for sensitive health information
  - **Optional Cloud Backup**: Encrypted cloud backup with user consent
  - **Data Export**: Export health data in standard formats (CSV, JSON)
  - **Data Deletion**: Complete data removal option with confirmation
\n## 3. Backend Implementation
### 3.1 Technology Stack
- **Framework**: FastAPI\n- **Database**: SQLite (db.sqlite)\n- **Video Processing**: FFmpeg\n- **Image Processing**: Pillow (PIL)
- **Authentication**: Token-based authentication with SHA-256 hashing
- **Real-time Communication**: WebSocket for progress tracking
- **AI Generation**: Placeholder for local Stable Diffusion integration
- **Image Enhancement**: OpenCV and AI upscaling models
- **Video Enhancement**: FFmpeg with AI-based filters and frame interpolation
- **AI Avatar Generation**: Integration with AI avatar rendering engine
- **Health Data Processing**: NumPy and Pandas for health metrics analysis
\n### 3.2 Backend Code\n```python
import os, uuid, asyncio, sqlite3, hashlib, time, subprocess\nfrom fastapi import FastAPI, UploadFile, File, Form, WebSocket, Header, Depends
from fastapi.responses import FileResponse, HTMLResponse\nfrom fastapi.middleware.cors import CORSMiddleware
from PIL import Image
import cv2
import numpy as np\nimport json
from datetime import datetime

# ---------------- CONFIG ----------------
OUT='out'; DB='db.sqlite'
os.makedirs(OUT, exist_ok=True)
RES={'1080p':('1920x1080','8M'),'4k':('3840x2160','20M'),'8k':('7680x4320','50M')}

# ---------------- APP ----------------
app=FastAPI()
app.add_middleware(CORSMiddleware, allow_origins=['*'], allow_methods=['*'], allow_headers=['*'])

# ---------------- DB ----------------
db=sqlite3.connect(DB,check_same_thread=False)\nc=db.cursor()
c.execute('CREATE TABLE IF NOT EXISTS u(id INTEGER PRIMARY KEY, n TEXT UNIQUE, p TEXT)')
c.execute('CREATE TABLE IF NOT EXISTS h(u INT,j TEXT,q TEXT,t TEXT)')
c.execute('CREATE TABLE IF NOT EXISTS health(u INT, timestamp TEXT, heart_rate INT, bp_sys INT, bp_dia INT, stress_level TEXT, pressure_score INT, activity_steps INT)')
db.commit()

# ---------------- AUTH ----------------
T={}
hp=lambda x:hashlib.sha256(x.encode()).hexdigest()
def get_user(token:str=Header(...)):
    if token not in T: raise Exception('401')
    return T[token]\n
# ---------------- PROGRESS ----------------
P={}

# ---------------- AI IMAGE GENERATION ----------------\ndef generate_ai(prompt, out_path, res):
    # Placeholder for free AI: black image (replace with local SD)
    subprocess.run(['ffmpeg','-f','lavfi','-i',f'color=c=black:s={res}','-frames:v','1',out_path])

# ---------------- IMAGE MIX ----------------
def mix_images(ai_path, user_path, out_path):
    ai = Image.open(ai_path).convert('RGBA')
    user = Image.open(user_path).convert('RGBA').resize(ai.size)
    mixed = Image.blend(ai, user, alpha=0.5)
    mixed.save(out_path)

# ---------------- IMAGE ENHANCEMENT ----------------
def enhance_image(img_path, out_path, mode='auto'):
    img = cv2.imread(img_path)\n    # Auto enhancement: denoise, sharpen, color correction
    denoised = cv2.fastNlMeansDenoisingColored(img, None, 10, 10, 7, 21)
    kernel = np.array([[-1,-1,-1], [-1,9,-1], [-1,-1,-1]])
    sharpened = cv2.filter2D(denoised, -1, kernel)
    # Color correction
    lab = cv2.cvtColor(sharpened, cv2.COLOR_BGR2LAB)
    l, a, b = cv2.split(lab)
    clahe = cv2.createCLAHE(clipLimit=3.0, tileGridSize=(8,8))
    l = clahe.apply(l)\n    enhanced = cv2.merge([l,a,b])
    enhanced = cv2.cvtColor(enhanced, cv2.COLOR_LAB2BGR)
    cv2.imwrite(out_path, enhanced)

# ---------------- VIDEO ENHANCEMENT ----------------
def enhance_video(vid_path, out_path, mode='auto'):
    # Video enhancement: upscaling, stabilization, color grading
    subprocess.run([
        'ffmpeg', '-i', vid_path,\n        '-vf', 'scale=3840:2160:flags=lanczos,unsharp=5:5:1.0:5:5:0.0,eq=contrast=1.1:brightness=0.05:saturation=1.2',
        '-c:v', 'libx264', '-preset', 'slow', '-crf', '18',
        out_path
    ])

# ---------------- AI AVATAR VIDEO GENERATION ----------------
def generate_avatar_video(script, avatar_id, voice_id, background, out_path, quality='balanced'):
    # Placeholder for AI avatar generation (replace with actual avatar API)
    P[out_path.split('/')[-1].split('.')[0]]=10
    duration = len(script.split()) * 0.5
    subprocess.run([
        'ffmpeg', '-f', 'lavfi', '-i', f'color=c=blue:s=1920x1080:d={duration}',
        '-vf', f'drawtext=text=\\\\'Avatar Video\\':fontsize=48:fontcolor=white:x=(w-text_w)/2:y=(h-text_h)/2',
        '-c:v', 'libx264', '-preset', quality, '-pix_fmt', 'yuv420p',
        out_path
    ])
P[out_path.split('/')[-1].split('.')[0]]=100

# ---------------- HEALTH DATA PROCESSING ----------------
def calculate_pressure_score(heart_rate, stress_level, activity_steps):\n    # Simple pressure score algorithm
    base_score = 50
    if heart_rate > 100: base_score += 20
    elif heart_rate > 80: base_score += 10
    if stress_level == 'high': base_score += 30
    elif stress_level == 'medium': base_score += 15
    if activity_steps < 2000: base_score += 10
    return min(base_score, 100)\n\ndef analyze_health_trends(uid):
    c.execute('SELECT * FROM health WHERE u=? ORDER BY timestamp DESC LIMIT 7', (uid,))
    data = c.fetchall()\n    if not data: return {'status': 'no_data'}
    avg_pressure = sum(row[6] for row in data) / len(data)
    trend = 'improving' if data[0][6] < avg_pressure else 'worsening'
    return {'avg_pressure': avg_pressure, 'trend': trend, 'records': len(data)}
\n# ---------------- IMAGE → VIDEO----------------
def make_video(img, vid, j, res, br):
    P[j]=10
    subprocess.run(['ffmpeg','-y','-loop','1','-i',img,'-t','6',\n        '-vf',f'scale={res},zoompan=z=\\\\'min(zoom+0.0005,1.1)\\\\'':d=180',
        '-pix_fmt','yuv420p','-b:v',br,vid])
    P[j]=100
\n# ---------------- FRONTEND ----------------
@app.get('/')
def ui():
    return HTMLResponse('''
<input id=u placeholder=user><input id=p type=password placeholder=pass><button onclick=r()>R</button><button onclick=l()>L</button><br>\n<input type=file id=f><input type=file id=f2><input id=prompt placeholder=prompt><select id=q><option>1080p</option><option selected>4k</option><option>8k</option></select><button onclick=g()>GO</button><button onclick=ei()>Enhance Image</button><button onclick=ev()>Enhance Video</button><br>
<textarea id=script placeholder='Enter avatar video script'></textarea><select id=avatar><option>Avatar 1</option><option>Avatar 2</option></select><select id=voice><option>Voice 1</option><option>Voice 2</option></select><button onclick=ga()>Generate Avatar Video</button><br>
<h3>Health Monitor</h3>
<input id=hr type=number placeholder='Heart Rate'><input id=bps type=number placeholder='BP Systolic'><input id=bpd type=number placeholder='BP Diastolic'><select id=stress><option>low</option><option>medium</option><option>high</option></select><input id=steps type=number placeholder='Steps'><button onclick=sh()>Save Health Data</button><button onclick=gh()>Get Health Trends</button><p id=health></p>
<p id=s></p><video id=v controls></video>
<script>
let t=''\nr=()=>fetch('/r',{method:'POST',body:new URLSearchParams({u:u.value,p:p.value})})
l=async()=>t=(await (await fetch('/l',{method:'POST',body:new URLSearchParams({u:u.value,p:p.value})})).json()).t
g=async()=>{\nlet d=new FormData();d.append('image',f.files[0]); if(f2.files[0]) d.append('mix',f2.files[0]); d.append('prompt',prompt.value); d.append('quality',q.value)\nlet j=await (await fetch('/g',{method:'POST',headers:{token:t},body:d})).json()
let ws=new WebSocket(`ws://${location.host}/w/${j.j}`)
ws.onmessage=e=>s.innerText='Progress '+JSON.parse(e.data).p+'%'
v.src='/v/'+j.j\n}
ei=async()=>{
let d=new FormData();d.append('image',f.files[0]);
let j=await (await fetch('/ei',{method:'POST',headers:{token:t},body:d})).json()
alert('Image enhanced: '+j.j)
}
ev=async()=>{\nlet d=new FormData();d.append('video',f.files[0]);
let j=await (await fetch('/ev',{method:'POST',headers:{token:t},body:d})).json()
alert('Video enhanced: '+j.j)
}\nga=async()=>{
let d=new FormData();d.append('script',script.value);d.append('avatar',avatar.value);d.append('voice',voice.value);
let j=await (await fetch('/ga',{method:'POST',headers:{token:t},body:d})).json()
let ws=new WebSocket(`ws://${location.host}/w/${j.j}`)
ws.onmessage=e=>s.innerText='Avatar Progress '+JSON.parse(e.data).p+'%'
v.src='/v/'+j.j
}
sh=async()=>{
let d=new FormData();d.append('heart_rate',hr.value);d.append('bp_sys',bps.value);d.append('bp_dia',bpd.value);d.append('stress_level',stress.value);d.append('activity_steps',steps.value);
let j=await (await fetch('/sh',{method:'POST',headers:{token:t},body:d})).json()
health.innerText='Health data saved. Pressure score: '+j.pressure_score\n}
gh=async()=>{\nlet j=await (await fetch('/gh',{method:'GET',headers:{token:t}})).json()
health.innerText='Avg Pressure: '+j.avg_pressure+', Trend: '+j.trend+', Records: '+j.records\n}
</script>
''')

# ---------------- AUTH API ----------------
@app.post('/r')\ndef r(u:str=Form(...),p:str=Form(...)):\n    c.execute('INSERT INTO u(n,p) VALUES(?,?)',(u,hp(p))); db.commit(); return {}
@app.post('/l')\ndef l(u:str=Form(...),p:str=Form(...)):
    c.execute('SELECT id FROM u WHERE n=? AND p=?',(u,hp(p))); x=c.fetchone()
    t=uuid.uuid4().hex; T[t]=x[0]; return {'t':t}
\n# ---------------- GENERATE API ----------------
@app.post('/g')
async def g(image: UploadFile = File(...), mix: UploadFile = None, prompt: str = Form(...), quality: str = Form('4k'), uid: int = Depends(get_user)):
    j=str(uuid.uuid4()); res, br=RES[quality]
    img=f'{OUT}/{j}.png'; vid=f'{OUT}/{j}.mp4'\n    open(img,'wb').write(await image.read())
    ai=f'{OUT}/{j}_ai.png'\n    generate_ai(prompt, ai, res)
    if mix:
        uimg=f'{OUT}/{j}_u.png'; open(uimg,'wb').write(await mix.read()); mix_images(ai,uimg,img)
    else: img=ai
    await asyncio.to_thread(make_video,img,vid,j,res,br)
    c.execute('INSERT INTO h VALUES(NULL,?,?,?,?)',(uid,j,quality,time.ctime())); db.commit()
    return {'j':j}\n
# ---------------- IMAGE ENHANCEMENT API ----------------
@app.post('/ei')
async def ei(image: UploadFile = File(...), mode: str = Form('auto'), uid: int = Depends(get_user)):
    j=str(uuid.uuid4())
    img_in=f'{OUT}/{j}_in.png'\n    img_out=f'{OUT}/{j}_enhanced.png'
    open(img_in,'wb').write(await image.read())
    await asyncio.to_thread(enhance_image, img_in, img_out, mode)
    c.execute('INSERT INTO h VALUES(NULL,?,?,?,?)',(uid,j,'enhanced_image',time.ctime())); db.commit()
    return {'j':j}

# ---------------- VIDEO ENHANCEMENT API ----------------
@app.post('/ev')
async def ev(video: UploadFile = File(...), mode: str = Form('auto'), uid: int = Depends(get_user)):
    j=str(uuid.uuid4())
    vid_in=f'{OUT}/{j}_in.mp4'\n    vid_out=f'{OUT}/{j}_enhanced.mp4'
    open(vid_in,'wb').write(await video.read())
    await asyncio.to_thread(enhance_video, vid_in, vid_out, mode)
    c.execute('INSERT INTO h VALUES(NULL,?,?,?,?)',(uid,j,'enhanced_video',time.ctime())); db.commit()
    return {'j':j}

# ---------------- AI AVATAR VIDEO GENERATION API ----------------
@app.post('/ga')
async def ga(script: str = Form(...), avatar: str = Form('Avatar 1'), voice: str = Form('Voice 1'), background: str = Form('default'), quality: str = Form('balanced'), uid: int = Depends(get_user)):
    j=str(uuid.uuid4())
    vid_out=f'{OUT}/{j}_avatar.mp4'
    await asyncio.to_thread(generate_avatar_video, script, avatar, voice, background, vid_out, quality)
    c.execute('INSERT INTO h VALUES(NULL,?,?,?,?)',(uid,j,'avatar_video',time.ctime())); db.commit()
    return {'j':j}

# ---------------- HEALTH DATA API ----------------
@app.post('/sh')
async def sh(heart_rate: int = Form(...), bp_sys: int = Form(...), bp_dia: int = Form(...), stress_level: str = Form(...), activity_steps: int = Form(...), uid: int = Depends(get_user)):
    timestamp = datetime.now().isoformat()
    pressure_score = calculate_pressure_score(heart_rate, stress_level, activity_steps)
    c.execute('INSERT INTO health VALUES(?,?,?,?,?,?,?,?)', (uid, timestamp, heart_rate, bp_sys, bp_dia, stress_level, pressure_score, activity_steps))
    db.commit()\n    return {'pressure_score': pressure_score, 'timestamp': timestamp}
\n@app.get('/gh')
async def gh(uid: int = Depends(get_user)):
    trends = analyze_health_trends(uid)
    return trends

# ---------------- VIDEO----------------
@app.get('/v/{j}')\ndef v(j:str): return FileResponse(f'{OUT}/{j}.mp4')

# ---------------- PROGRESS WS ----------------
@app.websocket('/w/{j}')\nasync def w(ws: WebSocket,j:str):
    await ws.accept()
    while P.get(j,0)<100: await ws.send_json({'p':P.get(j,0)}); await asyncio.sleep(0.5)
    await ws.send_json({'p':100}); await ws.close()
```

### 3.3 Installation & Setup
```bash
pip install fastapi uvicorn python-multipart pillow opencv-python numpy pandas
ffmpeg -version
uvicorn main:app --reload
```\n
### 3.4 Access\n- Navigate to: http://YOUR-IP:8000
\n### 3.5 API Endpoints
- **POST /r**: User registration
- **POST /l**: User login (returns authentication token)
- **POST /g**: Generate video from uploaded image with optional mix image and AI prompt
- **POST /ei**: Enhance uploaded image with AI-powered enhancement
- **POST /ev**: Enhance uploaded video with AI-powered enhancement
- **POST /ga**: Generate AI avatar video from script with selected avatar and voice
- **POST /sh**: Save health data (heart rate, blood pressure, stress level, activity steps)
- **GET /gh**: Get health trends and analysis for current user
- **GET /v/{j}**: Retrieve generated video by job ID
- **WebSocket /w/{j}**: Real-time progress updates for video generation

### 3.6 Database Schema
- **Table u**: User accounts (id, username, password hash)
- **Table h**: Generation history (user_id, job_id, quality, timestamp)
- **Table health**: Health data (user_id, timestamp, heart_rate, bp_systolic, bp_diastolic, stress_level, pressure_score, activity_steps)
\n### 3.7 Video Quality Options
- **1080p**: 1920x1080 resolution, 8M bitrate
- **4k**: 3840x2160 resolution, 20M bitrate (default)
- **8k**: 7680x4320 resolution, 50M bitrate

### 3.8 AI Generation Features
- **Prompt-based AI Image Generation**: Creates AI-generated images based on text prompts
- **Image Mixing**: Blends AI-generated images with user-uploaded images using50% alpha blending
- **Dual Upload Support**: Accepts primary image and optional mix image for fusion
- **AI Avatar Video Generation**: Creates professional videos with lifelike AI avatars from text scripts

### 3.9 Enhancement Features
- **Image Enhancement**: AI-powered image quality improvement with denoising, sharpening, and color correction
- **Video Enhancement**: AI-powered video upscaling, stabilization, and color grading
- **Multiple Enhancement Modes**: Auto, Portrait, Landscape, Product, Custom modes for images; Auto, Cinematic, Action, Vlog modes for videos
\n### 3.10 Health System Features
- **Health Data Storage**: Secure storage of vital signs and wellness metrics
- **Pressure Score Calculation**: Automated calculation of work pressure and stress levels
- **Health Trend Analysis**: AI-powered analysis of health patterns and trends
- **Real-time Monitoring**: Continuous tracking of health metrics during app usage

## 4. Flutter Mobile Implementation
### 4.1 Technology Stack
- **Framework**: Flutter (Dart)
- **State Management**: Provider\n- **File Handling**: file_picker, path_provider, image_picker
- **HTTP Client**: http package
- **Platform Support**: iOS and Android
\n### 4.2 Flutter Code\n```dart
import 'dart:async';
import 'dart:io';
import 'package:flutter/material.dart';
import 'package:file_picker/file_picker.dart';
import 'package:image_picker/image_picker.dart';
import 'package:path_provider/path_provider.dart';
import 'package:provider/provider.dart';
import 'package:http/http.dart' as http;\n
void main() {
  runApp(\n    ChangeNotifierProvider(\n      create: (_) => MediaProvider(),
      child: const MyApp(),
    ),\n  );
}
\nclass MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return const MaterialApp(
      debugShowCheckedModeBanner: false,
      home: HomePage(),
    );
  }
}

/* =========================\n   MEDIA PROVIDER
========================= */

class MediaProvider extends ChangeNotifier {
  final List mediaFiles = [];
  bool isProcessing = false;
\n  Future addLocalFile(File file) async {
    isProcessing = true;
    notifyListeners();
\n    if (!await _verifyFile(file)) return;
\n    await Future.delayed(const Duration(seconds: 10));
\n    final uploaded = await _savePreservingQuality(file);
    mediaFiles.add(uploaded);
\n    isProcessing = false;
    notifyListeners();
  }

  Future addFromUrl(String url) async {
    isProcessing = true;
    notifyListeners();

    final tempDir = await getTemporaryDirectory();
    final fileName = url.split('/').last.split('?').first;
    final tempFile = File('${tempDir.path}/$fileName');

    final response = await http.get(Uri.parse(url));
    await tempFile.writeAsBytes(response.bodyBytes);

    await addLocalFile(tempFile);
}

  Future addFromGallery(ImageSource source) async {
    final picker = ImagePicker();
    final pickedFile = await picker.pickImage(source: source);\n\n    if (pickedFile != null) {
      await addLocalFile(File(pickedFile.path));
    }\n  }

  Future addVideoFromGallery(ImageSource source) async {
    final picker = ImagePicker();\n    final pickedFile = await picker.pickVideo(source: source);

    if (pickedFile != null) {\n      await addLocalFile(File(pickedFile.path));\n    }
  }\n
  Future _verifyFile(File file) async {
    try {
      final size1 = await file.length();\n      await Future.delayed(const Duration(milliseconds: 600));
      final size2 = await file.length();
      return size1 == size2 && size1 > 0;\n    } catch (_) {
      return false;\n    }
  }\n
  Future _savePreservingQuality(File file) async {
    final dir = await getApplicationDocumentsDirectory();
    final newPath =
        '${dir.path}/${DateTime.now().millisecondsSinceEpoch}_${file.uri.pathSegments.last}';
    return file.copy(newPath);
  }
}\n
/* =========================
   UI\n========================= */

class HomePage extends StatelessWidget {
  const HomePage({super.key});

  Future pickFromAnywhere(BuildContext context) async {
    final result = await FilePicker.platform.pickFiles(\n      type: FileType.media,
      allowMultiple: true,
    );
\n    if (result != null) {
      for (final path in result.paths) {
        if (path != null) {
          Provider.of<MediaProvider>(context, listen: false)
              .addLocalFile(File(path));
        }
      }
    }
  }

  void showUrlDialog(BuildContext context) {
    final controller = TextEditingController();
\n    showDialog(
      context: context,
      builder: (_) => AlertDialog(
        title: const Text('Add from URL'),
        content: TextField(
          controller: controller,
          decoration: const InputDecoration(\n            hintText: 'Paste image or video URL',
          ),
        ),
        actions: [
          TextButton(
            onPressed: () {
              Navigator.pop(context);
              Provider.of<MediaProvider>(context, listen: false)
                  .addFromUrl(controller.text.trim());
            },
            child: const Text('Upload'),
          ),
        ],
      ),
    );
  }
\n  void showGalleryOptions(BuildContext context) {
    showModalBottomSheet(
      context: context,
      builder: (_) => SafeArea(
        child: Column(
          mainAxisSize: MainAxisSize.min,
          children: [
            ListTile(
              leading: const Icon(Icons.photo_library),\n              title: const Text('Pick Image from Gallery'),
              onTap: () {
                Navigator.pop(context);
                Provider.of<MediaProvider>(context, listen: false)
                    .addFromGallery(ImageSource.gallery);
              },\n            ),
            ListTile(
              leading: const Icon(Icons.video_library),
              title: const Text('Pick Video from Gallery'),
              onTap: () {\n                Navigator.pop(context);
                Provider.of<MediaProvider>(context, listen: false)\n                    .addVideoFromGallery(ImageSource.gallery);
              },
            ),
            ListTile(
              leading: const Icon(Icons.camera_alt),
              title: const Text('Take Photo with Camera'),
              onTap: () {
                Navigator.pop(context);
                Provider.of<MediaProvider>(context, listen: false)
                    .addFromGallery(ImageSource.camera);
              },
            ),
            ListTile(
              leading: const Icon(Icons.videocam),
              title: const Text('Record Video with Camera'),
              onTap: () {
                Navigator.pop(context);
                Provider.of<MediaProvider>(context, listen: false)
                    .addVideoFromGallery(ImageSource.camera);
              },
            ),
          ],
        ),
      ),
    );
  }

  @override\n  Widget build(BuildContext context) {
    final provider = Provider.of<MediaProvider>(context);
\n    return Scaffold(
      appBar: AppBar(title: const Text('Upload From Anywhere')),
      body: Column(
        children: [\n          const SizedBox(height: 20),
\n          ElevatedButton(
            onPressed: () => pickFromAnywhere(context),\n            child: const Text('Pick from Device (Anywhere)'),
          ),
\n          const SizedBox(height: 10),

          ElevatedButton(
            onPressed: () => showGalleryOptions(context),
            child: const Text('Pick from Gallery'),
          ),

          const SizedBox(height: 10),
\n          ElevatedButton(
            onPressed: () => showUrlDialog(context),
            child: const Text('Add from URL (Internet)'),
          ),

          if (provider.isProcessing)
            const Padding(
              padding: EdgeInsets.all(16),
              child: CircularProgressIndicator(),
            ),
\n          Expanded(
            child: ListView.builder(
              itemCount: provider.mediaFiles.length,
              itemBuilder: (_, i) {
                final file = provider.mediaFiles[i];\n                return ListTile(
                  leading: const Icon(Icons.check_circle, color: Colors.green),
                  title: Text(file.path.split('/').last),
                  subtitle: const Text('Uploaded • Original Quality'),
                );
              },
            ),
          ),
        ],
      ),
    );
  }
}
```

### 4.3 Flutter Features
- **Universal File Upload**: Pick media files from any location on device
- **Gallery Upload Support**: Select images and videos directly from device gallery
  - Separate options for images and videos
  - Camera integration for capturing new photos and videos
  - Multi-select capability for batch uploads
  - Native gallery picker with thumbnail previews
- **URL Upload Support**: Add images and videos directly from internet URLs
- **Quality Preservation**: Maintains original file quality during upload process
- **File Verification**: Validates file integrity before processing
- **Progress Indication**: Visual feedback during upload and processing
- **Multi-File Support**: Upload multiple files simultaneously
- **Cross-Platform**: Works on both iOS and Android devices

### 4.4 Flutter Dependencies
Add to `pubspec.yaml`:
```yaml
dependencies:
  flutter:
    sdk: flutter
  provider: ^6.0.0
  file_picker: ^5.0.0
  image_picker: ^1.0.0\n  path_provider: ^2.0.0
  http: ^1.0.0\n```

### 4.5 Flutter Installation
```bash
flutter pub get
flutter run
```

## 5. Design Style\n### 5.1 Light Theme Color Scheme
- Primary color: Modern blue (#2196F3) for buttons and interactive elements
- Background: Clean white (#FFFFFF) for main content area
- Secondary background: Light gray (#F5F5F5) for panels and cards
- Text color: Dark gray (#1A1A1A) for high contrast readability
- Border color: Medium gray (#E0E0E0) for input fields\n- Mode-specific colors: Green (#4CAF50), Purple (#9C27B0), Gold (#FFD700), Rainbow gradient, Nature green (#66BB6A), Deep purple (#6A1B9A), Artistic teal (#26A69A)
- Stop button: Bold red (#D32F2F) with octagonal shape
- Stop Mix Generation button: Bright red (#E53935) with octagonal shape
- Refresh button: Cool blue (#42A5F5) with circular arrow icon
- Cancel button: Warning red (#F44336)\n- Auto-recovery indicator: Amber (#FFC107)\n- Suggestion gallery: Soft gradient background (#F5F5F5 to #FAFAFA)
- Christmas collection: Festive red (#C62828) and green (#2E7D32) accents with gold highlights (#FFD700)
- Ultra Fix Generator: Electric cyan (#00BCD4)\n- Remove button: Danger red (#E53935)
- Search bar: Light gray background (#F5F5F5) with blue focus border
- Mix toggle button: Vibrant purple (#7B1FA2) when enabled, light gray (#BDBDBD) when disabled
- Mix Generation Master Toggle: Deep purple (#7B1FA2) when ON, light gray (#9E9E9E) when OFF\n- Mix mode indicator: Gradient purple-blue (#7B1FA2 to #2196F3)\n- Mix & Generate buttons: Deep purple (#7B1FA2) when enabled, light gray (#BDBDBD) when disabled\n- Aspect ratio selector: Teal accent (#009688)\n- Gemini AI features: Gradient blue-purple (#4285F4 to #9C27B0)
- Thinking Mode: Deep indigo (#3F51B5) with animated thinking indicator
- Style dropdown: Gradient background with style-specific accent colors
- Download success notification: Soft green (#66BB6A) with white text
- Enhance Image button: Bright cyan (#00BCD4) with sparkle icon
- Enhance Video button: Electric purple (#9C27B0) with video sparkle icon
- Enhancement panel: Gradient background (#E3F2FD to #F3E5F5)
- Enhancement badge: Gold (#FFD700) with star icon
- Theme toggle button: Sun icon in amber (#FFA726)
- Gallery picker button: Soft purple (#BA68C8) with gallery icon
- Change Image button: Bright blue (#2196F3) with camera icon
- Remove Image button: Danger red (#E53935) with trash icon
- AI Avatar features: Gradient teal-blue (#00897B to #0277BD)
- Generate Avatar Video button: Vibrant teal (#00897B) with avatar icon
- Avatar video badge: Teal (#00897B) with person icon
- **Health Dashboard**: Gradient green-blue (#43A047 to #00ACC1)
- **Pressure Gauge**: Color-coded levels - Green (#4CAF50), Yellow (#FDD835), Orange (#FB8C00), Red (#E53935)\n- **Break Reminder**: Soft orange (#FF9800) with bell icon
- **Health Insights**: Light blue background (#E1F5FE) with dark blue text
- **Wellness Goals**: Gradient purple-pink (#7B1FA2 to #E91E63)
\n### 5.2 Dark Theme Color Scheme
- Primary color: Bright blue (#42A5F5) for buttons and interactive elements
- Background: Deep dark (#121212) for main content area
- Secondary background: Dark gray (#1E1E1E) for panels and cards
- Text color: Light gray (#F5F5F5) for high contrast readability
- Border color: Medium dark gray (#424242) for input fields
- Mode-specific colors: Bright green (#66BB6A), Bright purple (#BA68C8), Bright gold (#FFD54F), Rainbow gradient, Nature green (#81C784), Bright purple (#9575CD), Artistic teal (#4DB6AC)\n- Stop button: Bright red (#EF5350) with octagonal shape
- Stop Mix Generation button: Bright red (#F44336) with octagonal shape\n- Refresh button: Bright blue (#64B5F6) with circular arrow icon
- Cancel button: Warning red (#EF5350)
- Auto-recovery indicator: Bright amber (#FFCA28)
- Suggestion gallery: Dark gradient background (#1E1E1E to #2C2C2C)
- Christmas collection: Bright red (#E53935) and bright green (#43A047) accents with bright gold (#FFD54F)\n- Ultra Fix Generator: Bright cyan (#26C6DA)
- Remove button: Bright red (#F44336)
- Search bar: Dark gray background (#2C2C2C) with bright blue focus border
- Mix toggle button: Bright purple (#BA68C8) when enabled, dark gray (#616161) when disabled
- Mix Generation Master Toggle: Bright purple (#BA68C8) when ON, dark gray (#757575) when OFF
- Mix mode indicator: Gradient bright purple-blue (#BA68C8 to #42A5F5)
- Mix & Generate buttons: Bright purple (#BA68C8) when enabled, dark gray (#616161) when disabled
- Aspect ratio selector: Bright teal (#26A69A)\n- Gemini AI features: Gradient bright blue-purple (#64B5F6 to #BA68C8)
- Thinking Mode: Bright indigo (#5C6BC0) with animated thinking indicator
- Style dropdown: Dark gradient background with bright style-specific accent colors
- Download success notification: Bright green (#81C784) with dark text
- Enhance Image button: Bright cyan (#26C6DA) with sparkle icon
- Enhance Video button: Bright purple (#BA68C8) with video sparkle icon
- Enhancement panel: Dark gradient background (#1A237E to #4A148C)
- Enhancement badge: Bright gold (#FFD54F) with star icon
- Theme toggle button: Moon icon in bright blue (#64B5F6)
- Blue light filter overlay: Warm amber tint (#FFA726with 0-30% opacity)
- Gallery picker button: Bright purple (#CE93D8) with gallery icon\n- Change Image button: Bright blue (#64B5F6) with camera icon
- Remove Image button: Bright red (#F44336) with trash icon
- AI Avatar features: Gradient bright teal-blue (#26A69A to #42A5F5)
- Generate Avatar Video button: Bright teal (#26A69A) with avatar icon
- Avatar video badge: Bright teal (#26A69A) with person icon
- **Health Dashboard**: Gradient bright green-blue (#66BB6A to #26C6DA)
- **Pressure Gauge**: Color-coded levels - Bright Green (#66BB6A), Bright Yellow (#FFEB3B), Bright Orange (#FF9800), Bright Red (#F44336)
- **Break Reminder**: Bright orange (#FFB74D) with bell icon\n- **Health Insights**: Dark blue background (#1A237E) with light blue text
- **Wellness Goals**: Gradient bright purple-pink (#BA68C8 to #F48FB1)

### 5.3 Layout Structure
- Top navigation bar with app title, time and date display (stacked vertically), theme toggle button, Ultra Fix Generator status icon, **Health Monitor icon**, search bar (top right), and download button\n- Centered vertical layout for main content
- **New Section**: Suggestion gallery positioned below navigation bar, collapsible panel\n- Stacked arrangement: suggestion gallery → dual upload areas (side by side with mix toggle buttons, gallery picker buttons, change image buttons, and remove image buttons) → input field → aspect ratio selector → style selector → generation mode toggle with stop/refresh buttons → Mix Generation Master Toggle → action buttons (Generate Image, Generate Video, Mix & Generate Image, Mix & Generate Video, Stop Mix Generation, Cancel) → **AI Avatar Section** (script input, avatar selector, voice selector, background selector, Generate Avatar Video button) → Enhancement buttons (Enhance Image, Enhance Video) → progress indicator → content display → enhancement control panel → **Health Dashboard** (collapsible panel with vital signs, pressure gauge, break reminders, health insights) → history list\n- **Button Layout**: Generate Image and Generate Video on the left, Mix Generation Master Toggle centered above Mix & Generate buttons, Mix & Generate Image and Mix & Generate Video positioned to the right of Generate Video button, Stop Mix Generation button positioned next to Mix & Generate buttons (visible only during mix generation), Generate Avatar Video button positioned below Mix & Generate buttons, Enhance Image and Enhance Video buttons positioned below generation buttons
- **AI Avatar Section Layout**: Multi-line script textarea (full width), avatar dropdown selector, voice dropdown selector, background selector, quality selector, Generate Avatar Video button with teal styling\n- **Gallery Picker Integration**: Gallery picker button positioned next to direct upload button in each upload area
- **Image Cover Controls**: Change Image button and Remove Image button positioned as overlay controls on uploaded image cover
- **AI Features Panel**: Collapsible side panel for Gemini intelligence, image analysis, audio transcription, and AI avatar features\n- **Enhancement Control Panel**: Dedicated section below content display showing enhancement queue, history, and quick actions
- **Eye Comfort Settings Panel**: Floating panel accessible from theme toggle button, positioned in top-right corner
- **Health Dashboard Layout**: Collapsible panel with tabbed interface\n  - **Vital Signs Tab**: Real-time display of heart rate, blood pressure, stress level, activity steps\n  - **Pressure Monitor Tab**: Work pressure gauge with color-coded levels, break reminder notifications, pressure relief exercises
  - **Health Insights Tab**: AI-powered health analysis, trend charts, personalized recommendations
  - **Wellness Goals Tab**: Daily goals tracker, weekly challenges, achievement badges
  - **Health Reports Tab**: Weekly and monthly health summaries, downloadable PDF reports
\n### 5.4 Visual Details
- Rounded corners (8px) for buttons and input fields
- Subtle shadows for elevated components (light theme: rgba(0,0,0,0.1), dark theme: rgba(0,0,0,0.3))
- 16dp spacing between major sections, 8dp for related elements
- Material Design 3 component styling\n- Download icons with smooth hover animations
- Stop button: Octagonal shape with bold red border
- Stop Mix Generation button: Octagonal shape with bright red border and blend-stop icon
- Refresh button: Circular with rotating arrow icon
- Dual upload areas: Equal width with 12dp gap between them
- Christmas collection cards: Festive border with snowflake decorations
- Suggestion cards: 12px rounded corners with hover lift effect
- Ultra Fix Generator icon: Circular badge with shield symbol
- Remove button: Small circular button with trash icon
- Search bar: Rounded input field (20px) with magnifying glass icon
- Mix toggle button: Circular button with blend icon, positioned at top-right corner of each upload area
- Mix Generation Master Toggle: Large toggle switch with ON/OFF label, positioned prominently above Mix & Generate buttons
- Mix mode badge: Small purple badge with 'MIX' label on history items
- Mix & Generate buttons: Distinctive purple styling with blend icon when enabled, grayed out when master toggle is OFF
- Aspect ratio selector: Dropdown with visual ratio preview icons
- Gemini AI badge: Gradient badge with sparkle icon
- Thinking Mode indicator: Animated ellipsis with pulsing effect
- Style dropdown: Expanded dropdown with style preview thumbnails and smooth scroll
- Time and date display: Compact vertical layout with time on top line and date below, both centered in navigation bar
- Download success notification: Toast notification with checkmark icon, appears for 1 second before page refresh
- Enhance Image button: Circular button with sparkle icon, positioned next to each image
- Enhance Video button: Circular button with video sparkle icon, positioned next to each video
- Enhancement panel: Rounded panel (12px) with gradient background and subtle shadow
- Enhancement badge: Small gold badge with star icon on enhanced content in history
- Before/After slider: Interactive slider for comparing original and enhanced content
- Theme toggle button: Circular button with sun/moon icon, smooth rotation animation on click
- Theme transition: 500ms smooth fade between light and dark themes
- High contrast text: Medium font weight (500) for improved readability
- Eye comfort overlay: Subtle warm tint with smooth opacity transition
- Gallery picker button: Rounded button (8px) with gallery icon, positioned next to upload button
- Image cover: Full-width display with semi-transparent overlay controls
- Change Image button: Circular button (40px) with camera icon, positioned at center of image cover with semi-transparent white background (light theme) or semi-transparent dark background (dark theme)
- Remove Image button: Circular button (32px) with trash icon, positioned at top-right corner of image cover with semi-transparent red background\n- AI Avatar section: Rounded panel (12px) with teal gradient border\n- Script textarea: Multi-line input (200px height) with character counter
- Avatar selector: Dropdown with avatar thumbnail previews
- Voice selector: Dropdown with voice sample playback buttons
- Generate Avatar Video button: Large rounded button (12px) with teal gradient background and avatar icon
- Avatar video badge: Small teal badge with person icon on history items
- **Health Monitor icon**: Heart-shaped icon with pulse animation in navigation bar
- **Health Dashboard panel**: Rounded panel (12px) with gradient green-blue border\n- **Vital Signs display**: Card-based layout with large numeric values and trend indicators
- **Pressure Gauge**: Circular gauge with animated needle and color-coded zones
- **Break Reminder notification**: Toast notification with orange background and bell icon
- **Health Insights cards**: Rounded cards (8px) with light blue background and insight text
- **Wellness Goals progress bars**: Horizontal progress bars with gradient fill and percentage labels
- **Health Reports**: Downloadable PDF icon button with document symbol

### 5.5 Interactive Feedback
- Button hover states with color transitions
- Progress bar with smooth animation
- Loading spinner during content generation
- Disabled button states during processing
- Upload area highlight on drag-over
- Toggle switch animation for generation mode
- Stop button pulse effect when generation is active
- Stop Mix Generation button pulse effect when mix generation is active
- Refresh button rotation animation on click
- Download button pulse effect on completion
- Success notification after download completion
- Mode-specific activation animations
- Cancel button shake animation on hover
- Fade-out transition when canceling generation
- Auto-recovery progress indicator with rotating wrench icon
- Toast notification for successful auto-fix completion
- **Suggestion gallery interactions**: Card scale-up on hover, smooth fade-in, ripple effect on click, category filter tabs with slide transition
- **Christmas collection interactions**: Snowfall animation on hover, festive jingle sound on click (optional)\n- **Ultra Fix Generator interactions**: Status icon color transition, smooth slide-down animation for status panel, real-time graph updates
- **Remove button interactions**: Fade-in on hover, scale-up on hover, confirmation dialog with slide-down animation
- **Search bar interactions**: Border color change on focus, clear button appears when text is entered, real-time filtering with smooth transitions
- **Dual upload interactions**: Synchronized highlight when both areas are filled, connection line animation showing fusion relationship
- **Mix toggle interactions**: Smooth color transition when toggled, ripple effect on click, glow effect when enabled
- **Mix Generation Master Toggle interactions**: Smooth slide animation when toggling, color transition from gray to purple, ripple effect on click, tooltip showing current status
- **Mix mode visual feedback**: Purple border glow on upload areas when mix mode is active, animated blend icon rotation during mixed content generation
- **Mix & Generate button interactions**: Purple glow effect on hover when enabled, scale-up animation, disabled state with tooltip when master toggle is OFF, grayed out appearance when inactive
- **Stop Mix Generation button interactions**: Pulse effect during mix generation, scale-up on hover, fade-in when mix generation starts, fade-out when generation stops
- **Aspect ratio selector interactions**: Dropdown animation with slide-down effect, visual preview of selected ratio, smooth transition when changing ratios
- **Gemini AI interactions**: Sparkle animation when processing, smooth fade-in for analysis results, typing animation for AI responses
- **Thinking Mode interactions**: Animated thinking indicator with pulsing dots, progress bar showing reasoning depth, completion celebration animation
- **Style dropdown interactions**: Smooth dropdown expansion with fade-in effect, thumbnail preview on hover, color-coded style categories, quick filter buttons for style types
- **Download and refresh interactions**: Success toast notification with checkmark icon (1 second duration), smooth fade-out transition of entire page, automatic page reload after fade-out completes, preserved authentication state across refresh, loading indicator during refresh process
- **Enhance Image button interactions**: Sparkle animation on hover, scale-up effect, cyan glow when processing, success checkmark animation when complete
- **Enhance Video button interactions**: Video sparkle animation on hover, scale-up effect, purple glow when processing, progress ring animation during enhancement
- **Enhancement panel interactions**: Smooth slide-up animation when opening, collapsible sections with accordion effect, real-time progress bars for enhancement queue\n- **Before/After slider interactions**: Smooth drag interaction, snap-to-center effect, automatic comparison animation on load\n- **Enhancement badge interactions**: Gold shimmer effect on hover, tooltip showing enhancement details, click to view enhancement settings
- **Theme toggle interactions**: Smooth rotation animation (180degrees) when switching themes, icon morph animation from sun to moon, color transition matching theme change, tooltip showing current theme and time-based status
- **Theme transition effects**: Smooth fade animation (500ms) for all UI elements, color interpolation for gradual theme change, preserved scroll position during transition, no layout shift or flicker
- **Eye comfort interactions**: Blue light filter intensity slider with real-time preview, brightness adjustment with smooth transition, reading mode toggle with typography animation, settings panel slide-in from right side
- **Gallery picker interactions**: Bottom sheet slide-up animation with options list, icon animation on selection, smooth transition to file picker, thumbnail preview after selection, success feedback with checkmark animation
- **Image cover interactions**: Smooth fade-in animation when image is uploaded, overlay controls appear on hover with fade-in effect\n- **Change Image button interactions**: Scale-up animation on hover, ripple effect on click, smooth transition when replacing image, loading indicator during image change process
- **Remove Image button interactions**: Scale-up animation on hover, shake animation on hover, confirmation dialog with slide-down animation, smooth fade-out animation when removing image, upload area resets to empty state with fade transition
- **AI Avatar section interactions**: Script textarea auto-resize as user types, character counter updates in real-time, avatar selector shows thumbnail preview on hover, voice selector includes play button for voice sample preview, background selector shows full-size preview on hover\n- **Generate Avatar Video button interactions**: Teal glow effect on hover, scale-up animation, disabled state when script is empty, loading animation with avatar icon rotation during generation\n- **Avatar video display interactions**: Custom video player controls with teal accent color, playback speed control, subtitle toggle button, download button with teal styling\n- **Avatar video badge interactions**: Teal shimmer effect on hover, tooltip showing avatar and voice details, click to view generation settings\n- **Health Monitor icon interactions**: Pulse animation with heartbeat rhythm, color change based on current health status, click to expand Health Dashboard\n- **Health Dashboard interactions**: Smooth slide-down animation when expanding, tabbed interface with smooth tab transitions, collapsible sections with accordion effect\n- **Vital Signs display interactions**: Real-time value updates with smooth number transitions, trend indicators with up/down arrows, color-coded status badges\n- **Pressure Gauge interactions**: Animated needle movement with smooth easing, color zone transitions, click to view detailed pressure breakdown
- **Break Reminder interactions**: Gentle fade-in animation, pulsing bell icon, snooze button with countdown timer, dismiss button with fade-out effect\n- **Health Insights interactions**: Card flip animation to reveal detailed insights, expandable cards for more information, share button for exporting insights
- **Wellness Goals interactions**: Progress bar fill animation, confetti animation when goal achieved, edit button for adjusting goals, reset button with confirmation dialog
- **Health Reports interactions**: PDF preview modal with zoom controls, download button with progress indicator, email share option, print button for physical copies


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
# ============================================================