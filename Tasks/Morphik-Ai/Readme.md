# 🧠 Morphik-Core (Docker Edition)


Morphik-Core is your **self-hosted, AI-powered knowledge engine**, containerized for easy deployment.  
With Docker at the helm, you can spin up an intelligent, multimodal search & retrieval system in minutes — no tangled dependencies, no manual setup pain.

---

## 👨‍💻 Tested By
- Adwaith Santhosh  
- Karthik Unnikrishnan  
- Shravan Balakrishnan  

---

## ⚙️ Features
- Full-stack AI knowledge engine  
- Self-hosted for maximum privacy  
- Multimodal document handling (PDFs, images, tables, videos)  
- Retrieval-Augmented Generation (RAG) ready  
- Knowledge graph generation  
- PostgreSQL + pgvector semantic search backend  
- Ollama-powered LLM inference  
- One-command deployment via Docker Compose  

---

## 🧠 Requirements
- Windows 11 / Linux 20+ / macOS (Docker Desktop installed)  
- Docker Compose v2+  
- 8 GB+ RAM (16 GB recommended)  
- 10 GB free storage for models and data  

---

## 🚀 How to Install

#### 1. Clone the repository
```bash
git clone https://github.com/morphik-org/morphik-core.git
cd morphik-core
```

#### 2. (Optional) Configure environment
```bash
cp .env.example .env
```
Edit `.env` and `morphik.toml` to:
- Change models (e.g., `ollama_llama` → `ollama_llama_docker`)  
- Set API keys, secrets, and ports  

#### 3. Start the application
```bash
docker compose up --build
```
First run will download models & set up PostgreSQL with pgvector.  
API will be available at **http://localhost:8000**.

---

## 📦 Common Commands

| Action                       | Command                          |
|------------------------------|-----------------------------------|
| Start services               | `docker compose up`               |
| Stop services                | `docker compose down`             |
| Reset all data & containers  | `docker compose down -v`           |
| View logs                    | `docker compose logs -f`           |
| Logs for one service         | `docker compose logs <service>`    |

---

## 🩺 Health Check
- API: [http://localhost:8000](http://localhost:8000)  
- Logs:  
```bash
docker compose logs -f
```
- Check container status:  
```bash
docker ps
```

---

## 🛠 Troubleshooting
- **Service not starting?**  
```bash
docker compose logs
```
- **Windows import issues?**  
Add to `docker-compose.yml`:
```yaml
volumes:
  - ./core:/app/core
```

---

<p align="center">
  By <a href="https://www.linkedin.com/in/adwaith-santhosh-046371334">Adwaith</a>, 
  <a href="https://www.linkedin.com/in/karthik-unnikrishnan-b40739334">Karthik</a> & 
  <a href="https://www.linkedin.com/in/shravan-balakrishnan">Shravan</a> <br>
  🐳 Docker &nbsp; | &nbsp; 🐘 PostgreSQL &nbsp; | &nbsp; 🤖 LLMs <br>
  💻 Powered by CURIOSITY · 🚀 Fueled by PASSION
</p>
