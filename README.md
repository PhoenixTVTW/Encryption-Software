
# Paragon 6

Paragon 6 is a modern desktop encryption utility for secure file, folder, and text encryption.

It allows you to encrypt and decrypt data using strong AES-GCM encryption, generate secure keys, work with folders, and switch between dark and light UI themes.

<p align="center">
  <img src="assets/Logo.png" alt="Paragon 6 logo" width="500" />
</p>

## Overview

Paragon 6 is built for users who want a simple, professional, and easy-to-use encryption tool with a modern GUI.

### Main features
- Encrypt files and folders
- Decrypt files and folders
- Encrypt and decrypt plain text directly
- Generate secure keys and save them to `.key` files
- Load existing keys and reuse them
- Configure character types for password/key generation
- Set encryption iterations
- Dark mode and light mode toggle
- Built-in support for folder ZIP packaging before encryption
- Standalone Windows executable build

## Screenshots

<p align="center">
  <img src="assets/Logo.png" alt="Paragon 6 app logo" width="220" />
</p>

## Tech stack
- Python 3.10+
- PyQt5
- cryptography
- PyInstaller

## Installation

### Option 1: Use the built Windows executable

You can use the packaged executable directly:

```powershell
cd "C:\Users\Tomad\Downloads\Codding\De-Encrypting Software V3"
.\dist\app.exe
```

### Option 2: Run from source

```powershell
cd "C:\Users\Tomad\Downloads\Codding\De-Encrypting Software V3"
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
python -m src.main
```

## Build the executable yourself

```powershell
cd "C:\Users\Tomad\Downloads\Codding\De-Encrypting Software V3"
.\.venv\Scripts\python.exe -m pip install pyinstaller
.\.venv\Scripts\pyinstaller --onefile --noconsole --icon=assets/app.ico app.py
```

## How to use

### Encrypt a file
1. Open the app
2. Go to the `Encrypt / Decrypt` tab
3. Select the input file or folder
4. Select the output path
5. Enter or load a key
6. Click `Encrypt`

### Decrypt a file
1. Select the encrypted file
2. Enter the same key used for encryption
3. Choose the output destination
4. Click `Decrypt`

### Encrypt text
1. Open the `Text` tab
2. Paste or type your text
3. Choose auto-generated key or use a custom key
4. Click `Encrypt Text`
5. Copy the result or decrypt it again later

### Generate a key
1. Open the `Key` tab
2. Adjust the sliders for letters, numbers, and symbols
3. Toggle included character types if needed
4. Click `Generate Key`
5. Save it to a `.key` file if needed

## Important notes
- Keep your key safe. Without it, encrypted data cannot be recovered.
- This tool is intended for personal and educational use.
- Always keep backups of important files before encrypting them.

## License

This project is provided as-is for learning, testing, and personal use.

## Project status

This project is a working desktop encryption utility with a modern GUI and Windows executable build.

## Contributing

Pull requests and improvements are welcome. For major changes, please open an issue first to discuss the proposed updates.
