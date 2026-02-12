# 📘 Chapter 6 – Containerization with Podman

## Week 2 – Session 1 (Learnings)

- Understood containerization and how it differs from virtual machines.
- Learned the difference between images and containers.
- Gained confidence using Podman as a Docker alternative.
- Learned how to run real applications inside containers.
- Understood why containers are ephemeral by default.
- Learned how volumes persist data safely.
- Understood container networking and service discovery.
- Learned how local LLMs can be containerized.
- Built a real Flask application backed by an LLM.
- Learned how frontend and backend services communicate.
- Understood common Podman issues in WSL environments.
- Built an architecture similar to real-world AI systems.

This session marked the transition from tooling to real system-building.




# Week 2 – Session 2 Learnings

This document summarizes the key concepts and takeaways from the session.

---

## 1. Containers vs Virtual Machines
- Containers are lightweight and faster than VMs
- Containers share the host OS kernel
- VMs provide stronger isolation but are resource-heavy
- Modern systems often use multiple containers (frontend, backend, database)

---

## 2. Docker vs Podman
- Both manage containers similarly
- Podman is daemon-less and more secure by default
- Docker is more widely adopted
- CLI commands are mostly compatible

---

## 3. Static Hosting with GitHub Pages
- GitHub Pages only serves static files
- No backend execution is possible
- `index.html` is mandatory
- Ideal for documentation and portfolios

---

## 4. FastAPI
- FastAPI is optimized for backend APIs
- Provides automatic validation and documentation
- Supports async programming
- Not designed for frontend rendering

---

## 5. HTTP Methods
- GET → Read data
- POST → Create data
- PUT → Replace entire resource
- PATCH → Partial update
- DELETE → Remove resource
- HEAD → Metadata only
- OPTIONS → Supported methods (CORS)

---

## 6. Serverless Deployment with Vercel
- No long-running servers
- Functions are short-lived
- Automatic GitHub-based deployments
- Preview deployments for branches

---

## 7. Vercel Limitations
- Execution time capped
- Read-only file system
- No background jobs
- WebSockets unreliable
- Not suitable for real-time systems

---

## 8. Environment Variables
- Secrets should never be hardcoded
- Environment variables improve security
- Vercel provides built-in secret management
- Same code can run across environments safely

---

## 9. ngrok
- Allows exposing local servers publicly
- Useful for testing webhooks
- Ideal for demos and collaboration

---

## 10. CORS
- Browser-level security mechanism
- Required when frontend and backend are on different origins
- Misconfigured CORS leads to blocked requests
- FastAPI provides simple middleware support

---

## Overall Takeaways
- Containers are the foundation of modern deployment
- Static and dynamic workloads must be separated
- Serverless platforms trade flexibility for simplicity
- Proper configuration is critical for successful deployment

# Week 2 – Session 3 Learnings

This document summarizes the **key learnings and takeaways** from completing the *Hands-On Guide: Cloud Development & Automation*. It focuses on **practical skills**, **conceptual understanding**, and **real-world readiness** gained throughout the process.

---

##  Git, WSL, and VS Code

### What I Learned
- How to install and configure Git in a Linux/WSL environment
- How Git tracks changes using commits, branches, and remotes
- How VS Code acts as a flexible editor that can connect to:
  - Local machines
  - WSL
  - Remote cloud environments (Codespaces)

### Key Takeaways
- Git is the foundation of collaborative and professional software development
- WSL provides a Linux-native experience on Windows for development
- VS Code is environment-agnostic and works seamlessly across local and cloud setups

---

##  GitHub Codespaces

### What I Learned
- How to create cloud-based development environments directly from GitHub
- How to use Codespaces via:
  - GitHub UI
  - VS Code
  - GitHub CLI
- How Dev Containers ensure consistent development environments

### Key Takeaways
- Codespaces eliminate “works on my machine” problems
- Development environments can be spun up instantly without local setup
- Dev containers make onboarding faster and reproducible

---

##  Hugging Face Spaces Deployment

### What I Learned
- How to deploy a live web application using Docker
- How Hugging Face Spaces automates builds and deployments
- How to expose FastAPI applications via a public URL
- How Git LFS is required for managing large model files

### Key Takeaways
- Git-based deployment simplifies application delivery
- Docker provides portability across environments
- Hugging Face Spaces is ideal for demos, ML apps, and APIs

---

##  GitHub Actions & Automation

### What I Learned
- How to write GitHub Actions workflows using YAML
- How to automate tasks using:
  - Scheduled cron jobs
  - Push-based triggers
- How CI/CD pipelines operate in real-world projects

### Key Takeaways
- Automation reduces manual effort and human error
- GitHub Actions enables CI/CD without external tools
- Scheduled workflows are powerful for data collection and maintenance tasks

---

##  End-to-End Workflow Understanding

### What I Learned
- How all tools integrate into a single development lifecycle:
  1. Write code locally or in the cloud
  2. Version control with Git
  3. Develop using Codespaces
  4. Deploy using Hugging Face Spaces
  5. Automate with GitHub Actions

### Key Takeaways
- Modern development is cloud-first and automation-driven
- Version control, deployment, and CI/CD are tightly coupled
- Understanding the full pipeline is critical for production-ready systems

---

##  Skills Gained

- Professional Git workflow (branches, commits, remotes)
- Cloud-based development using Codespaces
- Docker-based application deployment
- CI/CD automation with GitHub Actions
- Infrastructure-aware development mindset

---



