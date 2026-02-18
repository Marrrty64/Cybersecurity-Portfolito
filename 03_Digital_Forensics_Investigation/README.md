# Digital Forensics Investigation – IDTHEFT1.E01

---

## Objective

Perform a court-defensible forensic acquisition and registry-based investigation of suspect system **“KAL”** in relation to identity theft and illicit digital activity involving Elvis Polytech.

**Evidence Analyzed:** `IDTHEFT1.E01`

---

# Phase 1 – Evidence Acquisition & Integrity Verification

## Evidence Intake

- Evidence received: **20.4 GB Quantum Fireball HDD**
- Intake time documented
- Evidence photographed and cataloged
- Chain-of-custody maintained

---

## Forensic Imaging Process

- **Tool:** EnCase v21.1  
- **Hardware Write-Blocker:** Tableau SATA/IDE Bridge  
- Structured forensic case directories created:
  - Primary Evidence
  - Secondary Evidence
  - Backup
  - Export
  - Temp

---

## Hash Verification

**Primary Evidence MD5:**
***57AB40119ABD7DCC86902E6B55DBD8C7***

**Secondary Evidence MD5:**
***EC382F42CC909FCFB44AAE68CD185482***

- MD5 and SHA1 generated during acquisition
- Image verified successfully
- **0 errors reported**
- Status: **Completely Verified**

This confirms forensic integrity and evidentiary admissibility.

---

# Phase 2 – Registry Analysis (SYSTEM Hive)

## Computer Identification

**Computer Name:**
***KAL***

## Timezone Analysis

**ActiveTimeBias:**
0x00000168 (360)

Confirmed system operating in:
- **Pacific Daylight Time (UTC -7)**

---

# USB Artifact Analysis (UBSTOR)

Recovered removable storage history:

- USB DISK USB Device
- Apacer HandyDrive USB Device
- SanDisk ImageMate II USB Device (multiple instances)

These artifacts confirm prior removable storage usage, potentially for data transfer or exfiltration.

---

# Phase 3 – SAM Hive Analysis

## Identified User Accounts

- Administrator
- Guest
- HelpAssistant
- Keith
- Jo Ellen
- HTCIA
- ID THEFT DUDE
- Support_388945a

---

## SID Recovery & Validation

Full SIDs extracted using:

- EnCase manual registry inspection
- RegRipper v3.0 hive parsing

Matching RIDs and SIDs were confirmed across tools, validating registry interpretation accuracy.

---

# Last Logon Reconstruction

**User:** `ID THEFT DUDE`

- Last Logon (UTC):  
  `September 26, 2003 – 23:07:30 Z`

- Converted to PDT:  
  `September 26, 2003 – 09:07:30 AM`

Validated using:

- Windows FILETIME decoding
- RegRipper analysis
- SYSTEM hive timezone bias

---

# Phase 4 – NTUSER.DAT User Activity Analysis

## Illegal MP3 File Artifacts

Located within:
***Software\Microsoft\Windows\CurrentVersion\Explorer\RecentDocs.mp3***

Recovered filenames:

- La Femme Nikita
- Copy of “La Femme Nikita,” “Spies” – Coldplay
- “How You Remind Me” (Acoustic) – Nickelback

These artifacts demonstrate direct user interaction with unauthorized media files.

---

# Printer Configuration Analysis

Recovered printer device:
***HP DeskJet 3820 Series***

Located under:
***Printers\DeviceOld***

Confirms configured peripheral hardware on the system.

---

# Credential Recovery

Recovered POP account configuration:
**Mail Server:**
***mail.fakeid.com***

**Recovered Password (Protected Storage):**
***123fakeid123***

Registry Path:
***Software\Microsoft\Protected Storage System Provider***

Demonstrates plaintext credential storage within registry artifacts.

---

# Internet Explorer Artifact Analysis

## Homepage
***http://www.microsoft.com/isapi/redir.dll?prd=ie&pver=6&ar=msnhome***

## Last Download Location
- ***wmplayer.exe***
- ***D:\Music from WV\Midi\Ninja Gaiden***

Recovered via:
***ComDlg32\LastVisitedMRU***

Confirms browser activity and recent file access patterns.

---

# Investigative Conclusions

The forensic examination confirms:

- Use of removable USB devices
- Presence of unauthorized MP3 files
- Active user account activity (ID THEFT DUDE)
- Verified logon timeline reconstruction
- Recovered email credentials
- Internet browsing artifact recovery
- Court-admissible imaging process

Evidence supports intentional digital misconduct and user attribution.

---

# Skills Demonstrated

- Forensic Imaging & Hardware Write-Blocking
- MD5 / SHA1 Hash Validation
- Chain of Custody Documentation
- Registry Hive Analysis (SYSTEM, SAM, NTUSER.DAT)
- SID & RID Reconstruction
- Windows FILETIME Decoding
- USB Artifact Analysis (UBSTOR)
- Credential Recovery via Registry
- Internet Artifact Reconstruction
- RegRipper Parsing & Validation
- EnCase Evidence Processing
- Structured Forensic Reporting
