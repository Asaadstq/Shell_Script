# Introduction



Shell scripting is the practice of writing a sequence of commands in a file and having the shell execute them automatically. Instead of typing commands one by one in a terminal, you write them once in a script and run it whenever needed.
 
This guide covers the core building blocks of Bash scripting — from running your first script to working with variables, logic, loops, and functions.
 
## What is Bash
 
**Bash** stands for **Bourne Again SHell**. It serves two purposes:
 
| Role | Description |
|---|---|
| **Command-line interpreter** | Accepts and runs commands typed in a terminal |
| **Scripting language** | Executes a file of commands with support for variables, logic, and loops |
 
Bash is the default shell on most Linux distributions and was the default on macOS until 2019. It is available on virtually every Unix-based system.
 
## Why Bash Scripting?
 
- **Automation** — Run repetitive tasks automatically instead of manually
- **System control** — Interact directly with the OS, files, and processes
- **Ubiquity** — Available on every Linux and macOS machine with no installation required
- **Speed** — Scripts execute instantly with near-zero startup overhead
- **Composability** — Chain built-in tools together to build powerful workflows
## Running Your First Bash Script
 
The first line of every Bash script must be the **shebang**:
 
```bash
#!/bin/bash
```
 
This tells the OS which interpreter to use when running the file. Without it, the system may use a different shell that doesn't support all Bash syntax.
 
**1. Create the file:**
```bash
touch hello.sh
```
 
**2. Write the script:**
```bash
#!/bin/bash
 
echo "Hello, World!"
```
 
**3. Give it execute permission:**
```bash
chmod +x hello.sh
```
 
**4. Run it:**
```bash
./hello.sh
```
 
**Output:**
```
Hello, World!
```
 
---