# 🧩 Lab: Tomcat Takeover (Network Forensics)

## 📘 Summary
- **Platform:** CyberDefenders (Tomcat Takeover Lab)  
- **Category:** Network Forensics  
- **Tactics:** Reconnaissance, Execution, Persistence, Privilege Escalation, Credential Access, Discovery, Command & Control  
- **Tools:** Wireshark (primary), NetworkMiner (optional), tshark (optional)  
- **Difficulty:** Easy  
- **Lab Date:** Oct 19, 2025

**Scenario:** Network traffic was captured after suspicious activity on an internal Apache Tomcat server. The goal is to analyze the PCAP to determine how the server was compromised, what actions the attacker performed, the scope of compromise, and associated indicators of compromise (IOCs).

---

## 🎯 Objectives
1. Identify the initial vector used to compromise the Tomcat server.  
2. Extract any HTTP payloads or file uploads that show exploitation (webshells, uploads).  
3. Determine if credentials were captured or reused.  
4. Trace post-exploitation activity (persistence, privilege escalation, C2).  
5. Produce a timeline, IOCs, and mitigation recommendations.

---

## 🛠 Tools & Useful Filters / Command

### Wireshark 


##  📘 Screenshots for few hints
Statistics -> Conversations -> IPv4 Statistics
<img width="1825" height="546" alt="Screenshot 2025-10-19 141040" src="https://github.com/user-attachments/assets/303d609b-2d4d-4cd5-83ec-4a0119db9e39" />


ip.addr == 14.0.0.120 && tcp.port != 8080

<img width="1445" height="673" alt="Screenshot 2025-10-19 141019" src="https://github.com/user-attachments/assets/e74e4a53-af2c-4269-b5ea-9a1246bb9057" />



Using WHOis we were able to locate from where the IP adrr originated


<img width="1726" height="659" alt="Screenshot 2025-10-19 132422" src="https://github.com/user-attachments/assets/86b0c612-5385-4496-862f-98734a5330bb" />


Filtering with ip.src == 14.0.0.120 && http . You can see Gobuster tool is used


<img width="954" height="444" alt="Screenshot 2025-10-19 141724" src="https://github.com/user-attachments/assets/29ba4410-4139-4ecf-81a1-b9bab5d242c7" />




ip.src == 14.0.0.120 && http by idefntifying HTTP streams we can see many failed attemps


<img width="1248" height="510" alt="Screenshot 2025-10-19 141800" src="https://github.com/user-attachments/assets/4cd62cac-fa9a-4d51-920a-2b0fa8eea5eb" />


