---

## 📜Day 5 Report

### **Password Cracking & Hash Analysis**

### **Objective: Learn how weak passwords can be cracked.**
---

### **Introduction**
Passwords are the first line of defense in most authentication systems, but poor practices like weak passwords, unsalted hashes, or outdated algorithms leave systems vulnerable. Password cracking and hash analysis are critical skills for identifying these weaknesses, enabling defenders to strengthen security and attackers to exploit gaps.

### **Why This Matters**
🔹**Data Breaches:** Weak passwords account for 81% of hacking-related breaches.

🔹**Hash Vulnerabilities:** Attackers exploit poorly stored hashes (e.g., unsalted MD5) to reverse-engineer passwords.

🔹**Ethical Auditing:** Security teams use cracking tools to test password policies and patch vulnerabilities.


---
## **📜Tasks Completed**

### **1️⃣ Generated Password Hashes**
✔️ **MD5 Hash Creation:**
```
echo -n "password123" | md5sum  # -n avoids adding a newline character
```

✔️ **Output:**
```
482c811da5d5b4bc6d497ffa98491e38  -
```
✔️ **Analysis**
  - **MD5 is cryptographically broken and trivial to crack.**
  - **Modern systems should use bcrypt or SHA-256 with salting.**


---

### **2️⃣ Cracked Hashes with Hashcat**
**✔️ Installation:**
```
sudo apt install hashcat -y  # Installed Hashcat
```

**✔️ Cracking Command:**
```
hashcat -m 0 -a 0 hash.txt rockyou.txt
```

  🔹 **Flags:**
  - **`-m 0`:** MD5 hash mode.
  - **`-a 0`:** Dictionary attack.

🔹 **Workflow:**
- Stored the hash **`482c811da5d5b4bc6d497ffa98491e38`** in **`hash.txt`**.
- Used the **`rockyou.txt`** wordlist (common passwords).


📌 **Output:**
```
482c811da5d5b4bc6d497ffa98491e38:password123
```


---

### **3️⃣ Brute-Forced SSH with Hydra**
**✔️ Command Executed:**
```
hydra -l admin -P rockyou.txt ssh://192.168.0.4
```

**✔️Flags Explained:**
  - **`-l admin`:**  Target username "admin".
  - **`-P rockyou.txt`:** Password wordlist.

**✔️ Outcome:**
- Tested passwords like **`admin`**, **`123456`**, and **`password`** against SSH.
- Success if Hydra finds a match (e.g., **`[22][ssh] host: 192.168.1.10 login: admin password: admin123`**).
  

---
### **🚀Key Takeaways**
🔹**Weak Passwords Are Easy Targets:**
  - **`password123`** was cracked in seconds using MD5 and a wordlist.
  - Default credentials (e.g., **`admin:admin`**) are common in IoT devices.

🔹**Mitigation Strategies:**
  - **Strong Hashing:** Use bcrypt or Argon2 with salts.
  - **Password Policies:** Enforce 12+ characters, no dictionary words.
  - **Rate Limiting:** Block repeated login attempts.



![Screenshot 2025-03-04 110340](https://github.com/user-attachments/assets/68da232e-0613-4b3f-ba63-ff0dae9c0724)

![Screenshot 2025-03-04 110325](https://github.com/user-attachments/assets/5c49b035-0541-42d7-b6cd-5faf62072ca7)

![Screenshot 2025-03-04 110211](https://github.com/user-attachments/assets/24146875-7c1e-4d6c-8c74-7a9b3a629cad)

![Screenshot 2025-03-04 110129](https://github.com/user-attachments/assets/fc73ff3e-9be2-4d64-abf9-be4a04872108)

![Screenshot 2025-03-04 110048](https://github.com/user-attachments/assets/0edba1d5-ad83-4dcf-9e35-fba563f1d894)

![Screenshot 2025-03-04 110018](https://github.com/user-attachments/assets/3b755a07-97f4-4ba7-9015-54986b649cef)

![Screenshot 2025-03-04 110003](https://github.com/user-attachments/assets/2a9981e2-3709-4cb1-98d0-3505ab8ef825)

![Screenshot 2025-03-04 105951](https://github.com/user-attachments/assets/1fa81482-a68c-4b02-9c47-e8fb00379aae)

![Screenshot 2025-03-04 105940](https://github.com/user-attachments/assets/5dad63af-0fff-46c9-8d9a-25d1c8fb3926)

![Screenshot 2025-03-04 105832](https://github.com/user-attachments/assets/2b1dcb75-e4d8-4452-bb88-f64f69329bf3)

![Screenshot 2025-03-04 105758](https://github.com/user-attachments/assets/39bd0a65-670f-433e-8c23-4c69d4c31365)

![Screenshot 2025-03-04 105701](https://github.com/user-attachments/assets/e3288327-7cc6-4f52-bb71-6bc26e2b9178)
