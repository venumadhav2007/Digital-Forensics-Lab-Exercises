🧪 Evidence Acquisition Using AccessData FTK Imager

🎯 Aim
To acquire both volatile memory (RAM) and non-volatile memory (Disk Image) using AccessData FTK Imager, ensuring evidence integrity by generating forensic image files with hash verification.

🛠️ Tools Required
AccessData FTK Imager (version 4.x)
Windows System (Target Machine)
External Storage for saving evidence
(Optional) Write Blocker to prevent source disk modification
📖 Theory
Forensic Toolkit (FTK) Imager is a free tool provided by AccessData for acquiring forensic images.
It allows investigators to:

Capture volatile memory (RAM, pagefile)
Create disk images (physical drive, logical partitions, image files)
Export evidence in formats like Raw (dd), SMART, E01, AFF
Generate AD1 forensic image files for analysis
Verify integrity using MD5/SHA1 hash values
📝 Procedure / Steps
A) Acquiring Volatile Memory (RAM)
Open FTK Imager.
Click Capture Memory.
In the dialog:
Set Destination Path & Filename (memdump.mem).
Enable Include Pagefile (pagefile.sys).
Enable Create AD1 file (memcapture.ad1).
Click Capture Memory → Acquisition begins.
Observe progress and wait until completion.
Verify output files:
memdump.mem
pagefile.sys
memcapture.ad1, .ad2, .ad3
B) Acquiring Non-Volatile Memory (Disk Image)
Open FTK Imager → Click Create Disk Image.
Select Source Type (e.g., Physical Drive).
Choose the target disk → Click Finish.
Select Image Format:
Raw (dd)
SMART
E01
AFF
Enter Case Details (Case Number, Examiner Name, Notes).
Provide Destination Path, Filename, Fragment Size.
Set Fragment Size = 0 → single file.
Enable Verify Images after they are created.
Click Start → Image acquisition begins.
On completion, check the log file and confirm hash values match.
✅ Result
Successfully acquired volatile memory (RAM + pagefile) as .mem and .ad1 files.
Successfully created non-volatile memory disk image in selected format.
Integrity was verified through hash value confirmation.
Thus, evidence acquisition using FTK Imager was carried out successfully.
