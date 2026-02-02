# Fun CLI Tools for Arch Linux - Complete Guide

A curated collection of entertaining and useful command-line tools, tested and verified for Arch Linux.

---

## Table of Contents
1. [Quick Copy-Paste Commands](#quick-copy-paste-commands)
2. [Direct Install & Run](#direct-install--run)
3. [Interactive Tools (Require Input)](#interactive-tools-require-input)
4. [No Install Required (Just URLs)](#no-install-required-just-urls)
5. [Epic Combinations](#epic-combinations)
6. [Troubleshooting](#troubleshooting)

---

## Quick Copy-Paste Commands
*Essential commands you'll use most - just copy and paste!*

### Installation Commands
```bash
# Install everything at once (official repos)
sudo pacman -S cowsay fortune-mod cmatrix lolcat figlet sl neofetch htop bat tree

# Install yay (if you don't have it)
sudo pacman -S --needed git base-devel && git clone https://aur.archlinux.org/yay.git && cd yay && makepkg -si && cd .. && rm -rf yay

# Install AUR favorites
yay -S cbonsai pipes.sh peaclock asciiquarium ponysay ricksay tty-clock

# Install games
yay -S 2048-cli bastet gottet nudoku
```

### Most Used Commands
```bash
# Rainbow fortune cow (CLASSIC!)
fortune | cowsay | lolcat

# Live bonsai tree
cbonsai -l

# Pipes screensaver
pipes.sh

# Beautiful clock
peaclock

# Matrix effect
cmatrix

# Train (can't stop!)
sl

# System info
neofetch

# Weather
curl wttr.in

# Party parrot
curl parrot.live

# Star Wars
telnet towel.blinkenlights.nl

# Rick says something
ricksay | lolcat
```

### Quick Setups
```bash
# Add fortune to your shell startup (fish)
echo "fortune | cowsay | lolcat" >> ~/.config/fish/config.fish

# Add fortune to your shell startup (bash)
echo "fortune | cowsay | lolcat" >> ~/.bashrc

# Create alias for quick fun
echo "alias party='curl parrot.live'" >> ~/.config/fish/config.fish
echo "alias weather='curl wttr.in'" >> ~/.config/fish/config.fish
```

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

## Quick Examples

*For the full list of 100+ combinations, see [Epic Combinations](#epic-combinations) section!*

### Rainbow Fortune Cow
```bash
fortune | cowsay | lolcat
```

### Rick's Rainbow Wisdom
```bash
ricksay | lolcat
```

### Colorful System Info
```bash
neofetch | lolcat
```

---

## Epic Combinations
*Mix and match for maximum terminal fun!*

### Classic Combos
```bash
# Rainbow fortune cow (THE CLASSIC)
fortune | cowsay | lolcat

# Rainbow fortune pony
fortune | ponysay | lolcat

# Rick's rainbow wisdom
ricksay | lolcat

# Random wisdom from Rick
fortune | ricksay | lolcat
```

### System Info Combos
```bash
# Rainbow system info
neofetch | lolcat

# Colorful directory tree
tree | lolcat

# Rainbow file listing
ls -la | lolcat

# Colorful disk usage
df -h | lolcat

# Rainbow process list
ps aux | lolcat
```

### Text Art Combos
```bash
# Big rainbow text
figlet "AWESOME" | lolcat

# Cow says big text
figlet "Hello" | cowsay | lolcat

# Pony says big text
figlet "Hello" | ponysay | lolcat

# Rick says big text
figlet "Wubba Lubba" | ricksay | lolcat
```

### File Content Combos
```bash
# Rainbow cat
cat file.txt | lolcat

# Rainbow bat (better cat)
bat file.txt | lolcat

# Rainbow code with syntax
bat script.py | lolcat

# Fortune into file
fortune > wisdom.txt && cat wisdom.txt | cowsay | lolcat
```

### Weather & Info Combos
```bash
# Weather with announcement
echo "Today's Weather:" | figlet | lolcat && curl wttr.in

# Weather told by cow
curl -s wttr.in?format=3 | cowsay | lolcat

# Moon phase by pony
curl -s wttr.in/Moon?format=3 | ponysay | lolcat

# IP address announcement
echo "Your IP:" | figlet && curl ifconfig.me
```

### Multi-Tool Combos
```bash
# Fortune, big text, cow, rainbow
fortune | figlet | cowsay -n | lolcat

# System info with fortune
neofetch && echo "" && fortune | cowsay | lolcat

# Date and time colorful
date | figlet | lolcat

# Uptime announcement
uptime | cowsay | lolcat
```

### Command Output Combos
```bash
# Rainbow git status
git status | lolcat

# Colorful git log
git log --oneline | lolcat

# Rainbow package search
yay -Ss search_term | lolcat

# Colorful process tree
pstree | lolcat

# Rainbow network info
ip a | lolcat
```

### Pipes & Effects Combos
```bash
# Multiple pipes with colors
pipes.sh -p 10 -R -t 2

# Pipes with custom colors
pipes.sh -p 5 -c 1,2,3,4,5

# Fast pipes
pipes.sh -p 8 -f 75

# Slow artistic pipes
pipes.sh -p 3 -f 25 -t 9
```

### Screensaver Combos
```bash
# Matrix with color (in separate terminals)
# Terminal 1: cmatrix
# Terminal 2: pipes.sh

# Matrix with bonsai
# Terminal 1: cmatrix
# Terminal 2: cbonsai -l

# Aquarium with clock
# Terminal 1: asciiquarium
# Terminal 2: peaclock
```

### File System Combos
```bash
# Colorful file search
find . -name "*.txt" | lolcat

# Rainbow disk usage analyzer
du -sh * | sort -h | lolcat

# Colorful file count
ls -l | wc -l | figlet | lolcat

# Directory size with announcement
echo "Directory Sizes:" | figlet && du -sh */ | lolcat
```

### Fun Greeting Combos
```bash
# Morning greeting
echo "Good Morning!" | figlet | cowsay -n | lolcat && curl wttr.in?format=3

# Daily wisdom
date | figlet | lolcat && fortune | cowsay | lolcat

# Login greeting (add to shell config)
echo "Welcome back!" | figlet | lolcat && fortune | ricksay | lolcat
```

### Advanced Combos
```bash
# Random cowfile with fortune
fortune | cowsay -f $(ls /usr/share/cowsay/cows/ | shuf -n1) | lolcat

# All cows say fortune
for cow in /usr/share/cowsay/cows/*.cow; do fortune | cowsay -f $cow | lolcat; sleep 2; done

# Infinite rainbow fortune loop
while true; do fortune | cowsay | lolcat; sleep 3; done

# Random Rick quotes loop
while true; do ricksay | lolcat; sleep 5; done
```

### Bonsai Variations
```bash
# Live bonsai with message
cbonsai -l -m "Relax..."

# Infinite bonsai garden
cbonsai -i -l

# Bonsai with custom base
cbonsai -l -b 2

# Fast growing bonsai
cbonsai -l -t 0.5

# Screensaver mode bonsai
cbonsai -S -l
```

### Code & Development Combos
```bash
# Colorful git diff
git diff | lolcat

# Rainbow test output
npm test | lolcat

# Colorful build output
make | lolcat

# Pretty error messages
command_that_fails 2>&1 | cowsay | lolcat
```

### Monitoring Combos
```bash
# Watch with color
watch -c -n 1 "date | figlet | lolcat"

# Colorful system monitor
htop | lolcat  # Note: might break htop UI

# Network traffic with cow
speedometer -r eth0 -t eth0 | cowsay

# Live log viewing with color
tail -f /var/log/syslog | lolcat
```

### Party Mode Combos 🎉
```bash
# Ultimate party mode (run in different terminals)
# Terminal 1: 
cmatrix

# Terminal 2:
pipes.sh -p 10 -R

# Terminal 3:
while true; do fortune | cowsay | lolcat; sleep 3; done

# Terminal 4:
curl parrot.live
```

### Hacker Mode Combos 💻
```bash
# Fake hacking screen
cat /dev/urandom | hexdump -C | lolcat

# Matrix hacker mode
cmatrix -C green

# Hollywood hacker (if installed)
hollywood

# Fake decryption
ls -lR / | nms  # requires no-more-secrets
```

### Notification Combos
```bash
# Long task notification
long_running_command && notify-send "Done!" "$(fortune)"

# Build complete notification
make && fortune | cowsay | lolcat

# Download complete message
wget file.zip && echo "Download Complete!" | figlet | lolcat
```

### Custom Message Combos
```bash
# Motivational message
echo "You got this!" | figlet | cowsay -n | lolcat

# Break reminder
echo "Take a break!" | figlet | ponysay -n | lolcat

# Success message
echo "BUILD SUCCESS" | figlet | lolcat

# Warning message
echo "WARNING" | figlet | cowsay | lolcat
```

### URL No-Install Combos
```bash
# Weather + parrot party
curl wttr.in && curl parrot.live

# Location weather + moon
curl wttr.in/Tokyo && curl wttr.in/Moon

# Multiple cities weather
for city in Tokyo London Paris; do echo $city | figlet && curl wttr.in/$city?format=3; done

# QR code of IP address
curl ifconfig.me | xargs -I {} curl qrenco.de/{}
```

### Alias Suggestions
*Add these to your shell config for quick access!*

```bash
# For fish shell (~/.config/fish/config.fish)
alias fortune-cow='fortune | cowsay | lolcat'
alias fortune-rick='fortune | ricksay | lolcat'
alias fortune-pony='fortune | ponysay | lolcat'
alias bonsai='cbonsai -l'
alias pipes='pipes.sh -p 10 -R'
alias matrix='cmatrix'
alias clock='peaclock'
alias aquarium='asciiquarium'
alias weather='curl wttr.in'
alias moon='curl wttr.in/Moon'
alias parrot='curl parrot.live'
alias myip='curl ifconfig.me'
alias starwars='telnet towel.blinkenlights.nl'

# For bash shell (~/.bashrc)
alias fortune-cow='fortune | cowsay | lolcat'
alias fortune-rick='fortune | ricksay | lolcat'
alias fortune-pony='fortune | ponysay | lolcat'
alias bonsai='cbonsai -l'
alias pipes='pipes.sh -p 10 -R'
alias matrix='cmatrix'
alias clock='peaclock'
alias aquarium='asciiquarium'
alias weather='curl wttr.in'
alias moon='curl wttr.in/Moon'
alias parrot='curl parrot.live'
alias myip='curl ifconfig.me'
alias starwars='telnet towel.blinkenlights.nl'
```

### One-Line Script Bombs 💣
*Powerful one-liners you can save as scripts!*

```bash
# Random cow fortune loop (save as ~/bin/cow-loop)
while true; do fortune | cowsay -f $(ls /usr/share/cowsay/cows/ | shuf -n1) | lolcat; sleep 3; done

# Daily wisdom (save as ~/bin/daily-wisdom)
echo "$(date '+%A, %B %d, %Y')" | figlet | lolcat && fortune | cowsay | lolcat

# System dashboard (save as ~/bin/dashboard)
clear && neofetch | lolcat && echo "" && echo "Weather:" && curl -s wttr.in?format=3 && echo "" && fortune | cowsay | lolcat

# Pomodoro break (save as ~/bin/break-time)
echo "BREAK TIME!" | figlet | lolcat && cbonsai -l -t 2 -m "Rest for 5 minutes"
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
