# 🧠 Cloud Computing – Lab 05
### Java, apt vs apt-get, snap, GUI, Vim on Ubuntu Server

---

## 📋 Student Details
- **Name:** Hafsa Khalid
- **Registration No:** 2023-BSE-021
- **Section:** 5A
- **Course:** Cloud Computing
- **Instructor:** Engr. Muhammad Shoaib

---

## 🧪 Lab Overview
This lab provides practical experience in **Linux package management**, **software installation using apt, apt-get, and snap**, as well as **GUI setup**, **Vim editing**, and **YAML configuration** on an Ubuntu server.

---

## ⚙️ Tasks Performed

### **Task 1 – Discover Missing Command & Install Java Using apt Suggestion**
- Identified missing Java command on Ubuntu.
- Installed Java using `sudo apt install default-jre`.
- Verified Java installation with `java --version`.

### **Task 2 – Install & Remove Java Using apt-get**
- Used `sudo apt-get install` and `sudo apt-get remove` to explicitly install and uninstall Java.
- Understood the difference between `apt` (user-friendly) and `apt-get` (advanced, scriptable).

### **Task 3 – apt update vs apt upgrade**
- Ran both commands to understand:
  - `apt update` refreshes package lists.
  - `apt upgrade` installs updated versions of available packages.

### **Task 4 – Install Visual Studio Code via Snap**
- Installed VS Code using:
  ```bash
  sudo snap install code --classic
  ```
- Verified installation by launching VS Code.
- (Note: Code was not removed as per lab instructions.)

### **Task 5 – Install XFCE GUI + XRDP (Remote Desktop Access)**
- Installed minimal desktop environment:
  ```bash
  sudo apt install xfce4 xfce4-goodies xrdp -y
  ```
- Enabled remote desktop access and successfully launched VS Code in GUI mode.

### **Task 6 – Install LightDM-GTK-Greeter and GUI Verification**
- Installed and configured LightDM display manager:
  ```bash
  sudo apt install lightdm lightdm-gtk-greeter -y
  ```
- Started GUI session, verified successful launch, opened VS Code, and then exited GUI.

### **Task 7 – Install Google Chrome via apt Source & Key**
- Added Chrome’s repository and GPG key manually.
- Installed Chrome using `sudo apt install google-chrome-stable`.

### **Task 8 – Install Applications via PPA (Audacity & OBS)**
- Added PPA repositories and installed:
  ```bash
  sudo add-apt-repository ppa:ubuntuhandbook1/audacity
  sudo apt install audacity
  sudo add-apt-repository ppa:obsproject/obs-studio
  sudo apt install obs-studio
  ```
- Launched both applications to confirm successful installation.

### **Task 9 – Create a Kubernetes Sample YAML using Vim**
- Created and edited a YAML configuration file in Vim.
- Practiced correct indentation and structure.

### **Task 10 – Edit the Kubernetes YAML**
- Added annotation and verified changes.
- Practiced temporary modifications and discarded them to retain original version.

### **Task 11 – Vim Editing Practice**
- Practiced:
  - Deleting lines and words (`dd`, `dw`)
  - Undo operations (`u`)
  - Numeric deletes (`5dd`)
  - Navigation using `h`, `j`, `k`, `l`

### **Task 12 – Vim Search, Match, Substitute, Undo**
- Performed search using `/keyword`
- Added matches with `n` and `N`
- Substituted text using:
  ```vim
  :%s/old/new/g
  ```
- Undid changes and saved the final file.

---

## 🧰 Tools & Environment
- **Platform:** VMware
- **Operating System:** Ubuntu Server
- **Editors & Tools:** Vim, Visual Studio Code
- **Package Managers:** apt, apt-get, snap
- **Desktop Environment:** XFCE, LightDM
- **Additional Software:** Google Chrome, Audacity, OBS Studio

---

## 🏁 Conclusion
This lab provided extensive practice with **Linux software management**, **snap packages**, **remote GUI access**, and **text editing with Vim**. It also introduced **YAML configuration** for Kubernetes — a crucial skill in cloud computing and DevOps environments.

---

### 📅 Submitted by:
**Hafsa Khalid (2023-BSE-021)**  
**Section 5A – Cloud Computing**
