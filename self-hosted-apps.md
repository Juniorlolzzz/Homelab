# Self-Hosted Apps and Storage

Everything here runs on my [server](server.md) using TrueNAS SCALE. Instead of paying for cloud services, I host my own versions and manage them myself.

<img width="500" height="300" alt="image" src="https://github.com/user-attachments/assets/f09d5a15-7ea6-4da1-8d5a-8c6580dbb929" />


## Apps I Run

- Immich: automatic photo and video backup from our phones (my own Google Photos)
- Jellyfin and Plex: streaming my own movie and TV library to any device
- Frigate: records my PoE security camera and detects people and objects
- UniFi Network Application: manages my Ubiquiti access point
- Crafty: runs and manages my Minecraft servers
- Ollama and Open WebUI: a local AI chatbot running on my own hardware, no cloud needed
- Dockge: manages my Docker Compose apps from one page

## File Sharing

I set up Windows (SMB) shares so every computer in the house can reach the server like a regular network drive:

- media: movies and TV for the streaming apps
- everything: general files
- ISO: installer images for building virtual machines
- external_drive: the external backup drive

<img width="886" height="320" alt="image" src="https://github.com/user-attachments/assets/384b9675-fce8-4bb3-9933-5e0ebf9ae5f6" />


## Storage Pools

- An SSD pool for apps and their data, so they run fast
- A hard drive pool for bulk storage like media
- A separate pool for the external drive

I moved all my apps from one pool to another and added an NVMe drive to grow the SSD pool.

## Virtual Machines

I run virtual machines on the server to practice with different operating systems:

- Windows 10
- Ubuntu
- Kali Linux

## Game Servers and Website

- Host Minecraft servers for friends
- Built and host my own website to advertise the servers: [add link]
