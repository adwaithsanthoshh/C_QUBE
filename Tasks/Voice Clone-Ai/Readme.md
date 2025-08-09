F5-TTS: Fairytaler Text-to-Speech (Flow Matching)
F5-TTS is a next-generation, fully non-autoregressive Text-to-Speech system that uses Flow Matching and Diffusion Transformers to generate fluent, natural, and multilingual speech. It is built for speed, zero-shot capability, and expressive control.
👨‍💻 Tested By
Adwaith Santhosh
Karthik Unnikrishnan
Shravan Balakrishnan
⚙️ Features
Fully non-autoregressive TTS using Flow Matching + Diffusion Transformer (DiT)
ConvNeXt V2 for refined text representation and robust alignment
Sway Sampling — faster, high-quality inference
Achieves RTF ~0.15 for lightning-fast synthesis
Trained on 100K hours of multilingual data for expressive zero-shot, code-switching, and speed control
Modular architecture with CLI tools, Docker, Gradio web UI, and support for Triton & TensorRT-LLM
🧠 Requirements
Python 3.10 / Conda environment
GPU (CUDA / ROCm) or CPU-only fallback supported
Optional: Docker for containerized deployment
~10 GB disk space for model checkpoints
How to install 🚀?
1. Clone the repository
git clone https://github.com/SWivid/F5-TTS.git
cd F5-TTS
2. Create a Python 3.10 environment
conda create -n f5-tts python=3.10
conda activate f5-tts
3. Install dependencies
pip install torch torchaudio
pip install -e .
[ ⚠️ For inference only: ]
pip install f5-tts
4. (Optional) Docker usage
docker build -t f5tts:v1 .
docker run --rm -it --gpus all -p 7860:7860 ghcr.io/swivid/f5-tts:main f5-tts_infer-gradio --host 0.0.0.0
📦 Key Libraries Used
torch, torchaudio
gradio
docker
triton
tensorrt-llm
<p align="center"> By Adwaith, Karthik & Shravan <br> 🐍 Python &nbsp; | &nbsp; ⚡ Diffusion TTS &nbsp; | &nbsp; 🌍 Multilingual <br> ⌨️ Powered by Curiosity · 🚀 Fueled by Passion </p>
