---
title: Raspberry Pi 4 Home Server.
date: 2020-11-18 10:00:00 +07:00
tags: [Raspberry-Pi]
description: Nginx, Jenkins and other keywords
---
![hi](rasp-pi.jpg)

## Why do you need a home server?

-------------------

I chose to host my websites locally for privacy concerns, cost, other keyword reasons but mainly because I can.

## What do you host?  

I host a couple of web applications, a Jenkins dashboard, a couple of tools like cyberchef.

## Why a blog post?

The focus of this blog is not to explain why you need a home server or to convince you that you need a home server.

This is for documentation purposes for me so I can create a build script or a docker container to automate this. I heard ansible is also a good tool but I do not understand much about it **yet**.

## My raspberry pi installation guide. 

----

I had the idea to do this because I was switching from a raspberry pi 3b to a raspberry pi 4.

This might not seem like a big change but I gained 3GB of ram and a giga-byte port.

I planned on booting from a usb 3.1 SSD but raspberry pi 4 doesn't come with usb boot enabled by default so I had to update the EEPROM. 

Luckily, raspbian I was running on my old server is compatible with my new raspberry pi. I backed up my files before this as I did not know if it was actually going to work.

After enabling USB boot, I installed raspbian on the SSD. Any operating system compatible with arm7 works.



```bash
*# I assume you dont want your raspberry pi needing a monitor to use, use it in headless mode*

sudo systemctl enable ssh
sudo systemctl start ssh

*# if you have a provider that lets you assign static Ip addresses use it if not just assign a static ip using the ip address your DHCP server give you*

*#edit /etc/dhcpcd.conf and use the commented out static address*  
interface eth0
static ip_address=10.0.0.x/24
static routers=10.0.0.1
static domain_name_servers=10.0.0.1 8.8.8.8 

sudo ip link set eth0 down && sudo ip link set eth0 up
passwd
sudo apt update
sudo apt full-upgrade
sudo apt install git
sudo apt install neovim
sudo apt install nginx 
sudo apt install tmux
sudo apt install python3-pipi
sudo apt install zsh
*#jekyll*
sudo apt install ruby-full
sudo gem install bundler jekyll


#vim-plug 
​    sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'

sudo apt install openjdk-11-jre
wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -
sudo sh -c "echo 'deb https://pkg.jenkins.io/debian binary/' >> /etc/apt/sources.list.d/jenkins.list"
sudo apt install jenkins

*#raspberry pi doesnt ask for sudo password -- big securty risk*
sudo visudo /etc/sudoers.d/010_pi-nopasswd
change nopasswd to passwd 
```