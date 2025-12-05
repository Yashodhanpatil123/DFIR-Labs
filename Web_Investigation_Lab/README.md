# 📘 Lab - Web Investigation 
<img width="484" height="276" alt="image" src="https://github.com/user-attachments/assets/9fb2574b-2657-4929-958a-f8c174ef2c94" />

Room link : https://cyberdefenders.org/blueteam-ctf-challenges/web-investigation/

## Scenario - 
You are a cybersecurity analyst working in the Security Operations Center (SOC) of BookWorld, an expansive online bookstore renowned for its vast selection of literature. BookWorld prides itself on providing a seamless and secure shopping experience for book enthusiasts around the globe. Recently, you've been tasked with reinforcing the company's cybersecurity posture, monitoring network traffic, and ensuring that the digital environment remains safe from threats.
Late one evening, an automated alert is triggered by an unusual spike in database queries and server resource usage, indicating potential malicious activity. This anomaly raises concerns about the integrity of BookWorld's customer data and internal systems, prompting an immediate and thorough investigation.
As the lead analyst in this case, you are required to analyze the network traffic to uncover the nature of the suspicious activity. Your objectives include identifying the attack vector, assessing the scope of any potential data breach, and determining if the attacker gained further access to BookWorld's internal systems.

---

 **Category** : Network Forensics  
 
 **Tactics** : Initial Access,Persistence,Command and Control
 
 **Tools** : Wireshark,Network Miner

-----

<img width="1141" height="81" alt="image" src="https://github.com/user-attachments/assets/4cb425a5-544e-4c19-a9e9-7a8640a0a47a" />

First i usually analyze Conversations after analyzing it i saw Ineractions between IPs and I noticed external IP with large number of packet Exchange
Next, I filtered the traffic between these two IPs. After applying the filter, I discovered that the IP 111.* was attempting an injection attack in its requests.

<img width="1482" height="128" alt="image" src="https://github.com/user-attachments/assets/57fd2275-81de-4f1e-8fb5-51105046c1fa" />

------

<img width="1152" height="87" alt="image" src="https://github.com/user-attachments/assets/1928a1b2-5783-40a0-8f12-a800f6a16745" />

You can find it by using whois or online geolocations tools


-------

<img width="1126" height="87" alt="image" src="https://github.com/user-attachments/assets/d202d228-df63-4c8a-95bc-97a2ee6042e1" />


You can find answer by analyzing the first packet where attacker starts injection activity

-------

<img width="1052" height="98" alt="image" src="https://github.com/user-attachments/assets/6e5a381c-cd54-46da-87ee-85f2ebde6643" />

After going through all the Packets from the start . You will uncover the answer
<img width="1378" height="206" alt="image" src="https://github.com/user-attachments/assets/86f4247b-d87d-419f-ad9a-dcbcc0443b8c" />

---------

<img width="1113" height="96" alt="image" src="https://github.com/user-attachments/assets/4148e942-36f5-4256-b948-24021c42b635" />

To solve that question I used tcpdump through the terminal. Attackers need to understand the internal schema to access the available databases.

------

<img width="1139" height="83" alt="image" src="https://github.com/user-attachments/assets/c8bdea0d-dc67-444b-88c1-55c327230467" />

In any database, user records are typically structured with fields like [first name, last name], and so on. Therefore, I used grep with the first name to identify the database name.

------

<img width="1121" height="86" alt="image" src="https://github.com/user-attachments/assets/b27f9ccf-26e7-41e2-b5b8-0c7cefb5fca0" />

By appling this wireshark filter “ip.dst == 111.224.250.131 and http.response.code == 301”

<img width="851" height="431" alt="image" src="https://github.com/user-attachments/assets/49a441ca-9f6f-4f21-944b-19b00692dd55" />

------

<img width="1133" height="69" alt="image" src="https://github.com/user-attachments/assets/a8102811-d2d3-4e44-8f39-8ad35edc1ed1" />

Looking at the HTTP stream of the last request to /admin/login.php, we see that once inserting the username and password, user was then redirected to the index.php

------

<img width="1066" height="75" alt="image" src="https://github.com/user-attachments/assets/20b68f3d-7bb4-42af-9ebc-b8f4943d8588" />

Looking at the last POST call to /admin/index.php, we notice that the TA uploaded the file named NVri2vhp.php, which contains code to trigger a reverse shell, allowing the TA to have access to the underlaying OS.
