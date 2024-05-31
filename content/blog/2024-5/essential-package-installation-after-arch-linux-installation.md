+++
title = 'Essential Package Installation After Arch Linux Installation'
date = 2024-05-31T16:32:49+03:00
draft = false
author = "murat"
lang = "en"
type = "blog"
description = "Arch Linux"
slug = "essential-package-installation-after-arch-linux-installation"
keywords = "[linux]"
cover = { image = "", alt = "" }
+++


## Installing Packages with Pacman on Arch Linux
``` shell
sudo pacman curl git fastfetch rclone htop kitty zsh neovim vim emacs firefox docker
```

## This command installs the following pacman packages on Arch Linux:

```markdown
* curl: A command-line tool for transferring data by following URLs.
* git: A tool used for version control systems.
* fastfetch: A tool that allows you to quickly and easily view your system information.
* rclone: A tool used to copy and sync files between cloud storage services.
* htop: A tool that allows you to monitor active processes and system resources in real time.
* kitty: A feature-rich and easy-to-use terminal emulator.
* zsh: A powerful and customizable shell.
* neovim: A text editor designed as a modern alternative to Vim.
* vim: A powerful and customizable text editor.
* emacs: A text processing environment that is a customizable text editor, email client, and more.
* firefox: A popular web browser.
* docker: 
```

## Installing Packages with YAY AUR on Arch Linux
```shell
## Yet Another Yogurt - An AUR Helper Written in Go
pacman -Sy --needed git base-devel
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si
```
## YAY Command List
```shell
yay	## Alias to yay -Syu.
yay <Search Term> ## Present package-installation selection menu.
yay -Bi <dir>	## Install dependencies and build a local PKGBUILD.
yay -G <AUR Package>	## Download PKGBUILD from ABS or AUR. (yay v12.0+)
yay -Gp <AUR Package>	## Print to stdout PKGBUILD from ABS or AUR.
yay -Ps	## Print system statistics.
yay -Syu --devel	## Perform system upgrade, but also check for development package updates.
yay -Syu --timeupdate	## Perform system upgrade and use PKGBUILD modification time (not version number) to determine update.
yay -Wu <AUR Package>	## Unvote for package (Requires setting AUR_USERNAME and AUR_PASSWORD environment variables) (yay v11.3+)
yay -Wv <AUR Package>	## Vote for package (Requires setting AUR_USERNAME and AUR_PASSWORD environment variables). (yay v11.3+)
yay -Y --combinedupgrade --save	## Make combined upgrade the default mode.
yay -Y --gendb	## Generate development package database used for devel update.
yay -Yc	## Clean unneeded dependencies.
	
```

## Installing Packages with YAY AUR on Arch Linux
```shell
yay -S brave-bin lux-dl
```
## This command installs the following YAY AUR packages on Arch Linux:
```markdown
* brave-bin: Web browser that blocks ads and trackers by default (binary release)	
* lux-dl: Fast and simple video download library and CLI tool written in Go
```

## Installing spacemacs on Arch Linux
```shell
git clone https://github.com/syl20bnr/spacemacs $HOME/.emacs.d
```

## Installing doomemacs on Arch Linux
```shell
git clone --depth 1 https://github.com/doomemacs/doomemacs ~/.config/emacs
~/.config/emacs/bin/doom install
```

## Installing oh-my-zsh on Arch Linux
```shell
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

## Installing ollama on Arch Linux
```shell
curl -fsSL https://ollama.com/install.sh | sh
sudo systemctl enable --now ollama
ollama run llama3 ## then run command 
```

## Installing open-webui on Arch Linux
```shell
docker run -d -p 3000:8080 -v ollama:/root/.ollama -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:ollama

```
## Installing docker on Arch Linux
```shell
sudo pacman -S docker
sudo systemctl status docker
sudo systemctl start docker
sudo systemctl enable docker
```
