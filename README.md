#Home Lab


### Hardware
- ISP: WWZ. 10Gbps network. Fiber.
- Interface: GP1101X for symmetrical 10 Gbps bandwidth for IPTV video and data services
- WLAN-Router: Zyxel WLAN AX7501-B0
- Managed Switch:  Zyxel XS1930-10
- Intel NUC10i7FNH1 (Intel Core i7-10710U). 64Gb RAM. 1TB M.2
- LattePand v3. 32Gb RAM, 2x2 TB SSD
- OWC ThunderBay 4 Mini. 4x 1TB SSDs

### Networking
VLANs on the Zyxel XS1930-10 switch:
- VLANs setup to segregate network traffic.
	- VLAN 10: Home automation devices
	- VLAN 20: audio/video streaming
	- VLAN 30: Work workstation
	- VLAN 40: Proxmox host, Nextcloud VM

Note: currently reviewing Wireguard vs ZeroTier (self hosted)

### Software
- Proxmox VE 8.1
- Virtual machines (VM) in Proxmox
	- Self Hosted Cloud VM: Apache, MySQL, PHP, Nextcloud, Let's Encrypt Certbot
	- Self hosted ZeroTier / or other alternatives. For deployed Tailscale
- Containers 
	- Dashy
	- Metabase
	- Guacamole
	- MeshCentral
	- Pi-Hole
	- Vaultwarden
	- Cokpit

### Installation
#### Network
* Router: mostly hardening
* Managed switch: configure VLANs
* VPN: Tailscale 

#### Hypervisor
- Insall Proxmox 8.1
- Configure the OWC ThunderBay 4 Mini storage in Proxmox.
- Mount the RAID volume or individual drives as required.
- Install 
