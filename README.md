WHITE BAND ASSOCIATES

Ethical Hacking Task 02: Network Scanning &
Service Enumeration

Objective

The objective of this task was to perform a safe network scan on my own machine using Nmap. The purpose was to identify open ports, running services, and operating system information while understanding how network scanning supports ethical hacking and vulnerability assessment.


Part A: Install Nmap --


Step 1: Download Nmap

Windows: https://nmap.org/download.html


Install using default settings.ning:

Screenshot of Installation

<img width="1428" height="1101" alt="install shot" src="https://github.com/user-attachments/assets/17288d93-c8c6-4141-8a6d-54432e41fd5d" />


Step 2: Verify Installation by running 

Open Command Prompt and type:

nmap --version

Screenshot of  version

<img width="2170" height="263" alt="version shot" src="https://github.com/user-attachments/assets/0f216e2e-3164-429a-af16-b97a1a2ad93e" />



Part B: Scan Your Local Machine --

Scan computer using 

Run

nmap localhost

or

nmap 127.0.0.1


Screenshot of scan 

<img width="2171" height="724" alt="scan shot" src="https://github.com/user-attachments/assets/096dc68f-2783-4153-8c9a-383d85ca58c7" />





Part C: Service Version Detection --

Run

nmap -sV localhost

Screenshot of sevice

<img width="1860" height="846" alt="service shot" src="https://github.com/user-attachments/assets/5c21dbfa-4db2-4e4c-b3ba-65c2655f0764" />




Part D – Operating System Detection --

Run 

sudo nmap -O localhost

On Windows use:

nmap -O localhost


Answers :-

1. Was the operating system detected?

   
Yes, the operating system was successfully detected by Nmap.


2. Which OS was identified?


The scan identified the operating system as Microsoft Windows 11. (If your scan shows Windows 10 or another OS, write the actual result from your Nmap output instead.)


3. Why is OS detection useful during penetration testing?


Operating system detection helps penetration testers identify the target system and understand its configuration. Different operating systems have different services, vulnerabilities, and security features. By knowing the OS, security professionals can choose the appropriate testing methods, identify potential weaknesses, and recommend suitable security measures. It also helps avoid unnecessary or incompatible tests, making the assessment more accurate and efficient.




Screenshot of operating system detection

<img width="2043" height="770" alt="os detection shot" src="https://github.com/user-attachments/assets/edcd86b1-07e1-4b60-93a7-86e1a4f84019" />






Part E – Common Port Research --


Port 20/21 – FTP

Protocol: TCP

Purpose:
Transfers files between computers.

Security Risks

Plain-text authentication
Password theft
Anonymous login
File tampering



Port 22 – SSH

Protocol: TCP

Purpose

Secure remote login.

Security Risks

Weak passwords
Brute-force attacks
Outdated SSH versions



Port 23 – Telnet

Protocol: TCP

Purpose

Remote login.

Security Risks

Sends everything in plain text
Easy password interception
No encryption



Port 25 – SMTP

Protocol: TCP

Purpose

Email sending.

Security Risks

Spam relay
Email spoofing
Malware distribution



Port 53 – DNS

Protocol: TCP/UDP

Purpose

Converts domain names into IP addresses.

Security Risks

DNS poisoning
Amplification attacks
Information leakage



Port 80 – HTTP

Protocol: TCP

Purpose

Web browsing.

Security Risks

No encryption
Data interception
Session hijacking



Port 110 – POP3

Protocol: TCP

Purpose

Downloads emails.

Security Risks

Plain-text passwords
Data theft
Weak authentication


Port 143 – IMAP

Protocol: TCP

Purpose

Email synchronization.

Security Risks

Weak passwords
Unencrypted communication
Unauthorized mailbox access



Port 443 – HTTPS

Protocol: TCP

Purpose

Secure web communication.

Security Risks

SSL vulnerabilities
Certificate misuse
Misconfigured encryption



Port 445 – SMB

Protocol: TCP

Purpose

Windows file sharing.

Security Risks

Ransomware
Worm attacks
Unauthorized file access



Port 3389 – RDP

Protocol: TCP

Purpose

Remote Desktop access.

Security Risks

Brute-force attacks
Credential theft
Remote exploitation




Part F: Scan Analysis --


Answers for scan based analysis


1. Which services are currently running?

Based on the scan, the SSH (Secure Shell) service is currently running on port 22. SSH is used for secure remote access and administration of the system.

2. Are all open ports necessary?

Yes. Based on this scan, only one port (22) is open, which is commonly required for secure remote login and system administration. If remote access is needed, this port is necessary. Otherwise, it can be disabled to improve security.

3. Which services could become security risks if misconfigured?

The SSH service could become a security risk if it is misconfigured. Weak passwords, outdated SSH software, or allowing root login can make the system vulnerable to brute-force attacks or unauthorized access.

4. Which port would you disable if it wasn't required?

If remote access is not needed, I would disable port 22 (SSH). Closing unnecessary ports reduces the system's attack surface and improves overall security.



Part G: Scan Report --

Scan Date

26 June 2026


 Target System

Localhost (127.0.0.1)


 Commands Used

bash
nmap --version
nmap localhost
nmap -sV localhost
sudo nmap -O localhost



Open Ports

| Port   | State | Service |
| ------ | ----- | ------- |
| 22/tcp | Open  | SSH     |



 Running Services

| Port | Service            | Purpose                                                        |
| ---- | ------------------ | -------------------------------------------------------------- |
| 22   | SSH (Secure Shell) | Provides secure remote login and remote system administration. |



 Operating System

Ubuntu Linux (or the Linux distribution detected by your `nmap -O localhost` scan. If your OS detection showed Ubuntu, use Ubuntu. If it showed another Linux distribution, write that instead.)



Observations

* The localhost system is active and responding to network scans.
* Only one TCP port (22) is open.
* The SSH service is running, indicating that secure remote access is enabled.
* The remaining 999 scanned TCP ports are closed, which reduces the attack surface.
* No unnecessary services were detected during the basic scan.



Recommendations

* Keep the SSH service updated with the latest security patches.
* Use strong passwords or SSH key-based authentication.
* Disable SSH if remote access is not required.
* Configure a firewall to allow access only from trusted IP addresses.
* Regularly monitor open ports and running services using Nmap.
* Remove or disable unnecessary services to improve system security.



Conclusion 

This task helped me understand the scanning and enumeration phase of ethical hacking using Nmap. I learned how to scan my local machine to identify open ports, running services, and operating system information. The scan showed that only port 22 (SSH) was open, which indicates that secure remote access is enabled on the system. Since the remaining ports were closed, the system has a smaller attack surface and is less exposed to potential threats.

I also learned that identifying open ports and services is an important step in penetration testing because it helps security professionals understand which services are available and whether they could be exploited if misconfigured. Researching common network ports improved my understanding of their purposes and the security risks associated with each one. This task also reinforced the importance of performing scans only on authorized systems and following ethical hacking principles. Overall, the exercise provided valuable practical experience with Nmap and demonstrated how regular network scanning can help identify security weaknesses, improve system protection, and support effective vulnerability assessments.




Repository Contents include

* Nmap Scan Report.pdf

* Research Notes.pdf


  By

   Linta Tomy
  
  WHITE BAND ASSOCIATES - Ethical Hacking Internship
  
  Task -  Ethical Hacking Task 02
  
  Topic - Network Scanning & Service Enumeration
  
