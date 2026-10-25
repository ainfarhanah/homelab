# hardware used for my homelab

this document records the hardware used throught the development of the homelab

## Phase 1 - laptop-based server environment

the initial environment used a personal laptop to run Ubuntu Server inside VirtualBox.

| Component | Specs|
|-----------|---------------|
|Laptop|AfterShock/Level51 Forge 15R|
|CPU|Ryzen 5 3600|
|GPU|NVidia; GTX-series GPU|
|Hosting OS| Windows 11 Pro|
|Virtualization| Oracle VirtualBox|
|Guest OS| Ubuntu Server 23.04.3 LTS

### Purpose
the laptop provided the initial environment for learning linux administration and deploy services without requiring a separate physical server.

### Limitation
running server workloads inside a virtual machine shares resources with the host os. CPU, RAM, storage performance, and background workloads can affect virtual-machine responsiveness.

## Phase 2 - dedicated homelab host

the homelab subsequently moved to a Lenovo ThinkCentre M900 Tiny running Proxmox VE.

|Component|Specs|
|---------|-----|
|Model|Lenovo ThinkCentre M900 Tiny|
|CPU|Intel Core i5-6500T|
|RAM|16GB|
|Storage| 256GB + 500GB SSD|
|Hypervisor|Proxmox VE|
|Workloads|Linux containers (LXC) and self-hosted services|

### Purpose
the dedicated host separates homelab workloads from everyday desktop environment and provides a platform for managing services independently through proxmox.

### Storage Notes
the storage has two SSDs. their actual assignments, filesystem layouts, capacity allocation and backup destinations should be documented after verification

## Phase 3 - planned hardware improvement
potential improvements include additional storage, a dedicated managed switch, structured cabling and network segmentation.