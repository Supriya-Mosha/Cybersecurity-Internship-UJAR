# Password Cracking Challenge Using John the Ripper

## Overview
This project demonstrates practical password cracking techniques using John the Ripper in a controlled Kali Linux environment. The exercise highlights the vulnerabilities of weak passwords and outdated hashing algorithms like MD5, while emphasizing the importance of strong password policies and modern cryptographic defenses.

## Objectives
- Generate MD5 hashes from sample passwords
- Perform dictionary attacks using the rockyou.txt wordlist
- Attempt brute-force attacks on resistant passwords
- Analyze the effectiveness of different password complexities
- Understand the importance of modern hashing algorithms

## Tools Used
- **Kali Linux**: Penetration testing distribution
- **John the Ripper**: Password cracking tool
- **OpenSSL**: Cryptographic toolkit for hash generation
- **rockyou.txt**: Wordlist containing over 14 million real passwords

## Project Steps

### 1. Environment Setup
Launch Kali Linux VM and update the system:

sudo apt update

### 2. Prepare Wordlist
Decompress the rockyou.txt wordlist:

sudo gunzip /usr/share/wordlists/rockyou.txt.gz

### 3. Generate Target Hashes
Create MD5 hashes for testing:

echo -n "password123" | openssl md5
echo -n "letmein" | openssl md5
echo -n "admin" | openssl md5
echo -n "SecurePassword" | openssl md5

### 4. Create Hashes File
Store hashes in hashes.txt with usernames

### 5. Dictionary Attack
Execute dictionary attack using John the Ripper:

john --wordlist=/usr/share/wordlists/rockyou.txt --format=Raw-MD5 hashes.txt

### 6. View Results
Display cracked passwords:

john --show --format=Raw-MD5 hashes.txt

### 7. Brute-Force Attack (Optional)
Attempt brute-force on remaining hashes:

john --incremental --format=Raw-MD5 hashes.txt

### 8. Clean Up
Clear John the Ripper's session data:

john --format=Raw-MD5 --remove hashes.txt
# or
rm ~/.john/john.pot

## 📝 Conclusion
This project practically demonstrates:

✅ Weak passwords crack instantly with dictionary attacks

✅ Strong passwords resist brute-force attempts

✅ MD5 is dangerously vulnerable (21M guesses/second)

✅ Modern algorithms (bcrypt/Argon2) are essential

✅ Ethical hacking requires controlled environments

## ⚠️ Disclaimer
Legal & Ethical Use Only: This project must be conducted in personal, controlled environments only. Unauthorized testing against systems you don't own is illegal. Always obtain explicit permission before security testing.
