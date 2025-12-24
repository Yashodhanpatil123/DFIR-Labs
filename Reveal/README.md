**LAB - Reveal**

<img width="1404" height="717" alt="image" src="https://github.com/user-attachments/assets/bcaaf8c9-9c73-4879-9799-0d1c32b021a7" />


Category: Endpoint Forensics

Level: Easy

By: cyberdefenders

**Summary** -
You are a forensic investigator at a financial institution, and your SIEM flagged unusual activity on a workstation with access to sensitive financial data. Suspecting a breach, you received a memory dump from the compromised machine. Your task is to analyze the memory for signs of compromise, trace the anomaly's origin, and assess its scope to contain the incident effectively.

**TOOLS USED** -  Volatility3, Kali linux , Python

----------

**NOTE** - I will be only giving hints of the answers 


--------

**Questions**

<img width="1036" height="60" alt="image" src="https://github.com/user-attachments/assets/104ef589-2a2f-4381-8ecf-46a69ce1dd56" />

python3 vol.py -f /home/alim/Desktop/192-Reveal.dmp windows.pstree > /home/alim/Desktop/Reveal.txt
Note: “-f” take the path of the file so you change it as per your device
“windows.pstree” to see all the process


<img width="1105" height="83" alt="image" src="https://github.com/user-attachments/assets/5c12ba18-a5fd-4244-9f83-1790b4e2d3fc" />

With the use of "windows.pstree" you will get the PID also 

<img width="1161" height="93" alt="image" src="https://github.com/user-attachments/assets/c1495301-6203-4ce1-848b-7bdca843873b" />
Next, let’s list loaded DLLs to check if the malware used any external payloads:

Python vol.py -f <path_of_Memory_dump> windows.cmdline | grep "PID"

<img width="1130" height="95" alt="image" src="https://github.com/user-attachments/assets/f165117b-0e5d-4264-ba29-bd9962d1a85d" />
To check mapped network drives that the malware accessed:

Python vol.py -f <path_of_Memory_dump> windows.cmdline | grep "PID"


<img width="1008" height="72" alt="image" src="https://github.com/user-attachments/assets/70733e71-600b-4a19-bc39-5d7cea28f13b" />

Using MITRE ATT&CK, we identify the sub-technique used:

The attacker used rundll32.exe to execute a DLL payload, which matches ***** .


<img width="1136" height="87" alt="image" src="https://github.com/user-attachments/assets/fbdb85ff-d100-4b6e-8f69-216e70fa6f81" />
To find the user under which the malicious process ran:

Python vol.py -f <path_of_Memory_dump> windows.sessions | grep "PID"


<img width="1149" height="85" alt="image" src="https://github.com/user-attachments/assets/5b0008a1-6652-4f89-87f2-71844bc387e4" />
To correlate findings with known malware, we use VirusTotal:

sha256sum 3435.dll

Copy the hash or simply copy the ip address and search it on VirusTotal.

-------


*That's for Today CYA*

<img width="381" height="800" alt="image" src="https://github.com/user-attachments/assets/7a879c86-35f8-48f9-adb4-94449f5e8807" />










 

