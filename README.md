CIA Triad Report
📄 Overview
This project explains the CIA Triad — Confidentiality, Integrity, and Availability, which are the core principles of cybersecurity. It explores each principle in detail, provides real-world examples, and demonstrates how Linux file permissions support these concepts.

🛡 CIA Triad Principles
1. Confidentiality – Keeps Data Secret
Ensures sensitive information is accessible only to authorized individuals.

2. Integrity – Keeps Data Accurate
Ensures data remains correct, complete, and unaltered.

3. Availability – Keeps Data Accessible
Ensures systems and data are available when needed.

🌐 Real-World Applications
Gmail – Protects emails with encryption, prevents tampering, and ensures high uptime.
WhatsApp – Uses end-to-end encryption, message verification, and reliable connectivity.
Banking Apps – Protect accounts with OTP, encryption, and continuous availability.

💻 Linux File Permissions & CIA Triad
Linux permissions support all three CIA principles:
Confidentiality – Restrict read permissions.
Integrity – Restrict write permissions.
Availability – Allow execute permissions for required programs.

Example Commands:
ls -l                     # List files with permissions
chmod 600 secret.txt      # Confidentiality
chmod 644 file.txt        # Integrity
chmod 755 script.sh       # Availability
chown user:group file.txt # Change file owner
chgrp group file.txt      # Change file group
stat file.txt             # View file details

📌 Conclusion
The CIA Triad is the foundation of cybersecurity. Understanding and applying these principles in real-world systems — from email to banking to Linux servers — helps protect data, maintain trust, and ensure continuous service availability.

📂 Contents
CIA_Triad_Report.docx – Detailed report with examples and Linux commands.

