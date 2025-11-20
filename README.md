# Plant Disease Detection

A deep learning application for detecting plant diseases using ensemble of Xception and DenseNet121 models. The system can classify plant leaves into four categories: Healthy, Multiple Diseases, Rust, and Scab.

## Features

- **Ensemble Model**: Combines Xception and DenseNet121 for better accuracy
- **Web Interface**: User-friendly Streamlit web application
- **Real-time Prediction**: Upload images and get instant disease classification
- **Confidence Scores**: Shows prediction probabilities for all classes
- **Modern Architecture**: Built with TensorFlow 2.x and modern best practices

## Project Structure

```
Plant-Disease-Detection/
├── app.py                 # Streamlit web application
├── utils.py              # Utility functions for image processing
├── train_model.py        # Model training script
├── prepare_data.py       # Data preparation and validation
├── test_app.py          # System testing script
├── requirements.txt      # Python dependencies
├── model.h5             # Trained model (after training)
└── README.md            # This file
```

## Quick Start

### ⚠️ Important: Python Version Compatibility

**TensorFlow requires Python 3.8-3.11. Python 3.14 is not supported yet.**

### Option 1: Check Your System (Recommended First Step)
```bash
python check_python.py
```

### Option 2: Auto-Setup with Python 3.11 (Windows)
```bash
setup_python311.bat
```

### Option 3: Manual Setup

#### 1. Install Python 3.11
- Download from https://www.python.org/downloads/
- Choose Python 3.11.x (latest 3.11 version)
- ✅ Check "Add Python to PATH" during installation

#### 2. Create Virtual Environment
```bash
# Create environment with Python 3.11
py -3.11 -m venv plant_disease_env

# Activate environment (Windows)
plant_disease_env\Scripts\activate

# Activate environment (Linux/Mac)
source plant_disease_env/bin/activate
```

#### 3. Install Dependencies
```bash
pip install --upgrade pip
pip install -r requirements.txt
```

#### 4. Test the System
```bash
python test_app.py
```

#### 5. Run the Web Application
```bash
streamlit run app.py
```

### Option 4: Using Conda
```bash
conda create -n plant_disease python=3.11
conda activate plant_disease
pip install -r requirements.txt
streamlit run app.py
```

## Dataset Structure

Organize your training data in the following structure:

```
dataset/
├── healthy/
│   ├── image1.jpg
│   ├── image2.jpg
│   └── ...
├── multiple_diseases/
│   ├── image1.jpg
│   ├── image2.jpg
│   └── ...
├── rust/
│   ├── image1.jpg
│   ├── image2.jpg
│   └── ...
└── scab/
    ├── image1.jpg
    ├── image2.jpg
    └── ...
```

## Model Architecture

The system uses an ensemble approach combining:

1. **Xception Model**: Pre-trained on ImageNet, fine-tuned for plant disease detection
2. **DenseNet121 Model**: Pre-trained on ImageNet, fine-tuned for plant disease detection
3. **Ensemble**: Averages predictions from both models for improved accuracy

## Classes

- **Healthy**: Normal, disease-free plant leaves
- **Multiple Diseases**: Leaves affected by multiple diseases
- **Rust**: Leaves affected by rust disease
- **Scab**: Leaves affected by scab disease

## Requirements

- Python 3.8+
- TensorFlow 2.13+
- Streamlit 1.28+
- PIL (Pillow)
- NumPy
- Pandas
- Matplotlib
- Scikit-learn

## Usage

### Web Application

1. Start the Streamlit app: `streamlit run app.py`
2. Open your browser to the provided URL (usually http://localhost:8501)
3. Upload a plant leaf image (JPG or PNG)
4. View the prediction results and confidence scores

### Training Your Own Model

1. Prepare your dataset using `prepare_data.py`
2. Modify training parameters in `train_model.py` if needed
3. Run training: `python train_model.py`
4. The trained model will be saved as `model.h5`

## Troubleshooting

### Common Issues

1. **Import Errors**: Run `python test_app.py` to check all dependencies
2. **Model Loading Issues**: Ensure `model.h5` exists in the project directory
3. **Memory Issues**: Reduce batch size in training script
4. **Slow Predictions**: Model loading is cached after first use

### Performance Tips

- Use GPU for training if available
- Resize images to 512x512 for optimal performance
- Ensure sufficient RAM (8GB+ recommended)

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## License

This project is open source and available under the MIT License.

## Acknowledgments

- TensorFlow team for the deep learning framework
- Streamlit team for the web application framework
- Original research on plant disease detection

## Support

If you find this project helpful, please consider:
- Starring the repository
- Reporting issues
- Contributing improvements

For questions and support, please open an issue on GitHub.