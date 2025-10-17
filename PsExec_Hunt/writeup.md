# 🧩 Lab: PsExec Hunt

## 🎯 Objective
Investigate lateral movement using PsExec based on Windows event logs.

## 🧠 Tools Used
- Wireshark (Mostly)
- Event Viewer
- PowerShell (Get-WinEvent)

## 🔍 Key Steps
1. Filtered logs for Event IDs: **7045**, **4624**, **4688**, **5140**  
2. Found `PSEXESVC` service creation — indicates PsExec use.  
3. Checked nearby logons and network share events to confirm remote execution.  
4. Built a short timeline showing attacker activity.  

## 🧾 Findings
- Attacker used PsExec for remote code execution.  
- Evidence in Event ID 7045 (service install), 4624 (network logon), and 4688 (process creation).  
- Attack path: `Remote logon → service creation → PsExec execution`.  

## 🧩 Conclusion
The host was compromised via PsExec lateral movement.  
Next steps: block attacker IP, rotate admin credentials, and add detections for service creation events.

---

  
