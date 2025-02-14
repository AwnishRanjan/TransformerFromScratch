# Transformer-based NLP Model

This repository contains an implementation of a Transformer-based NLP model for sequence-to-sequence tasks such as machine translation.

# Open issues : train it in Virual Gpus for more epoches , I tried but my device is not capable to train it more :) 

## Features
- Tokenization using Hugging Face `tokenizers`
- Custom Transformer model implementation
- Training pipeline with PyTorch
- Validation and performance metrics
- GPU and MPS acceleration support

## Setup

### 1. Clone the Repository
```sh
git clone <repository-url>
cd Transformer
```

### 2. Create a Virtual Environment
```sh
python3 -m venv venv
source venv/bin/activate  # On macOS/Linux
venv\Scripts\activate  # On Windows
```

### 3. Install Dependencies
```sh
pip install -r requirements.txt
```

## Training the Model
```sh
python train.py
```

## Running Inference
To generate translations using a trained model:
```sh
python inference.py --input "Hello, how are you?"
```

## Common Issues & Troubleshooting
### MPS Backend Out of Memory (macOS)
If you encounter an out-of-memory error on MPS, try running on CPU:
```sh
export PYTORCH_MPS_HIGH_WATERMARK_RATIO=0.0
python train.py --device cpu
```
## License
This project is licensed under the MIT License.
