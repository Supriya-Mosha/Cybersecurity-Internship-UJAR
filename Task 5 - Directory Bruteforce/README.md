# Task 05 – Directory Bruteforce

## Tool Used
Dirb v2.22

## Target Environment
Local web server running on http://localhost:8000  
(Started using: `python3 -m http.server 8000`)

## Key Findings
- /admin → 301 redirect (resource exists)
- /index.html → 200 OK (page is accessible)
- /secret → 301 redirect (resource exists)
- /uploads → 301 redirect (resource exists)

