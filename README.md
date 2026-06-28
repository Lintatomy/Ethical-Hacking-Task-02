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

Screenshot of operating system detection

<img width="2043" height="770" alt="os detection shot" src="https://github.com/user-attachments/assets/edcd86b1-07e1-4b60-93a7-86e1a4f84019" />
