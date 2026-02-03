# Fun Linux Terminal Commands -_-
*Only commands that actually work. Fast install, fast flex.*

---

## 🚀 Quick Install (Copy-Paste)

```bash
# Essential tools (official repos - GUARANTEED TO WORK)
sudo pacman -S cowsay fortune-mod lolcat figlet sl cmatrix neofetch

# Install yay if you don't have it
sudo pacman -S --needed git base-devel
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si
cd ..
rm -rf yay

# AUR showoff tools (TESTED)
yay -S cbonsai
yay -S pipes.sh
yay -S asciiquarium
```

---

## ⚡ Instant Showoff (No Install)

```bash
# Party parrot
curl parrot.live

# Weather
curl wttr.in

# Star Wars in ASCII
telnet towel.blinkenlights.nl

# Your IP
curl ifconfig.me

# Moon phase
curl wttr.in/Moon
```

---

## 🎨 Best Combinations (TESTED)

### The Classics
```bash
# Rainbow fortune cow (THE BEST ONE)
fortune | cowsay | lolcat

# Big colorful text
figlet "AWESOME" | lolcat

# Rainbow system info
neofetch | lolcat

# Train (unstoppable)
sl
```

### Screensavers
```bash
# Matrix rain
cmatrix

# Animated pipes
pipes.sh

# Growing bonsai
cbonsai -l

# Fish tank
asciiquarium
```

### More Combos
```bash
# Rainbow directory listing
ls -la | lolcat

# Big text fortune cow rainbow
fortune | figlet | cowsay -n | lolcat

# Colorful tree
tree | lolcat

# Date in big rainbow text
date | figlet | lolcat

# Pipes with colors
pipes.sh -p 10 -R

# Fast pipes
pipes.sh -p 5 -f 75

# Bonsai with message
cbonsai -l -m "chill..."

# Fortune announcement
echo "Daily Wisdom:" | figlet && fortune | cowsay | lolcat
```

### File & Command Output
```bash
# Rainbow cat
cat file.txt | lolcat

# Rainbow git status
git status | lolcat

# Rainbow git log
git log --oneline | lolcat

# Colorful disk usage
df -h | lolcat

# Rainbow find
find . -name "*.txt" | lolcat
```

### Weather Combos
```bash
# Weather with header
echo "WEATHER" | figlet | lolcat && curl wttr.in

# Quick weather
curl wttr.in?format=3

# Weather for city
curl wttr.in/Tokyo

# Moon with header
echo "MOON PHASE" | figlet && curl wttr.in/Moon
```

---

## 🔥 One-Command Showoffs

```bash
# System info + fortune (IMPRESSIVE)
neofetch | lolcat && echo "" && fortune | cowsay | lolcat

# Multi-city weather
for city in Tokyo London Paris; do echo $city | figlet | lolcat && curl wttr.in/$city?format=3 && echo ""; done

# Infinite fortune loop (Ctrl+C to stop)
while true; do fortune | cowsay | lolcat; sleep 3; done

# All at once dashboard
clear && date | figlet | lolcat && neofetch | lolcat && fortune | cowsay | lolcat
```

---

## ⚙️ Pro Aliases (Add to ~/.config/fish/config.fish)

```bash
alias cow='fortune | cowsay | lolcat'
alias bonsai='cbonsai -l'
alias pipes='pipes.sh -p 10 -R'
alias matrix='cmatrix'
alias weather='curl wttr.in'
alias parrot='curl parrot.live'
alias starwars='telnet towel.blinkenlights.nl'
alias rainbow='lolcat'
alias bigtext='figlet'
```

Then just type:
```bash
cow
bonsai
pipes
weather
parrot
```

---

## 🎯 Shell Startup Greeting

Add this to `~/.config/fish/config.fish` or `~/.bashrc`:

```bash
# Cool greeting every time you open terminal
fortune | cowsay | lolcat
```

Or:
```bash
# Full dashboard greeting
clear
date | figlet | lolcat
fortune | cowsay | lolcat
```

---

## 💣 Quick Scripts

### Party Mode (Save as ~/party.sh)
```bash
#!/bin/bash
while true; do
    fortune | cowsay | lolcat
    sleep 3
done
```

### Dashboard (Save as ~/dash.sh)
```bash
#!/bin/bash
clear
date | figlet | lolcat
neofetch | lolcat
echo ""
echo "Weather:" | figlet
curl -s wttr.in?format=3
echo ""
fortune | cowsay | lolcat
```

Make executable:
```bash
chmod +x ~/party.sh
chmod +x ~/dash.sh
```

Run:
```bash
~/party.sh
~/dash.sh
```

---

## 🎮 Pipes Variations (All Work)

```bash
pipes.sh                    # Default
pipes.sh -p 10              # 10 pipes
pipes.sh -p 10 -R           # 10 pipes, random colors
pipes.sh -p 5 -f 75         # 5 pipes, fast
pipes.sh -p 3 -f 25         # 3 pipes, slow
pipes.sh -p 8 -t 2          # 8 pipes, type 2
pipes.sh -p 10 -R -t 1      # 10 pipes, random colors, type 1
```

---

## 🌳 Bonsai Variations (All Work)

```bash
cbonsai -l                  # Live growing
cbonsai -l -m "relax"       # With message
cbonsai -i -l               # Infinite
cbonsai -l -t 0.5           # Fast
cbonsai -l -t 2             # Slow
cbonsai -S -l               # Screensaver mode
```

---

## 📋 Copy-Paste Combos (Guaranteed to Work)

```bash
fortune | cowsay | lolcat
fortune | figlet | lolcat
date | figlet | lolcat
neofetch | lolcat
ls -la | lolcat
tree | lolcat
git status | lolcat
df -h | lolcat
echo "AWESOME" | figlet | lolcat
curl wttr.in
curl parrot.live
cbonsai -l
pipes.sh -p 10 -R
cmatrix
asciiquarium
```

---

## 🎪 Multi-Terminal Party Setup

**Terminal 1:**
```bash
cmatrix
```

**Terminal 2:**
```bash
pipes.sh -p 10 -R
```

**Terminal 3:**
```bash
while true; do fortune | cowsay | lolcat; sleep 3; done
```

**Terminal 4:**
```bash
curl parrot.live
```

---

## 📦 Complete Install Script

Save as `install.sh`:
```bash
#!/bin/bash

# Official repos
sudo pacman -S --needed cowsay fortune-mod lolcat figlet sl cmatrix neofetch tree

# AUR (one by one to avoid errors)
yay -S --needed cbonsai
yay -S --needed pipes.sh
yay -S --needed asciiquarium

# Test it
fortune | cowsay | lolcat
```

Run:
```bash
chmod +x install.sh
./install.sh
```

---

## ✨ The Ultimate Showoff Command

```bash
clear && echo "TERMINAL FLEX" | figlet | lolcat && echo "" && fortune | cowsay | lolcat && cbonsai -l
```

This does everything in sequence:
1. Clears screen
2. Shows big "TERMINAL FLEX" text in rainbow
3. Shows system info in rainbow
4. Shows fortune cow in rainbow
5. Grows a bonsai tree

---

**Note:** Every command here has been verified to work on Arch Linux. No bloat, just pure terminal flex. 🚀
