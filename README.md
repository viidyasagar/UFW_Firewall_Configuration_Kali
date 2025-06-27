# UFW_Firewall_Configuration_Kali

## 📘 Description

This project demonstrates basic firewall configuration using **UFW (Uncomplicated Firewall)** on **Kali Linux**. The objective was to understand how to manage inbound traffic rules, test blocked ports, and ensure essential ports like SSH remain accessible.
Screenshots of each step are included for reference.

---

## 📂 Steps Performed

### 1️⃣ Install UFW

Updated package list and installed UFW:

```bash
sudo apt update
sudo apt install ufw
```

### 2️⃣ Check Existing Firewall Rules

Checked if UFW is active and listed current rules:

```bash
sudo ufw status numbered
```

### 3️⃣ Enable UFW

Enabled UFW to start filtering:

```bash
sudo ufw enable
```

### 4️⃣ Block Port 23 (Telnet)

Added rule to block inbound Telnet connections:

```bash
sudo ufw deny in 23
```

### 5️⃣ Test Block Rule

Tested Telnet access to port 23 to verify the block:

```bash
telnet localhost 23
```

**Result:** `Connection refused`, confirming block was successful.

### 6️⃣ Allow SSH (Port 22)

Ensured SSH access was allowed to avoid getting locked out:

```bash
sudo ufw allow ssh
```

### 7️⃣ Delete Test Rule

Removed the Telnet block rule to restore original state:

```bash
sudo ufw delete 1
```

*Note: Adjust the rule number based on the output from `ufw status numbered`.*

---

## 🧾 Summary

UFW is a simplified interface for managing iptables rules. It allows users to easily:

* Allow/deny traffic based on port numbers and protocols
* Enable or disable firewall rules quickly
* Apply basic security configurations without deep networking knowledge

In this example:

* Port 23 was blocked and verified.
* SSH on port 22 was permitted.
* The test block rule was deleted to maintain original state.

---

## 📸 Screenshots

Included screenshots:

* 📦 UFW installation and setup
* ✅ Rule addition and verification
* 🔍 Telnet connection test
* 🗑️ Rule deletion

---

## 🛠️ Tools Used

* 🐧 Kali Linux (Terminal)
* 🔥 UFW (Uncomplicated Firewall)
* 📡 Telnet
* 📸 Screenshot tool (GNOME/Kali default)

---

## 🧠 Learnings

* How UFW filters inbound traffic based on defined rules.
* Importance of verifying each firewall rule.
* Ensuring SSH access before making restrictive changes.
* Using `telnet` to test port accessibility.

---

## 📁 Repository Structure

```
📂 ufw-firewall-lab
├── 📸 Screenshot_1: UFW Install & Enable
├── 📸 Screenshot_2: Rules Applied
├── 📸 Screenshot_3: Telnet Test & Delete Rule
└── README.md
```


Beginner in cybersecurity exploring firewall configurations as part of hands-on labs.


