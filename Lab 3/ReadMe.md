# Router Configuration (Creating Passwords, Configuring Interfaces)

This guide covers the basic steps for configuring a router in **Cisco Packet Tracer**, including **creating passwords** for security and **configuring interfaces** to enable network communication.

## Table of Contents
- [Introduction](#introduction)
- [Creating Passwords on a Router](#creating-passwords-on-a-router)
  - [Step 1: Console Password](#step-1-console-password)
  - [Step 2: Enable Password](#step-2-enable-password)
  - [Step 3: VTY (Telnet/SSH) Password](#step-3-vty-telnetssh-password)
  - [Step 4: Enable Secret Password](#step-4-enable-secret-password)
- [Configuring Interfaces](#configuring-interfaces)
  - [Step 1: Assigning IP Addresses](#step-1-assigning-ip-addresses)
  - [Step 2: Enabling Interfaces](#step-2-enabling-interfaces)
  - [Step 3: Verify Interface Status](#step-3-verify-interface-status)
- [Conclusion](#conclusion)
- [References](#references)

---

## Introduction

In this guide, we will configure a router by setting up various passwords to secure access and configuring the router's interfaces for communication. Configuring a router properly is essential for enabling data transmission within a network and ensuring security.

---

## Creating Passwords on a Router

### Step 1: Console Password

The **console password** protects access to the router's console (physical access).

1. Enter **global configuration mode**:
    ```bash
    configure terminal
    ```
2. Access the **console line configuration**:
    ```bash
    line console 0
    ```
3. Set the console password:
    ```bash
    password <your_password>
    ```
4. Enable login to require the password:
    ```bash
    login
    ```
5. Exit the console configuration:
    ```bash
    exit
    ```

### Step 2: Enable Password

The **enable password** protects access to **privileged EXEC mode**.

1. Enter **global configuration mode**:
    ```bash
    configure terminal
    ```
2. Set the enable password:
    ```bash
    enable password <your_password>
    ```

### Step 3: VTY (Telnet/SSH) Password

The **VTY password** is used to secure remote access via **Telnet** or **SSH**.

1. Access the **VTY line configuration**:
    ```bash
    line vty 0 4
    ```
2. Set the VTY password:
    ```bash
    password <your_password>
    ```
3. Enable login to require the password:
    ```bash
    login
    ```
4. Exit the VTY configuration:
    ```bash
    exit
    ```

### Step 4: Enable Secret Password

The **enable secret** is a more secure version of the enable password because it is encrypted.

1. Enter **global configuration mode**:
    ```bash
    configure terminal
    ```
2. Set the enable secret password:
    ```bash
    enable secret <your_secret_password>
    ```

---

## Configuring Interfaces

### Step 1: Assigning IP Addresses

To configure an interface, you need to assign it an IP address and subnet mask.

1. Enter **global configuration mode**:
    ```bash
    configure terminal
    ```
2. Enter the **interface configuration mode** for the desired interface (e.g., GigabitEthernet 0/0):
    ```bash
    interface gigabitEthernet 0/0
    ```
3. Assign an IP address and subnet mask to the interface:
    ```bash
    ip address <IP_address> <subnet_mask>
    ```

### Step 2: Enabling Interfaces

After assigning an IP address, the interface needs to be enabled to be operational.

1. Enter the **interface configuration mode** (if not already in it):
    ```bash
    interface gigabitEthernet 0/0
    ```
2. Use the following command to enable the interface:
    ```bash
    no shutdown
    ```

### Step 3: Verify Interface Status

To verify that the interfaces are correctly configured and up, use the following command in **privileged EXEC mode**:
```bash
show ip interface brief
