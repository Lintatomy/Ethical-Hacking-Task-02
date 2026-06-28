WHITE BAND ASSOCIATES

Ethical Hacking Task 02: Network Scanning &
Service Enumeration

Objective

The purpose of this task is to understand the second phase of Ethical Hacking — Scanning and
Enumeration.
In this task, i learned how to identify active hosts, open ports, running services, and basic network
information using safe and authorized methods.


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
