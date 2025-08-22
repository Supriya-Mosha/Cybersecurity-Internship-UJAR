# Task 9: Man-in-the-Middle (MITM) Attack using ARP Spoofing

## Overview
This task demonstrates a Man-in-the-Middle (MITM) attack performed using ARP spoofing with Ettercap on a local network. The goal was to intercept and analyze network traffic between a victim and the gateway.

## Key Concepts
- **MITM Attack:** An attack where an attacker secretly intercepts and relays communication between two parties.
- **ARP Spoofing:** A technique to send fake ARP messages to a LAN, tricking devices into sending traffic to the attacker's machine.

## Steps Executed
1.  **Lab Setup:** Used Kali Linux (attacker) and a Windows host (victim) on the same Wi-Fi network.
2.  **IP Forwarding:** Enabled on Kali to forward traffic: `echo 1 > /proc/sys/net/ipv4/ip_forward`
3.  **Ettercap Launch:** Started the GUI: `sudo ettercap -G`
4.  **Scanning:** Scanned the network for hosts.
5.  **Target Selection:** Added the gateway as `Target 1` and the victim as `Target 2`.
6.  **ARP Poisoning:** Initiated the MITM attack with `Sniff remote connections` enabled.
7.  **Sniffing:** Started packet capture to intercept traffic.
8.  **Analysis:** Used Wireshark to analyze captured packets.

## Observations
- **Successful ARP Poisoning:** Verified by a constant flood of ARP packets from the attacker's IP.
- **Unencrypted Traffic (HTTP):** Fully visible in plain text, including potential login credentials.
- **Encrypted Traffic (HTTPS):** Only the destination was visible; the data content was encrypted and unreadable.

## Why It's Dangerous
- Allows theft of sensitive data like passwords and cookies.
- Enables session hijacking and data manipulation.
- Difficult to detect for the average user.

## Prevention
- **Use HTTPS:** Encrypts web traffic.
- **Employ a VPN:** Encrypts all network traffic.
- **Network Monitoring:** Use IDS/IPS to detect ARP spoofing.
- **Static ARP Entries:** Prevents ARP table poisoning on critical systems.
