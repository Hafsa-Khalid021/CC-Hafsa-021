# Cloud Computing – Lab 06  
**Submitted by:** Hafsa Khalid  
**Reg No:** 2023-BSE-021  
**Section:** 5A  
**Course:** Cloud Computing  
**Instructor:** Engr. Muhammad Shoaib  

---

## 🧩 Overview
This lab focuses on Linux user and group management, file permissions, scripting, and setting up a graphical desktop environment (GUI) using GitHub Codespaces with VNC (noVNC).

---

## ⚙️ Tasks Summary

### **Task 1 – Switch Users**
- Switched to root user using `su -`  
- Returned to normal user using `exit`

### **Task 2 – User Creation & Verification**
- Created a new user:  
  ```bash
  sudo adduser tom
  ```
- Verified the user in `/etc/passwd`, `/etc/group`, and `/etc/shadow`

### **Task 3 – Group Management**
- Created groups using `groupadd`
- Changed *tom*’s primary and secondary groups:
  ```bash
  usermod -g primarygroup -G secondarygroup tom
  ```

### **Task 4 – Create/Delete Users and Groups**
- Created users `Jerry`, `Scooby`  
- Created groups `jolly`, `anime`  
- Demonstrated deletion using:
  ```bash
  sudo deluser Jerry
  sudo groupdel jolly
  ```

### **Task 5 – Ownership and File Types**
- Created a new user `Student`
- Created files and changed ownership:
  ```bash
  chown Student filename
  chgrp Student filename
  file filename
  ```

### **Task 6 – Symbolic Permissions**
- Modified file permissions using:
  ```bash
  chmod u+x,g-w,o+r filename
  ```

### **Task 7 – Set Symbolic Mode (u=, g=, o=)**
- Example:
  ```bash
  chmod u=rwx,g=rx,o= filename
  ```

### **Task 8 – Numeric (Octal) Permissions**
- Example:
  ```bash
  chmod 754 filename
  ```

### **Task 9 – Pipes, Pagers, and Redirects**
- Practiced:
  ```bash
  cat /var/log/syslog | grep error
  less /var/log/syslog
  ```

### **Task 10–13 – Bash Script (setup.sh)**
Implemented:
- **Variables** and **Command Substitution**
- **File and Directory Checks**
- **Permissions Handling**
- **Argument Comparisons** (`eq, ne, gt, lt, ge, le`)
- **String Tests**
- **Loops** (`for`, `while`)
- **Functions**
  
Example:
```bash
#!/bin/bash
if [ $# -eq 0 ]; then
  echo "No arguments provided"
else
  for arg in "$@"; do
    echo "Argument: $arg"
  done
fi
```

---

## 💻 Task 14 – Codespaces GUI (VNC Setup)

### **Step 1: Install XFCE Desktop**
```bash
sudo apt update
sudo apt install xfce4 xfce4-goodies -y
```

### **Step 2: Configure VNC Startup**
```bash
nano ~/.vnc/xstartup
```
Add:
```bash
#!/bin/bash
xrdb $HOME/.Xresources
startxfce4 &
```
Then:
```bash
chmod +x ~/.vnc/xstartup
```

### **Step 3: Start VNC and noVNC**
```bash
vncserver :1
/usr/share/novnc/utils/novnc_proxy --vnc localhost:5901 --listen 6080
```

### **Step 4: Open VNC in Browser**
1. In **VS Code → Ports Tab**, find port **6080**
2. Copy the forwarded URL (like `https://<yourcodespace>-6080.githubpreview.dev`)
3. Open it with `/vnc.html` at the end:
   ```
   https://<yourcodespace>-6080.githubpreview.dev/vnc.html
   ```

### **Step 5: Connect**
- Enter your VNC password (set using `vncpasswd`)
- XFCE desktop appears on successful connection

---

## ✅ Outcome
- Successfully managed Linux users, groups, and permissions  
- Created and tested Bash automation scripts  
- Configured and launched a functional **Linux GUI (XFCE)** inside **GitHub Codespaces** using **noVNC**

---

## 📦 Files Included
- `setup.sh` – Automation script
- `~/.vnc/xstartup` – VNC startup configuration
- `README.md` – Lab summary
