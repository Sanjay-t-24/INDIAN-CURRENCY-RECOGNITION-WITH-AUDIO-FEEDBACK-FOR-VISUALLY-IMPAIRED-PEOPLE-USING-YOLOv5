# Indian Currency Recognition with Audio Feedback for Visually Impaired People using YOLOv5

This project aims to assist visually impaired individuals by recognizing Indian currency notes and providing real-time audio feedback on the denomination. The model is built using the YOLOv5 object detection framework and is capable of recognizing various denominations of Indian currency. It leverages audio output to announce the identified denomination to the user, enhancing accessibility and independence.

## Features

- **Currency Recognition**: Identifies Indian currency notes of various denominations in real-time.
- **Audio Feedback**: Provides verbal feedback to inform the user of the recognized currency denomination.
- **High Accuracy**: Uses YOLOv5, a state-of-the-art object detection model, to ensure reliable and accurate recognition.
- **Real-time Performance**: Optimized for quick response, allowing users to experience minimal delay between recognition and feedback.

## Project Overview

### Technology Stack

- **YOLOv5**: Object detection framework for currency recognition
- **Python**: Core programming language
- **OpenCV**: For image processing and webcam integration
- **Text-to-Speech Library**: Provides audio feedback on recognized currency (e.g., Pyttsx3 or gTTS)
- **PyTorch**: For model training and inference
- **Dataset**: Custom-labeled images of Indian currency denominations

### Workflow

1. **Image Capture**: Uses a webcam or smartphone camera to capture the currency note in real-time.
2. **Currency Recognition**: YOLOv5 model detects the currency note and identifies its denomination.
3. **Audio Feedback**: The identified denomination is converted into an audio message and played for the user.

## Setup

### Prerequisites

Ensure you have the following installed:

- Python 3.8+
- PyTorch (compatible with YOLOv5)
- OpenCV
- Text-to-Speech Library (Pyttsx3 or gTTS)
- YOLOv5 dependencies (`pip install -r requirements.txt` in the YOLOv5 directory)

### Installation

1. Clone this repository and navigate to the project directory:

   ```bash
   git clone https://github.com/your-username/indian-currency-recognition.git
   cd indian-currency-recognition
   ```

2. Install the required Python packages:

   ```bash
   pip install -r requirements.txt
   ```

3. Download or prepare a dataset of labeled Indian currency notes for training YOLOv5 (or use a pretrained model).

4. Train the YOLOv5 model or use the pretrained weights provided in the repository.

5. Test the model using a webcam or video feed.

### Training the Model

If you are training the YOLOv5 model from scratch:

1. Organize the dataset in YOLO format, with images and their corresponding label files.
2. Run the YOLOv5 training script:

   ```bash
   python train.py --img 640 --batch 16 --epochs 50 --data data.yaml --weights yolov5s.pt
   ```

3. After training, save the best weights for inference.

## Usage

1. Run the main recognition script:

   ```bash
   python recognize_currency.py
   ```

2. Point the camera at an Indian currency note. The script will detect the currency and provide audio feedback on the denomination.

### Example

```plaintext
"100 Rupees note detected."
```

## Model Performance

- **Precision**: 
- **Recall**: 
- **mAP (Mean Average Precision)**: 

Include evaluation metrics and accuracy after training to provide insights into model performance.

## Future Enhancements

- Add support for recognizing torn or damaged notes.
- Integrate more advanced audio feedback options.
- Optimize model for deployment on mobile devices or Raspberry Pi for portability.

## Contributing

Feel free to open issues and submit pull requests to enhance this project. Contributions are welcome!
