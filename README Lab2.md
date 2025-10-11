# Cloud Computing – Lab 02  
**Submitted by:** Hafsa Khalid  
**Registration No:** 2023-BSE-021  
**Section:** 5A  
**Submitted to:** Engr. Muhammad Shoaib & Engr. Waqas Saleem  

---

## 📘 Lab Overview
This lab focuses on **Git and GitHub** for version control, exploring repository management, SSH connection, branching strategies, collaboration, and code review workflows.

---

## 🧩 Tasks Summary

### **Task 1: Create Private GitHub Repository**
- Create a new **private repository** on GitHub.  
- Name it appropriately (e.g., `CC-Lab02`).

---

### **Task 2: Connect Repository via SSH**
- Copy the **SSH URL** from the repository.  
- Open **Git Bash** on your desktop and connect using SSH.

---

### **Task 3: Configure Git Username and Email**
- Use the following commands to set identity:
  ```bash
  git config --global user.name "Your Name"
  git config --global user.email "your_email@example.com"
  ```

---

### **Task 4: Explore the .git Folder**
- Initialize a Git repository locally.  
- Open the hidden `.git` folder to explore internal files (HEAD, config, refs, etc.).

---

### **Task 5: Local Repository Management**
- Create and manage files using:
  ```bash
  git init
  git add .
  git commit -m "Initial commit"
  git remote add origin <ssh-url>
  git push -u origin main
  ```

---

### **Task 6: File Status & Staging**
- Use the following to track file states:
  ```bash
  git status
  git add <filename>
  git commit -m "Message"
  ```

---

### **Task 7: Branch Creation Using GitHub GUI**
- Create a new branch directly from **GitHub’s interface**.  
- Name it according to the feature or purpose.

---

### **Task 8: Branch Creation and Push Using Git Bash**
- Create and push branches via command line:
  ```bash
  git branch <branch-name>
  git checkout <branch-name>
  git push -u origin <branch-name>
  ```

---

### **Task 9: Branching & Merging**
- Switch between branches and merge changes:
  ```bash
  git checkout main
  git merge <branch-name>
  ```

---

### **Task 10: Pull Request and Branch Review (GitHub GUI)**
- Open a **Pull Request (PR)** from the feature branch.  
- Request review and merge after approval.

---

### **Task 11: Detailed Branch Strategy (Develop/Staging)**
- Implement multi-environment branches:
  - **develop:** for ongoing development  
  - **staging:** for testing before production  
  - **main:** stable production-ready branch  

---

### **Bonus Task: Simulated Team Collaboration**
- Simulate collaboration by:
  - Creating separate branches for each team member.  
  - Performing merges and resolving conflicts.

---

### **Task 12: Code Review Workflow**
- Review pull requests and comment on changes.  
- Approve, suggest modifications, or request updates.

---

### **Task 13: Branch Cleanup Best Practices**
- Delete merged branches to keep repository clean:
  ```bash
  git branch -d <branch-name>
  git push origin --delete <branch-name>
  ```

---

## 🧠 Exam Evaluation Topics
1. **Advanced Branching & Merge Verification**  
   Understanding and testing complex branching scenarios.

2. **Multi-Stage Workflow Simulation**  
   Practical use of multiple environments (develop, staging, main).

3. **Collaboration & Conflict Resolution**  
   Handling simultaneous edits and merge conflicts.

---

## 🏁 Conclusion
This lab provides a complete understanding of **Git and GitHub workflows**, including SSH setup, branching strategies, merging, pull requests, and collaboration—essential skills for real-world cloud and software development projects.

---
