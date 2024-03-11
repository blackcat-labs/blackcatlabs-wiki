# Alturas
## :fontawesome-solid-info: Basic Info
**Server type:** Dedicated server  
**Hosting provider:** :simple-hetzner: Hetzner  
**Datacenter:**  HEL1-DC2

**OS:** Proxmox VE 8.1//Debian Bookworm

## :fontawesome-solid-network-wired: Network
**Hostname:** `alturas.blkcat.space`  
**Primary WAN IP:** `95.216.102.203` (:material-wall-fire: Firewall closed to outside connections - Hetzner stateless FW)  
**Additional WAN IPs:** `95.216.102.201` - :simple-opnsense: OPNsense firewall/router  
**On Tailnet:** :material-check-circle-outline: Yes  
**Tailnet IP:**  
`100.115.52.77` PVE Bare Metal  
`100.93.18.75` OPNsense Subnet

## :octicons-cpu-24: Hardware
**Processor:** Intel Core i7-8700  
**Memory:** 4x RAM 16384 MB DDR4 = ~64GB total  
**Storage:** 2x SSD M.2 NVMe 1 TB @ RAID1 = ~1TB total  
**NIC:**  NIC 1 Gbit Intel I219-LM

## :octicons-pencil-24: Other notes
Primary IP Info:  
```
IPv4: 95.216.102.203/26
Gateway: 95.216.102.193
Routed to WAN Proxmox bridge
```

Secondary IP Info:
```
IPv4: 95.216.102.201
Virtual MAC address: 00:50:56:01:16:F1
Routed to OPNsense firewall/router
```