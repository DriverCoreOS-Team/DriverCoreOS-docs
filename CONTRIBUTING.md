# 🤝 Contributing to DriverCoreOS

Welcome, and thank you for your interest in contributing to **DriverCoreOS**!  
This project is a modular, open-source driving platform made for any OBD-II vehicle.  
Whether you're fixing bugs, improving documentation, creating plugins, or adding new features—your help is appreciated!

---

## 📦 Repository Structure

The DriverCoreOS project is organized into several repositories:

| Repo                                 | Description                                 |
| ------------------------------------ | ------------------------------------------- |
| `DriverCoreOS-main`                  | Superproject with submodules & coordination |
| `DriverCoreOS-esp32`                 | ESP32 firmware for OBD, GPS, LEDs           |
| `DriverCoreOS-rpi`                   | RPi apps, media UI, map, plugin system      |
| `DriverCoreOS-nixos`                 | Custom NixOS image & configuration          |
| `DriverCoreOS-installer`             | Flashing tools, install scripts             |
| `DriverCoreOS-docs`                  | Markdown-based docs (mdBook)                |
| `DriverCoreOS-tools`                 | Shared Nix flake, dev environments          |
| `DriverCoreOS-rpi-plugin-template`   | Templates for RPi plugin development        |
| `DriverCoreOS-esp32-plugin-template` | Template for ESP32 plugin development       |

---

## 🧰 Requirements

You’ll need:

- **Git** (with submodule support)
- **Nix** (with flakes enabled strongly recommended)
- For ESP32: [PlatformIO](https://platformio.org/ not mandatory but recommended)
- For RPi: Python 3, PyQt5 (managed via `nix develop`)
- A GitHub account for PRs/issues

---

## 🚀 Getting Started

1. **Clone the main project** with submodules:

```bash
git clone --recurse-submodules https://github.com/DriverCoreOS-Team/DriverCoreOS-main.git
cd DriverCoreOS-main
```

2. **Enter the dev environment** (via Nix):

```bash
nix develop ./repos/tools
```

3. **Start coding** in one of the submodules:
   - ESP32: `cd repos/esp32`
   - RPi: `cd repos/rpi`
   - NixOS config: `cd repos/nixos`

---

## 🧪 How to Contribute

### 🛠️ Fix a Bug or Add a Feature

1. Fork the repository you want to modify
2. Create a new branch:

```bash
git checkout -b my-feature
```

3. Make your changes (use the dev shell if needed)
4. Run/test your code
5. Commit with a meaningful message
6. Push your branch and open a Pull Request (PR)

### 📚 Improve Documentation

- Head to [`DriverCoreOS-docs`](https://github.com/DriverCoreOS-Team/DriverCoreOS-docs)
- Run the preview locally
- Edit the `.md` files and submit a PR

### 🧩 Create a Plugin

- Use one of the plugin templates:
  - [ESP32 Plugin Template](https://github.com/DriverCoreOS-Team/DriverCoreOS-esp32-plugin-template)
  - [RPi Plugin Template](https://github.com/DriverCoreOS-Team/DriverCoreOS-rpi-plugin-template)
- Clone the template, rename it, and build your feature!
- Optionally share it with the community.

---

## 🔍 Code Guidelines

- Follow [C++ best practices](https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines) for ESP32 code
- Use modern Python 3+ and [PEP8](https://peps.python.org/pep-0008/) for RPi code
- Separate logic and UI (MVC/command pattern when possible)
- Favor modularity and keep plugin interfaces clean

---

## ✅ Pull Request Checklist

Before submitting your PR:

- [ ] Code builds and passes local tests
- [ ] No sensitive credentials committed
- [ ] You've updated relevant docs or README
- [ ] You've rebased and squashed your commits if needed
- [ ] PR title is descriptive (e.g. `feat: add race overlay plugin`)

---

## 📬 Contact & Support

Need help?

- Discord: `mathisdlg`
- GitHub Discussions: [DriverCoreOS-Team](https://github.com/orgs/DriverCoreOS-Team/discussions)
- Instagram: [@mathisdlg](https://instagram.com/mathisdlg)

---

Thank you again for contributing to **DriverCoreOS**! 💙
