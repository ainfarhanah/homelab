# My homelab server setup (hannah@homelab) 
Updated: 24-Nov-25 (configuration in progress -------50%------)

A simple and clean homelab running on VirtualBox with Ubuntu Server 24.04.  
This setup is used to host my self-built applications, learn deployment, and practice server management.

## Overview
**Virtualization:** VirtualBox  
**OS:** Ubuntu Server 24.04  
**Main Purpose:** Host apps, learn deployment, improve DevOps knowledge, build portfolio

## Host Machine (Laptop)
CPU: AMD Ryzen 5 3600 (6 cores / 12 threads, up to 4.2 GHz)
RAM: 16 GB DDR4
Storage: 512 GB NVMe SSD
Display: 15.6" FHD (1920x1080)
Keyboard: RGB Backlit
OS (Host): Windows / Linux (based on your current setup)

## Virtualization
Virtualizer: VirtualBox
Allocated vCPU: 2–4 cores
Allocated RAM: 4–8 GB
Allocated Storage: 50–100 GB Virtual Disk (VDI)

## Guest VM (Server)
OS: Ubuntu Server 24.04 LTS
Services:
  - MySQL Database Server
  - Nginx Reverse Proxy
  - Flask App (systemd managed)
  - Docker Engine
  - CasaOS for container management
