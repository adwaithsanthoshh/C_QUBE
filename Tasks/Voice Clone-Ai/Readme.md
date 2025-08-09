# F5‑TTS: Fairytaler Text‑to‑Speech (Flow Matching)

**F5‑TTS** is a next-generation, fully non‑autoregressive Text‑to‑Speech system that uses flow matching and Diffusion Transformers to generate fluent, faithful, and natural speech. It supports multilingual zero‑shot synthesis, is extremely fast, and offers expressive control.

---

## 👨‍💻 Tested By

- Adwaith Santhosh  
- Karthik Unnikrishnan  
- Shravan Balakrishnan

---

## ⚙️ Features

- Fully non‑autoregressive TTS with Flow Matching + Diffusion Transformer (DiT)  
- ConvNeXt V2 for robust text representation and alignment  
- Sway Sampling for faster, high-quality inference  
- RTF ~0.15 for lightning-fast synthesis  
- Trained on 100K+ hours of multilingual data  
- Supports zero‑shot, code‑switching, speed control, and emotional styles  
- Modular architecture with CLI, Docker, Gradio UI, Triton & TensorRT-LLM support

---

## 🧠 Requirements

- Python 3.10  
- GPU (CUDA / ROCm) or CPU-only fallback  
- ~10 GB disk space for model checkpoints  
- Optional: Docker for containerized deployment

---

## How to install 🚀?

#### 1. Clone the repository

```bash
git clone https://github.com/SWivid/F5‑TTS.git
cd F5‑TTS
```

#### 2. Create a Python environment

```bash
conda create -n f5-tts python=3.10
conda activate f5-tts
```

#### 3. Install dependencies

```bash
pip install torch torchaudio
pip install -e .
```
*For inference only:*
```bash
pip install f5-tts
```

#### 4. (Optional) Docker usage

```bash
docker build -t f5tts:v1 .
docker run --rm -it --gpus all -p 7860:7860 ghcr.io/swivid/f5-tts:main f5-tts_infer-gradio --host 0.0.0.0
```

---

## 📦 Key Commands

- CLI inference: `f5-tts_infer-cli --model F5-TTS_Base --gen_text "Hello world"`  
- Gradio Web UI: `f5-tts_infer-gradio --port 7860`  
- Finetune with Gradio: `f5-tts_finetune-gradio`  
- Custom config: `f5-tts_infer-cli -c custom.toml`

---

<p align="center">
  By Adwaith, Karthik & Shravan <br>
  🐍 Python &nbsp; | &nbsp; ⚡ Diffusion TTS &nbsp; | &nbsp; 🌐 Multilingual <br>
  ❤️ Powered by curiosity · 🚀 Fueled by passion
</p>
