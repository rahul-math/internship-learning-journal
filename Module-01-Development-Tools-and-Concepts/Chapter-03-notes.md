# 🖥️ Operating System Boot Process, Cloud Basics & WSL Navigation



## 🔄 System Boot Process Flow

- Power On  
- BIOS / UEFI  
- POST Check  
- Locate Drive  
- Run Bootloader  
- Select OS  
  - Linux → Kernel + systemd  
  - Windows → NT Kernel  
- User Login  

---

## ☁️ Cloud Infrastructure & Virtualization

- Cloud data centers use enterprise-grade CPUs, large RAM, and high-capacity HDDs/SSDs.
- A hypervisor is installed on physical servers to virtualize hardware resources.
- Multiple virtual machines (VMs) run on a single physical machine.
- Each VM is allocated CPU, memory, storage, and an operating system to meet user needs.

---

## 🔐 Hypervisor and Role-Based Access Control

- A hypervisor enables virtualization and manages virtual machines.
- Role-based access control (RBAC) is implemented through management tools working with the hypervisor.
- RBAC ensures controlled access based on user roles.
- This improves security and resource management in cloud environments.

---

## 🧭 Navigating the Ubuntu File System in WSL

### 📁 File Location
- Files created in WSL are stored inside the Ubuntu (Linux) file system.
- They are not saved in normal Windows directories.

---

### 📝 Creating and Managing Files

- Create a new file named `NEWFILE`:
  ```bash
  touch NEWFILE
  ```
Open or edit the file using vi:
```bash
vi NEWFILE
```


OR open/edit the file using Windows Notepad from WSL:
```bash
notepad.exe NEWFILE
```

Display the contents of the file:
```bash
cat NEWFILE
```
---
📂 Directory Navigation

Change or move to a directory:
```bash
cd <directory_name>
```

Move into the test directory:
```bash
cd test
```

List files and directories:
```
ls
```

Open or edit a file inside the directory:
```bash
vi NEWFILE
```
---
### 📍 Absolute vs Relative Paths in Linux
Absolute Path

Starts from the root directory /

Example:
```bash
/home/user/test/NEWFILE
```
Relative Path

Starts from the current directory

Example:
```bash
test/NEWFILE
```
🧹 Clear the Terminal

Clear the terminal screen:
```bash
clear
```
---
### 🆚 Windows vs Linux File System

| Feature | Windows | Linux |
|------|--------|-------|
| Root Directory | `C:\` | `/` |
| Path Separator | `\` | `/` |
| Drive Handling | Separate drives (C:, D:) | Mounted under `/mnt` |
| Case Sensitivity | Not case-sensitive | Case-sensitive |
| User Home | `C:\Users\Username` | `/home/username` |
| System Files | `C:\Windows` | `/etc`, `/bin`, `/usr` |
---

### Access Windows Files in WSL

Windows drives are mounted inside:

```
/mnt/c
/mnt/d
```

Example:

```bash
cd /mnt/c/Users
```

So:

```
C:\Users
```

becomes:

```
/mnt/c/Users
```

---

### Basic Linux Commands

Navigation:

```bash
pwd
ls
cd
clear
```

Special symbols:

```
.   → current directory
..  → parent directory
```

Paths:
- Absolute → start with /
- Relative → start from current folder

Linux uses:
```
/
```

Windows uses:
```
\
```

---

### VS Code with WSL

Open project directly:

```bash
code .
```

Benefits:
- Linux terminal inside VS Code
- Easy development
- Integrated workflow

---

### Installing UV Tool

UV is a Python automation and package management tool.

Install:

```bash
pip install uv
```

Check:

```bash
uv --version
```

---

### Installing LLM Tool

LLM CLI allows interacting with AI models from terminal.

Install:

```bash
uv tool install llm
```

Uninstall:

```bash
uv tool uninstall llm
```

---

### Setting API Keys

Gemini (Google AI Studio):

```bash
llm key set gemini
```

OpenAI / GPT:

```bash
llm key set openai
```

Keys stored in:

```
~/.bashrc or ~/.zshrc
```

---

### Running AI Models from Terminal

Examples:

```bash
llm "Explain Linux commands"
llm -m gemini-2.5 "Who are you?"
llm -m gpt-4 "Summarize this text"
```

Use cases:
- Ask questions
- Generate code
- Automate tasks
- Summarize text

---

#  Objectives of this Session

- Understand boot process
- Learn hypervisors
- Navigate Linux file system
- Use WSL effectively
- Integrate VS Code
- Install UV and LLM tools
- Use AI models from terminal

---

##  Session 3 Completed 🎉
