#Home Lab


## Setup
### Hardware

    ISP: WWZ. 10Gbps network. Fiber. 
    Interface: GP1101X for symmetrical 10 Gbps bandwidth for IPTV video and data services
    WLAN-Router: Zyxel WLAN AX7501-B0
    Managed Switch:  Zyxel XS1930-10
    Intel NUC
    OWC ThunderBay 4 Mini. 4x 1TB SSDs,  zfs, RAID-0 (tbc)

### Networking
VLANs on the Zyxel XS1930-10 switch:
VLANs setup to segregate network traffic.
    VLAN 10: Home automation devices
    VLAN 20: audio/video streaming
    VLAN 30: Work workstation
    VLAN 40: Proxmox host, Nextcloud VM, and Zerotier VM

### Software
Proxmox VE 7.3 on the Intel NUC

Configure the OWC ThunderBay 4 Mini storage in Proxmox. Mount the RAID volume or individual drives as required.

Unbuntu Virtual machine (VM) in Proxmox

Apache, MySQL, PHP, Nextcloud, Let's Encrypt Certbot, and ZeroTier on the Ubuntu VM.


