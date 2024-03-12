# PVE Install on Hetzner dedicated server

## Install PVE using Rescue
1. Reboot the dedicated server into the rescue system - [:octicons-link-external-16: Hetzner doc](https://docs.hetzner.com/robot/dedicated-server/troubleshooting/hetzner-rescue-system/)  
      1. !!! warning
        Make sure you choose your correct SSH key when activating the rescue system! Our policy is to avoid using passwords for SSH whenever possible.

2. SSH into the server in rescue:  
``` bash
ssh root@SERVER-PRIMARY-IP
```
3. Run the Hetzner *installimage* tool:  
```
installimage
```
4. Scroll down to ***Other (No Support)***
5. Select ***PVE on Debian Bullseye***
6. In the config editor, choose RAID1 if at all possible (unless the situation changes and we have more disks to choose from)
7. Setting the hostname, grab an unused name from the [:material-arrow-right: Server name list](../Servers/server-naming-convention.md) and make it a subdomain of `blkcat.space`, so that you end up with something like `servernamefromlist.blkcat.space`
8. Use the following configuration for disk partitioning:  
```
PART  /boot  ext3  1024M
PART  lvm    vg0   all

LV  vg0  swap  swap  swap  6G
LV  vg0  root  /     ext3  all
```
1. Hit ++f10++ to save and continue
2. Say yes / confirm that we're going to delete all existing data from all disks
3. Watch as the magic happens
4. Once the install is finished, run `reboot` to reboot the server out of the rescue system and into your beautiful new Proxmox install!

## Configure PVE Initial Install from Command Line