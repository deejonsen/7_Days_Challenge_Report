---

## 📜Day 7 Report

### **Simple Capture The Flag (CTF) Challenge**

### **Objective: Solve beginner-friendly security challenges.**
---

### **Introduction**
CTFs are cybersecurity competitions where participants solve puzzles, exploit vulnerabilities, and analyze systems to find hidden "flags"—secret strings of text that prove successful completion of a task. Designed for learning and skill-building, CTFs simulate real-world scenarios in a safe, legal environment.

### **Why Digital Forensics Matters**
🔹**Hands-On Learning:** Practice hacking skills (ethically!) without real-world risks.

🔹**Skill Diversity:** Tackle challenges in cryptography, forensics, web exploitation, reverse engineering, and more.

🔹**Data Recovery:** Retrieve deleted or corrupted files from damaged devices.

🔹**Community & Competition:** Join global platforms like [Hack The Box](https://www.hackthebox.com/) or [CTFtime](https://ctftime.org).


---
## **📜Tasks Completed**

### **1️⃣Joined PicoCTF**
🔹**Sign-Up:** Created an account at [PicoCTF](https://picoctf.org), a free platform for learning cybersecurity through CTF challenges.

🔹**Navigated to Practice Arena: Accessed the Practice section to find beginner challenges.**

---

### **2️⃣ Solved the "Basic File Read" Challenge**
**✔️Challenge Link:** 
 - https://play.picoctf.org/practice/challenge/147?page=4


 - **Category:** Web Exploitation

 - **Difficulty:** Easy


**✔️ Steps to Solve:**
- **Challenge Description:**
  - A website allows users to "read files" from the server. The file had a flag in plain sight (aka "in-the-clear"). 

- **File Acquisition:**
  - Downloaded the file to kali environment.
 
  - - **Initial Analysis:**
  - On the terminal, switched to the directory in which the downloaded file was stored.
  - Executed the `cat` command in the terminal to directly output the file's contents.


**✔️ Flag Extraction:**
-  Flag was immediately visible wit, unencrypted and unobscured.
-  Copied the flag.
- Submitted the contents of the file and retrieved the flag:
```
picoCTF{s4n1ty_v3r1f13d_f28ac910}
```

---

### **3️⃣ Wrote a CTF Write-Up**
💡**Challenge Write-Up: Obedient Cat (PicoCTF 2021)**
🔹**Challenge Overview**
  - This introductory CTF challenge required analyzing a provided file to locate a hidden flag.

🔹**Steps Taken:**
1. File Acquisition: Downloaded the challenge file to my local environment. 
2. Initial Analysis: Executed the cat command in the terminal to directly output the file's contents. 
3. Flag Identification: The flag was immediately visible within the file, unencrypted and unobscured. 

🔎 **Outcome:** 
The flag was successfully captured from the file’s plaintext content and submitted to complete the challenge. 

---

## **🚀Key Takeaways**  
🔹 **LFI Risks**: Unrestricted file access can expose sensitive system files.  
🔹 **Defense**: Sanitize user input and restrict file paths (e.g., allow only whitelisted files).  
🔹 **CTF Mindset**: Think like an attacker—test assumptions and common vulnerabilities.  

---



![Screenshot 2025-03-04 114329](https://github.com/user-attachments/assets/ae381b56-a10e-44a0-bd04-524e83d27b43)

![Screenshot 2025-03-04 111911](https://github.com/user-attachments/assets/6501c734-693e-487a-b352-4467defceb2c)

![Screenshot 2025-03-04 111859](https://github.com/user-attachments/assets/6d90a521-3361-40bd-9dc8-f696c9ed78af)

![Screenshot 2025-03-04 111846](https://github.com/user-attachments/assets/2ba4c81a-5ad3-4b5b-8beb-f1a030c9982e)

![Screenshot 2025-03-04 111830](https://github.com/user-attachments/assets/7b461e3e-faa4-4baa-90ea-4c1cbf47a63f)

![Screenshot 2025-03-04 111750](https://github.com/user-attachments/assets/c1985a97-9373-4a38-ac6f-76a12b197d0d)

![Screenshot 2025-03-04 111729](https://github.com/user-attachments/assets/3ad4ed22-a12d-47ce-b566-ea00af153af7)

![Screenshot 2025-03-04 111716](https://github.com/user-attachments/assets/57684e60-94ee-49d9-a99f-df9563713105)

![Screenshot 2025-03-04 111636](https://github.com/user-attachments/assets/7de03b1a-7eba-4630-a76d-b80c70034632)

![Screenshot 2025-03-04 111615](https://github.com/user-attachments/assets/8f512be3-c3ce-4169-87b2-2284230d34db)
