<img width="1900" height="692" alt="image" src="https://github.com/user-attachments/assets/61e9cc01-2859-4cfa-858f-b16f7c1f6aba" />

## Lab - Red Stealer 

**Platform** - Cyberdefenders 
link - https://cyberdefenders.org/blueteam-ctf-challenges/red-stealer/

-----

## Scenario -
You are part of the Threat Intelligence team in the SOC (Security Operations Center). An executable file has been discovered on a colleague's computer, and it's suspected to be linked to a Command and Control (C2) server, indicating a potential malware infection. Your task is to investigate this executable by analyzing its hash. The goal is to gather and analyze data beneficial to other SOC members, including the Incident Response team, to respond to this suspicious behavior efficiently.

---- 
**Category** : Threat Intel

**Tactics**: Execution,Persistence,Privilege Escalation,Defense Evasion

**Tools**: Whois,VirusTotal,MalwareBazaar,ThreatFox,ANY.RUN

------
## Questions

<img width="1124" height="89" alt="image" src="https://github.com/user-attachments/assets/ad901bee-6dcf-469d-a6b4-d914487e0838" />

Analyzing it using VirusTotal we get to know that this is a *****.

------

<img width="1054" height="86" alt="image" src="https://github.com/user-attachments/assets/bf86e402-9e52-4f2e-989a-0647f75a97eb" />

go VirusTotal, go to the Details section,Locate the File Name field.

-----

<img width="1134" height="89" alt="image" src="https://github.com/user-attachments/assets/52d9a2b5-5cdc-4355-ada6-d02b6c75738d" />

Go to VirusTotal > History Section,Find the First Submission Timestamp.

------

<img width="1108" height="89" alt="image" src="https://github.com/user-attachments/assets/a2c0d8c2-ff64-4d53-a820-4cafc14653ed" />

In VirusTotal, go to the Behavior section.Look under MITRE ATT&CK Tactics & Techniques.Click on Collection and find Data from Local System.

-----

<img width="808" height="81" alt="image" src="https://github.com/user-attachments/assets/5eab313d-3bd7-4394-9229-4b6846a58202" />

In VirusTotal, go to the Network Communication section.Navigate to DNS Resolutions.Identify the domains contacted by the malware.

------

<img width="1138" height="99" alt="image" src="https://github.com/user-attachments/assets/cb362cbd-e6f3-4c72-9eab-03cebfffa131" />

In VirusTotal, go to Behavior > IP Traffic.

-----

<img width="1124" height="99" alt="image" src="https://github.com/user-attachments/assets/41eacc27-5cc9-4bf6-9f30-0bb475b1c57a" />

Go to Malware Bazaar.Search for the malware’s hash.Navigate to the YARA rules section.

------

<img width="1144" height="100" alt="image" src="https://github.com/user-attachments/assets/14f7182a-225d-4346-99bb-852fff015b21" />


Visit ThreatFox.Search for 77.91.124.55.Locate the Malware Alias field.

-------

<img width="1140" height="104" alt="image" src="https://github.com/user-attachments/assets/ee6fd6fc-21c4-4ab1-80bc-df7e46aa24e4" />

In VirusTotal, go to the Behavior tab.Look under Runtime Modules for loaded DLLs.






