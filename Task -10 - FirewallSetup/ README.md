
# Task 10 - UFW Firewall Setup

## Rules Configured:

1.  **Default Policies:**
    - `default deny incoming`: Blocks all incoming connections that are not explicitly allowed. This is the most secure starting point.
    - `default allow outgoing`: Allows all traffic originating from this server. This is necessary for the system to function (e.g., download updates, query websites).

2.  **Allowed Services:**
    - `allow ssh`: Allows incoming SSH connections on port 22. This is crucial for remote administration.
    - `allow 80/tcp`: Allows incoming HTTP traffic for web servers.
    - `allow 443/tcp`: Allows incoming HTTPS traffic for secure web servers.

3.  **Block Rule:**
    - `deny from 192.168.1.100`: Demonstrates how to block all incoming traffic from a specific, potentially malicious, IP address.

## Concepts Demonstrated:
- Principle of least privilege (deny all, then allow specific needs).
- Controlling traffic based on port and protocol.
- Controlling traffic based on source IP address.
