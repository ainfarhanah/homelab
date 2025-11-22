# My homelab server setup (hannah@homelab) 
Updated: 14-Nov-25 (configuration in progress — 55%)

A simple and clean homelab running on VirtualBox with Ubuntu Server 24.04.  
This setup is used to host my self-built applications, learn deployment, and practice server management.

## Overview
**Virtualization:** VirtualBox  
**OS:** Ubuntu Server 24.04  
**Main Purpose:** Host apps, learn deployment, build portfolio

## Homelab Architechture Diagram
```mermaid

flowchart LR
 subgraph UbuntuVM["Ubuntu Server 24.04.3 LTS<br>4GB RAM • 1TB Storage"]
        Nginx["Nginx Reverse Proxy<br>(Future Expansion)"]
        Docker["🐳 Docker Containers<br>(Future Expansion)"]
        SystemD["Van Cik Lin App<br>systemd + Gunicorn"]
        CasaOS["📦 CasaOS"]
        MySQL[("MySQL DB")]
        SSH["SSH Access"]
        CloudflareTunnel["☁️ Cloudflare Tunnel"]
  end
 subgraph PhysicalHost["Aftershock Forge 15R<br>16GB RAM • 512GB SSD"]
        VirtualBox["VirtualBox"]
        UbuntuVM
  end
 subgraph ClientDevices["Clients"]
        LaptopClient["💻 Laptop"]
        DesktopClient["🖥️ Desktop"]
        PhoneClient["📱 Phone"]
  end
    Internet(("🌐 Internet")) --> Router["Fiber Home<br>HG6240A"]
    Router --> WifiMesh["Maxis Wi-fi CERTIFIED EasyMesh"]
    WifiMesh --> PhysicalHost
    WifiMesh --> ClientDevices
    VirtualBox --> UbuntuVM
    ClientDevices --> CloudflareTunnel

```
## Host Machine (Laptop)
CPU: AMD Ryzen 5 3600 (6 cores / 12 threads, up to 4.2 GHz)

RAM: 16 GB DDR4

OS (Host): Windows 11

## Virtualization
Virtualizer: VirtualBox

Allocated vCPU: 4cores

Allocated RAM: 8GB

Allocated Storage: 1TB Virtual Disk


## Guest VM (Server)
OS: Ubuntu Server 24.04 LTS
Services:
  - MySQL Database Server
  - Nginx Reverse Proxy - future expansion
  - Flask App (systemd managed) 
  - Docker Engine - future expansion
  - CasaOS for container management
