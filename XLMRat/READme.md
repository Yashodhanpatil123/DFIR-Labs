---
<img width="901" height="502" alt="Screenshot 2025-10-24 140914" src="https://github.com/user-attachments/assets/81aaa708-0c22-4997-a6d5-908e51f17e6e" />

## 🧩 Lab: xmlrat (Network Forensics)

**Category:** Network Forensics

**Tactics:** Execution, Defense Evasion  

**Tools:** Wireshark, tshark, CyberChef, VirusTotal, Python3, PowerShell  

**Difficulty:** easy

### 📘 Summary

Analyze network traffic to identify malware delivery, deobfuscate scripts, and map attacker techniques using MITRE ATT&CK, focusing on stealthy execution and reflective code loading.

## I wont be giving answers as it will be unfair just some screenshots for hints

### Questions:

- 1 The attacker successfully executed a command to download the first stage of the malware. What is the URL from which the first malware stage was installed?

- <img width="1789" height="356" alt="Screenshot 2025-10-24 142543" src="https://github.com/user-attachments/assets/4bd69e48-9178-48ca-86e3-20c08c507e63" />



- 2 Which hosting provider owns the associated IP address?
 
  we just need to scan ip address to whois

- 3 By analyzing the malicious scripts, two payloads were identified: a loader and a secondary executable. What is the SHA256 of the malware executable?
- 
- 1. Export the FILE.jpg
- 2. Open the FILE.jpg, Copy the hexadecimal headers (loaders & executables)
- 3. Paste only the loaders in the cyberchef -> From Hex -> save it (download.dat)
- 4. sha256sum download.dat


- 4 What is the malware family label based on Alibaba?
- paste the sha256 hash in virustotal for your ans


- 5 What is the timestamp of the malware's creation?
- paste sha256 hash on virustotal get your ans


- 6  Which LOLBin is leveraged for stealthy process execution in this script? Provide the full path.

<img width="955" height="721" alt="Screenshot 2025-10-24 143628" src="https://github.com/user-attachments/assets/73732fb2-a8e8-4746-b53a-a556641da8a9" />



- 7 The script is designed to drop several files. List the names of the files dropped by the script.
  
- During the analysis process of FILE.jpg i finded the same file name with different extensions (.vbs, .ps1, .bat)




## SEE YOU LATER 
<img width="531" height="368" alt="image" src="https://github.com/user-attachments/assets/ad8676a8-85ae-4ce1-8dc2-96b4cbdf45f8" />



