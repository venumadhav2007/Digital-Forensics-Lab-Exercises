# 📧 Experiment 4: Mail Header Analyzer (MHA)

**Aim:**  
To trace an email's origin and verify its authenticity by examining its header for signs of spoofing using a **Mail Header Analyzer**.

---

## 📝 Procedure

### Step 1: Get the Email Header
- Open the email client (e.g., Gmail).  
- Use **Show Original** to copy the full raw header.  

### Step 2: Use Mail Header Analyzer Tool
- Navigate to an analyzer site like **MXToolbox – Email Header Analyzer**.  
- Paste the raw header into the input box.  
- Click **Analyze** to generate a parsed, human-readable report.  

### Step 3: Analyze SPF, DKIM, DMARC
- **SPF** (Sender Policy Framework): Passed – sending server is authorized.  
- **DKIM** (DomainKeys Identified Mail): Authentication failed ❌ (signature mismatch).  
- **DMARC** (Domain-based Message Authentication, Reporting & Conformance): Passed ✅  

### Step 4: Trace Delivery Path
- Review the email’s delivery route.  
- Confirm if the sending server (e.g., Mailgun server) matches the SPF record.  

### Step 5: Investigate DKIM Failure
- Analyze why DKIM failed while SPF & DMARC passed.  
- This indicates a possible issue with the signing domain or unauthorized modification.  

---

## ✅ Conclusion
- Email passed **SPF and DMARC**, confirming authorized sending servers.  
- **DKIM authentication failed**, raising concerns about integrity.  
- Demonstrates the importance of checking **all three standards (SPF, DKIM, DMARC)** for detecting spoofing attempts.  

---
