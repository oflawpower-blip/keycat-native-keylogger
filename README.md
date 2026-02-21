<div align="center">

```
  /\_____/\
 ( =^·^= )
  (       )   KeyCat — Keystroke Logger
   )     (
  (_)___(_)
```

# 🐾 KeyCat

**A fun, personal keystroke logger with a gorgeous Catppuccin UI.**
Log keystrokes from a specific app (or all apps) silently in the background.

![Python](https://img.shields.io/badge/Python-3.8+-cba6f7?style=flat-square&logo=python&logoColor=11111b)
![Windows](https://img.shields.io/badge/Windows-supported-89b4fa?style=flat-square&logo=windows&logoColor=11111b)
![Linux](https://img.shields.io/badge/Linux-supported-a6e3a1?style=flat-square&logo=linux&logoColor=11111b)
![Theme](https://img.shields.io/badge/Theme-Catppuccin-f5c2e7?style=flat-square)

</div>

---

## 📖 What is KeyCat?

KeyCat is a personal-use keystroke logger that runs quietly in your system tray. You pick a target app, hit Start, and every key you type in that window gets saved cleanly to a `.txt` file. Built as a fun project with a full [Catppuccin](https://github.com/catppuccin/catppuccin) themed UI — all 4 flavours included.

---

## ✨ Features

- 🎯 **Target a specific app** — log only keystrokes from `chrome.exe`, `discord`, or any window title keyword. Leave blank to log everything.
- 📋 **Live process picker** — browse all running processes and click to select your target
- 🎨 **4 Catppuccin themes** — Mocha (default), Macchiato, Frappé, Latte — switch instantly with no restart
- 🐾 **Custom paw-print icon** — in the titlebar, taskbar, and system tray
- 📌 **System tray** — close the window and KeyCat keeps logging silently in the background. Right-click the tray icon to control it.
- 🔴 **Live feed** — watch keystrokes appear in real time, colour-coded
- 📄 **Clean log files** — each session gets a timestamped header in the `.txt` file
- 🔁 **Resizable window** — drag it to any size you like
- 🪟 **Windows** + **🐧 Linux** native versions

---

## 📁 Files

| File | Platform | Description |
|------|----------|-------------|
| `keystroke_logger.py` | 🪟 Windows | Main application |
| `launch_keycat.bat` | 🪟 Windows | Launcher — no CMD window, auto-installs deps |
| `keycat_linux.py` | 🐧 Linux | Main application |
| `launch_keycat.sh` | 🐧 Linux | Launcher — runs in background, auto-installs deps |

---

## 🚀 Getting Started

### 🪟 Windows

**Requirements:** Python 3.8+ ([python.org](https://www.python.org/downloads/))

1. Put `keystroke_logger.py` and `launch_keycat.bat` in the same folder
2. Double-click `launch_keycat.bat`
3. That's it — dependencies install silently and the app launches with no CMD window

> **First run only:** the installer may take 10–15 seconds silently in the background before the window appears.

### 🐧 Linux

**Requirements:** Python 3.8+, Tkinter, xdotool

```bash
# Install system dependencies (Debian/Ubuntu)
sudo apt install python3-tk python3-pip xdotool

# Fedora
sudo dnf install python3-tkinter xdotool

# Then launch
bash launch_keycat.sh
```

> On **Wayland**, `xdotool` only works under XWayland. Active-window filtering may not work on pure Wayland — it will fall back to logging all windows (same as leaving the target blank). The tray icon also gracefully falls back to window minimize if your DE doesn't support it.

---

## 🎮 How to Use

1. **Launch** the app via the `.bat` or `.sh` launcher
2. **Set a target** — type a process name (e.g. `chrome.exe` on Windows, `firefox` on Linux) or a window title keyword in the Target field. Or leave it blank to log everything.
3. **Choose your output file** — defaults to `keycat_log.txt` on your Desktop (Windows) or home folder (Linux). Click Browse to change it.
4. **Click ▶ Start Logging** — the status pill turns green and the live feed activates
5. **Switch to your target app** and type away
6. **Click ⏹ Stop** when done — the log file is saved and the session is closed cleanly

### 🔲 Hiding to the Tray

- Click **📌 Hide to System Tray** or just close the window — KeyCat keeps running and logging in the background
- **Right-click the tray icon** (paw print 🐾) for a quick menu: Show, Start, Stop, Open Log, Quit
- To fully exit, use **Quit KeyCat** from the tray menu

---

## 🎨 Themes

All four official [Catppuccin](https://github.com/catppuccin/catppuccin) flavours are built in. Switch between them instantly using the buttons at the top of the app — no restart needed. The window icon and tray icon repaint too.

| Flavour | Vibe |
|---------|------|
| 🌙 **Mocha** | Dark, warm — the default |
| 🌊 **Macchiato** | Dark, cool-toned |
| ☁️ **Frappé** | Medium, muted |
| ☀️ **Latte** | Light theme |

---

## 📄 Log File Format

Each session is clearly separated with a header and footer:

```
────────────────────────────────────────────────────────────
  KeyCat Session [Mocha] — 2026-02-21 14:32:07
  Target: chrome.exe
────────────────────────────────────────────────────────────

hello world[BACK][BACK]↵
this is everything i typed in chrome↵

[Session ended - 47 keys logged]
```

Special keys are written in `[brackets]`: `[Ctrl]`, `[Alt]`, `[BACK]`, `[Del]`, `[F5]`, arrow keys, etc. Space and Enter are written as literal space/newline so the text reads naturally.

---

## 📦 Dependencies

Installed automatically on first launch:

| Package | Purpose |
|---------|---------|
| `pynput` | Keyboard listener (cross-platform) |
| `pywin32` | Active window detection (Windows only) |
| `psutil` | Process name lookup |
| `pystray` | System tray icon |
| `Pillow` | Paw-print icon rendering |

---

## ⚠️ Disclaimer

KeyCat is built as a **personal fun project**. Only use it to log your own keystrokes on your own machine. Do not use it to monitor other people without their knowledge or consent — that would be illegal in most places and just plain not cool. 🐱

---

## 💜 Credits

Colour palette by [Catppuccin](https://github.com/catppuccin/catppuccin) — the most adorable colour scheme ever made.

Built with Python, Tkinter, pynput, pystray, and Pillow.

---

<div align="center">
Made with 🐾 and Catppuccin &nbsp;•&nbsp; For fun & personal use only
</div>
