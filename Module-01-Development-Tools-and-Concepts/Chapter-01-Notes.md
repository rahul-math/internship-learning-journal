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
- reference : [WSL Installation Tutorial](https://youtu.be/G4AVNkd_u0E?si=vSAVOCtVasxyj_PG)

### Step 3: Verify WSL Installation
Run the following command in **PowerShell**:
```bash
wsl --version
```
### Step 4: List Available Linux Distributions
```bash
wsl --list --online
```
### Step 5: Install Ubuntu (LTS Version)
```bash
wsl --install ubuntu-24.04
```
### Step 6: Create Linux User and Password
```bash
Create default UNIX user account: rahul
New password:
Retype new password:
```
### Step 7:Use Ubuntu in Windows
Ubuntu is now ready to use in the Windows OS.
```bash
You can start it from:
Start Menu → Ubuntu
PowerShell / Command Prompt using wsl
```
Session 1 Completed..!!

