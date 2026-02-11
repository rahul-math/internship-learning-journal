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
