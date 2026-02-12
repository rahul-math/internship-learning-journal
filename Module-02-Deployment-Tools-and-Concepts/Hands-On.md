## Week 2 – Session 1 (Hands-on)

### Podman Setup
- Updated system packages.
- Installed Podman inside WSL.
- Verified installation using `podman --version`.

### Testing Podman
- Ran a test Alpine container.
- Listed images and running containers.

### Project 1: Jupyter Lab
- Pulled Jupyter base image.
- Ran Jupyter Lab with port mapping.
- Ran container in detached mode.
- Retrieved access token from logs.
- Accessed Jupyter in browser.

### Container Management
- Stopped running containers.
- Removed containers and images.

### Volume Persistence
- Created local directory for data.
- Mounted volume into Jupyter container.
- Verified notebook persistence after restart.

### Project 2: Ollama (Local LLM)
- Pulled Ollama image.
- Ran Ollama container.
- Pulled Gemma model.
- Verified LLM startup via logs.

### LLM API Interaction
- Sent chat requests using curl.
- Received JSON responses from LLM.

### Networking
- Created a custom Podman network.
- Connected Ollama container to the network.
- Verified container name-based communication.

### Project 3: Flask + LLM
- Wrote Flask app code.
- Implemented function to call Ollama API.
- Ran Flask container bound to `0.0.0.0`.
- Accessed web app in browser.
- Submitted prompts and received LLM responses.

### Debugging
- Checked container logs.
- Verified ports and network configuration.

Session 1 hands-on completed successfully.

# Week 2 – Session 2 Hands-on

This document records the practical steps performed during the session covering **GitHub Pages**, **FastAPI**, **Vercel deployment**, and **ngrok**.

---

## 1. GitHub Pages – Static Site Deployment

### Steps Performed
1. Created a new GitHub repository  
2. Added an `index.html` file  
3. Enabled GitHub Pages from repository settings  
4. Selected `main` branch as the source  

### Sample `index.html`
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>My GitHub Pages Site</title>
</head>
<body>
  <h1>Hello from GitHub Pages</h1>
  <p>This is a static website.</p>
</body>
</html>
```

### Result
- Site deployed successfully  
- Accessible via:  
  ```
  https://<username>.github.io/<repo-name>/
  ```

---

## 2. FastAPI – Basic API Setup

### Installation
```bash
pip install fastapi uvicorn
```

### Basic FastAPI App (`main.py`)
```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def read_root():
    return {"message": "Hello from FastAPI"}

@app.post("/items")
def create_item(item: dict):
    return {"received": item}
```

### Run Locally
```bash
uvicorn main:app --reload
```

### Test Endpoints
- Browser:  
  ```
  http://127.0.0.1:8000
  ```

- Interactive Docs:  
  ```
  http://127.0.0.1:8000/docs
  ```

---

## 3. FastAPI Automatic Documentation

### Accessed Routes
- Swagger UI:  
  ```
  /docs
  ```

- ReDoc UI:  
  ```
  /redoc
  ```

### Tested
- GET requests  
- POST requests with JSON body  

---

## 4. Vercel Deployment

### Install Vercel CLI
```bash
npm install -g vercel
```

### Login
```bash
vercel login
```

### Project Deployment
```bash
vercel
```

### Production Deployment
```bash
vercel --prod
```

### Required Files
- `requirements.txt`
- `vercel.json`

### Sample `vercel.json`
```json
{
  "builds": [
    {
      "src": "main.py",
      "use": "@vercel/python"
    }
  ],
  "routes": [
    {
      "src": "/(.*)",
      "dest": "main.py"
    }
  ]
}
```

---

## 5. ngrok – Exposing Local Server

### Start Tunnel
```bash
ngrok http 8000
```

### Use Cases Tested
- Sharing local FastAPI app  
- Webhook testing  

---

## Summary
This session demonstrated:
- Static site deployment using GitHub Pages  
- Creating and running a FastAPI application  
- Using automatic API documentation  
- Deploying FastAPI to Vercel  
- Exposing local servers with ngrok  

---
✅ End of Session 2 – Hands-on

---

## Week 2 – Session 3 (Hands-on)


## 🛠️ Hands-On Guide: Cloud Development & Automation

This hands-on guide covers:

-Git, WSL, and VS Code basics

-GitHub Codespaces

-Hugging Face Spaces deployment

-GitHub Actions automation

-Each section is practical and executable.
---
### 1️⃣ Hands-On: Git, WSL, and VS Code Setup
Install Git (WSL / Linux)
```bash

