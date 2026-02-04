# SwingExtractor ⚾

> **Automated Baseball Bat Hit Detection & Video Clip Extraction**
>
> A hobbyist project designed to save parents time by automatically extracting quality batting clips from baseball game videos using advanced audio analysis and FFmpeg filtering.

## 📖 Overview

SwingExtractor is a Python-based tool that automatically detects bat hits in baseball game recordings and extracts video clips around those moments. As a parent filming your children's baseball games, you no longer need to spend hours scrubbing through footage to find the perfect at-bat moments. SwingExtractor does the heavy lifting for you!

### The Problem It Solves

Recording your child's baseball games is easy. Finding and editing quality clips of their at-bats? That's time-consuming and tedious. SwingExtractor automates this process by:

- **Detecting the sound of bat hits** using advanced audio analysis
- **Automatically extracting video clips** around each hit
- **Saving you hours** of manual video editing
- **Letting you focus on what matters** - sharing great moments with your family

## ✨ Key Features

- 🎯 **Automatic Bat Hit Detection**: Uses audio analysis to identify the distinctive sound of a bat hitting a ball
- 🎬 **Smart Video Extraction**: Extracts clips with configurable pre/post-hit buffers to capture the complete action
- 🔊 **Advanced FFmpeg Audio Filtering**: Leverages FFmpeg's powerful audio processing capabilities for accurate detection
- ⚡ **Batch Processing**: Process multiple game videos at once
- 🎨 **Configurable Parameters**: Customize sensitivity, clip length, and output formats to match your needs
- 💾 **Multiple Output Formats**: Export clips in various video formats for easy sharing

## 🔧 How It Works

1. **Audio Analysis**: SwingExtractor analyzes the audio track of your baseball game video
2. **Pattern Recognition**: Identifies the distinctive frequency and amplitude patterns of bat hits
3. **Timestamp Detection**: Records the exact timestamps of each detected hit
4. **Clip Extraction**: Uses FFmpeg to extract video clips around each hit timestamp
5. **Output Organization**: Saves clips with meaningful names and timestamps for easy review

## 📋 Requirements

- **Python 3.7+**
- **FFmpeg** (installed and available in PATH)
- **librosa** (for audio analysis)
- **numpy** (for numerical processing)
- **Additional Python dependencies** (see `requirements.txt`)

## 🚀 Installation

### Prerequisites

1. **Install FFmpeg**:
   ```bash
   # macOS (using Homebrew)
   brew install ffmpeg
   
   # Ubuntu/Debian
   sudo apt-get update
   sudo apt-get install ffmpeg
   
   # Windows (using Chocolatey)
   choco install ffmpeg
   ```

2. **Clone the Repository**:
   ```bash
   git clone https://github.com/jeamajoal/SwingExtractor.git
   cd SwingExtractor
   ```

3. **Set Up a Virtual Environment** (Recommended):
   
   Using a virtual environment helps isolate project dependencies and avoid conflicts with other Python projects.
   
   **On Linux/macOS**:
   ```bash
   # Create a virtual environment
   python3 -m venv venv
   
   # Activate the virtual environment
   source venv/bin/activate
   ```
   
   **On Windows**:
   ```bash
   # Create a virtual environment
   python -m venv venv
   
   # Activate the virtual environment
   venv\Scripts\activate
   ```
   
   When the virtual environment is activated, you'll see `(venv)` in your command prompt.

4. **Install Python Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```
   
   **Note**: Make sure your virtual environment is activated before installing dependencies.

## 📝 Usage

**Note**: If you're using a virtual environment, make sure it's activated before running SwingExtractor:
```bash
# Linux/macOS
source venv/bin/activate

# Windows
venv\Scripts\activate
```

### Basic Usage

```bash
python swing_extractor.py --input game_video.mp4 --output clips/
```

### Advanced Usage

```bash
python swing_extractor.py \
  --input game_video.mp4 \
  --output clips/ \
  --sensitivity 0.8 \
  --pre-buffer 2 \
  --post-buffer 3 \
  --min-interval 5
```

### Configuration Options

| Option | Description | Default |
|--------|-------------|---------|
| `--input` | Input video file path | Required |
| `--output` | Output directory for clips | `./clips` |
| `--sensitivity` | Hit detection sensitivity (0.0-1.0) | `0.75` |
| `--pre-buffer` | Seconds before hit to include | `2.0` |
| `--post-buffer` | Seconds after hit to include | `3.0` |
| `--min-interval` | Minimum seconds between hits | `3.0` |
| `--format` | Output video format (mp4, mov, avi) | `mp4` |

## 💡 Example Use Cases

### Family Game Day
Record your child's entire game, then run SwingExtractor to get all their at-bat highlights automatically compiled.

### Season Highlight Reel
Process multiple game videos throughout the season, then compile the best clips into a memorable highlight reel.

### Coaching Analysis
Extract batting clips to analyze swing mechanics and track improvement over time.

### Social Media Sharing
Quickly generate shareable clips for posting on social media or sharing with family and friends.

## 🎯 Tips for Best Results

1. **Audio Quality Matters**: Ensure your recording device captures clear audio of bat hits
2. **Minimize Background Noise**: Position yourself away from excessive crowd noise when possible
3. **Adjust Sensitivity**: Start with default settings and adjust sensitivity if you get too many or too few detections
4. **Test on Sample Videos**: Run SwingExtractor on a short test video first to fine-tune your settings
5. **Use Consistent Recording Position**: Recording from similar positions helps maintain consistent detection accuracy

## 🛠️ Troubleshooting

### Virtual Environment Issues
- **Command not found after installation**: Make sure your virtual environment is activated
- **To deactivate the virtual environment**: Simply run `deactivate` in your terminal
- **To reactivate later**: Navigate to the project directory and run the activation command again

### Too Many False Positives
- Increase the sensitivity value (closer to 1.0)
- Increase the `min-interval` setting
- Check for excessive background noise in your recordings

### Missing Some Hits
- Decrease the sensitivity value (closer to 0.5)
- Verify FFmpeg is properly installed and in PATH
- Ensure audio quality is sufficient in your source video

### Poor Clip Quality
- Use higher quality source videos
- Adjust the `pre-buffer` and `post-buffer` settings
- Check your output format settings

## 🔮 Future Enhancements

- [ ] GUI interface for easier configuration
- [ ] Real-time processing during recording
- [ ] Machine learning model for improved detection accuracy
- [ ] Support for different baseball scenarios (pitching, fielding plays)
- [ ] Cloud processing for batch jobs
- [ ] Mobile app integration
- [ ] Automatic highlight reel generation with music

## 🤝 Contributing

This is a hobbyist project, but contributions are welcome! If you have ideas for improvements or encounter issues:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - feel free to use it, modify it, and share it with other baseball parents!

## 🙏 Acknowledgments

- Built with love for baseball parents everywhere
- Powered by FFmpeg and the Python audio processing community
- Inspired by countless hours of watching youth baseball

## 📧 Contact

**Project Creator**: [@jeamajoal](https://github.com/jeamajoal)

**Project Link**: [https://github.com/jeamajoal/SwingExtractor](https://github.com/jeamajoal/SwingExtractor)

---

*Made with ❤️ to capture those special baseball moments*
