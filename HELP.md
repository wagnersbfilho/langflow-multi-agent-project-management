# Langflow Installation Guide (Windows with WSL – Ubuntu)

This guide describes how to install and run **Langflow** on a Windows environment using **Windows Subsystem for Linux (WSL)** with **Ubuntu**.

---

## Prerequisites

- Windows 10 or Windows 11
- Administrator access to enable WSL
- Internet connection

---

## Step 1 – Install WSL with Ubuntu

Open **PowerShell as Administrator** and run:

```powershell
wsl --install -d Ubuntu
```

After installation, restart your computer if prompted and complete the Ubuntu user setup.

## Step 2 – Update the System and Install Python 3.12

Open the Ubuntu (WSL) terminal and execute:

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install python3.12 python3.12-venv python3.12-distutils -y
```

This installs Python 3.12 and the required virtual environment and packaging tools.

## Step 3 – Create a Virtual Environment for Langflow

Create a dedicated directory for Langflow and initialize a virtual environment:

```bash
mkdir ~/langflow_env
cd ~/langflow_env
python3.12 -m venv VENV_LANGFLOW
```

Activate the virtual environment:

```bash
source VENV_LANGFLOW/bin/activate
```

## Step 4 – Install Langflow Using uv

Install the `uv` package manager:

```bash
pip install uv
```

Use `uv` to install Langflow:

```bash
uv pip install langflow
```

## Step 5 – Run Langflow

Start the Langflow application:

```bash
uv run langflow run
```

By default, Langflow will be available in your browser at:

[http://localhost:7860](http://localhost:7860)

---

## Notes

- Always activate the virtual environment before running Langflow.
- To stop Langflow, press `CTRL + C` in the terminal.
- This setup is recommended for development and academic environments.
