# CS Algorithm & Coding Q&A Assistant

A fine-tuned LLM for answering computer science algorithm and coding questions with detailed explanations, working code, and complexity analysis.

## Model
- **Base Model:** Google Gemma 2B
- **Fine-tuning Method:** QLoRA (4-bit quantization + LoRA adapters)
- **Task:** Instruction tuning for CS Q&A

## Project Structure
```
cs-algo-assistant/
├── data/
│   ├── raw/          # Raw collected data
│   ├── cleaned/      # Cleaned data
│   └── processed/    # Tokenized, ready for training
├── notebooks/        # Colab notebooks for each step
├── models/
│   ├── base/         # Base model cache
│   ├── adapters/     # Trained LoRA adapters
│   └── checkpoints/  # Training checkpoints
├── src/
│   ├── data/         # Data processing scripts
│   ├── training/     # Training scripts
│   ├── evaluation/   # Evaluation scripts
│   └── deployment/   # Gradio app
├── outputs/
│   ├── logs/         # Training logs
│   ├── results/      # Evaluation results
│   └── samples/      # Sample outputs
├── configs/          # YAML config files
└── scripts/          # Utility scripts
```

## Pipeline Steps
1. Research & Environment Setup
2. Dataset Collection & Cleaning
3. Tokenization & Data Preprocessing
4. Model Loading & QLoRA Setup
5. Fine-Tuning
6. Evaluation
7. Deployment
8. Documentation

## Setup
```bash
pip install -r requirements.txt
```

## Usage
Run notebooks in order inside Google Colab with GPU enabled.
