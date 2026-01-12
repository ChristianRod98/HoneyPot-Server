# HoneyPot-Server

Deployeed and managed a cloud-based honeypot using T-Pot on DigitalOcean to capture and analyze real world malicious activity. Utilized Windows PowerShell for secure remote management and automation, monitored attacker behavior through generated logs, and analyzed brute-force attempts, scanning activity, and exploitation techniques. Collected and reviewed attack data to support threat detection, log analysis, and SOC-style alert triage.


## what is a honeypot?
A deliberately vulnerable system set up to attract, detect, and study malicious activity, without putting real systems at risk.

## Getting started
Build and deploy vulnerable cloud server using DigitalOcean
- Click Create dropdown tab
- Seclect Droplet (create cloud servers

<img width="1180" height="291" alt="Screenshot 2026-01-12 151027" src="https://github.com/user-attachments/assets/6df4a309-64a0-40ea-b65c-b37f04874b25" />

- Select region and desired OS & version

<img width="1206" height="1040" alt="Screenshot 2026-01-12 113522" src="https://github.com/user-attachments/assets/5206a605-a754-4835-b5da-10dedb7b2a14" />

- Select desired plan. (4GB ram is recommended)
- Create host name and create droplet
<img width="1196" height="564" alt="Screenshot 2026-01-12 113825" src="https://github.com/user-attachments/assets/dcdff365-9a39-4d87-bc5f-5c5cc40030b3" />
<img width="1196" height="564" alt="Screenshot 2026-01-12 113825" src="https://github.com/user-attachments/assets/d8acd04a-b981-46db-9ed2-af479f099b32" />
<img width="1272" height="825" alt="Screenshot 2026-01-12 113911" src="https://github.com/user-attachments/assets/1fdd8420-60a7-4d0d-9be0-3711c1e71cca" />

## ssh into server using Windows powershell
- Use ssh commans to root into created server using the public IP
- Once in the server, use "apt-get update && apt-get upgrade -y" to update any toold and repositories needed
<img width="569" height="145" alt="Screenshot 2026-01-12 114351" src="https://github.com/user-attachments/assets/3a3b7672-9e07-4863-a95b-f20fc922d6b7" />
<img width="917" height="613" alt="Screenshot 2026-01-12 114929" src="https://github.com/user-attachments/assets/b685382a-230c-43ba-bf88-25f4bcd99cc5" />

- Crate a user account using the "adduser" command
- add admin privileges to the user. "sudo usermod -aG sudo (user account)"
- switch to the user account. "su (user account)"
- switch to home account. "cs /home/(user account)"

## Clone T-pot gitHub repository
- clone the repository into user account. "git clone https://github.com/telekom-security/tpotce"
- change directory. "cd tpotce/"
- run install.sh. "./install.sh"
<img width="1456" height="820" alt="Screenshot 2026-01-11 154816" src="https://github.com/user-attachments/assets/9b0fb190-e3f2-4998-8ef1-9ac8bfea0524" />

- Select T-Pot Standard installation.
- reboot and reconnect using ssh on tcp/64297
- ssh back into server. "ssh -p 64295 root@(public IP)"
<img width="1447" height="734" alt="Screenshot 2026-01-11 154848" src="https://github.com/user-attachments/assets/cf825068-f16b-4cbb-83f7-3477066de52d" />
<img width="1449" height="668" alt="Screenshot 2026-01-11 154914" src="https://github.com/user-attachments/assets/b3853a8e-7700-4583-87c6-c62dd920d27c" />

## Loginto web guey
- with the sever on and after ssh into server
- open web guey on your webrowser using the public IP and port number.
- "https://(public IP):64295
<img width="1613" height="1238" alt="Screenshot 2026-01-11 155931" src="https://github.com/user-attachments/assets/1f42129b-f7d7-4408-bff8-97d4576c409a" />/>

