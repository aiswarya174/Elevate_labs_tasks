# Network Configuration Overview

The command used here is:
                             ifconfig

# Ethernet Interface (`eth0`)

* Status: Active and running with broadcast and multicast enabled
* Addressing: Configured with both IPv4 and IPv6
* Hardware (MAC) Address: Hidden for privacy
* MTU: Standard Ethernet size
* Packet Statistics:

  * Received (RX): Few packets with a small amount of data
  * Transmitted (TX): Some packets successfully sent
  * Errors/Collisions: None

> This represents a typical wired or virtual network interface with no reported issues.

---

# Loopback Interface (`lo`)

* Status: Active and used for internal system communication
* Addressing: Configured with standard loopback IPv4 and IPv6 addresses
* MTU: Larger size to support local traffic
* Packet Statistics:

  * RX and TX: Minimal packet activity, expected for loopback
  * Errors/Collisions: None

> The loopback interface is essential for testing and internal service communication.

---

# Summary

The configuration shows a functional network environment with both an Ethernet interface and a loopback interface operating correctly. There are no signs of transmission errors or dropped packets, indicating a healthy setup suitable for network-based tasks and local development.


After finding the ip address i used nmap for identifying open ports.
#  Nmap Network Scan Summary

This section provides a brief summary of a network scan conducted using `nmap`. The scan was performed to identify live hosts and check the status of common TCP ports across a local subnet.

# Scan Command Used

```bash
                     nmap -sS <subnet>/24
```

* Scan Type: TCP SYN scan (`-sS`)
* Target: Local /24 subnet
* Tool Version: Nmap 7.95
* Total Hosts Scanned: 256
* Live Hosts Found: 4
* Scan Duration: \~8.65 seconds

> IPs and MAC addresses have been redacted for privacy.

---

# Scan Results Overview

# Host 1

* Status: Online
* Open Ports: None detected
* Port State: All ports filtered (no response)
* MAC Vendor: VMware (redacted)

---

# Host 2

* Status: Online
* **Open Port Detected**:

  * Port 53 (DNS) – **Filtered**
* Other Ports: Closed or filtered
* MAC Vendor: VMware (redacted)

---

# Host 3

* Status: Online
* Port State: All ports filtered (no response)
* MAC Vendor: VMware (redacted)

---

# Host 4 (Scanning System)

* Status: Online
* Open Ports: None detected
* Port State: All ports closed
* MAC Vendor: Redacted

---

# Conclusion

The scan revealed:

* *4 active hosts* within the subnet
* Most ports were either filtered or closed, indicating potential firewall protection or non-responsive services
* One host had *DNS (port 53)* in a *filtered* state, suggesting that the port is monitored or protected by firewall rules

---

# Note

The scan results indicate a tightly controlled network environment, likely running in a virtualized lab setting. This kind of controlled response is common in secure setups or internal testing environments.

---
