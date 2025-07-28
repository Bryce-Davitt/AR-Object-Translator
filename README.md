# AR English Word App

An augmented reality application that helps Spanish speakers learn English by displaying English words for objects detected through the camera.

## Features

- **Real-time Object Detection**: Uses YOLOv5 to detect objects in your camera feed
- **English Word Display**: Shows English words above detected objects
- **Friendly Learning Interface**: Clean, attractive UI designed for language learning
- **Object Tracking**: Smooth animations and fade effects for detected objects
- **Interactive Sidebar**: Shows all currently detected words with learning tips

## Screenshots

*[Add screenshots here once you have them]*

## Installation

### Prerequisites

- Python 3.8 or higher
- Webcam
- Git

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/ar-english-word-app.git
   cd ar-english-word-app
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Download YOLO model** (if not already present)
   ```bash
   # The app will automatically download yolov5x.pt on first run
   # Or manually download from: https://github.com/ultralytics/yolov5/releases
   ```

## Usage

### Running the App

```bash
python main.py
```

### Controls

- **Q**: Quit the application
- **R**: Reset all detected words
- **F**: Toggle fullscreen mode
- **ESC**: Exit fullscreen mode

### How to Use

1. Point your camera at objects around you
2. The app will detect objects and display English words above them
3. Check the sidebar on the right for a list of all detected words
4. Use this as a learning tool to build your English vocabulary!

## Configuration

You can customize the app behavior by editing `config.py`:

- **Camera settings**: Resolution, FPS
- **Detection settings**: Confidence thresholds
- **UI settings**: Colors, fonts, overlay transparency
- **Performance**: Detection intervals, max tracked objects

## Project Structure

```
ar-english-word-app/
├── main.py              # Main application logic
├── config.py            # Configuration settings
├── requirements.txt     # Python dependencies
├── README.md           # This file
├── .gitignore          # Git ignore rules
└── LICENSE             # License information
```

## Dependencies

- **torch**: PyTorch for YOLO model inference
- **opencv-python**: Camera capture and UI rendering
- **ultralytics**: YOLOv5 model loading and inference
- **numpy**: Numerical computing
- **requests**: HTTP requests (for future translation features)
- **seaborn**: Data visualization (dependency of ultralytics)

## How It Works

1. **Camera Capture**: OpenCV captures frames from your webcam
2. **Object Detection**: YOLOv5 processes each frame to detect objects
3. **Word Display**: English object names are displayed above detected objects
4. **UI Rendering**: OpenCV draws overlays, bounding boxes, and the sidebar
5. **Object Tracking**: Maintains state of detected objects for smooth animations

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [Ultralytics](https://github.com/ultralytics/ultralytics) for YOLOv5
- [OpenCV](https://opencv.org/) for computer vision capabilities
- [PyTorch](https://pytorch.org/) for deep learning framework

## Troubleshooting

### Common Issues

**"No module named 'cv2'"**
```bash
pip install opencv-python
```

**"No module named 'ultralytics'"**
```bash
pip install ultralytics
```

**Camera not working**
- Check if your webcam is connected and not in use by another application
- Try running with a different camera index in `config.py`

**Slow performance**
- Reduce camera resolution in `config.py`
- Increase `DETECTION_INTERVAL` to skip more frames
- Use a smaller YOLO model (yolov5s.pt instead of yolov5x.pt)

## Future Enhancements

- [ ] Add pronunciation audio for English words
- [ ] Implement word difficulty levels
- [ ] Add vocabulary tracking and progress
- [ ] Support for multiple languages
- [ ] Integration with language learning APIs
- [ ] Mobile app version

## Support

If you encounter any issues or have questions, please open an issue on GitHub. 