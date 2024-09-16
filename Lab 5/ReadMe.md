# Static and Default Routing

This guide explains how to configure **static** and **default routing** on routers using **Cisco Packet Tracer**. Both types of routing are important for controlling the flow of traffic within a network and ensuring that packets are routed correctly.

## Table of Contents
- [Introduction](#introduction)
- [Static Routing](#static-routing)
  - [Step 1: Basic Static Route Configuration](#step-1-basic-static-route-configuration)
  - [Step 2: Verifying Static Route](#step-2-verifying-static-route)
- [Default Routing](#default-routing)
  - [Step 1: Basic Default Route Configuration](#step-1-basic-default-route-configuration)
  - [Step 2: Verifying Default Route](#step-2-verifying-default-route)
- [Troubleshooting Routing](#troubleshooting-routing)
- [Conclusion](#conclusion)
- [References](#references)

---

## Introduction

In networking, routers use **routing tables** to determine where to send packets. Routers can learn about routes dynamically or through manual configuration. **Static routing** requires manual configuration of routes, while **default routing** is a special type of static route that defines where to send traffic when no specific route exists in the routing table.

---

## Static Routing

### What is Static Routing?

Static routing involves manually configuring routes on the router. It provides direct control over routing but requires manual intervention when there are network topology changes.

### Step 1: Basic Static Route Configuration

1. **Enter global configuration mode**:
    ```bash
    configure terminal
    ```
2. To create a static route, use the following syntax:
    ```bash
    ip route <destination_network> <subnet_mask> <next_hop_ip_address or exit_interface>
    ```
    Example:
    ```bash
    ip route 192.168.2.0 255.255.255.0 192.168.1.2
    ```
    In this example, traffic destined for the `192.168.2.0` network will be sent to the next hop IP address `192.168.1.2`.

3. Alternatively, you can specify the **exit interface** instead of the next hop IP address:
    ```bash
    ip route 192.168.2.0 255.255.255.0 gigabitEthernet 0/1
    ```

### Step 2: Verifying Static Route

After configuring the static route, use the following command to verify if the route has been added to the routing table:
```bash
show ip route
