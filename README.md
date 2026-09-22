# WeMod Auto Patcher

An automated patcher for WeMod focused on reverse-engineering, local compatibility testing, and Electron/ASAR research.

## 🚀 Features
- **Auto-Detect:** Automatically locates your latest WeMod installation (`app-*`).
- **Resilient Patching:** Applies a local wrapper around selected internal request/error-handling logic for research and compatibility testing.
- **Auto-Repack:** Extracts `app.asar`, applies the patch, and repacks it seamlessly using `asar`.
- **Backup System:** Safely backs up your original `app.asar` before making any changes.

## ⚙️ Requirements
- [Node.js](https://nodejs.org/) — required for `npx asar` extraction and repacking.
- Python 3.x — if running from source.

## 🛠 Usage
1. Close WeMod completely from the system tray.
2. Run `Wemod(Wand)_Patcher.exe` (or the source version, if available).
3. Wait for the extraction, patching, and repacking process to finish.
4. Open WeMod and verify the modified behavior in your local test environment.

## 📝 How it works
WeMod is built as an Electron application, with much of its application logic packaged inside `app.asar`. This tool automates the process of locating the installed app, backing up the original archive, extracting it, modifying selected internal JavaScript logic, and repacking the archive.

The project is intended to demonstrate how Electron applications can be inspected and modified for debugging, interoperability, compatibility testing, and reverse-engineering research.

---

*Disclaimer: This tool is for educational, interoperability, and reverse-engineering research only. Use it only on software you are authorized to inspect or modify, and respect applicable licenses, terms of service, and access controls.*
