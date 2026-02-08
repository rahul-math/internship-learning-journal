# Chapter 1: Foundation
## Week 1 – Session 1

## WSL Installation (Ubuntu)

### Step 1: Enable Windows Features
- Open **Control Panel**
- Go to **Programs → Turn Windows features on or off**
- Enable the following options:
  - Virtual Machine Platform
  - Windows Hypervisor Platform
  - Windows Subsystem for Linux
- Click **OK**
- Restart your PC

### Step 2: Install WSL
- After restarting, install WSL by following any trusted installation video on YouTube
- Complete the installation process

### Step 3: Verify WSL Installation
Run the following command in **PowerShell**:
```bash
wsl --version
