# Comparative-Evaluation-of-Language-Models-LLMs-within-Dialog-Agent
Comparative Evaluation of Language Models (LLMs) within Dialog Agent

# GPT-2 and T5 Training and Evaluation Pipeline

## Overview
This project focuses on training and evaluating language models, specifically GPT-2 (DialoGPT-small) and T5 (t5-small), using the Hugging Face Transformers library. The pipeline includes model initialization, dataset loading and preprocessing, training, evaluation, system usage monitoring, and visualization.

## Features
- **Model Initialization**: Loads the tokenizer and model for both GPT-2 and T5.
- **Dataset Loading & Preprocessing**:
  - Loads a persona-based chat dataset using the Hugging Face datasets library.
  - Concatenates all utterances within each dialogue and maps them to the `dialog` key.
  - Encodes the dataset with padding and truncation.
- **Training Configuration**:
  - Defines training arguments such as output directory, number of epochs, weight decay, and logging settings.
- **Training**:
  - Trains GPT-2 using the `Trainer` class from Transformers.
  - Trains T5 using the same `Trainer` class.
- **System Usage Monitoring**:
  - Collects and visualizes CPU and memory usage during training.
  - Utilizes the `psutil` library for system resource tracking.
- **Evaluation**:
  - Calculates **BLEU scores** by generating responses and comparing them with reference texts.
  - Computes **distinct metrics (DIST-1 & DIST-2)** to measure response diversity.
- **Visualization**:
  - Plots **self-attention matrices** for GPT-2 and T5.

## Installation
To set up the environment, install the required dependencies:
```bash
pip install transformers datasets torch psutil matplotlib
```

## Usage
Run the training and evaluation pipeline with:
```bash
python train.py
```

## Evaluation Metrics
- **BLEU Score**: Measures the similarity between generated and reference responses.
- **DIST-1 & DIST-2**: Measures the diversity of generated text based on unique n-grams.

## System Monitoring
- CPU and memory usage data are collected and plotted to analyze system performance during training.

## Attention Visualization
- Self-attention patterns for GPT-2 and T5 models are visualized for better interpretability.

## Contributing
Feel free to open issues or submit pull requests for improvements.

## License
This project is licensed under the MIT License.


