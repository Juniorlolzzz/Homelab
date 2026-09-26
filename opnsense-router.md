# OPNsense Router

My home router runs OPNsense, a free, open-source firewall I installed and set up myself instead of using a store-bought router. It controls my whole network: the firewall, my VLANs, DHCP, DNS, and a VPN I built into it.

<img width="300" height="400" alt="OPNsense router" src="https://github.com/user-attachments/assets/7414ea3c-4dd9-4e34-bfc3-ab37a9ba05f9" />

## Hardware

- Device: Dell OptiPlex 3020 (small form factor)
- CPU: Intel Core i5-4590 (4 cores, 3.3 GHz)
- RAM: 8GB DDR3
- Storage: 240GB SATA SSD
- Network: dual-port gigabit PCIe network card

## What It Does

- Routes and firewalls all traffic for my home network
- Handles DHCP and DNS for every device
- Connects to a Cisco Catalyst 3850 switch that carries multiple VLANs
- Works with a Ubiquiti access point to run two separate Wi-Fi networks
- Supports both IPv4 and IPv6 on my main network

## My Networks

- LAN: my main home network
- VPNWIFI (VLAN 20): the Wi-Fi network that goes through the VPN
- protonvpn: the WireGuard tunnel interface

## VPN Wi-Fi

I made a second Wi-Fi network that sends everything through a VPN automatically. Any device that joins it is protected without needing a VPN app.

- Set up a WireGuard tunnel from OPNsense to ProtonVPN
- Made a separate VLAN (VLAN 20) just for the VPN network
- Tagged VLAN 20 on the Cisco switch and gave it its own SSID on the Ubiquiti access point
- Set up DHCP so devices on the VPN network get their own addresses
- Wrote firewall rules that force all VLAN 20 traffic through the VPN
- Added a killswitch: if the VPN drops, that network loses internet instead of leaking out unprotected

<img width="600" height="300" alt="OPNsense screenshot" src="https://github.com/user-attachments/assets/8a9ea254-9fcb-41bf-8e47-5d41636589ad" />

<img width="600" height="300" alt="OPNsense screenshot" src="https://github.com/user-attachments/assets/5f6d0974-4ec0-41f0-8fe5-73e0d4959824" />

## Proof It Works

I tested it with ipleak.net from my phone on both Wi-Fi networks:

- On my normal Wi-Fi, it shows my home internet provider in Oregon
- On the VPN Wi-Fi, it shows ProtonVPN in Washington
- On the VPN Wi-Fi, my phone gets an address from the VLAN 20 network
- IPv6 doesn't get through on the VPN Wi-Fi, so it can't leak around the tunnel

[add your two ipleak screenshots here, with your home IP blurred]

## What I Learned

- How VLANs and trunking work between a router, a switch, and an access point
- How to send traffic a certain way based on which network a device is on
- How to write firewall rules and test them so traffic can't leak
- How DNS can leak around a VPN, and how to check for it
