# 🚀 FastAPI App Project

This project contains a FastAPI application that uses [uv](https://docs.astral.sh/uv/) as a package and application runner. It is containerized using a multi-stage Docker build for performance and efficiency.

---

## 🛠️ How to Run Locally

```bash
git clone https://github.com/<your-username>/fastapi-uv-docker.git
cd fastapi-uv-docker
uv sync
uv run fastapi run server.py
```

> Ensure [uv is installed](https://docs.astral.sh/uv/getting-started/installation/) on your system.

---

## 🐳 Docker Support

The project is Dockerized using **multi-stage builds**.

### 🔧 Build the Docker Image

```bash
docker build -t fastapi-uv-app .
```

### 🚀 Run the Container

```bash
docker run -p 8000:8000 fastapi-uv-app
```

Access the app at `http://localhost:8000`

---

## 🧱 Dockerfile Highlights

- Uses `python:3.11-slim` base image
- Multi-stage build for lightweight image
- Installs dependencies using `uv`
- Copies built app from builder stage
- Disables virtualenv to avoid issues in Docker

---