sudo apt update
sudo apt install git -y
```
Configure Git
```
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```
Verify Installation
```
git --version
```
Clone a Repository
```
git clone https://github.com/OWNER/REPO.git
cd REPO
```
### Branch Management
Create a new branch
```
git checkout -b feature-branch
```
Switch branches
```
git checkout main
```
Push branch to remote
```
git push origin feature-branch
```
Key Concept

- WSL → Where tools are installed

- VS Code → Editor that connects to WSL or cloud

- Git → Version control system
---
### 2️⃣ Hands-On: GitHub Codespaces
Option A: Create Codespace from GitHub UI
```
Open repository on GitHub

Click Code → Codespaces → New codespace
=
Select:

Branch

Machine type

Click Create codespace
```
Option B: Create Codespace from VS Code
```
Open command palette:

Ctrl + Shift + P   # Windows/Linux
Cmd + Shift + P    # macOS


Select:

Codespaces: Create New Codespace
```
Option C: GitHub CLI (Recommended)
Authenticate
```
gh auth login
```
Create Codespace
```
gh codespace create --repo OWNER/REPO
```
List Codespaces
```
gh codespace list
```
Open in VS Code
```
gh codespace code
```
SSH into Codespace
```
gh codespace ssh
```
Dev Container Configuration

Folder Structure
```
.devcontainer/
└── devcontainer.json

Example devcontainer.json
{
  "name": "Python Codespace",
  "image": "mcr.microsoft.com/devcontainers/python:3.10",
  "extensions": [
    "ms-python.python",
    "ms-toolsai.jupyter"
  ],
  "postCreateCommand": "pip install -r requirements.txt"
}
```
Run Code Inside Codespace
```
python --version
pip install fastapi uvicorn
```
---

### 3️⃣ Hands-On: Deploying with Hugging Face Spaces

Step 1: Create a Space

- Go to Hugging Face → Spaces

- Click Create New Space

-Select:

   - SDK: Docker

   - Visibility: Public

Step 2: Install Git LFS
```
git lfs install
```

Track large files:
```
git lfs track "*.bin"
```
Step 3: Sample FastAPI App
app.py
```
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def read_root():
    return {"message": "Hello from Hugging Face Space"}
```
Step 4: Dockerfile
```
FROM python:3.10-slim

WORKDIR /app
COPY . .

RUN pip install fastapi uvicorn

CMD ["uvicorn", "app:app", "--host", "0.0.0.0", "--port", "7860"]
```
Step 5: Push to Hugging Face
```
git clone https://huggingface.co/spaces/USERNAME/SPACE_NAME
cd SPACE_NAME

git add .
git commit -m "Deploy FastAPI app"
git push
```

✅ App will be available via a public URL
✅ Auto-build & auto-deploy

- Space Limits

- 2 CPUs, 16 GB RAM (default)

- Auto shutdown after 48 hours

- Git LFS required for large models
--- 
### 4️⃣ Hands-On: GitHub Actions Automation
Folder Structure
```
.github/
└── workflows/
    └── iss-tracker.yml

Example: Scheduled Workflow (ISS Location)
.github/workflows/iss-tracker.yml
name: ISS Location Tracker

on:
  schedule:
    - cron: "0 0 * * *"

jobs:
  fetch-iss-location:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout repository
        uses: actions/checkout@v4

      - name: Fetch ISS location
        run: |
          curl http://api.open-notify.org/iss-now.json > iss_location.json

      - name: Commit and push changes
        run: |
          git config --global user.name "github-actions"
          git config --global user.email "github-actions@github.com"
          git add iss_location.json
          git commit -m "Update ISS location" || exit 0
          git push
```
Trigger on Code Push
```
on:
  push:
    branches:
      - main
```
---
Common GitHub Actions Use Cases

- Run tests automatically

- Lint and format code

- Deploy applications

- Schedule cron jobs

- Enforce CI/CD pipelines
---
✅ End of Session 3 – Hands-on
