# Network Traffic Analysis

## Filters Used
- **ip.addr == <target IP>** – to isolate traffic related to a specific host  
- **dns** – to view DNS query/response packets  
- **tcp.handshake** – to inspect TCP connection setup  
- **http** – to check any web traffic in cleartext  

## Interesting Findings
- **DNS Lookups:** Multiple domain queries were observed (e.g., `example.com`, `tesla.com`,google.com).  
- **TCP Handshakes:** Several successful TCP three-way handshakes detected, confirming active connections.  
- **HTTP Requests:** Some unencrypted HTTP traffic visible, allowing inspection of URLs.    

## Summary of Observations
- The capture shows standard DNS resolution followed by TCP connections to the resolved IPs.  
- Traffic patterns suggest normal client-server communication without signs of scanning or flooding.  
- No sensitive data observed in plaintext other than standard HTTP requests.  




