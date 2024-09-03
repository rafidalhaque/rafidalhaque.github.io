---
title: Install CasaOS in Arch Linux
description: Tutorial to install casaos in arch linux
slug: casaos-in-arch
date: 2023-12-17 15:00:00+0600
categories:
  - writeups
  - tutorial
tags:
  - writeups
  - casaos
  - home server
  - arch linux
  - tutorial
draft: true
---

Assalamu Alaikum Wa Rahmatullah. CasaOS is a personal homelab management system. Today we are going to see how it could be installed in archlinux. 

> CasaOS is not officially tested in Archlinux. Beware about this before proceed out!

1. Update The Archlinux

update the archlinux.

```bash
sudo pacman -Syu
```

2. Install required dependencies from Arch Official repository

```bash
sudo pacman -S wget curl smartmontools ntfs-3g net-tools samba apparmor docker parted cifs-utils unzip docker-compose rclone
```

3. Install required dependencies from AUR via YAY

```bash
yay -Syu
yay -S udevil mergerfs
```

4. Enable and Start Docker

```bash
sudo systemctl enable --now docker
```


https://wiki.casaos.io/en/guides/install-on-arch-linux