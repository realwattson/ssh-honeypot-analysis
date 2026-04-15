# 🛡️ Cowrie SSH Honeypot Analysis Lab

## 📌 Overview
This project demonstrates a deployed **Cowrie SSH honeypot** used to capture and analyze real-world attacker behavior targeting exposed SSH services. The honeypot simulates a vulnerable Linux SSH server to log malicious activity for security analysis.

---

## 🧪 Tools & Technologies
- Cowrie Honeypot
- Docker / Linux Environment
- SSH (OpenSSH)
- Log Analysis
- Terminal / CLI

---

## 🎯 Objectives
- Deploy a fake SSH server (honeypot)
- Capture unauthorized login attempts
- Monitor attacker behavior after login
- Analyze common reconnaissance commands
- Understand real-world SSH attack patterns

---

## 📊 Attack Summary (From Logs)

### 🔐 1. Connection Attempt
- Attacker connected to SSH service:
  - Source: `172.17.0.1`
  - Target: Cowrie SSH port `2222`

---

### 👤 2. Login Attempt
- Username: `root`
- Password tried: `b'watson`
- Authentication: **Accepted (simulated by honeypot)**

> Cowrie allows fake authentication to observe attacker behavior.

---

### 💻 3. Attacker Commands Observed
After gaining access, the attacker executed basic Linux reconnaissance commands:

- `pwd` → check current directory
- `ls` → list files
- `whoami` → identify current user
- `uname -a` → check system information

---

### ⏱ 4. Session Termination
- Session ended due to timeout / inactivity
- Attacker disconnected after basic probing

---

## 🧠 Security Insights

This log reveals a typical automated SSH attack pattern:

### 🔴 Stage 1: Scanning
Attackers locate exposed SSH services.

### 🔴 Stage 2: Credential Guessing
Common usernames like `root` are tested with weak passwords.

### 🔴 Stage 3: System Reconnaissance
After login, attackers attempt to understand:
- System identity
- File structure
- Environment details

### 🔴 Stage 4: Exit
If no valuable data is found, session ends quickly.

---

## 📈 Key Learnings

- Real-world SSH brute-force behavior
- Honeypot deployment and monitoring
- Linux command usage in attack scenarios
- Log analysis and threat interpretation
- Understanding attacker workflows

---

## 📸 Evidence
(Add your screenshot of Cowrie logs here)

---

## 🚀 Conclusion

This project demonstrates how attackers behave inside a controlled environment. It provides valuable insight into SSH brute-force attacks and reconnaissance techniques used by automated bots and malicious actors.

---

## 🔐 Author

cyberWatts
