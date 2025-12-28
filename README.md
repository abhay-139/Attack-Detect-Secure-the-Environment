# Attack-Detect-Secure-the-Environment
What is this project?

This project shows how hackers attack cloud servers and how security teams detect and stop them using Microsoft Azure.

I created a small company-like network in the cloud, attacked it like a hacker, then protected it like a security engineer.

Network Setup (What I built)

I made two separate network parts:

Network Area	Purpose
DMZ Network	Public server that anyone on the internet can reach
Internal Network	Private servers that should not be accessible from outside
Servers
Server	What it does
Web Server	Website (Apache) exposed to the internet
File Server	Stores important company files (SMB)
SIEM Server	Monitors logs and attacks (Wazuh)
Attacker	Kali Linux used to attack
What the Hacker (Red Team) did
Step 1 – Scan the web server

Used tools to find:
• Open ports
• Old software
• Hidden folders

Step 2 – Break into the web server

Used password attack (brute force) and web scanning
→ Web server got hacked

Step 3 – Move inside the network

Used the hacked web server to access the internal file server
→ Internal private server also got hacked

What the Defender (Blue Team) did

Using Wazuh SIEM, I detected:

• Thousands of wrong login attempts
• Web scanning activity
• Strange traffic between private servers

How I fixed it
Security Fix	What it did
Disabled password login	Stopped brute force
Used SSH keys only	Strong login security
Hid Apache version info	Prevented fingerprinting
Blocked unnecessary internal traffic	Stopped lateral movement
Final Result

After fixing:

• Hackers could not break in
• No more internal movement
• SIEM alerts became normal
• Servers became secure

Why this project is important

This project proves:

A small mistake in cloud security can allow full company network compromise — and proper monitoring + network rules can stop it.

If you want, next I can help you convert this into:

• Viva / presentation explanation
• Diagram
• Resume bullet points
• Interview answers
