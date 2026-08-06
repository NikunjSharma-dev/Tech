# Tech — Generative AI & Deep Learning Systems Architecture 🤖🔥

> **Custom Transformer Models, PyTorch nanoGPT Architectures, Chinchilla Scaling Laws, and Interactive GenAI Persona Agents.**

[![PyTorch](https://img.shields.io/badge/PyTorch-2.0%2B-ee4c2c.svg)](https://pytorch.org)
[![Transformers](https://img.shields.io/badge/Transformers-Attention%20is%20All%20You%20Need-blue.svg)](#architecture)
[![Python](https://img.shields.io/badge/Python-3.11%20%7C%203.12-blue.svg)](https://python.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## 🎯 Candidate Showcase & GenAI Engineering Highlights

This repository contains custom Deep Learning architectures, PyTorch Transformer implementations, scaling law benchmarks, and interactive persona-based generative AI systems:

- **Custom PyTorch Transformer Architecture (`nanoGPT`):** Implements multi-head self-attention, causal language modeling masks, Rotary Positional Embeddings (RoPE), LayerNorm pre-activation, and GELU non-linearities.
- **Compute-Optimal Scaling Law Analysis:** Benchmarks loss vs. FLOPs across parameter counts ($10^6$ to $10^9$) following Chinchilla & Kaplan scaling trajectories to evaluate compute efficiency.
- **Interactive Persona Query Engine (`Infobot` / `Nano GPT Rapper`):** Combines campus knowledge graphs with custom prompt framing, structured RAG query routing, and real-time response generation.
- **FlashAttention & BFloat16 Training Benchmarks:** Uses PyTorch 2.0 `torch.compile` and mixed-precision `autocast` to double training throughput on GPU accelerators.

---

## 🏛️ System Architecture & Model Pipeline

```
┌────────────────────────────────────────────────────────────────────────┐
│                        DATAINGESTION & DATASET                         │
│  · Custom Corpus Tokenization · Byte-Pair Encoding (BPE / tiktoken)    │
└──────────────────────────────────┬─────────────────────────────────────┘
                                   │
                                   ▼
┌────────────────────────────────────────────────────────────────────────┐
│                      CUSTOM PYTORCH TRANSFORMER                        │
│  · Causal Multi-Head Self-Attention (FlashAttention v2)               │
│  · Feed-Forward SwiGLU / GELU Networks · Residual Connections         │
└──────────────────────────────────┬─────────────────────────────────────┘
                                   │
                                   ▼
┌────────────────────────────────────────────────────────────────────────┐
│                      TRAINING & SCALING ANALYSIS                       │
│  · Mixed Precision (AMP BFloat16) · Cosine Decay Learning Schedules    │
│  · Chinchilla Loss vs. FLOPs Trajectory Curve Notebook                 │
└──────────────────────────────────┬─────────────────────────────────────┘
                                   │
                                   ▼
┌────────────────────────────────────────────────────────────────────────┐
│                       GENAI PERSONA & UI LAYER                         │
│  · Interactive Web UI (`UI.html`) · RAG Router · Persona System Bounds │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 📁 Repository Structure

```
Tech/
├── Infobot/
│   ├── nanoGPT-master/         # PyTorch Transformer implementation
│   │   ├── model.py            # GPT architecture (Attention, MLP, Block, GPT)
│   │   ├── train.py            # Training loop with DDP + FlashAttention
│   │   ├── bench.py            # PyTorch 2.0 benchmark script
│   │   └── scaling_laws.ipynb  # Compute-optimal scaling trajectory analysis
│   ├── UI.html                 # Interactive Web UI client
│   ├── UI.jpeg                 # UI interface screenshot demo
│   └── README.md               # Infobot project specifications
└── README.md                   # Core Deep Learning repository guide
```

---

## 🛠️ Technology Stack

| Layer | Technology | Engineering Purpose |
|-------|------------|---------------------|
| **Deep Learning Framework** | PyTorch 2.0+ | Autograd, CUDA acceleration, `torch.compile` |
| **Model Architecture** | Custom GPT | Multi-Head Self-Attention, Causal Masking, LayerNorm |
| **Tokenization** | tiktoken / BPE | Subword Byte-Pair Encoding |
| **Optimization & Benchmarking** | FlashAttention v2 / AMP | BFloat16 mixed-precision, AdamW weight decay |
| **Frontend UI** | HTML5 / JavaScript / CSS3 | Interactive response streaming interface |

---

## ⚡ Quick Start

### 1. Clone & Environment Setup

```bash
git clone https://github.com/NikunjSharma-dev/Tech.git
cd Tech/Infobot/nanoGPT-master

python -m venv .venv
source .venv/bin/activate
pip install torch tiktoken numpy datasets tqdm
```

### 2. Run Benchmarks & Model Training

```bash
# Run PyTorch 2.0 speed benchmark
python bench.py

# Train micro GPT model locally
python train.py --batch_size=12 --compile=True
```

### 3. Launch UI Client
Open `Tech/Infobot/UI.html` in any modern web browser to interact with the frontend client.

---

## 📄 License

Distributed under the MIT License. See [LICENSE](LICENSE) for details.
