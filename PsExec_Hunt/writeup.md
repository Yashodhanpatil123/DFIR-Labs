# 🧩 Lab: PsExec Hunt (Network Forensics)

## 📘 Summary
- **Platform:** CyberDefenders  
- **Category:** Network Forensics  
- **Tactics:** Execution, Defense Evasion, Discovery, Lateral Movement  
- **Tool(s):** Wireshark (primary), tshark (optional), NetworkMiner (optional)  
- **Difficulty:** Easy  
- **Estimated Time:** 30 mins

**Scenario:** An IDS flagged suspicious lateral movement involving PsExec. Use the provided PCAP to trace attacker activity, identify entry point(s), compromised hosts, credentials (if present), and administrative share usage.

## 🛠️ Tools & Useful Filters / Commands

### Wireshark (GUI)
- Open the PCAP in Wireshark.
- Useful display filters:
  - `smb || smb2` — show SMB/SMB2 protocol traffic (file/share activity).
  - `tcp.port == 445` — raw SMB over TCP.
  - `ntlmssp` or `smb.ntlmssp` — show NTLM authentication messages (username, domain info).
  - `rpc || msrpc` — RPC calls (useful for service control / svcctl calls).
  - `smb2.cmd == 1 || smb2.cmd == 5` — (optional) show specific SMB2 command types (create/open/write).  
  - `frame.time >= "YYYY-MM-DD HH:MM:SS"` — filter by time range if needed.

- Helpful GUI actions:
  - **Follow → TCP Stream** on suspicious TCP connections to view the entire session.  
  - **Analyze → Display Filter Macros** (useful to save filters).  
  - **File → Export Objects → SMB** to extract any files transferred over SMB.  
  - Inspect **NTLMSSP** challenge/response details in packet details to identify usernames/domains.


