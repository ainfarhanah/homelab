# homelab

my homelab started in Nov'25 with an Ubuntu Server VM running on my laptop. it has nice grown into a Proxmox setup for hosting applications, experiments with services, and learning server administration and networking.

this repo documents my progress, configurations, troubleshooting, and lessons learned.

## purpose

- host my Van Cik Lin invoicing system and portfolio website.
- learn Linux administration, virtualization and container management.
- practice networking, alongside my CCNA studies and preparation.
- experiments with monitoring, local AI and game server.

## hardware
| device | specification | role |
|--------|---------------|------|
|Aftershock/Level51 Forge 15R | Ryzen 5 3600. 16GB RAM, 512 GB SSD | Original VirtualBox host|
|Lenovo ThinkCentre M900 Tiny| Intel i-6500T, 16GB RAM, 256GB + 512GB| Proxmox host|

## homelab journey
### phase 1 - starting with a laptop
i began by installing ubuntu server 24.04.3 LTS in VirtualBox on my laptop.

- adjusted VM cpu allocation to improve performance.
- purchased a domain for server testing and DNS configuration.
- configured SSH access and UFW.
- set up Cloudflare Tunnel and public hostname for SSH.
- installed Docker, Docker compose and CasaOS.
- installed MySQL and prepared Python environment for Van Cik Lin.
- fixed an application PDF generation issue involving code and database queries.

### phase 2 - moving to Proxmox
i moved to a Lenovo ThinkCentre M900 to build a dedicated homelab server.
- migrated to Proxmox.
- configured static ip addresses for node and LXC containers.
- enabled firewall and resolved rules blocked application access.
- recorded an internet outage caused by a fiber cut.

### phase 3 - improving the setup
i focused on hardware improvements, service liability, service liability, and networking skills.
- upgrade the mini pc to 16gb ram.
- build a custom rack and assembled an arylic mini pc mount
- continued updating the python application
- created an offline page using Cloudflare Pages
- configured services to start automatically and tested them after shutdown.
- completed five days of CCNA training.

## hosted services and experiments
| services | purpose |
|----------|---------|
| vanciklin|host the invoicing and payment tracking for my mother's school transport service|
|portfolio website| host my personal portfolio using Nginx|
|MySQL| provide a local database for van cik lin|
|cloudflare tunnel|provide remote access to selected services|
|AI server| experiments with self-hosted AI model using ollama|
|Better Minecraft 5| hosted a modded Minecraft server for personal gaming|

the AI and minecraft servers are later additions and are not included in my homelab progress log.

## repository content
- documentation: setup guides, progress logs, and troubleshooting notes.
- configurations: sanitized services configurations files.
- scripts: reviewed automation and maintenance scripts.
- assets: screenshots, hardware photos, and architecture diagram.

## next steps
- [ ] document backup and recovery procedures
- [ ] routing, switching and vlan practices
- [ ] configure monitoring page

## lesson learned

this homelab has helped me to understand how vm resources, permission, firewall rules, and service setup setting affect hosted applications.

each installation and troubleshooting session is part of the learning process. i document both the working setup and the problems encountered along the way.
