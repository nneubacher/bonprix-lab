# 🛍️ Bon Prix Personalization Lab - Complete Beginner's Guide

> **Welcome!** This guide will help you run an AI-powered shopping assistant demo, even if you've never programmed before. We'll walk through every step together, explaining everything in plain English.

---

## 📖 Table of Contents

1. [What This Demo Does (In Simple Terms)](#-what-this-demo-does-in-simple-terms)
2. [Part 1: Installing Python](#-part-1-installing-python-choose-your-operating-system)
3. [Part 2: Understanding Virtual Environments](#-part-2-understanding-virtual-environments-the-sandbox-concept)
4. [Part 3: Setting Up Your Project Environment](#-part-3-setting-up-your-project-environment)
5. [Part 4: Setting Up Your IBM Credentials](#-part-4-setting-up-your-ibm-credentials)
6. [Part 5: Understanding the Notebook Variants](#-part-5-understanding-the-notebook-variants)
7. [Part 6: Running the Demo](#-part-6-running-the-demo)
8. [Part 7: Verification Checklist](#-part-7-verification-checklist)
9. [Part 8: Troubleshooting Guide](#-part-8-troubleshooting-guide)
10. [Part 9: Understanding What You Built](#-part-9-understanding-what-you-built)
11. [Part 10: Next Steps](#-part-10-next-steps-and-learning-resources)
12. [Appendix](#-appendix)

---

## 🎯 What This Demo Does (In Simple Terms)

### The Problem
Imagine you're shopping online for a dress. There are 500 customer reviews. Some people love it, some hate it. Reading all 500 reviews would take hours! Plus, what matters to you (like "Is it comfortable?") might be different from what matters to someone else (like "Is it formal enough for work?").

### The Solution
This demo creates a **personal shopping assistant** powered by artificial intelligence (AI). Here's what it does:

1. **Learns about you**: It looks at products you've liked before to understand your preferences
2. **Reads all the reviews**: It processes hundreds of customer reviews instantly
3. **Creates a personalized summary**: It tells you specifically what YOU would want to know about the product
4. **Shows you visualizations**: It creates charts showing product ratings and features

### Real-World Example
Let's say you're "Nadine" who loves comfortable, high-quality clothes. When you look at a new dress:
- **Without AI**: You see "4.2 stars (487 reviews)" - not very helpful!
- **With this AI**: You see "Based on your preference for comfort, customers say this dress is very soft and breathable. However, some mention it runs small, so consider sizing up."

### What You'll See at the End
A web interface where you can:
- Select different customers (each with different preferences)
- Choose products to analyze
- See personalized AI-generated summaries
- View interactive charts showing product features

**Time to complete**: 45-90 minutes for first-time setup
**No programming experience needed**: We'll explain everything step by step!

---

## 🖥️ Part 1: Installing Python (Choose Your Operating System)

### What is Python?
Python is a programming language - think of it as the "language" that computers understand. It's like English for humans, but for computers. We need Python installed on your computer to run this demo.

**Which version do we need?** Python 3.11 (the version number is like a model year for cars)

---

### 🪟 Option A: Installing Python on Windows

#### Step 1: Download Python

1. Open your web browser (Chrome, Edge, Firefox, etc.)
2. Go to: https://www.python.org/downloads/
3. You'll see a big yellow button that says **"Download Python 3.11.x"**
4. Click that button to download the installer
5. Wait for the download to complete (usually takes 1-2 minutes)

#### Step 2: Run the Installer

1. Find the downloaded file (usually in your "Downloads" folder)
2. It will be named something like `python-3.11.x-amd64.exe`
3. **Double-click** the file to start the installer
4. **⚠️ CRITICAL STEP**: At the bottom of the first screen, you'll see a checkbox that says **"Add Python 3.11 to PATH"**
   - **YOU MUST CHECK THIS BOX!** This is the most common mistake beginners make
   - This checkbox tells Windows where to find Python
   - Without it, nothing will work later
5. Click **"Install Now"**
6. Wait for installation (takes 2-5 minutes)
7. When you see "Setup was successful", click **"Close"**

#### Step 3: Verify Python is Installed

Now let's make sure Python is working correctly.

1. **Open Command Prompt**:
   - Press the **Windows key** on your keyboard (the one with the Windows logo)
   - Type: `cmd`
   - Press **Enter**
   - A black window will open - this is the Command Prompt

2. **Check Python version**:
   - In the black window, type exactly: `python --version`
   - Press **Enter**
   - You should see something like: `Python 3.11.x`

3. **Check pip (Python's package installer)**:
   - Type: `pip --version`
   - Press **Enter**
   - You should see something like: `pip 23.x.x from ...`

#### ✅ Success Looks Like:
```
C:\Users\YourName> python --version
Python 3.11.9

C:\Users\YourName> pip --version
pip 23.2.1 from C:\Users\YourName\AppData\Local\Programs\Python\Python311\lib\site-packages\pip (python 3.11)
```

#### ❌ If You See an Error:

**Error: "python is not recognized as an internal or external command"**
- **Problem**: Python wasn't added to PATH (you missed the checkbox in Step 2)
- **Solution**: 
  1. Uninstall Python (Control Panel → Programs → Uninstall a program)
  2. Download the installer again
  3. Run it again, but this time CHECK the "Add Python to PATH" box
  4. Try the verification steps again

**Error: "Access is denied"**
- **Problem**: You need administrator permissions
- **Solution**: Right-click the installer and choose "Run as administrator"

---

### 🍎 Option B: Installing Python on macOS

#### Step 1: Download Python

1. Open Safari (or your preferred browser)
2. Go to: https://www.python.org/downloads/
3. Click the big yellow button: **"Download Python 3.11.x"**
4. Wait for the download (1-2 minutes)

#### Step 2: Run the Installer

1. Find the downloaded file (usually in your "Downloads" folder)
2. It will be named something like `python-3.11.x-macos11.pkg`
3. **Double-click** the file
4. Follow the installation wizard:
   - Click **"Continue"** through the introduction screens
   - Click **"Agree"** to the license
   - Click **"Install"**
   - Enter your Mac password when prompted
5. Wait for installation (2-5 minutes)
6. Click **"Close"** when finished

#### Step 3: Verify Python is Installed

1. **Open Terminal**:
   - Press **Command (⌘) + Space** to open Spotlight
   - Type: `terminal`
   - Press **Enter**
   - A white or black window will open - this is Terminal

2. **Check Python version**:
   - In Terminal, type: `python3 --version`
   - Press **Enter**
   - You should see: `Python 3.11.x`

3. **Check pip**:
   - Type: `pip3 --version`
   - Press **Enter**
   - You should see: `pip 23.x.x from ...`

#### ✅ Success Looks Like:
```
YourMac:~ yourname$ python3 --version
Python 3.11.9

YourMac:~ yourname$ pip3 --version
pip 23.2.1 from /Library/Frameworks/Python.framework/Versions/3.11/lib/python3.11/site-packages/pip (python 3.11)
```

#### 📝 Important Note for Mac Users:
On Mac, you need to use `python3` and `pip3` (with the "3") instead of just `python` and `pip`. This is because Macs come with an older version of Python pre-installed, and we want to use the new version you just installed.

#### ❌ If You See an Error:

**Error: "command not found: python3"**
- **Problem**: Installation didn't complete properly
- **Solution**: Try installing again, or check if you have Xcode Command Line Tools:
  ```bash
  xcode-select --install
  ```

---

### 🐧 Option C: Installing Python on Linux

#### For Ubuntu/Debian-based Systems:

1. **Open Terminal**:
   - Press **Ctrl + Alt + T**
   - Or search for "Terminal" in your applications

2. **Update package list**:
   ```bash
   sudo apt update
   ```
   - Type your password when prompted
   - Press **Enter**

3. **Install Python 3.11**:
   ```bash
   sudo apt install python3.11 python3.11-venv python3-pip
   ```
   - Type `Y` when asked to confirm
   - Wait for installation (2-5 minutes)

4. **Verify installation**:
   ```bash
   python3.11 --version
   pip3 --version
   ```

#### For Fedora/RHEL-based Systems:

1. **Open Terminal**

2. **Install Python 3.11**:
   ```bash
   sudo dnf install python3.11 python3-pip
   ```

3. **Verify installation**:
   ```bash
   python3.11 --version
   pip3 --version
   ```

#### ✅ Success Looks Like:
```
user@linux:~$ python3.11 --version
Python 3.11.9

user@linux:~$ pip3 --version
pip 23.2.1 from /usr/lib/python3/dist-packages/pip (python 3.11)
```

---

## 🏠 Part 2: Understanding Virtual Environments (The "Sandbox" Concept)

### What is a Virtual Environment?

Think of your computer as a house with many rooms. Each room (project) might need different tools:
- Your kitchen needs cooking tools
- Your garage needs car tools
- Your garden needs gardening tools

If you mixed all these tools together in one big pile, it would be chaos! You might accidentally use a garden hose in your kitchen.

**A virtual environment is like having a separate toolbox for each room.** It keeps all the tools (Python packages) for this project separate from other projects.

### Why Do We Need This?

**Without virtual environments:**
- Installing packages for this project might break other Python projects
- Different projects might need different versions of the same tool
- Your computer gets cluttered with packages you don't need anymore

**With virtual environments:**
- Each project has its own clean, isolated space
- You can delete a project's environment without affecting anything else
- You know exactly what packages each project needs

### Visual Representation:

```
Your Computer
│
├── Global Python (the main installation)
│   └── Basic Python only
│
├── Project 1 Virtual Environment
│   ├── Python
│   └── Project 1's specific packages
│
├── Project 2 Virtual Environment
│   ├── Python
│   └── Project 2's specific packages
│
└── Bon Prix Project Virtual Environment (.venv)
    ├── Python
    └── pandas, gradio, jupyterlab, etc.
```

### Key Terms:
- **venv**: Short for "virtual environment"
- **.venv**: The folder name we'll use (the dot makes it hidden on Mac/Linux)
- **Activate**: Turn on the virtual environment (like opening your toolbox)
- **Deactivate**: Turn off the virtual environment (like closing your toolbox)

---

## 📦 Part 3: Setting Up Your Project Environment

### Step 1: Download the Project Files

You need to get all the project files onto your computer.

**Option A: If you have the files as a ZIP:**
1. Download the ZIP file
2. Right-click it and choose "Extract All" (Windows) or double-click (Mac)
3. Remember where you extracted it (like `C:\Users\YourName\Downloads\bonprix` or `/Users/yourname/Downloads/bonprix`)

**Option B: If you're using Git:**
```bash
git clone [repository-url]
cd bonprix
```

### Step 2: Open Your Command Line/Terminal

**Windows:**
1. Press **Windows key**
2. Type: `cmd` or `powershell`
3. Press **Enter**

**macOS:**
1. Press **Command (⌘) + Space**
2. Type: `terminal`
3. Press **Enter**

**Linux:**
1. Press **Ctrl + Alt + T**

### Step 3: Navigate to the Project Folder

You need to tell your computer to "go to" the project folder. This is like walking to a specific room in your house.

**The command is `cd` (which stands for "change directory"):**

**Windows example:**
```bash
cd C:\Users\YourName\Downloads\bonprix
```

**Mac/Linux example:**
```bash
cd /Users/yourname/Downloads/bonprix
```

**💡 Tip**: You can drag and drop the folder into the terminal window, and it will automatically type the path for you!

**How to know you're in the right place:**
Type `dir` (Windows) or `ls` (Mac/Linux) and press Enter. You should see files like:
- `bonprix_lab-wx.ipynb`
- `personalization_users_visible.csv`
- `reviews_all_users_in_shop.csv`
- `.env.template`

### Step 4: Create Your Virtual Environment

Now we'll create that "separate toolbox" for this project.

**For all operating systems, type this command:**

**Windows:**
```bash
python -m venv .venv
```

**macOS/Linux:**
```bash
python3 -m venv .venv
```

**What this command means:**
- `python` or `python3`: Use Python
- `-m venv`: Run the virtual environment module
- `.venv`: Name the folder ".venv"

**What's happening:**
Python is creating a new folder called `.venv` that contains a complete, isolated copy of Python just for this project. This takes about 30 seconds.

**You'll know it worked when:**
- The command finishes without errors
- You can see a new `.venv` folder (you might need to show hidden files to see it)

### Step 5: Activate Your Virtual Environment

Now we need to "open the toolbox" - activate the virtual environment.

**⚠️ IMPORTANT**: You need to activate the virtual environment EVERY TIME you open a new terminal window to work on this project.

#### Windows (Command Prompt):
```bash
.venv\Scripts\activate.bat
```

#### Windows (PowerShell):
```powershell
.venv\Scripts\Activate.ps1
```

**⚠️ PowerShell Users**: If you get an error about execution policies, run this first:
```powershell
Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned
```
Then try activating again.

#### macOS/Linux:
```bash
source .venv/bin/activate
```

**✅ How to know it worked:**
You'll see `(.venv)` appear at the beginning of your command line:

**Windows:**
```
(.venv) C:\Users\YourName\Downloads\bonprix>
```

**Mac/Linux:**
```
(.venv) yourname@computer:~/Downloads/bonprix$
```

That `(.venv)` is like a badge that says "You're now working in the virtual environment!"

### Step 6: Install Required Packages

Now we'll install all the tools (packages) this project needs. Think of this like buying all the ingredients before cooking a meal.

**We've made this easier! All required packages are listed in a file called `requirements.txt`.**

**Copy and paste this command:**

```bash
pip install -r requirements.txt
```

**Press Enter and wait.** This will take a few minutes.

**What this does:** The `-r requirements.txt` tells pip to read the list of packages from the requirements.txt file and install them all automatically.

**What each package does (in simple terms):**

| Package | What It Does | Analogy |
|---------|--------------|---------|
| **pandas** | Works with data tables | Like Microsoft Excel for Python |
| **gradio** | Creates web interfaces | Builds the buttons and dropdowns you'll click |
| **plotly** | Makes interactive charts | Creates the graphs and visualizations |
| **python-dotenv** | Manages secret keys | Keeps your passwords safe and organized |
| **jupyterlab** | The notebook environment | Like Microsoft Word, but for code |
| **ibm-watsonx-ai** | Connects to IBM's AI | The phone line to IBM's smart AI brain |
| **ollama** | Local AI (optional) | An AI that runs on your computer |
| **langfuse** | Tracks AI performance | Like a fitness tracker, but for AI |
| **iprogress** | Shows progress bars | Visual feedback while things load |

**What you'll see:**
```
Collecting pandas
  Downloading pandas-2.x.x-cp311-cp311-win_amd64.whl (11.5 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 11.5/11.5 MB 5.2 MB/s eta 0:00:00
Collecting gradio
  Downloading gradio-4.x.x-py3-none-any.whl (12.3 MB)
...
Successfully installed pandas-2.x.x gradio-4.x.x plotly-5.x.x ...
```

**✅ Success looks like:**
- No red error messages
- Ends with "Successfully installed..." listing all the packages
- You're back at the command prompt with `(.venv)` still showing

**⚠️ Common Issues:**

**"pip is not recognized"**
- Make sure your virtual environment is activated (you should see `(.venv)`)
- If not, go back to Step 5

**"Could not find a version that satisfies the requirement"**
- Check your internet connection
- Make sure you're using Python 3.11 (run `python --version` to check)

**Installation is very slow**
- This is normal! Some packages are large
- Be patient, it can take up to 5 minutes

---

## 🔑 Part 4: Setting Up Your IBM Credentials

### What Are Credentials?

Credentials are like a username and password that let this demo talk to IBM's AI service. Think of it like logging into Netflix - you need an account to access the service.

### What You Need:

You need three pieces of information from your IBM Cloud account:

1. **WATSONX_API_KEY**: Your secret password (like a very long password)
2. **WATSONX_PROJECT_ID**: Your project's ID number (like an account number)
3. **WATSONX_URL**: The web address of IBM's AI service (automatically set to us-south for all students)

### 🎯 Two Ways to Configure Credentials

You have **two options** for providing your credentials. Choose the one that works best for you:

#### Option 1: Using .env File (RECOMMENDED - More Secure)

This is the recommended approach because it keeps your credentials separate from your code.

#### Option 2: Hardcoding in Notebook (Quick Testing Only)

If you have trouble with the .env file, you can enter credentials directly in the notebook code.

---

### Step 1: Find Your IBM watsonx.ai Credentials

**If you already have IBM Cloud access:**

1. **Log into IBM Cloud**:
   - Go to: https://cloud.ibm.com
   - Sign in with your IBM ID

2. **Find your API Key**:
   - Click your name in the top right corner
   - Select **"Manage"** → **"Access (IAM)"**
   - Click **"API keys"** in the left sidebar
   - Click **"Create"** to make a new API key (or use an existing one)
   - **Copy the API key** - you'll need this in a moment
   - ⚠️ **Save it somewhere safe!** You can't see it again after closing the window

3. **Find your Project ID**:
   - Go to: https://dataplatform.cloud.ibm.com
   - Click on your watsonx.ai project
   - Click the **"Manage"** tab
   - Look for **"Project ID"**
   - **Copy the Project ID**

4. **URL (No Action Needed)**:
   - For all students, the URL is: `https://us-south.ml.cloud.ibm.com`
   - The code automatically uses this as a fallback, so you don't need to worry about it
   - If your .env file has a different URL or it's empty, the code will use us-south automatically

---

### Step 2A: Setup Using .env File (RECOMMENDED)

The `.env` file is where we'll store your credentials securely.

1. **Find the file named `.env.template`** in your project folder

2. **Rename it to `.env`**:
   - **Windows**: Right-click → Rename → change to `.env`
   - **Mac**: Right-click → Rename → change to `.env`
   - **Linux**: In terminal: `mv .env.template .env`

3. **Open the `.env` file** in a text editor:
   - **Windows**: Right-click → Open with → Notepad
   - **Mac**: Right-click → Open With → TextEdit
   - **Linux**: Use nano, vim, or any text editor

4. **Fill in your credentials**:

The file has detailed comments explaining each field. You only need to fill in:
```
WATSONX_API_KEY="your-api-key-here"
WATSONX_PROJECT_ID="your-project-id-here"
```

**Example:**
```
WATSONX_API_KEY="oQfC_1234567890abcdefghijklmnopqrstuvwxyz"
WATSONX_URL="https://us-south.ml.cloud.ibm.com"
WATSONX_PROJECT_ID="a2d3b93f-1234-5678-90ab-cdef12345678"
```

**📝 Important Notes:**
- Keep the quotes around your keys
- Don't add extra spaces before or after the `=` sign
- The URL line can be left as-is (or even empty - the code will use us-south automatically)
- The Langfuse keys are optional (only needed for the `*_tracing.ipynb` notebooks)

5. **Save the file**:
   - Press **Ctrl + S** (Windows/Linux) or **Command + S** (Mac)
   - Close the text editor

6. **Verify it works**:
   - When you run the notebook, you should see: `✅ Credentials erfolgreich aus .env geladen`
   - If you see an error, check that your API key and Project ID are correct

---

### Step 2B: Setup Using Hardcoded Credentials (Alternative)

If you prefer to enter credentials directly in the code (or if the .env file isn't working):

1. **Open your notebook** (e.g., `bonprix_lab-wx.ipynb`)

2. **Find the configuration section** (near the top of the first code cell):
   ```python
   # OPTION 1: Credentials aus .env Datei (EMPFOHLEN für Sicherheit)
   USE_ENV_FILE = True
   
   # OPTION 2: Credentials direkt hier eintragen (NUR für schnelle Tests)
   HARDCODED_API_KEY = ""
   HARDCODED_PROJECT_ID = ""
   ```

3. **Change `USE_ENV_FILE` to `False`**:
   ```python
   USE_ENV_FILE = False
   ```

4. **Fill in your credentials**:
   ```python
   HARDCODED_API_KEY = "oQfC_1234567890abcdefghijklmnopqrstuvwxyz"
   HARDCODED_PROJECT_ID = "a2d3b93f-1234-5678-90ab-cdef12345678"
   ```

5. **Save the notebook** (Ctrl+S or Command+S)

6. **Verify it works**:
   - When you run the cell, you should see: `✅ Hardcoded Credentials werden verwendet`

⚠️ **Warning**: This method is less secure because your credentials are in the code. Only use this for quick testing or if the .env file isn't working.

---

### 🔍 Troubleshooting Credentials

#### Error: "WATSONX_API_KEY ist nicht gesetzt!"

**Cause**: Your API key is missing or empty.

**Solutions**:
1. **If using .env file**:
   - Check that you renamed `.env.template` to `.env`
   - Open `.env` and verify the API key is filled in
   - Make sure there are no extra spaces: `WATSONX_API_KEY="your-key"` (not `WATSONX_API_KEY = "your-key"`)
   - Try restarting JupyterLab after editing the .env file

2. **If using hardcoded credentials**:
   - Make sure `USE_ENV_FILE = False`
   - Check that `HARDCODED_API_KEY` has your actual API key
   - Verify the quotes are correct: `HARDCODED_API_KEY = "your-key"`

#### Error: "WATSONX_PROJECT_ID ist nicht gesetzt!"

**Cause**: Your Project ID is missing or empty.

**Solutions**: Same as above, but for the Project ID field.

#### Error: "API Key ist ungültig oder abgelaufen"

**Cause**: The API key is incorrect or has been deleted.

**Solutions**:
1. Go back to IBM Cloud and verify your API key
2. Create a new API key if needed
3. Copy the new key carefully (no extra spaces)
4. Update your .env file or hardcoded value

#### Error: "Project ID ist falsch"

**Cause**: The Project ID doesn't match your watsonx.ai project.

**Solutions**:
1. Go to https://dataplatform.cloud.ibm.com
2. Open your project
3. Click "Manage" tab
4. Copy the exact Project ID
5. Update your .env file or hardcoded value

#### The notebook runs but shows: "⚠️ Keine URL angegeben, verwende Standard: us-south"

**This is normal!** The code automatically uses the us-south region (which is correct for all students). You can ignore this message.

---

### ⚠️ Security Warning:

**NEVER share your .env file or credentials with anyone!** They contain your secret credentials.
- Don't upload them to GitHub or any public place
- Don't email them
- Don't post them in chat or forums
- Think of them like your bank password

The `.gitignore` file in this project is already set up to prevent accidentally uploading `.env` to GitHub.

**If you used hardcoded credentials**: Remember to remove them before sharing your notebook with others!

---

## 📓 Part 5: Understanding the Notebook Variants

### What is a Jupyter Notebook?

A Jupyter Notebook is like a digital lab notebook. It lets you:
- Write and run code in small chunks (called "cells")
- See results immediately
- Add notes and explanations
- Create visualizations

Think of it like a recipe book where you can actually cook the recipe right on the page and see how it turns out!

### The Four Notebook Options

This project has four different notebooks. They all do the same basic thing (create personalized shopping recommendations), but they differ in two ways:

1. **Which AI they use** (Cloud vs. Local)
2. **Whether they track performance** (Tracing)

Here's a breakdown:

| Notebook | AI Provider | Tracing | Best For |
|----------|-------------|---------|----------|
| **bonprix_lab-wx.ipynb** | IBM watsonx.ai (Cloud) | ❌ No | ⭐ **RECOMMENDED FOR BEGINNERS** |
| **bonprix_lab-wx_tracing.ipynb** | IBM watsonx.ai (Cloud) | ✅ Yes | Advanced users who want to see AI performance metrics |
| **bonprix_lab-ollama.ipynb** | Ollama (Local) | ❌ No | Users who want to run AI on their own computer |
| **bonprix_lab-ollama_tracing.ipynb** | Ollama (Local) | ✅ Yes | Advanced local AI users |

### Which One Should You Use?

**Use this decision guide:**

```
Do you have IBM watsonx.ai credentials?
│
├─ YES → Do you want to see detailed AI performance metrics?
│        │
│        ├─ YES → Use: bonprix_lab-wx_tracing.ipynb
│        │
│        └─ NO → Use: bonprix_lab-wx.ipynb ⭐ START HERE
│
└─ NO → Do you want to install Ollama and run AI locally?
         │
         ├─ YES → Use: bonprix_lab-ollama.ipynb
         │         (Note: You'll need to install Ollama first)
         │
         └─ NO → Get IBM watsonx.ai credentials first
```

### Detailed Explanation of Each Option:

#### 1. bonprix_lab-wx.ipynb ⭐ RECOMMENDED

**What it uses**: IBM watsonx.ai (cloud-based AI)

**Pros:**
- Simplest to set up (just needs API keys)
- Uses powerful enterprise AI
- No need to download large AI models
- Works on any computer

**Cons:**
- Requires IBM Cloud account
- Uses internet connection
- May have usage costs (check your IBM plan)

**When to use**: If you have IBM credentials and want the easiest experience

#### 2. bonprix_lab-wx_tracing.ipynb

**What it uses**: IBM watsonx.ai + Langfuse tracking

**Pros:**
- Everything from option 1
- Plus: See detailed metrics (response time, token usage, costs)
- Great for understanding AI performance

**Cons:**
- Requires Langfuse account (free tier available)
- Slightly more complex setup
- More information to process

**When to use**: If you want to learn how AI performs behind the scenes

#### 3. bonprix_lab-ollama.ipynb

**What it uses**: Ollama (local AI on your computer)

**Pros:**
- No API keys needed
- No internet required (after initial setup)
- No usage costs
- Complete privacy (data never leaves your computer)

**Cons:**
- Must install Ollama separately
- Must download large AI models (several GB)
- Slower on older computers
- Requires more disk space

**When to use**: If you want to run everything locally or don't have IBM access

#### 4. bonprix_lab-ollama_tracing.ipynb

**What it uses**: Ollama + Langfuse tracking

**Pros:**
- Everything from option 3
- Plus: Performance tracking

**Cons:**
- Most complex setup
- Requires both Ollama and Langfuse

**When to use**: Advanced users who want local AI with performance metrics

### Our Recommendation for Beginners:

**Start with `bonprix_lab-wx.ipynb`**

Why?
- Simplest setup (you already have the credentials)
- Fastest to get results
- Most reliable
- You can always try the other notebooks later

---

## 🚀 Part 6: Running the Demo

Now for the exciting part - actually running the demo!

### Step 1: Start JupyterLab

Make sure:
- ✅ Your virtual environment is activated (you see `(.venv)`)
- ✅ You're in the project folder
- ✅ Your `.env` file is configured

**Type this command:**
```bash
jupyter lab
```

**What happens:**
1. You'll see some text appear in the terminal
2. After a few seconds, your web browser will automatically open
3. You'll see the JupyterLab interface

**What you'll see in the terminal:**
```
[I 2024-01-27 10:15:30.123 ServerApp] Jupyter Server 2.x.x is running at:
[I 2024-01-27 10:15:30.123 ServerApp] http://localhost:8888/lab?token=abc123...
[I 2024-01-27 10:15:30.123 ServerApp] Use Control-C to stop this server
```

**What you'll see in your browser:**
A file browser showing all your project files on the left side.

**💡 Tips:**
- Don't close the terminal window - JupyterLab needs it running
- If the browser doesn't open automatically, copy the URL from the terminal (the one that starts with `http://localhost:8888`)
- The terminal will show log messages - this is normal

### Step 2: Open Your Notebook

1. In the JupyterLab file browser (left side), find **`bonprix_lab-wx.ipynb`**
2. **Double-click** it to open
3. The notebook will open in the main area

**What you'll see:**
- A document with text and code blocks
- Each code block is called a "cell"
- Some cells have explanatory text (like this guide)
- Some cells have code (Python commands)

### Step 3: Understanding the Notebook Interface

**Key parts of the interface:**

```
┌─────────────────────────────────────────────────────┐
│  File  Edit  View  Run  Kernel  Tabs  Settings      │  ← Menu bar
├─────────────────────────────────────────────────────┤
│  ▶ Run  ⏸ Stop  ⟳ Restart  [Kernel: Python 3.11]   │  ← Toolbar
├─────────────────────────────────────────────────────┤
│                                                      │
│  📝 Text Cell (Markdown)                            │
│  This is explanatory text                           │
│                                                      │
│  ┌────────────────────────────────────────────┐    │
│  │ # This is a code cell                       │    │  ← Code Cell
│  │ print("Hello, World!")                      │    │
│  └────────────────────────────────────────────┘    │
│                                                      │
│  Output: Hello, World!                              │  ← Output Area
│                                                      │
└─────────────────────────────────────────────────────┘
```

**How to run a cell:**
- **Method 1**: Click the cell, then click the ▶ "Run" button in the toolbar
- **Method 2**: Click the cell, then press **Shift + Enter** on your keyboard
- **Method 3**: Click the cell, then press **Ctrl + Enter** (runs but doesn't move to next cell)

### Step 4: Running the Notebook Cell-by-Cell

Now we'll go through each cell and explain what it does. **Run them in order from top to bottom.**

#### 📘 Cell 1: Title and Introduction

**What it looks like:**
```markdown
# 🛍️ Case Study: Bon Prix Personalization Lab
...
```

**What it is:** Just text explaining the project
**What to do:** Read it, then move to the next cell (you don't need to "run" text cells)

---

#### 💻 Cell 2: Setup and Imports

**What it looks like:**
```python
# ==========================================
# 1. WERKZEUGKASTEN & SETUP
# ==========================================
import pandas as pd
import gradio as gr
...
```

**What it does:**
- Loads all the tools (packages) we installed earlier
- Sets up file paths
- Creates functions to save/load cached results

**How to run it:**
1. Click on the cell
2. Press **Shift + Enter**

**What you'll see:**
- The cell will run (you might see a `[*]` briefly, then `[1]`)
- Usually no output (which is good!)
- Might see a warning about iprogress - this is normal and safe to ignore

**⏱️ Time:** 2-5 seconds

**✅ Success looks like:**
- No red error messages
- Cell number appears: `[1]`
- You can move to the next cell

**❌ If you see an error:**
- "ModuleNotFoundError: No module named 'pandas'" → Your virtual environment isn't activated, or packages didn't install
- Go back to Part 3, Step 5 and make sure you activated the venv

---

#### 📊 Cell 3: Loading Customer Data

**What it looks like:**
```python
class BonPrixEngine:
    def __init__(self):
        # 1. Alle Shop-Rezensionen laden
        ...
```

**What it does:**
- Creates the "engine" that powers the personalization
- Loads customer profiles from `personalization_users_visible.csv`
- Loads product reviews from `reviews_all_users_in_shop.csv`
- Organizes the data so the AI can use it

**How to run it:**
1. Click on the cell
2. Press **Shift + Enter**

**What you'll see:**
- The cell runs
- No visible output (the data is loaded in the background)

**⏱️ Time:** 1-2 seconds

**What's happening behind the scenes:**
Think of this like opening a filing cabinet and organizing all the customer cards and product reviews so they're easy to find later.

---

#### 🤖 Cell 4: Creating the AI Prompt

**What it looks like:**
```python
def build_student_prompt(user_name, profile, product_name, current_product_reviews):
    """
    ...
```

**What it does:**
- Creates a function that builds instructions for the AI
- These instructions tell the AI:
  - Who the customer is
  - What they like
  - What product they're looking at
  - What other customers said about it
  - How to create a personalized summary

**How to run it:**
1. Click on the cell
2. Press **Shift + Enter**

**What you'll see:**
- The cell runs
- No visible output (the function is defined and ready to use)

**⏱️ Time:** < 1 second

**Analogy:**
This is like writing a detailed instruction manual for a personal shopper. You're telling them: "Here's what this customer likes, here's the product, here's what others said - now create a personalized recommendation."

---

#### 🎯 Cell 5: The Main Analysis Function

**What it looks like:**
```python
def run_analysis(user_name, product_selection):
    if not user_name or not product_selection:
        return [None]*3 + ["### ⚠️ Bitte links Kundin und Produkt wählen!", ""]
    ...
```

**What it does:**
This is the "brain" of the application. It:
1. Takes a customer name and product name
2. Finds that customer's preferences
3. Finds all reviews for that product
4. Creates a prompt for the AI
5. Sends it to IBM watsonx.ai
6. Gets back a personalized summary
7. Creates visualizations (charts)
8. Returns everything to display

**How to run it:**
1. Click on the cell
2. Press **Shift + Enter**

**What you'll see:**
- The cell runs
- No visible output yet (the function is ready but not called yet)

**⏱️ Time:** < 1 second

**What's happening:**
You're setting up the main "workflow" - the step-by-step process that happens when someone selects a customer and product.

---

#### 🎨 Cell 6: Creating the Web Interface

**What it looks like:**
```python
engine = BonPrixEngine()

with gr.Blocks(theme=gr.themes.Soft(), title="Bon Prix Personalization Lab") as demo:
    ...
```

**What it does:**
- Creates the actual web interface you'll interact with
- Sets up dropdowns for selecting customers and products
- Creates tabs for different views
- Connects everything together

**How to run it:**
1. Click on the cell
2. Press **Shift + Enter**

**What you'll see:**
- The cell runs
- After a few seconds, you'll see: "Running on local URL: http://127.0.0.1:7860"
- A link will appear - click it!

**⏱️ Time:** 5-10 seconds

**What happens next:**
A new browser tab opens with the interactive demo interface!

---

### Step 5: Using the Interactive Demo

**You should now see a web interface with:**

**Left side (Configuration):**
- 🛠️ Konfiguration
- Dropdown: "1. Kundin wählen" (Choose customer)
- Dropdown: "2. Produkt wählen" (Choose product)

**Right side (Results):**
- Three tabs:
  - 📝 KI-Beratung (AI Recommendation)
  - 📊 Produkt-Analyse (Product Analysis)
  - 👤 Kundenprofil (Customer Profile)

**How to use it:**

1. **Select a customer:**
   - Click the first dropdown
   - Choose a name (like "Nadine", "Sarah", etc.)
   - Each customer has different preferences

2. **Select a product:**
   - Click the second dropdown
   - Choose a product (like "Bandeau-Kleid", "Pullover", etc.)

3. **Wait for the AI:**
   - The system will process (takes 5-15 seconds)
   - You'll see a loading indicator

4. **View the results:**
   - **📝 KI-Beratung tab**: See the personalized AI summary
   - **📊 Produkt-Analyse tab**: See charts showing product features
   - **👤 Kundenprofil tab**: See the customer's preferences and history

**What you're seeing:**

**In the AI Recommendation tab:**
- A personalized summary written specifically for that customer
- It considers their past preferences
- It highlights aspects they care about
- It's different for each customer!

**In the Product Analysis tab:**
- A radar chart showing product features (comfort, quality, style, etc.)
- Based on what customers mentioned in reviews

**In the Customer Profile tab:**
- The customer's past purchases
- Their ratings
- Their preferences

**Try this experiment:**
1. Select "Nadine" and a product - read the AI summary
2. Select "Sarah" and the SAME product - read the AI summary
3. Notice how they're different! The AI personalizes based on each customer's preferences

---

### Step 6: Understanding What's Happening

**Behind the scenes, here's the process:**

```
1. You select a customer and product
   ↓
2. System finds customer's preferences
   ↓
3. System finds all reviews for that product
   ↓
4. System creates a detailed prompt for the AI
   ↓
5. Prompt is sent to IBM watsonx.ai
   ↓
6. AI reads the prompt and generates a personalized summary
   ↓
7. Summary is sent back to your computer
   ↓
8. System creates visualizations
   ↓
9. Everything is displayed in the interface
```

**The AI is:**
- Reading hundreds of reviews instantly
- Understanding the customer's preferences
- Identifying relevant information
- Writing a natural, personalized summary
- All in about 10 seconds!

---

### Step 7: Stopping the Demo

When you're done exploring:

1. **Close the demo browser tab**

2. **Stop JupyterLab:**
   - Go back to your terminal window
   - Press **Ctrl + C** (hold Control and press C)
   - You'll see: "Shutdown this Jupyter server (y/[n])?"
   - Type `y` and press **Enter**

3. **Deactivate your virtual environment:**
   ```bash
   deactivate
   ```
   - The `(.venv)` will disappear from your command prompt

4. **Close the terminal** (optional)

**💡 Next time you want to run the demo:**
1. Open terminal
2. Navigate to project folder: `cd path/to/bonprix`
3. Activate virtual environment: `source .venv/bin/activate` (Mac/Linux) or `.venv\Scripts\activate` (Windows)
4. Start JupyterLab: `jupyter lab`
5. Open the notebook and run all cells

---

## ✅ Part 7: Verification Checklist

Use this checklist to make sure everything is working correctly:

### Python Installation
- [ ] Python 3.11 is installed
- [ ] `python --version` (or `python3 --version`) shows Python 3.11.x
- [ ] `pip --version` (or `pip3 --version`) works without errors

### Project Setup
- [ ] Project files are downloaded and extracted
- [ ] You can navigate to the project folder in terminal
- [ ] You can see all the required files (notebooks, CSV files, .env.template)

### Virtual Environment
- [ ] Virtual environment is created (`.venv` folder exists)
- [ ] Virtual environment activates successfully
- [ ] You see `(.venv)` in your command prompt when activated
- [ ] All packages installed without errors

### Credentials
- [ ] `.env` file exists (renamed from `.env.template`)
- [ ] WATSONX_API_KEY is filled in
- [ ] WATSONX_PROJECT_ID is filled in
- [ ] WATSONX_URL is correct for your region

### JupyterLab
- [ ] `jupyter lab` command starts without errors
- [ ] Browser opens automatically (or you can open the URL manually)
- [ ] You can see the file browser with your project files

### Notebook Execution
- [ ] Notebook opens when you double-click it
- [ ] Cell 1 (imports) runs without errors
- [ ] Cell 2 (data loading) runs without errors
- [ ] Cell 3 (prompt function) runs without errors
- [ ] Cell 4 (analysis function) runs without errors
- [ ] Cell 5 (interface) runs and shows a URL

### Demo Interface
- [ ] Demo interface opens in browser
- [ ] You can select a customer from the dropdown
- [ ] You can select a product from the dropdown
- [ ] AI generates a personalized summary (takes 5-15 seconds)
- [ ] You can see visualizations in the Product Analysis tab
- [ ] You can see customer profile in the Customer Profile tab

### Cleanup
- [ ] You can stop JupyterLab with Ctrl+C
- [ ] You can deactivate the virtual environment
- [ ] You can restart everything and it still works

**If you can check all these boxes, congratulations! 🎉 Everything is working perfectly!**

---

## 🔧 Part 8: Troubleshooting Guide

### Windows-Specific Issues

#### Issue: "python is not recognized as an internal or external command"

**Cause:** Python wasn't added to PATH during installation

**Solution:**
1. Uninstall Python:
   - Control Panel → Programs → Uninstall a program
   - Find Python 3.11 and uninstall it
2. Download Python installer again
3. Run installer
4. **CHECK the "Add Python to PATH" box** (this is critical!)
5. Complete installation
6. Open a NEW command prompt
7. Test: `python --version`

---

#### Issue: "Activate.ps1 cannot be loaded because running scripts is disabled"

**Cause:** PowerShell's security settings prevent running scripts

**Solution:**
```powershell
Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned
```
Then try activating again:
```powershell
.venv\Scripts\Activate.ps1
```

**Alternative:** Use Command Prompt instead of PowerShell:
```bash
.venv\Scripts\activate.bat
```

---

#### Issue: Antivirus blocking Python or pip

**Cause:** Some antivirus software flags Python scripts as suspicious

**Solution:**
1. Add Python to your antivirus exceptions:
   - Usually in: `C:\Users\YourName\AppData\Local\Programs\Python\Python311`
2. Add your project folder to exceptions
3. Temporarily disable antivirus during installation (not recommended long-term)

---

### macOS-Specific Issues

#### Issue: "command not found: python3"

**Cause:** Python installation didn't complete or isn't in PATH

**Solution 1 - Reinstall Python:**
1. Download Python 3.11 from python.org
2. Run the installer again
3. Make sure it completes successfully

**Solution 2 - Install Xcode Command Line Tools:**
```bash
xcode-select --install
```
This installs development tools that Python needs.

---

#### Issue: "Permission denied" when running commands

**Cause:** File permissions issue

**Solution:**
```bash
chmod +x .venv/bin/activate
```
Then try activating again.

---

#### Issue: Multiple Python versions causing conflicts

**Cause:** Mac comes with Python 2.7 pre-installed, plus you might have other versions

**Solution:**
Always use `python3` and `pip3` explicitly:
```bash
python3 --version
pip3 install package-name
python3 -m venv .venv
```

**Check which Python you're using:**
```bash
which python3
```
Should show: `/Library/Frameworks/Python.framework/Versions/3.11/bin/python3`

---

### Linux-Specific Issues

#### Issue: "python3.11: command not found"

**Cause:** Python 3.11 not installed or not in PATH

**Solution for Ubuntu/Debian:**
```bash
sudo apt update
sudo apt install python3.11 python3.11-venv python3-pip
```

**Solution for Fedora:**
```bash
sudo dnf install python3.11 python3-pip
```

---

#### Issue: "Permission denied" or "Access denied"

**Cause:** Need administrator privileges

**Solution:**
Use `sudo` for system-wide installations:
```bash
sudo apt install python3.11
```

But DON'T use sudo for:
- Creating virtual environments
- Installing packages in virtual environment
- Running the notebook

---

#### Issue: "externally-managed-environment" error

**Cause:** Some Linux distributions prevent installing packages globally

**Solution:**
This is why we use virtual environments! Make sure:
1. You created a virtual environment: `python3 -m venv .venv`
2. You activated it: `source .venv/bin/activate`
3. You see `(.venv)` in your prompt
4. Then install packages: `pip install ...`

---

### Common Issues (All Platforms)

#### Issue: Virtual environment won't activate

**Symptoms:**
- Command runs but no `(.venv)` appears
- Or error message appears

**Solutions:**

**1. Make sure you're in the project directory:**
```bash
pwd  # Mac/Linux - shows current directory
cd   # Windows - shows current directory
```
Should show your project folder path.

**2. Make sure .venv exists:**
```bash
ls -la .venv  # Mac/Linux
dir .venv     # Windows
```
If it doesn't exist, create it:
```bash
python -m venv .venv  # Windows
python3 -m venv .venv # Mac/Linux
```

**3. Use the correct activation command for your OS:**
- Windows CMD: `.venv\Scripts\activate.bat`
- Windows PowerShell: `.venv\Scripts\Activate.ps1`
- Mac/Linux: `source .venv/bin/activate`

---

#### Issue: Package installation fails

**Symptoms:**
- "Could not find a version that satisfies the requirement"
- "ERROR: Could not install packages"
- Installation hangs or times out

**Solutions:**

**1. Check internet connection:**
```bash
ping google.com
```
Press Ctrl+C to stop. If it doesn't work, fix your internet first.

**2. Upgrade pip:**
```bash
pip install --upgrade pip
```

**3. Install packages one at a time:**
Instead of installing all at once, try:
```bash
pip install pandas
pip install gradio
pip install plotly
# ... etc
```
