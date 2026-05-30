---
title: Linux Mint
summary: All things Linux Mint
date: 2024-11-09T15:06:00+08:00
lastmod: 2024-11-09T15:06:00+08:00
_build:
  render: always
  list: always
draft: false
categories: 📝 Notes
tags:
  - linux
---
## Apps

### golang

https://go.dev/doc/install

rm -rf /usr/local/go && tar -C /usr/local -xzf go1.14.3.linux-amd64.tar.gz

export PATH=$PATH:/usr/local/go/bin

go version

### git

apt-get install git

### vlc

apt-get install vlc

### bimp

https://github.com/alessandrofrancesconi/gimp-plugin-bimp?tab=readme-ov-file#compiling-and-installing-on-linux

sudo apt-get install libgimp2.0-dev libgegl-dev

### ffmpeg

apt-get install ffmpeg

### vscodium

https://vscodium.com/#install

wget -qO - https://gitlab.com/paulcarroty/vscodium-deb-rpm-repo/raw/master/pub.gpg \
    | gpg --dearmor \
    | sudo dd of=/usr/share/keyrings/vscodium-archive-keyring.gpg

echo 'deb [ signed-by=/usr/share/keyrings/vscodium-archive-keyring.gpg ] https://download.vscodium.com/debs vscodium main' \
    | sudo tee /etc/apt/sources.list.d/vscodium.list

sudo apt update && sudo apt install codium

### brave

https://brave.com/linux/

sudo apt install curl

sudo curl -fsSLo /usr/share/keyrings/brave-browser-archive-keyring.gpg https://brave-browser-apt-release.s3.brave.com/brave-browser-archive-keyring.gpg

echo "deb [signed-by=/usr/share/keyrings/brave-browser-archive-keyring.gpg] https://brave-browser-apt-release.s3.brave.com/ stable main"|sudo tee /etc/apt/sources.list.d/brave-browser-release.list

sudo apt update

sudo apt install brave-browser

### media info

https://github.com/linux-man/nemo-mediainfo-tab/releases/tag/v1.0.4

### hugo 

https://github.com/gohugoio/hugo/releases
