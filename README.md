# Fun-CLI-Tools-for-Arch-Linux---Complete-Guide

A curated collection of entertaining and useful command-line tools, tested and verified for Arch Linux.

---

## Table of Contents
1. [Direct Install & Run](#direct-install--run)
2. [Interactive Tools (Require Input)](#interactive-tools-require-input)
3. [No Install Required (Just URLs)](#no-install-required-just-urls)
4. [Troubleshooting](#troubleshooting)

---

## Direct Install & Run
*These tools install easily and run with a single command - no additional input needed.*

### From Official Repositories (pacman)

```bash
# Install all at once
sudo pacman -S cowsay fortune-mod cmatrix lolcat figlet sl neofetch htop bat tree

# Or install individually:
sudo pacman -S cowsay          # ASCII cow with speech bubble
sudo pacman -S fortune-mod     # Random quotes and fortunes
sudo pacman -S cmatrix         # Matrix-style falling characters
sudo pacman -S lolcat          # Rainbow colored text output
sudo pacman -S figlet          # ASCII art text generator
sudo pacman -S sl              # Steam locomotive (punishment for typo)
sudo pacman -S neofetch        # System info with ASCII logo
sudo pacman -S htop            # Interactive process viewer
sudo pacman -S bat             # Better 'cat' with syntax highlighting
sudo pacman -S tree            # Display directory tree structure
```

**How to use:**
```bash
fortune                        # Get a random fortune
cowsay "Hello World"          # Make the cow say something
cmatrix                       # Matrix rain (Ctrl+C to exit)
echo "Rainbow text" | lolcat  # Colorful output
figlet "Cool Text"            # Big ASCII text
sl                            # Train animation (can't stop it!)
neofetch                      # Show system info
htop                          # System monitor
bat filename.txt              # View file with highlighting
tree                          # Show directory structure
```

**Fun combinations:**
```bash
fortune | cowsay | lolcat     # Rainbow fortune from a cow
```

---

### From AUR (yay)

**Prerequisites:** Make sure you have `yay` installed. If not:
```bash
sudo pacman -S --needed git base-devel
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si
cd ..
rm -rf yay
```

**Install these tools:**
```bash
# Install individually (recommended to avoid conflicts)
yay -S cbonsai              # Grow a bonsai tree animation
yay -S peaclock             # Beautiful terminal clock
yay -S tty-clock            # Simple digital clock
yay -S asciiquarium         # ASCII fish tank
yay -S nyancat              # Nyan cat animation
yay -S ponysay              # Like cowsay but with ponies
yay -S pipes.sh             # Animated pipes screensaver
yay -S ricksay              # Rick and Morty version of cowsay
yay -S mapscii              # World map in ASCII (interactive)
```

**How to use:**
```bash
cbonsai                       # Default bonsai
cbonsai -l                    # Live growing animation
cbonsai -m "Relax..."        # With custom message
peaclock                      # Beautiful clock display
tty-clock                     # Simple clock
tty-clock -c                  # Centered clock
asciiquarium                  # Aquarium (Ctrl+C to exit)
nyancat                       # Nyan cat (Ctrl+C to exit)
ponysay "Hello"              # Pony says hello
pipes.sh                      # Pipes animation
pipes.sh -p 10 -t 2          # 10 pipes, type 2
ricksay                       # Random Rick quote
ricksay "Wubba lubba dub dub" # Rick says your text
mapscii                       # Interactive world map
```

---

## Interactive Tools (Require Input)
*These tools need additional commands or interaction after launching.*

### From Official Repositories

```bash
sudo pacman -S nethack        # Classic dungeon crawler game
sudo pacman -S moon-buggy     # Side-scrolling game
```

**How to use:**
```bash
nethack                       # Start game, follow on-screen prompts
moon-buggy                    # Use arrow keys and spacebar
```

---

### From AUR

```bash
yay -S 2048-cli              # 2048 puzzle game
yay -S bastet                # Evil Tetris
yay -S nudoku                # Sudoku game
yay -S termsaver             # Terminal screensaver collection
yay -S gottet                # Falling blocks game (Tetris)
yay -S maze-cli              # Maze generator/solver
yay -S no-more-secrets       # Decrypt effect (needs text input)
```

**How to use:**
```bash
2048                          # Use arrow keys to play
bastet                        # Arrow keys to play Tetris
nudoku                        # Follow prompts to play Sudoku
termsaver                     # Choose screensaver from menu
gottet                        # Arrow keys for Tetris
maze-cli                      # Follow prompts to generate/solve
no-more-secrets               # Type: ls -l | nms
```

**no-more-secrets examples:**
```bash
ls -l | nms                   # Decrypt effect on directory listing
echo "Secret message" | nms   # Decrypt your text
```

---

## No Install Required (Just URLs)
*These work directly via curl/telnet - no installation needed!*

```bash
# Weather forecast for your location
curl wttr.in

# Weather for specific city
curl wttr.in/London

# Party parrot animation
curl parrot.live

# Crypto currency rates
curl rate.sx

# Star Wars Episode IV in ASCII
telnet towel.blinkenlights.nl
# Press Ctrl+] then type 'quit' to exit

# QR code generator
curl qrenco.de/YOUR_TEXT_HERE

# Check your IP
curl ifconfig.me

# ASCII art archive
curl -L http://artscene.textfiles.com/vt100/

# Moon phase
curl wttr.in/Moon
```

---

## Combination Examples

### Rainbow Fortune Cow
```bash
fortune | cowsay | lolcat
```

### Rick's Rainbow Wisdom
```bash
ricksay | lolcat
```

### Matrix Bonsai
```bash
# Run in split terminal:
# Terminal 1:
cmatrix
# Terminal 2:
cbonsai -l
```

### Colorful System Info
```bash
neofetch | lolcat
```

### Colorful Directory Tree
```bash
tree | lolcat
```

### Pipes with Color
```bash
pipes.sh -p 10 -R              # -R for random colors
```

### Fortune Pony Rainbow
```bash
fortune | ponysay | lolcat
```

---

## Troubleshooting

### Package Not Found
```bash
# Update your system first
sudo pacman -Syu
yay -Syu
```

### AUR Build Fails
```bash
# Clean build cache
yay -Sc

# Try installing dependencies manually
yay -S base-devel

# Install one package at a time instead of multiple
```

### Permission Errors
```bash
# Never use sudo with yay
# Only use sudo with pacman
```

### yay Not Installed
```bash
sudo pacman -S --needed git base-devel
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si
cd ..
rm -rf yay
```

### Tool Not Running
```bash
# Check if it's installed
which <tool-name>

# Reinstall if needed
yay -S <package-name>
# or
sudo pacman -S <package-name>
```

### Curl Commands Not Working
```bash
# Check internet connection
ping google.com

# Try with -L flag for redirects
curl -L <url>
```

---

## Quick Reference Card

| Tool | Type | Command | Exit |
|------|------|---------|------|
| cowsay | Direct | `cowsay "text"` | Auto |
| fortune | Direct | `fortune` | Auto |
| cmatrix | Direct | `cmatrix` | Ctrl+C |
| lolcat | Direct | `echo "text" \| lolcat` | Auto |
| figlet | Direct | `figlet "text"` | Auto |
| sl | Direct | `sl` | Wait |
| neofetch | Direct | `neofetch` | Auto |
| cbonsai | Direct | `cbonsai -l` | Ctrl+C |
| pipes.sh | Direct | `pipes.sh` | Ctrl+C |
| asciiquarium | Direct | `asciiquarium` | Ctrl+C |
| ponysay | Direct | `ponysay "text"` | Auto |
| ricksay | Direct | `ricksay` | Auto |
| peaclock | Direct | `peaclock` | Ctrl+C |
| mapscii | Interactive | `mapscii` | q |
| nethack | Interactive | `nethack` | Ctrl+C |
| 2048-cli | Interactive | `2048` | q |
| wttr.in | URL | `curl wttr.in` | Auto |
| parrot.live | URL | `curl parrot.live` | Ctrl+C |
| Star Wars | URL | `telnet towel...` | Ctrl+] quit |

---

## Installation Script

Save this as `install-fun-tools.sh`:

```bash
#!/bin/bash

echo "Installing fun CLI tools..."

# Official repos
echo "Installing from official repositories..."
sudo pacman -S --needed cowsay fortune-mod cmatrix lolcat figlet sl neofetch htop bat tree

# Check if yay is installed
if ! command -v yay &> /dev/null; then
    echo "yay not found. Installing yay..."
    sudo pacman -S --needed git base-devel
    git clone https://aur.archlinux.org/yay.git
    cd yay
    makepkg -si
    cd ..
    rm -rf yay
fi

# AUR packages (install one by one to avoid conflicts)
echo "Installing from AUR..."
yay -S --needed cbonsai
yay -S --needed peaclock
yay -S --needed tty-clock
yay -S --needed asciiquarium
yay -S --needed ponysay
yay -S --needed pipes.sh
yay -S --needed ricksay

echo "Installation complete!"
echo "Try: fortune | cowsay | lolcat"
```

Make it executable and run:
```bash
chmod +x install-fun-tools.sh
./install-fun-tools.sh
```

---

## Recommended Starter Pack

**Minimum fun (official repos only):**
```bash
sudo pacman -S cowsay fortune-mod lolcat figlet sl
fortune | cowsay | lolcat
```

**Medium fun (add some AUR):**
```bash
sudo pacman -S cowsay fortune-mod lolcat figlet sl cmatrix
yay -S cbonsai pipes.sh
cbonsai -l
```

**Maximum fun (everything):**
```bash
# Run the installation script above
./install-fun-tools.sh
```

---

## Notes

- Most animations can be stopped with `Ctrl+C`
- `sl` (steam locomotive) cannot be stopped - you must wait!
- Tools with `| lolcat` at the end add rainbow colors
- Telnet Star Wars requires `telnet` package: `sudo pacman -S inetutils`
- Some AUR packages may take time to build

---

**Created for Arch Linux with Caelestia-dots**  
Last updated: February 2026
