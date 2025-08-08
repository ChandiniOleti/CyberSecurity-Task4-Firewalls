# CyberSecurity-Task4-Firewalls


# 🔒 Cyber Security Internship – Task 4

## 🔧 Task Title:
**Basic Firewall Configuration using UFW on Kali Linux**

---

## 📝 Objective

To configure and test firewall rules on a Linux system using UFW (Uncomplicated Firewall).  
The goal is to allow or block specific ports and understand how firewall rules filter network traffic.

---

## 🛠️ Tools Used

| Tool        | Purpose                                              |
|-------------|------------------------------------------------------|
| Kali Linux  | Operating System                                     |
| UFW         | Firewall configuration (frontend for iptables)      |
| Telnet      | Used to test if a port is open or blocked           |

---

## 📌 Task Summary

This task involves using UFW to:
- Enable the firewall on Kali Linux
- Block Telnet (port 23)
- Allow SSH (port 22)
- Test the rules using the Telnet tool
- Restore firewall state by deleting the test rule

---

## 🧪 Steps Followed

### 🔹 1. Update System
```
sudo apt update
```

### 🔹 2. Install UFW
```
sudo apt install ufw -y
```

### 🔹 3. Enable the Firewall
```
sudo ufw enable
```

### 🔹 4. Check Existing Firewall Rules
```
sudo ufw status numbered
```

### 🔹 5. Block Port 23 (Telnet)
```
sudo ufw deny 23
```

### 🔹 6. Allow Port 22 (SSH)
```
sudo ufw allow 22
```

### 🔹 7. Install Telnet to Test Port Block
```
sudo apt install telnet -y
```

### 🔹 8. Test Port 23 Block (Should Fail)
```
telnet localhost 23
```
Expected output:  
`Connection refused` or `Unable to connect to remote host`

### 🔹 9. Remove the Test Rule for Port 23
```
sudo ufw delete deny 23
```

---
