# Network Scanner using Scapy

A simple and efficient Python-based network scanner that scans a given IP subnet and identifies live hosts with their IP, MAC, and Hostname.

## Features

- Scans IP ranges/subnets (CIDR support)
- Uses ARP packets to detect live hosts
- Retrieves MAC address and hostname
- Multithreaded for faster scanning

---

## Requirements

- Python 3.6+
- [Scapy](https://scapy.net/)
- Administrative/root privileges

Install required modules:

```
pip install scapy
```
🛠️ How to Use
```
python network_scaner.py
```
You will be prompted to enter the network range in CIDR format:

```
Enter network ip address: 192.168.1.0/24
```
## Example Output:

```
Edit
IP                   MAC                 Hostname
------------------------------------------------------------
192.168.1.1          ab:cd:ef:12:34:56   router.local
192.168.1.4          de:ad:be:ef:23:45   laptop
```
## How It Works
Sends ARP requests to each IP address in the provided subnet.

Captures replies to determine live hosts.

Uses reverse DNS lookup to get hostnames.

## Note
This tool is intended for educational and ethical network auditing purposes only. Always scan networks you own or have permission to analyze.

