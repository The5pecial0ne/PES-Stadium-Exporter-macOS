# PES Stadium Exporter — macOS Setup

This is a macOS-compatible fork of the PES Stadium Exporter Blender addon.
The original addon bundles Windows binaries and assumes Windows-style file
paths everywhere, so this version runs those same binaries through
Mono/Wine and patches the addon's path handling so it actually works on
macOS, Apple Silicon included.

## Before you install the addon

Run through these steps in Terminal first.

### 1. Install Homebrew

Skip this if you already have it.

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### 2. Install Mono

Lets Mac run `GzsTool.exe`, `FtexTools.exe`, and
`FoxTool.exe` - .NET/Mono assemblies rather than native
Windows binaries, no emulation needed.

```bash
brew install mono
```

### 3. Install CrossOver

```bash
brew install --cask crossover
```

Once it's installed, you're done — the addon automatically finds
CrossOver's bundled Wine binary on its own. Nothing else to configure.

### 4. Install the addon in Blender

Blender → Preferences → Add-ons → Install... → select the addon `.zip` →
enable it.
