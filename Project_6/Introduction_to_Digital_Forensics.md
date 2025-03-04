---

## 📜Day 6 Report

### **Introduction to Digital Forensics**

### **Objective: Learn how to recover deleted files and analyze evidence.**
---

### **Introduction**
Digital forensics is the scientific process of collecting, preserving, analyzing, and presenting digital evidence from electronic devices to investigate cybercrimes, data breaches, or unauthorized activities. It plays a critical role in incident response, legal proceedings, and understanding attack vectors in cybersecurity.

### **Why Digital Forensics Matters**
🔹**Incident Response:** Identify how a breach occurred, what data was compromised, and who was responsible.

🔹**Legal Evidence:** Provide court-admissible proof for cybercrime prosecutions.

🔹**Data Recovery:** Retrieve deleted or corrupted files from damaged devices.

🔹**Threat Intelligence:** Uncover attacker tactics, techniques, and procedures (TTPs).


---
## **📜Tasks Completed**

### **1️⃣Installed Autopsy (Digital Forensics Tool)**
✔️ **Installation:**
```
sudo apt install autopsy -y  # Installed Autopsy
```

✔️ **Launch:**
- **Start Autopsy: `autopsy` in the terminal.**
- **Access via browser: `http://localhost:9999/autopsy`.**

---

### **2️⃣ Analyzed a USB Drive Image**
**✔️ Workflow:**
- **Created a Case**
  - **Named the case (e.g., "USB_Recovery").**
  - **Added the disk image (`usb_image.dd`) as a data source.**


**✔️ Recovered Deleted Files:**
- **Used the File Recovery module to scan unallocated space.**
- **Identified recoverable files (e.g., deleted documents, images).**


**✔️ Key Findings:**
- **Recovered a deleted `secret_document.txt` from the USB image.**
- **Extracted file timestamps (created/modified times).**



---

### **3️⃣ Extracted Metadata with ExifTool**
**✔️ Installation (if missing):**
```
sudo apt install exiftool -y
```

**✔️ Command:**
```
exiftool image.jpg  # Extracted metadata from a sample image
```

**✔️ Output Example:**
```
File Name           : image.jpg  
File Size           : 2.5 MB  
Camera Model        : Canon EOS R5  
GPS Latitude        : 34.0522 N  
GPS Longitude       : 118.2437 W  
Date/Time Original  : 2023:10:15 14:30:22
```

---
### **🚀Key Takeaways**
🔹**Data Persistence:** Deleted files often remain recoverable until overwritten.

🔹**Metadata Risks:**
  - **EXIF data (e.g., GPS, timestamps) can leak sensitive information.**
  - Tools like **`ExifTool`** help investigators trace file origins.

🔹**Forensic Best Practices:**
  - Use **write blockers** to avoid altering original evidence.
  - Document chain of custody for legal admissibility.
---



![Screenshot 2025-03-04 111447](https://github.com/user-attachments/assets/3cbfb12f-ca21-45e4-a5cf-f718bfc8f416)

![Screenshot 2025-03-04 111242](https://github.com/user-attachments/assets/a8768767-e3f4-4846-b521-c10bf848c692)

![Screenshot 2025-03-04 111220](https://github.com/user-attachments/assets/218cf4d3-57fa-44d1-87e7-7b80d206251f)

![Screenshot 2025-03-04 111158](https://github.com/user-attachments/assets/f07bb3d2-1ffe-4dd3-9e6c-e54b5ae40fb3)

![Screenshot 2025-03-04 111140](https://github.com/user-attachments/assets/a05fc995-72fa-4fdb-a030-e68066f07bc2)

![Screenshot 2025-03-04 111122](https://github.com/user-attachments/assets/a8a5ed79-2245-4af6-8da2-d1136e786c5c)

![Screenshot 2025-03-04 111037](https://github.com/user-attachments/assets/09d141b4-684e-44c9-a5a8-6f4b984bc3fa)

![Screenshot 2025-03-04 111020](https://github.com/user-attachments/assets/2699901d-5f99-41b2-9f54-fffd30a5ade3)

![Screenshot 2025-03-04 110958](https://github.com/user-attachments/assets/66a9d1e6-e96f-405d-8fc6-dd62135100dc)

![Screenshot 2025-03-04 110934](https://github.com/user-attachments/assets/863dea68-7e98-4606-9923-0258f09ea494)

![Screenshot 2025-03-04 110904](https://github.com/user-attachments/assets/ce5673b1-40a0-46ec-b2a1-208ae15ebfb6)

![Screenshot 2025-03-04 110853](https://github.com/user-attachments/assets/78e8b89c-fb97-43e9-9105-f7bbe4340cb1)

![Screenshot 2025-03-04 110827](https://github.com/user-attachments/assets/8a23f4c9-0234-45c6-ad0f-80932c979bdd)

![Screenshot 2025-03-04 110813](https://github.com/user-attachments/assets/237b2460-edd3-4f7b-b439-881b4c95763d)

![Screenshot 2025-03-04 110753](https://github.com/user-attachments/assets/c26a91b6-fdaa-4bac-a1be-30ef19b8e7f4)
