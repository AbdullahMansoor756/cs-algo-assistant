# 🤖 CS Algorithm Q&A Assistant

A fine-tuned LLM that answers questions about Data Structures & Algorithms, built using QLoRA on Gemma 2B.

## 🌐 Live Demo
**[cs-algo-assistant.vercel.app](https://cs-algo-assistant.vercel.app)**

## 📸 Preview
![CS Algorithm Assistant](frontend/preview.png)

## 🎯 What it does
Ask any question about Data Structures & Algorithms and get a clear explanation:
- Binary Search, BFS, DFS, Dynamic Programming
- Time & Space Complexity analysis
- Algorithm explanations with examples

## 🏗️ Architecture
```
User → Vercel Frontend → Flask API (Colab) → Fine-tuned Gemma 2B → Response
```

## 🔧 Tech Stack
| Component | Technology |
|-----------|-----------|
| Base Model | Google Gemma 2B |
| Fine-tuning | QLoRA (r=16, alpha=32) |
| Training | Kaggle T4 GPU |
| Dataset | 4,496 custom DSA samples |
| API | Flask + ngrok |
| Frontend | HTML/CSS/JS |
| Deployment | Vercel |
| Model Hub | HuggingFace |

## 📊 Training Results
| Metric | Value |
|--------|-------|
| Initial Loss | 1.187 |
| Final Loss | 0.226 |
| Training Samples | 4,496 |
| Validation Samples | 500 |
| Epochs | 3 |
| Trainable Parameters | 19.6M (1.28%) |

## 🚀 Pipeline Steps
1. **Research & Environment Setup**
2. **Dataset Collection** — 68 handcrafted + 4,428 external DSA samples
3. **Tokenization & Preprocessing** — Gemma chat format
4. **Model Loading & QLoRA Setup** — 4-bit NF4 quantization
5. **Fine-Tuning** — 3 epochs, cosine LR scheduler
6. **Evaluation & Inference** — tested on DSA questions
7. **Deployment** — Flask API + Vercel frontend

## 🤗 Model
Model available on HuggingFace: [Abdullah756/cs-algo-assistant](https://huggingface.co/Abdullah756/cs-algo-assistant)

## 💻 Run Locally

### Backend (requires GPU)
```python
# In Google Colab with T4 GPU
# 1. Install dependencies
pip install transformers peft bitsandbytes flask flask-cors pyngrok

# 2. Load model and start API
# See notebooks/inference.ipynb
```

### Frontend
```bash
# Just open frontend/index.html in browser
# Or deploy to Vercel
```

## 📁 Project Structure
```
cs-algo-assistant/
├── frontend/
│   └── index.html          # Web interface
├── notebooks/              # Training notebooks
├── README.md
```

## ⚠️ Note
The model requires a GPU to run. The Vercel frontend shows
🔴 Model Offline when the Colab backend is not running.
To activate: run the Colab inference notebook and the
website will automatically connect.

## 👤 Author
**Abdullah Rauf**
- GitHub: [@AbdullahMansoor756](https://github.com/AbdullahMansoor756)
- HuggingFace: [Abdullah756](https://huggingface.co/Abdullah756)
