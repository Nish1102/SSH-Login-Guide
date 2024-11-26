
# SSH Login Guide

This repository provides step-by-step instructions for configuring SSH login for the first time and testing the connection.

---

## **Steps to Configure and Test SSH Login**

### **1. Generate an SSH Key**
Run the following command to generate an SSH key:
```bash
ssh-keygen -t ed25519 -C "your.email@example.com"
```
- Replace `your.email@example.com` with your email address.
- The key pair will be saved in `~/.ssh/`.

### **2. Add the SSH Key to Your GitHub Account**
1. Copy the public key:
   ```bash
   cat ~/.ssh/id_ed25519.pub
   ```
2. Log in to your GitHub account.
3. Go to **Settings > SSH and GPG keys > New SSH key**.
4. Paste the key and save it.

### **3. Test the SSH Connection**
Run the following command to test the connection:
```bash
ssh -T git@github.com
```
You should see:
```
Hi <username>! You've successfully authenticated, but GitHub does not provide shell access.
```

### **4. Clone a Repository Using SSH**
Use the SSH URL to clone a repository:
```bash
git clone git@github.com:username/repository.git
```

---

## **First-Time Git Configuration**

### Set Global Username and Email:
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### Verify the Configuration:
```bash
git config --global --list
```

---
