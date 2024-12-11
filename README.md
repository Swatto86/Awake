# Awake

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Version](https://img.shields.io/badge/version-0.1.0-blue.svg)](https://github.com/yourusername/awake/releases)

A simple system tray application to prevent your system from going to sleep. Built with Rust and Tauri.

<div align="center">
  <img src="docs/screenshot.png" alt="Awake Screenshot" width="200"/>
</div>

## Features

- 🔒 Prevent system sleep without requiring sudo/admin privileges
- 🔔 Simple system tray interface
- 💡 Visual indication of active state
- 🚀 Lightweight and efficient
- 🎯 Clean shutdown on system exit

## Installation

### Pre-built Binaries

Download the latest version for your operating system from the [Releases](https://github.com/yourusername/awake/releases) page.

### System Requirements

#### Linux
- Requires `xdotool` package for keyboard simulation
  ```bash
  # Manjaro/Arch:
  sudo pacman -S xdotool
  
  # Ubuntu/Debian:
  sudo apt-get install xdotool
  ```

#### Windows
- No additional requirements
- Uses Windows API for keyboard simulation

#### macOS
- No additional requirements
- Uses macOS Quartz Event Services for keyboard simulation

## Usage

1. Launch the application
2. Click the system tray icon to access the menu
3. Select "Disable Sleep" to prevent the system from sleeping
4. Select "Enable Sleep" to return to normal system behavior
5. Select "Quit" to exit the application

## How it Works

Awake uses a user-space approach to keep your system awake by simulating a key press every minute. This method:
- Doesn't require administrator privileges
- Is lightweight and efficient
- Works in the background

## Building from Source

If you're interested in building from source, please see our [build instructions](BUILD.md).

## Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

Please make sure to update tests as appropriate and follow the existing code style.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Built with [Tauri](https://tauri.app/)
- Inspired by the need for a simple, cross-platform solution to prevent system sleep
