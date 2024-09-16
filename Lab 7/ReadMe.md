# Enable and Configure RIP Version 1 (RIPv1) on Cisco Packet Tracer

This guide explains how to enable and configure **RIP Version 1 (RIPv1)** on routers in **Cisco Packet Tracer**. **RIPv1** is a classful, distance-vector routing protocol used to enable dynamic routing between routers.

## Table of Contents
- [Requirements](#requirements)
- [Steps to Configure RIP](#steps-to-configure-rip)
  - [Step 1: Access Router CLI](#step-1-access-router-cli)
  - [Step 2: Enable RIP](#step-2-enable-rip)
  - [Step 3: Advertise Networks](#step-3-advertise-networks)
  - [Step 4: Verify RIP Configuration](#step-4-verify-rip-configuration)
- [Troubleshooting](#troubleshooting)
- [Useful Commands](#useful-commands)
- [References](#references)

## Requirements
- **Cisco Packet Tracer**
- Two or more routers connected via appropriate interfaces
- Basic knowledge of network addressing

## Steps to Configure RIP

### Step 1: Access Router CLI
1. Open **Cisco Packet Tracer**.
2. Select the router you want to configure, then click the **CLI** tab.
3. Enter **privileged EXEC mode** by typing:
    ```bash
    enable
    ```

### Step 2: Enable RIP
1. Enter **global configuration mode**:
    ```bash
    configure terminal
    ```
2. Enable **RIP Version 1** by typing the following command:
    ```bash
    router rip
    ```

### Step 3: Advertise Networks
1. To configure the networks that should participate in RIP, use the `network` command followed by the **network address**. 
    ```bash
    network <network_address>
    ```
    Example:
    ```bash
    network 192.168.1.0
    network 192.168.2.0
    ```
    Note: RIPv1 is a **classful** protocol, so it does not support subnet masks. Make sure to enter classful network addresses (e.g., 192.168.1.0 for a Class C network).

### Step 4: Verify RIP Configuration
1. Exit global configuration mode:
    ```bash
    exit
    ```
2. Verify the RIP routing table by using the following command:
    ```bash
    show ip route
    ```
3. You can also view the RIP configuration with:
    ```bash
    show running-config
    ```
4. To confirm that RIP is sending and receiving routing updates, use:
    ```bash
    debug ip rip
    ```

## Troubleshooting
- Ensure that the routers are connected and their interfaces are up.
- If networks are not being advertised correctly, make sure you’ve used the **correct classful network addresses**.
- Use the `no shutdown` command to ensure the router interfaces are enabled.

## Useful Commands
- `enable`: Enter privileged EXEC mode.
- `configure terminal`: Enter global configuration mode.
- `router rip`: Enable RIP routing protocol.
- `network <network_address>`: Advertise a network.
- `show ip route`: Display the IP routing table.
- `show running-config`: Display the current configuration.
- `debug ip rip`: Monitor RIP updates.

## References
- [Cisco IOS RIP Command Reference](https://www.cisco.com)
- [Networking Basics: RIP Configuration](https://www.networklessons.com)
