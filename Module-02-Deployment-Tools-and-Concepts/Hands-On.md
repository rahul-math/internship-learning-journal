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

✅ **End of Session 2 – Hands-on**
