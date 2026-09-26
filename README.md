# Homelab

This is my home network and server lab. I built it to host my own services, teach myself networking from the ground up, and get comfortable with the same kinds of tools used in real IT jobs. Everything here I set up, broke, and fixed myself.

## Network Diagram

<img width="1000" height="590" alt="Network diagram" src="https://github.com/user-attachments/assets/39c14ec4-4b99-4d54-b7f1-601d77636f95" />

## What I Built

- Built my own server from parts I picked out and bought one by one
- Turned a Dell OptiPlex 3020 into a firewall and router running OPNsense
- Split my network into separate VLANs
- Set up two Wi-Fi networks, one of which sends everything through a VPN automatically
- Configured a Cisco Catalyst 3850 switch from the command line (VLANs, trunking, ports)
- Run a Ubiquiti access point managed by a UniFi controller I host myself
- Run TrueNAS SCALE for storage, file sharing, and self-hosted apps
- Set up a PoE security camera with Frigate for recording and detection
- Self-host media streaming, game servers, and automatic photo backups
- Built and hosted my own website to advertise my Minecraft servers
- Run virtual machines on my server, including Windows 10, Ubuntu, and Kali Linux
- Run a local AI chatbot on my own hardware with Ollama and Open WebUI
- Set up Tailscale so I can reach my server from anywhere without opening any ports

## Project Pages

- [Server build](server.md): the hardware and how it's set up
- [OPNsense router and VPN Wi-Fi](opnsense-router.md): my firewall, VLANs, and VPN network
- [Wi-Fi and switching](wifi-and-switching.md): the Cisco switch and Ubiquiti access point
- [Self-hosted apps and storage](self-hosted-apps.md): everything running on TrueNAS
- [Problems I solved](problems-i-solved.md): things that broke and how I fixed them
