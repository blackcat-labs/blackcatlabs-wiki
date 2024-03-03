# PVE Install on Hetzner dedicated server

## Install PVE using Rescue
- Reboot the dedicated server into the rescue system - [:octicons-link-external-16: Hetzner doc](https://docs.hetzner.com/robot/dedicated-server/troubleshooting/hetzner-rescue-system/)
- SSH into the server in rescue
- Run `installimage` to boot into the install assistant
- Scroll down to *Other (No Support)*
- Select *PVE on Debian Bullseye*
- In the config editor, choose RAID1 if at all possible (unless the situation changes and we have more disks to choose from)
- Setting the hostname, grab an unused name from the [:material-arrow-right: Server name list](../Servers/server-naming-convention.md) and make it a subdomain of `blkcat.space`, so that you end up with something like `servernamefromlist.blkcat.space`
- Unless it bites us in the butt later, leave the disk partitions as they are
- Hit ++f10++ to save and continue
- Say yes / confirm that we're going to delete all existing data from all disks
- Watch as the magic happens
- Once the install is finished, run `reboot` to reboot the server out of the rescue system and into your beautiful new Proxmox install!