# Network Address Translation (NAT) Configuration with Cisco Packet Tracer

This repository contains projects and examples related to **Network Address Translation (NAT)** using **Cisco Packet Tracer**. NAT is essential for translating private IP addresses to public IP addresses and vice versa, enabling multiple devices on a local network to share a single public IP address.

## Table of Contents
- [Introduction](#introduction)
- [Technologies](#technologies)
- [Project Features](#project-features)
- [How to Use](#how-to-use)
- [File Structure](#file-structure)
- [Contributions](#contributions)
- [License](#license)

## Introduction

**Network Address Translation (NAT)** allows a router or firewall to translate private IP addresses used within a local network to a public IP address for external communication. This project demonstrates how to configure NAT on Cisco routers, including:

- **Static NAT**: Maps a specific internal IP address to a specific public IP address.
- **Dynamic NAT**: Maps internal IP addresses to a pool of public IP addresses.
- **PAT (Port Address Translation)**: Maps multiple internal IP addresses to a single public IP address with port differentiation.

## Project Features

- **Static NAT Configuration**: Examples showing one-to-one mapping between internal and public IP addresses.
- **Dynamic NAT Configuration**: Demonstrations of how to configure NAT with a pool of public IP addresses.
- **PAT Configuration**: Setting up PAT to allow multiple devices to share a single public IP address.
- **Testing and Verification**: Tools to verify NAT operation, including ping and traceroute tests.

## How to Use

### Prerequisites
- [Cisco Packet Tracer](https://www.netacad.com/courses/packet-tracer) installed on your system.
- Basic understanding of NAT concepts and IP addressing.

### Steps:
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/nat-configuration-packet-tracer.git
