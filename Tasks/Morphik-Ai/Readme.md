# 🧠 Morphik-Core (Docker Edition)

**💻 Powered by CURIOSITY • 🚀 Fueled by PASSION**

Morphik-Core is your **self-hosted, AI-powered knowledge engine**, containerized for easy deployment.  
With Docker at the helm, you can spin up an intelligent, multimodal search & retrieval system in minutes — no tangled dependencies, no manual setup pain.

---

## 📦 What's Inside?

- **Morphik API** – the brain of the operation  
- **PostgreSQL + pgvector** – your semantic memory store  
- **Ollama** – local LLM inference for blazing-fast completions and embeddings  
- **Docker Compose** – one command to run it all  

---

## ⚙️ Prerequisites

Before you launch, make sure you have:

- [Docker](https://docs.docker.com/get-docker/) installed  
- [Docker Compose v2+](https://docs.docker.com/compose/install/) ready to go  
- At least **8 GB RAM** (more = smoother performance)  
- ~**10 GB free disk space** for models and data  

---

## 🚀 Quick Start


### 1. Clone the repo
```git clone https://github.com/morphik-org/morphik-core.git```

```cd morphik-core```

### 2. Start everything
```docker compose up --build```


✅ First run will download required models & set up your database  
✅ API available at: ```http://localhost:8000```

---

### 🛠 Common Commands

| Action                       | Command                          |
|------------------------------|-----------------------------------|
| Start services               | `docker compose up`               |
| Stop services                | `docker compose down`             |
| Reset all data & containers  | `docker compose down -v`           |
| View logs                    | `docker compose logs -f`           |
| Logs for one service         | `docker compose logs <service>`    |

---

### 🎯 Configuration

1. **Copy the example config:**
    ```bash
    cp .env.example .env
    ```
2. **Edit** `.env` and `morphik.toml` to:
    - Change models (e.g., `ollama_llama` → `ollama_llama_docker`)  
    - Set API keys, secrets, and ports  
    - Adjust paths and resource limits  
3. **Restart services**:
    ```bash
    docker compose down && docker compose up -d
    ```

---

### 🩺 Health Check

- API: [http://localhost:8000](http://localhost:8000)  
- Logs: `docker compose logs -f`  
- Container status: `docker ps`

---

### 💡 Why Morphik-Core?

- **Multimodal** – handles PDFs, images, tables, even videos  
- **RAG Ready** – retrieval-augmented generation with your documents  
- **Knowledge Graphs** – visualize and query complex relationships  
- **Self-Hosted** – keep your data private while running locally or on your server  

---

### 🛠 Troubleshooting

- **Service not starting?**  
  Check logs:
  ```bash
  docker compose logs
  ```
- **Windows import issues?**  
  Mount the `core` directory:
  ```yaml
  volumes:
    - ./core:/app/core
  ```

---

### ✅ Tested By

- Adwaith  
- Karthik  
- Shravan  
