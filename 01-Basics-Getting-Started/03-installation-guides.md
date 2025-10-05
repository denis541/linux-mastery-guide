# Linux Installation Guides

There are multiple ways to install Linux, depending on your needs and hardware. 

## 1. Virtual Machine (Recommended)
- Install VirtualBox or VMware.
- Create a VM, attach the downloaded Linux ISO.
- Recommended settings: 2–4 GB RAM, 20 GB disk space.
- Install Linux like you would on a real machine.

## 2. Dual Boot
- Shrink your existing Windows partition.
- Create a bootable USB with Rufus (Windows) or BalenaEtcher (Linux/macOS).
- Boot from USB and select "Install alongside Windows".
- Set up user accounts, then reboot.

## 3. Dedicated Machine
- Use the whole disk for Linux.
- Fastest and cleanest option if you don’t need Windows/macOS.

## 4. Cloud Server
- Create a VPS on DigitalOcean/AWS/GCP.
- Choose Ubuntu/Debian/Fedora image.
- Connect via SSH:
```bash
ssh user@server-ip

