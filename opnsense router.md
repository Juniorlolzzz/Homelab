OPNsense Router

My home router runs OPNsense open-source firewall I set up myself instead of using a regular store-bought router. It controls my whole network firewall, Wi-Fi networks, and a persoanlly built VPN.

<img width="300" height="500" alt="20260923_001652" src="https://github.com/user-attachments/assets/7414ea3c-4dd9-4e34-bfc3-ab37a9ba05f9" />



Hardware

- Device: optiplex3020
- CPU: Intel(R) Core(TM) i5-4590 CPU
- RAM: 8gb DDR3
- Storage: 240gb sata ssd
- Network ports: Dual-Port 1gb PCIe Gigabit Network Card

What It Does

- Routes and firewalls all traffic for my home network
- Connects to a Cisco Catalyst 3850 switch that carries multiple VLANs
- Works with a Ubiquiti access point to run two separate Wi-Fi networks

VPN Wi-Fi

I made a second Wi-Fi network that automatically sends everything through a VPN. Any device that joins it will be protected without needing a VPN app.

- Set up a WireGuard tunnel from OPNsense to ProtonVPN
- Made a separate VLAN (VLAN 20) just for the VPN network
- Tagged VLAN 20 on the Cisco switch and gave it its own SSID on the Ubiquiti access point
- Set up DHCP so devices on the VPN network get their own addresses
- Wrote firewall rules that force all VLAN 20 traffic through the VPN
- Added a killswitch: if the VPN drops, that network loses internet instead of leaking out unprotected

<img width="300" height="500" alt="image" src="https://github.com/user-attachments/assets/8a9ea254-9fcb-41bf-8e47-5d41636589ad" />

<img width="300" height="500" alt="image" src="https://github.com/user-attachments/assets/5f6d0974-4ec0-41f0-8fe5-73e0d4959824" />
