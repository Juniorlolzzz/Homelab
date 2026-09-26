# Wi-Fi and Switching

## Cisco Catalyst 3850 Switch

This is an enterprise switch, the kind used in offices and schools. I configured it by hand from the command line instead of a web page.

- Created VLANs to keep my networks separate
- Set up a trunk link to the router so multiple VLANs share one cable
- Set up the port going to the access point to carry both Wi-Fi networks
- Set up access ports for wired devices

<img width="500" height="300" alt="image" src="https://github.com/user-attachments/assets/76ebb489-6f54-4482-a92c-594eaf8c3f36" />



## Ubiquiti Access Point

My Wi-Fi comes from a Ubiquiti UniFi AP AC HD. I manage it with the UniFi Network Application, which I host myself on my server instead of buying a UniFi controller.

- Two Wi-Fi networks (SSIDs): my normal one and a VPN one on VLAN 20
- Both 2.4 GHz and 5 GHz bands
- 40 MHz channel width on 5 GHz for a steadier connection
- 100% Wi-Fi connection success rate in the UniFi dashboard (connecting, logging in, getting an address, and DNS)

[add your UniFi dashboard screenshot here]

## What I Learned

- How to use the Cisco command line (IOS) to set up VLANs and trunks
- How one Wi-Fi access point can put devices on different networks
- How to read Wi-Fi health info like signal strength and retries
