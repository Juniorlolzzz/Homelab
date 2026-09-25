OPNsense Router

My home router runs OPNsense, a free, open-source firewall I set up myself instead of using a regular store-bought router. It controls my whole network: firewall, Wi-Fi networks, and a built-in VPN.

[paste a photo of the router here]

Hardware

- Device: [model of the box OPNsense runs on]
- CPU: [cpu]
- RAM: [ram]
- Storage: [drive]
- Network ports: [how many / speed]

What It Does

- Routes and firewalls all traffic for my home network
- Connects to a Cisco Catalyst 3850 switch that carries multiple VLANs
- Works with a Ubiquiti access point to run two separate Wi-Fi networks

VPN Wi-Fi

I made a second Wi-Fi network that automatically sends everything through a VPN. Any device that joins it is protected without needing a VPN app.

- Set up a WireGuard tunnel from OPNsense to ProtonVPN
- Made a separate VLAN (VLAN 20) just for the VPN network
- Tagged VLAN 20 on the Cisco switch and gave it its own SSID on the Ubiquiti access point
- Set up DHCP so devices on the VPN network get their own addresses
- Wrote firewall rules that force all VLAN 20 traffic through the VPN
- Added a killswitch: if the VPN drops, that network loses internet instead of leaking out unprotected

[paste a screenshot of the WireGuard status or firewall rules here]
