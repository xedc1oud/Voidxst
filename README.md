<p align="center">
<img src="./assets/ambxst/ambxst-logo-color.svg" alt="Ambxst Logo" style="width: 50%;" align="center" />
  <br>
  <br>
<i><b>WORK IN PROGRESS 🚧</b></i><br>
A <i><b>Void</b>-native</i> fork of <a href="https://github.com/Axenide/Ambxst">Ambxst</a> — an <i><b>Ax</b>tremely</i> customizable shell.
</p>

  <p align="center">
  <a href="https://github.com/xedc1oud/Voidxst/stargazers">
    <img src="https://img.shields.io/github/stars/xedc1oud/Voidxst?style=for-the-badge&logo=github&color=E3B341&logoColor=D9E0EE&labelColor=000000" alt="GitHub stars">
  </a>
  <a href="https://github.com/Axenide/Ambxst">
    <img src="https://img.shields.io/badge/Based_on-Ambxst-8839ef?style=for-the-badge&logo=github&logoColor=D9E0EE&labelColor=000000" alt="Based on Ambxst">
  </a>
</p>

---

> [!NOTE]
> **Voidxst** is an unofficial fork of [Ambxst](https://github.com/Axenide/Ambxst) by [Axenide](https://github.com/Axenide), adapted to run on [Void Linux](https://voidlinux.org/). All credit for the original design, architecture, and features goes to the upstream project.

---

<h2><sub><img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Camera%20with%20Flash.png" alt="Camera with Flash" width="32" height="32" /></sub> Screenshots</h2>

<div align="center">
  <img src="./assets/screenshots/1.png" width="100%" />

  <br />

  <img src="./assets/screenshots/2.png" width="32%" />
  <img src="./assets/screenshots/3.png" width="32%" />
  <img src="./assets/screenshots/4.png" width="32%" />

  <img src="./assets/screenshots/5.png" width="32%" />
  <img src="./assets/screenshots/6.png" width="32%" />
  <img src="./assets/screenshots/7.png" width="32%" />

  <img src="./assets/screenshots/8.png" width="32%" />
  <img src="./assets/screenshots/9.png" width="32%" />
  <img src="./assets/screenshots/10.png" width="32%" />
</div>

---

<h2><sub><img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Package.png" alt="Package" width="32" height="32" /></sub> Installation</h2>

### Prerequisites

- [Void Linux](https://voidlinux.org/) (glibc or musl)
- [Hyprland](https://hyprland.org/) installed and working

### Install

```bash
git clone https://github.com/xedc1oud/Voidxst.git
cd Voidxst
./install.sh
```

The install script will use `xbps-install` to pull in all required dependencies and set up Voidxst.

After installation the `ambxst` command will be available in your terminal.

### Hyprland

1. Run the installation steps above.

2. Run `ambxst install hyprland` to add Voidxst's configuration to Hyprland. This will source a config file that applies Voidxst's settings. It will look like this:

```bash
# Voidxst
source = ~/.local/share/ambxst/hyprland.conf

# OVERRIDES
# Down here you can write or source anything that you want to override from Voidxst's settings.
```


As stated, anything you want to override from Voidxst's settings should be written under the "OVERRIDES" section.

3. Start Voidxst by running `ambxst` in your terminal. If you want to keep it running without having the terminal window open, you can run `ambxst & disown`. This will only be necessary for your first test run, as Voidxst will start automatically on login after step 2.

> [!IMPORTANT]
> The only pre-requisite is having Hyprland installed. Some optional features (e.g. `gpu-screen-recorder`) may require additional packages — the install script will inform you about them.

---

## Will this change my config?

Nope! Besides the source line in your `hyprland.conf`, Voidxst is designed to be non-intrusive. It won't modify any of your existing configurations.

---

## What changed compared to upstream Ambxst?

- **Package management** — all dependency resolution uses `xbps-install` instead of `pacman`/`dnf`/`nix`.
- **Service management** — uses `runit` where applicable instead of `systemd`.
- **Dependency patches** — some packages that are unavailable in the Void repos are built from source or substituted with Void-compatible alternatives.
- Everything else remains faithful to the original Ambxst.

---

<h2><sub><img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Telegram-Animated-Emojis/main/Activity/Sparkles.webp" alt="Sparkles" width="32" height="32" /></sub> Features</h2>

All features are inherited from upstream [Ambxst](https://github.com/Axenide/Ambxst):

- [x] Customizable components
- [x] Themes
- [x] System integration
- [x] App launcher
- [x] Clipboard manager
- [x] Quick notes (and not so quick ones)
- [x] Wallpaper manager
- [x] Emoji picker
- [x] [tmux](https://github.com/tmux/tmux) session manager
- [x] System monitor
- [x] Media control
- [x] Notification system
- [x] Wi-Fi manager
- [x] Bluetooth manager
- [x] Audio mixer
- [x] [EasyEffects](https://github.com/wwmm/easyeffects) integration
- [x] Screen capture
- [x] Screen recording
- [x] Color picker
- [x] OCR
- [x] QR and barcode scanner
- [x] "Mirror" (webcam)
- [x] Game mode
- [x] Night mode
- [x] Power profile manager
- [x] AI Assistant
- [x] Weather
- [x] Calendar
- [x] Power menu
- [x] Workspace management
- [x] Support for different layouts (dwindle, master, scrolling, etc.)
- [x] Multi-monitor support
- [x] Customizable keybindings
- [ ] Plugin and extension system
- [ ] Compatibility with other Wayland compositors

---

## I need help!

- For **Voidxst-specific** issues (installation on Void, missing packages, runit integration), please open an issue on this repository.
- For **general Ambxst** questions and feature requests, please refer to the upstream project:
  - [Ambxst Discord](https://discord.com/invite/gHG9WHyNvH)
  - [Ambxst Discussions](https://github.com/Axenide/Ambxst/discussions)
  - [Ambxst Issues](https://github.com/Axenide/Ambxst/issues)
- The main configuration is located at `~/.config/voidxst`.

---

## Credits

### Upstream

This project would not exist without [**Ambxst**](https://github.com/Axenide/Ambxst) by [**Axenide**](https://github.com/Axenide). Massive thanks for creating such an incredible, feature-rich shell and making it open source. 💖

All original credits from the Ambxst project:

- [outfoxxed](https://outfoxxed.me/) for creating Quickshell and great documentation!
- [end-4](https://github.com/end-4) for his awesome projects.
- [soramane](https://github.com/soramanew) for helping with Quickshell.
- [tr1x_em](https://trix.is-a.dev/) for being a great friend and helping find great tools.
- [Darsh](https://github.com/its-darsh) for creating Fabric — without Fabric, Ax-Shell wouldn't exist, so Ambxst wouldn't either.
- [Mario](https://github.com/mariokhz) for showing Quickshell!
- [Samouly](https://samouly.is-a.dev/) for being Samouly. :3
- [Brys](https://github.com/brys0) for continuous support.
- [Zen](https://github.com/wer-zen) for helping with Quickshell.
- [kh](https://www.youtube.com/watch?v=dQw4w9WgXcQ) for being awesome.

### Voidxst

- [Axenide](https://github.com/Axenide) — for creating and maintaining Ambxst, the project this fork is based on.
- The [Void Linux](https://voidlinux.org/) community — for keeping a fantastic independent distribution alive.
- And you, the user, for trying out Voidxst! 💖
