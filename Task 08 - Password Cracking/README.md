# Password Cracking with John the Ripper

## What I Did
- Created a password hash file (`hash.txt`) containing an MD5-based crypt hash.  
- Used **John the Ripper** with the `rockyou.txt` wordlist to perform a dictionary attack.  
- Successfully cracked the hash, revealing the original password.  
- Saved the cracked password into a file (`cracked.txt`) for reference.

## What I Learned
- How to format and feed hashed passwords into John the Ripper.  
- How to specify a custom wordlist to increase cracking success.  
- How to display and store cracked passwords using `john --show`.  
- Gained a better understanding of how weak or common passwords can be easily recovered using dictionary attacks.
