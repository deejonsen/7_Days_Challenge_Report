---

## 🛠️Day 2 Report

### **Network Traffic Monitoring & Packet Analysis**

### **Objective: Capture and analyze network traffic for suspicious activity.**

---
### **Introduction**
Wireshark is an advanced tool used to capture and analyze network traffic in real time. It provides a comprehensive view of what’s happening on the network, which is invaluable for cybersecurity professionals, network administrators, and analysts. One of Wireshark's most powerful features is its ability to apply **display filters**. Display filters allow users to isolate and examine specific types of network traffic, making the task of identifying potential security threats much easier.

---
## **📜Tasks Completed**

### **1️⃣ Installed Wireshark**
✔️ **Linux/Ubuntu:**
```
sudo apt install wireshark -y  # Installed Wireshark via terminal
```
🔹 **✅Kali Linux:**

✔️ Wireshark is pre-installed. Launched with:
```
wireshark
```


### **2️⃣ Captured Network Traffic**
**✔️ Steps Taken:**
- **Selected an active network interface (e.g., `eth0` or `wlan0`).**
- **Started capturing live traffic.**
- **Applied filters to isolate specific protocols:**
```
http  # Filter HTTP traffic (websites, unencrypted logins)
dns   # Filter DNS queries (domain lookups)
icmp  # Filter ICMP packets (ping requests)
```


### **3️⃣ Analyzed a PCAP File**
**✔️ Sample PCAP File:**
**Downloaded **PCAP file** from** [https://wiki.wireshark.org/uploads/27707187aeb30df68e70c8fb9d614981/http.cap)).

**🎯 Key Findings:**
  - **Plaintext Credentials:**
    - **Found HTTP traffic with unencrypted username/password fields.**
    - **Example packet: POST /login HTTP/1.1 → username=admin&password=12345.**
  
  - **💡Protocol Risks:**
    - **Highlighted insecure protocols like **HTTP, FTP, & Telnet**  transmitting data unencrypted.**


### **4️⃣ Identified Suspicious Activity**
**🚨 Red Flags:**

  - **Large Data Transfers:**
    - **Filtered for **`tcp.len > 1000`** to detect large payloads (e.g., file exfiltration).**

  - **Failed Logins:**
    - **Searched for repeated **`HTTP 401 Unauthorized`** or **`SSH Failed password alerts`**.**
   
  - **Unknown IPs:**
    - **Used **`ip.addr == 192.168.1.100`** to track unrecognized IPs communicating with the host.
  

### **🚀Key Takeaways**
- **Wireshark Filters are critical for efficient analysis (e.g., `http.request.method == "POST`").**
- **Plaintext protocols (HTTP, FTP) expose sensitive data to eavesdroppers.**
- **Unusual traffic patterns (e.g., spikes in ICMP requests) may indicate reconnaissance or attacks.**


![Screenshot 2025-03-04 103451](https://github.com/user-attachments/assets/82defe1a-93f8-458d-b261-d6047f2ced73)

!![Screenshot 2025-03-04 103538](https://github.com/user-attachments/assets/0adf788f-abd2-4216-9a16-8c161fa2358a)

![Screenshot 2025-03-04 103245](https://github.com/user-attachments/assets/b3616ef0-347f-4a11-a017-6fbbdc48dbca)

![Screenshot 2025-03-04 103222](https://github.com/user-attachments/assets/80736375-415b-4932-bec1-6ccfb31b399f)

![Screenshot 2025-03-04 103148](https://github.com/user-attachments/assets/99a75a67-9764-4afb-ae53-b5b7b115098c)

![Screenshot 2025-03-04 103121](https://github.com/user-attachments/assets/016e0a51-aacd-4fad-97ea-6fe1af6d479b)

![Screenshot 2025-03-04 103107](https://github.com/user-attachments/assets/c658dc74-c561-4343-ac4d-f9e2958ad305)

![Screenshot 2025-03-04 103047](https://github.com/user-attachments/assets/72f573cd-7b14-450e-ad86-1c1de74abc62)

![Screenshot 2025-03-04 103018](https://github.com/user-attachments/assets/41a748c7-bbb2-4087-a85d-4566e7ea92cc)

![Screenshot 2025-03-04 103000](https://github.com/user-attachments/assets/02828804-6f84-4684-81c9-7352402e79b2)

![Screenshot 2025-03-04 102933](https://github.com/user-attachments/assets/15cd6907-fac0-4c2c-87e2-516b91026c24)

![Screenshot 2025-03-04 102858](https://github.com/user-attachments/assets/423b9689-c14d-4ddb-8911-c3ae52b950c3)

![Screenshot 2025-03-04 102815](https://github.com/user-attachments/assets/eeeb7ca6-e06b-477b-a7f2-9ab8eab9b7f9)
![Screenshot 2025-03-04 102758](https://github.com/user-attachments/assets/ea5d78fc-df7c-40d9-9abb-0132a8d4af5d)
![Screenshot 2025-03-04 103451](https://github.com/user-attachments/assets/569a4b70-f840-4fdf-b077-fec785613ed9)
