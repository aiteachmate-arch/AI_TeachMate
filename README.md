# AI_TeachMate
# 🤖 AI TeachMate - Your AI Learning Companion

> **Transform Education with AI** - Personalized, interactive learning powered by AI avatars, voice interaction, and adaptive content.

## 🌟 Features

### 🎙️ **Voice-Powered Learning**
- Natural speech recognition for asking questions
- Hands-free interaction with the AI tutor
- Real-time speech-to-text conversion

### 🤖 **AI Avatar Teacher**
- Engaging 3D animated avatar
- Multiple video states (speaking, listening, thinking, idle)
- Realistic teaching experience

### 📚 **Curriculum-Aligned Content**
- **Classes**: 5, 6, 7, 8, 9, 10
- **Subjects**: English, Maths, Science, Social Studies
- Subject-specific explanations and formatting

### 🎯 **Personalized Learning**
- Adaptive content delivery
- Smart topic suggestions based on learning history
- Context-aware question answering

### 📝 **Smart Note-Taking**
- Automatic note generation during lessons
- Manual editing capabilities
- Export notes as text files

### 🏆 **Progress Tracking**
- Learning dashboard with statistics
- Achievement system
- Learning streak tracking
- Topic completion history

### 💡 **Smart Suggestions**
- AI-powered topic recommendations
- Recent topics quick access
- Most frequent topics tracking
- Subject and class-based suggestions

### 🔊 **Text-to-Speech**
- Natural voice synthesis using Edge TTS
- Adjustable speech rate for different subjects
- Pause, resume, and stop controls

## 🚀 Getting Started

### Prerequisites

- **Python 3.8 or higher**
- **Windows OS** (for full video support)
- **Microphone** (for voice input feature)
- **Internet connection** (for AI responses and TTS)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/YOUR_USERNAME/AI-TeachMate.git
   cd AI-TeachMate
   ```

2. **Install required dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Install optional dependencies** (for full features)
   ```bash
   # For speech recognition
   pip install SpeechRecognition pyaudio
   
   # For text-to-speech
   pip install pygame edge-tts
   
   # For video support
   pip install opencv-python
   ```

4. **Set up video templates** (optional)
   - Create folder: `~/AI_TEACHMATE_DSR/VIDEO_TEMPLATE/`
   - Add your avatar video files (or the app will work without videos)

5. **Run the application**
   ```bash
   python ai_teachmate.py
   ```

## 📦 Requirements

### Core Dependencies
```
PyQt5>=5.15.0
requests>=2.28.0
```

### Optional Dependencies
```
SpeechRecognition>=3.10.0
pyaudio>=0.2.13
pygame>=2.5.0
edge-tts>=6.1.0
opencv-python>=4.8.0
appdirs>=1.4.4
```

### AI Backend
```
# Your RAG Agent implementation
# Located in: APPLICATION/RAG_AGENT_DSR.py
```

## 🎮 How to Use

### 1. **Select Class & Subject**
   - Choose your class (5-10)
   - Select subject (English, Maths, Science, Social)

### 2. **Enter a Topic**
   - Type in the topic input field
   - Or click on smart suggestions

### 3. **Learn Interactively**
   - Watch AI avatar explain concepts
   - Read synchronized text content
   - Take automatic notes

### 4. **Ask Questions**
   - Click 🎤 to ask via voice
   - Or type your question
   - Get instant contextual answers
   - Continue from where you left off

### 5. **Track Progress**
   - View dashboard (📊 button)
   - Check learning streak
   - Unlock achievements

## 🎨 Project Structure

```
AI-TeachMate/
│
├── ai_teachmate.py              # Main application file
├── APPLICATION/
│   └── RAG_AGENT_DSR.py        # AI backend (RAG Agent)
│
├── ~/AI_TEACHMATE_DSR/
│   └── VIDEO_TEMPLATE/          # Avatar video files
│       ├── static_position-Forward.mp4
│       ├── explanation_DSR_Forward.mp4
│       ├── hearing_dsr.mp4
│       └── thinking_part_1.mp4
│
├── ~/.ai_teachmate/             # User data directory
│   ├── user_progress.json
│   ├── topic_history.json
│   └── temp_audio/
│
├── requirements.txt             # Python dependencies
├── README.md                    # This file
└── LICENSE                      # MIT License
```

## ⚙️ Configuration

### Video Paths
Edit `VIDEO_PATHS` in `ai_teachmate.py` to customize avatar videos:
```python
VIDEO_PATHS = {
    "startup": ["path/to/startup_video.mp4"],
    "speaking": ["path/to/speaking_video.mp4"],
    "listening": ["path/to/listening_video.mp4"],
    "thinking": ["path/to/thinking_video.mp4"],
}
```

### Color Scheme
Customize colors in `COLORS` dictionary:
```python
COLORS = {
    'primary': '#667eea',
    'accent': '#00d4ff',
    'success': '#4ade80',
    # ... more colors
}
```

## 🔧 Features in Detail

### Voice Recognition
- Uses Google Speech Recognition (free)
- Supports ambient noise calibration
- Configurable timeout and phrase limits

### AI Avatar
- Video states: startup, speaking, listening, thinking
- Automatic video switching based on activity
- Loop support for idle states

### Progress System
- Topics completed tracking
- Question count
- Learning streak calculation
- Achievement unlocking system

### Smart Suggestions
- Recent topics (last 10)
- Most frequent topics
- Class/Subject filtered suggestions
- Default curriculum-based suggestions

## 🐛 Troubleshooting

### Speech Recognition Issues
```bash
# On Windows, install PyAudio from wheel
pip install pipwin
pipwin install pyaudio
```

### Video Not Playing
- Ensure video files exist in correct path
- Check OpenCV installation: `pip install opencv-python`
- Verify video codec compatibility

### TTS Not Working
```bash
# Reinstall edge-tts and pygame
pip uninstall edge-tts pygame
pip install edge-tts pygame
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**DSR Sridhar Dornadula [SD50]**

- GitHub: [@YOUR_GITHUB_USERNAME](https://github.com/YOUR_GITHUB_USERNAME)
- LinkedIn: [Your LinkedIn](https://linkedin.com/in/YOUR_PROFILE)
- Email: your.email@example.com

## 🙏 Acknowledgments

- PyQt5 for the amazing GUI framework
- OpenCV for video processing
- Edge TTS for natural voice synthesis
- Google Speech Recognition for voice input
- All educators and students who provided feedback

## 🗺️ Roadmap

- [ ] Mobile app (Android/iOS)
- [ ] Multi-language support
- [ ] Offline mode
- [ ] Parent/Teacher dashboard
- [ ] Quiz and assessment module
- [ ] Cloud sync for progress
- [ ] Screen recording for revision
- [ ] Collaborative learning features

## 📊 Stats

- **Version**: 2.0
- **Python**: 3.8+
- **Platform**: Windows (primary), Linux/Mac (partial support)
- **License**: MIT

## 💬 Support

If you encounter any issues or have questions:

1. Check the [Issues](https://github.com/YOUR_USERNAME/AI-TeachMate/issues) page
2. Create a new issue with detailed description
3. Contact: your.email@example.com

## ⭐ Star History

If you find this project useful, please consider giving it a star! ⭐

---

<div align="center">
  <p>Made with ❤️ by DSR Sridhar Dornadula</p>
  <p>© 2025 AI TeachMate - All Rights Reserved</p>
</div>
