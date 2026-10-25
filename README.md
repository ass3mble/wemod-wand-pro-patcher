# WeMod (Wand) Patcher

A Windows utility for examining how a local WeMod installation can be modified and repackaged. The project focuses on Electron application archives, local compatibility experiments, and reverse-engineering research.

**What is available here:** This repository currently contains the compiled `Wemod(Wand)_Patcher.exe`, a short guide, and a Git ignore file. The patcher's source code is not included. Its internal behavior cannot be independently verified from this repository alone.

## What the tool is intended to do

According to the project's original documentation, the executable is designed to:

- Find an installed WeMod application directory.
- Back up its `app.asar` archive before making changes.
- Extract the Electron archive and apply local changes to selected application logic.
- Repackage the archive for local testing.

These are documented design goals, not a guarantee that every version of WeMod is supported.

## Before you start

- Use a Windows machine and an installation you are authorized to inspect.
- Close WeMod fully, including its background process.
- Make your own copy of the original `app.asar` and keep it outside the installation folder.
- Review the executable's origin and scan it with your security software.
- Be aware that application updates may overwrite the modified archive or make the patch incompatible.
- Node.js may be needed for archive operations, depending on how the executable was packaged.

## Running the packaged utility

1. Download `Wemod(Wand)_Patcher.exe` from this repository.
2. Verify that WeMod is closed and your original archive is backed up.
3. Run the utility only in a local test environment where you have permission to modify the application.
4. Check the result. If anything behaves unexpectedly, close WeMod and restore your original `app.asar`.

There is no source-based build procedure in this repository because the source files have not been published here.

## What is an ASAR archive?

Electron desktop applications often store JavaScript, HTML, and related files in a single `app.asar` archive. Researchers can unpack that archive to inspect how an application is structured, then repack it after making local changes.

Changing those files can break startup, updates, or other application behavior. Treat the archive backup as essential.

## Scope and limitations

This is an independent research project, not an official WeMod release. It is not affiliated with or endorsed by WeMod. There is no public compatibility matrix, reproducible build, or automated test suite in this repository. No claim is made that the executable works with the latest application version.

Only inspect or modify software when you have authorization. Respect applicable licenses, service terms, and access controls. Do not use this utility to gain unauthorized access to paid features or services.
