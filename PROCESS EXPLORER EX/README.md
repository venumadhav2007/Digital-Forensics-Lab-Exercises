# 🧩 Experiment 9: Process Explorer – Identifying Suspicious Processes

**Aim:**  
To use **Process Explorer** (from Microsoft Sysinternals) to identify, analyze, and investigate suspicious processes running on a Windows system.

---

## 📝 Procedure

### Step 1: Download and Launch Process Explorer
- Go to the **Microsoft Sysinternals website** and download Process Explorer.  
- Extract the ZIP file and run `procexp64.exe` (for 64-bit) as **Administrator**.  
- Accept the license agreement to launch the tool.

---

### Step 2: Observe the Interface
- The Process Explorer main window lists all active processes in a **tree view**.  
- Each process is color-coded:
  - 🟩 **Green:** Newly created processes  
  - 🟥 **Red:** Terminated processes  
  - 🟦 **Blue:** Processes belonging to the current user  
  - 🟪 **Purple:** Packed or protected processes  
- Columns display important data like PID, CPU usage, Memory, and Description.

---

### Step 3: Identify Suspicious Processes
- Look for **unfamiliar or unsigned processes**.  
- Right-click → **Properties → Image tab** → verify the **digital signature**.  
- Check the **path** of the executable file — legitimate system files are usually found in  
  `C:\Windows\System32\` or `C:\Program Files\`.  
- Examine **CPU or memory spikes** that may indicate malicious behavior.

---

### Step 4: Inspect Network Activity
- Right-click the suspicious process → **Properties → TCP/IP tab**.  
- Check for unknown remote connections.  
- Unexpected network traffic from unknown executables often signals malware activity.

---

### Step 5: Terminate or Suspend Processes
- If a process is confirmed malicious:  
  - Select the process → **Kill Process** to stop it.  
  - Or use **Suspend** to freeze it temporarily while investigating further.  
- After termination, manually locate the executable via its path and remove it safely.  

---

### Step 6: Validate and Scan
- Run an antivirus or **Windows Defender** full scan after termination.  
- Use tools like **VirusTotal** or **ProcessLibrary.com** to verify if the process is known malware.  

---

### Example Output (Process Analysis)

Process Name: randomname123.exe  
Path: C:\Users\AppData\Local\Temp\randomname123.exe  
CPU Usage: 45%  
Network Connections: Active to unknown IP (104.27.144.23)  
Signature: Invalid  
Verdict: Malicious – Terminate Immediately
---

## ✅ Conclusion  
- Successfully used **Process Explorer** to monitor and analyze system processes.  
- Identified suspicious executables by examining their **digital signatures**, **CPU usage**, and **memory behavior**.  
- Investigated unknown network connections through the **TCP/IP tab** to detect possible external communication.  
- Demonstrated the importance of process monitoring in **malware detection and forensic investigation**.  
- Thus, the experiment to identify suspicious processes using **Process Explorer** was successfully completed.

---
