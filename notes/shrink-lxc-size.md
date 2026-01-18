# Shrink LXC storage size

I put too much storage for a web app container. So I decided to shrink the size from 200GB to 15GB. 

Stop the LXC first.

Open the node terminal

Backup everything in the container ```102```
```bash
vzdump 102 -storage local -compress lzo
```
Then, destroy the container
```bash
pct destroy 102
```
And restore the ```102``` container with size ```15GB```
```bash
pct restore 102 /var/lib/vz/dump/vzdump-lxc-102-2026_01_18-21_19_44.tar.lzo --rootfs local-lvm:15
```
