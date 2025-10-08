<div align="center">
    
# 🎨 Windows 11 Customization
A curated collection of tools, configurations, and resources to transform your Windows 11 experience into a personalized and productive environment.****

</div>

## What you get here:
Whether you're a power user, developer, or just someone who likes a clean and efficient desktop, this repo aims to help you:
- Personalize your Windows 11 look and feel  
- Improve workflow and aesthetics with selected tools  
- Share a consistent environment setup across devices

---

## 🚀 Features & Components

This repository is organized into several “modules” or “components,” each with configuration files, install scripts (if any), or guidance on how to apply tweaks. These are the main categories:

| Component | Type | Purpose | Config / Notes |
|---|---|---|---|
| **GlazeWM** | Core tool | A tiling window manager for Windows — helps arrange windows more efficiently | Contains config files and instructions |
| **yasb** | Core tool | “Yet Another Status Bar” — a customizable status bar to display system info | Config folder included |
| **Windhawk** | Core tool | System-level tweak engine — allows UI tweaks, mods, patches | Includes profiles / plugins |
| **Flow Launcher** | Core tool | Fast launcher for apps, files, etc. | Has config / theme files |
| **Windows Terminal** | Core tool | Enhanced terminal experience (PowerShell, etc.) | Custom `settings.json` and profiles |
| **JetBrains Mono (Font)** | Core tool | Overrides default system font for cleaner visuals | Scripts or instructions to change system font |
| **Discord** | App config | Theming, CSS, UI tweaks for Discord | CSS / theme files included |
| **File Explorer** | App config | Explorer tweaks — appearance, behaviors | Registry tweaks, config files |
| **OBS** | App config | Optimized configs for OBS Studio | Presets, settings files |
| **Wallpaper** | Asset | A curated set of wallpapers fitting the visual theme | `.png` or `.jpg` files |

---

## 📥 Setup / Getting Started

Follow these steps to apply the customizations to your system:

1. **Clone the repository**  
   ```bash
   git clone https://github.com/abdullah-al-faahim/win11-customization.git
   cd win11-customization
   ```
2. **Install the required tools/applications:** Manually download and install the tools referenced in the Components section (GlazeWM, Windhawk, Flow Launcher, etc.). Many links are included in each component’s folder or documentation.

3. **Apply configurations:** For each tool/app you wish to customize, go into its folder and follow the instructions:
- Copy / merge config files to the proper paths
- Execute scripts (where applicable)
- Adjust or override settings as needed
Example:
If you want to apply your yasb config, you might put files into
```bash
C:\Users\<YourUser>\.config\yasb\
```
4. **Restart / relogin:** Some changes (fonts, Explorer tweaks) may need a logoff or system restart to take full effect.


## 🛠 Tips & Best Practices

- Backup first. Always back up current config files, registry settings, or system state before applying.
- One tool at a time. Roll out changes component by component to isolate issues.
- Check compatibility. Some tweaks might conflict with Windows updates or system policies.
- Use version control. Keep track of your own customizations via Git in a fork or local branch.


## Files Directory
```bash
win11-customization/
├─ GlazeWM/
│   ├─ config.json
│   ├─ README.md
├─ YASB/
│   ├─ statusbar-config.toml
│   ├─ README.md
├─ Windhawk/
│   ├─ mods/
│   ├─ profile/
├─ Flow Launcher/
│   ├─ themes/
│   ├─ settings.json
├─ Terminal/
│   ├─ settings.json
│   ├─ README.md
├─ Change Windows Default Font/
│   ├─ install-font.ps1
│   ├─ README.md
├─ Discord/
│   ├─ custom.css
│   ├─ README.md
├─ File Explorer/
│   ├─ tweak.reg
│   ├─ README.md
├─ OBS/
│   ├─ profiles/
│   ├─ presets/
│   ├─ README.md
├─ Wallpaper/
│   ├─ *.jpg / *.png
│   ├─ README.md
└─ README.md
```



<p align="center">
Made with ❤️ by abdullah-al-faahim
</p>
