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
