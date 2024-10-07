# Configuring RIP Version 2 (RIPv2) in Cisco Packet Tracer
This guide provides step-by-step instructions for configuring RIPv2 on routers in Cisco Packet Tracer. RIP is a distance-vector routing protocol that uses hop count as the metric for determining the best path.

## Steps to Enable RIPv2 on a Router
**Step 1: Access the Router CLI**
- Click on the router in Cisco Packet Tracer to open the CLI.
- Enter privileged EXEC mode by typing:
```bash
Router> enable
```
**Step 2: Enter Global Configuration Mode**
- To enter global configuration mode, type:

```bash
Router# configure terminal
```

**Step 3: Enable RIP and Select Version 2**
- Enable RIP and configure the router to use RIP version 2 by typing:

```bash
Router(config)# router rip
Router(config-router)# version 2
```

**Step 4: Add Network Statements**
- Specify the networks that will participate in RIP routing. For each network, use:

```bash
Router(config-router)# network [network-address]
```

**Example :**

```bash
Router(config-router)# network 192.168.1.0
Router(config-router)# network 10.0.0.0
```

**Step 5: Disable Auto-Summarization (Optional)**
- By default, RIP performs automatic summarization at classful boundaries. 
- To disable auto-summarization, type:

```bash
Router(config-router)# no auto-summary
```

**Step 6: Verify RIP Configuration**
- To verify that RIPv2 is configured properly, use the following command:

```bash
Router# show ip protocols
```
This command will display details about the routing protocols configured, including RIP and its version.