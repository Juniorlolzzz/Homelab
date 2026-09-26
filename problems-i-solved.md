# Problems I Solved

Things that broke in my homelab and how I fixed them.

## Getting 39+ GB of photos back after an app reset

**What happened:** While reinstalling Immich, my photo backup app, I accidentally deleted it. That wiped its database. The photos were still on the drive, but the app didn't know they existed.

**How I fixed it:** I figured out where Immich stores its files on my server, set the app back up pointing at the same storage, and used its External Library feature to scan the photos back in.

**What I learned:** An app's files and its database are two separate things. Now I back up both.

## Moving all my apps to a new storage pool

**What happened:** I moved my apps from my old storage pool to a new SSD pool. A leftover app folder on the old pool conflicted with the new one.

**How I fixed it:** I found the orphaned folder, cleared up the conflict, and finished the move.

**What I learned:** Plan a storage move before you start, and check what gets left behind.

## Checking my VPN Wi-Fi for leaks

**What happened:** I wanted to make sure the VPN Wi-Fi was hiding everything, not just most of it.

**How I checked:** I ran leak tests from my phone on both Wi-Fi networks. The VPN network showed ProtonVPN's address instead of my home one, and IPv6 was blocked so it couldn't get around the tunnel. I also checked which DNS servers the VPN network uses.

**What I learned:** A VPN can still leak through IPv6 or DNS even when your IP looks right, so you have to test for each one.

