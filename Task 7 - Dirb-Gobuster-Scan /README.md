# Directory Enumeration Task

## Target
- **URL:** http://testphp.vulnweb.com  
- **Type:** Public test server for vulnerability scanning

## Tool Used
- **Gobuster v3.6**  
- **Wordlist:** /usr/share/wordlists/dirb/common.txt  
- **Threads:** 10  
- **Timeout:** 10 seconds  

## Sample Output and Findings
- `/admin` → **301** (Redirect)  
- `/cgi-bin` → **403** (Forbidden)  
- `/crossdomain.xml` → **200** (OK)  
- `/CVS/Root` → **200** (OK)  
- `/images` → **301** (Redirect)  
- `/secured` → **301** (Redirect)  
- `/vendor` → **301** (Redirect)  

## Explanation of HTTP Status Codes
- **200 OK:** The resource exists and is accessible.  
- **301 Moved Permanently:** The directory exists but redirects to another location.  
- **403 Forbidden:** The resource exists but access is denied.  
- **404 Not Found:** The resource does not exist (filtered out by Gobuster).  

## Key Observations
- Several important directories are exposed (`/admin`, `/secured`, `/vendor`) which could contain sensitive information.
- Presence of `/cgi-bin` indicates possible legacy scripts that may be vulnerable.
- `403 Forbidden` responses confirm that some directories exist even though access is blocked.

---

