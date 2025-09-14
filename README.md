# Sign_language_model

<img width="266" alt="image" src="https://github.com/user-attachments/assets/082ebdb3-5c35-4f8e-8095-3e5672e11e5a">

<img width="420" alt="image" src="https://github.com/user-attachments/assets/5354f53e-23d4-4db6-9abe-b354ceb6cb23">

# Sign Language Detector

A real-time sign language detection system using Python, OpenCV, and MediaPipe that recognizes hand gestures and translates them into corresponding letters.

## Features

- Real-time hand gesture recognition using webcam
- Detects sign language letters: A, C, V
- Uses MediaPipe for hand landmark detection
- Machine learning model trained with scikit-learn
- Visual feedback with bounding boxes and predictions

## Requirements

- Python 3.7+
- Webcam

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/sign-language-detector-python.git
cd sign-language-detector-python
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

## Usage

### Data Collection
Collect training images for each sign:
```bash
python collect_imgs.py
```

### Dataset Creation
Process collected images and extract hand landmarks:
```bash
python create_dataset.py
```

### Model Training
Train the classification model:
```bash
python train_classifier.py
```

### Real-time Detection
Run the sign language detector:
```bash
python inference_classifier.py
```

## Project Structure

```
├── data/                   # Raw image data
│   ├── 0/                 # Images for class 0 (V)
│   ├── 1/                 # Images for class 1 (A)
│   └── 2/                 # Images for class 2 (C)
├── dataSet/               # Processed datasets
│   ├── trainingData/
│   └── testingData/
├── collect_imgs.py        # Image collection script
├── create_dataset.py      # Dataset preprocessing
├── train_classifier.py    # Model training
├── inference_classifier.py # Real-time detection
├── model.p               # Trained model file
├── data.pickle           # Processed dataset
└── requirements.txt      # Dependencies
```

## How It Works

1. **Hand Detection**: Uses MediaPipe to detect hand landmarks in real-time
2. **Feature Extraction**: Extracts normalized coordinates of hand landmarks
3. **Classification**: Uses a trained Random Forest classifier to predict the sign
4. **Visualization**: Displays the prediction with bounding boxes on the video feed

## Supported Signs

Currently supports detection of:
- **A** - Class 1
- **C** - Class 2  
- **V** - Class 0

## Dependencies

- `opencv-python==4.7.0.68` - Computer vision operations
- `mediapipe==0.9.0.1` - Hand landmark detection
- `scikit-learn==1.2.0` - Machine learning model

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Demo

The system provides real-time detection with visual feedback showing detected hand landmarks and predicted sign language letters.
