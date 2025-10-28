# yay-gui

A simple GUI application for Arch User Repository (AUR) helpers, providing an easy-to-use interface for managing AUR packages.

## Features

- **Search packages**: Search through AUR packages with a simple text input
- **Install packages**: Select and install packages from search results
- **Remove packages**: Uninstall packages from your system
- **Multiple AUR helper support**: Works with `yay`, `paru`, and other AUR helpers

## Requirements

- Python 3
- PyQt5
- An AUR helper installed (`yay`, `paru`, etc.)

## Installation

```bash
# Install PyQt5 if not already installed
pip install PyQt5
```

## Usage

### Basic Usage (with yay)

```bash
python yay-gui.py
```

### Using a Different AUR Helper

You can specify a different AUR helper by passing it as a command line argument:

```bash
# Using paru
python yay-gui.py paru

# Using any other AUR helper
python yay-gui.py <helper-name>
```

If no argument is provided, the application defaults to using `yay`.

## Current Limitations

- Must be run from a terminal to allow for:
  - Entering sudo password when required
  - Confirming package installation/removal
  - Viewing installation progress and output

## How It Works

The application provides a PyQt5-based GUI that wraps around your chosen AUR helper, making it easier to search and manage AUR packages without memorizing command-line flags.
