---
title: "Homelab"
description: "An overview of my home lab: the hardware it runs on, how storage is organized, and the services it hosts."
date: 2026-09-24
---

## Hardware

I take a semi-scavenged approach. My homelab is made up of repurposed hardware with as few new parts as possible.

### Server

The heart of things is a custom-built server made using old parts, new hard drives, all tucked into a Node 804 case. It has an i7-9700k CPU and 64GB of DDR4 RAM, running TrueNAS Scale. It is accompanied by a couple of Raspberry Pis that I've had for years (before the great RAM crisis).

### Raspberry Pis

- One Pi3 running PiHole. I prefer to have anything that could bring the entire network down on dedicated hardware rather than virtualized. I'm aware I could run a failover, but I haven't had the need to do so yet.
- A Pi4 running HomeAssistant. Again for reliability and simplicity, this is decoupled from the main server.

## Storage

The main pool is 4 x 4TB drives in a ZFS array. I don't keep a ton of media, so this is plenty for what I archive. Important files are backed up offsite to encrypted cloud storage.

## Services

All services that don't run on dedicated hardware mentioned above run in Docker containers using Compose files.

- Media
  - Navidrome
  - Immich (photo backup)
- Networking
  - PiHole
  - Wireguard (VPN for external access)
