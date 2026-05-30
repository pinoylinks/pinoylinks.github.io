---
title: pyautogui
summary: How to install pyautogui in Linuxmint.
date: 2025-07-05T06:56:00+08:00
lastmod: 2025-07-05T06:56:00+08:00
_build:
  render: always
  list: always
draft: false
categories: 📝 Notes
tags:
  - python
---
# How to Install `pyautogui` in a Virtual Environment on Linux Mint

## Step 1: Install Python & Pip (Skip if you already have them)

Open the **Terminal** (`Ctrl+Alt+T`) and run:

```bash
sudo apt update
sudo apt install python3 python3-pip python3-venv
```

## Step 2: Create a Virtual Environment

Navigate to your project folder or create one:

```bash
mkdir myproject
cd myproject
```

Create the virtual environment (I'll call it `venv` but you can name it anything):

```bash
python3 -m venv venv
```

## Step 3: Activate the Virtual Environment

```bash
source venv/bin/activate
```

You’ll notice your terminal prompt changes to show `(venv)` — this means you're inside the virtual environment.

## Step 4: Install `pyautogui` inside the Virtual Environment

```bash
pip install pyautogui
```

Optionally, you can check if it's installed:

```bash
pip show pyautogui
```

## Step 5: Run Your Python Script

Example:

```bash
python3 test.py
```

Then inside Python:

```python
import pyautogui
import time

time.sleep(5)
pyautogui.press('m')
time.sleep(.1)
pyautogui.press('m')
time.sleep(.1)
pyautogui.press('m')
time.sleep(.1)
pyautogui.press('n')
time.sleep(.3)
pyautogui.press('c')
time.sleep(.1)
pyautogui.press('m')
```

## Step 6: Deactivate the Virtual Environment

When you’re done:

```bash
deactivate
```
