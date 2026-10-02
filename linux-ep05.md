# Master Linux Service Management with `systemctl` (Nginx Edition)

Welcome to the hands-on code and command reference for the **Linux Service Management with `systemctl`** video tutorial. This guide demonstrates how to control, manage, and troubleshoot system services on Linux using **Nginx** as a practical example.

---

## 📌 Video Overview

In this tutorial, you will learn the full lifecycle of a Linux system service using `systemctl`. We cover everything from basic service checks and enabling services on boot to advanced operations like masking services to prevent accidental execution.

### Key Concepts Covered:
- Listing active system services
- Starting, stopping, and restarting services
- Checking active and enabled statuses programmatically
- Enabling services to automatically launch on boot
- Masking and unmasking units for maintenance/security

---

## 🛠️ Prerequisites

Before running these commands, ensure you have:
1. A Linux system running `systemd` (e.g., Ubuntu, Debian, CentOS, RHEL, Fedora).
2. `sudo` or root privileges.
3. **Nginx** installed on your machine (`sudo apt install nginx` or `sudo dnf install nginx`).

---

## 🚀 Command Cheat Sheet & Workflow

Follow along with the commands in order:

### Step 1: Inspect Loaded Services & Initial Status
List running system services and inspect the current status of Nginx:
```bash
# List all loaded active services
systemctl list-units --type=service

# Check detailed status of Nginx
systemctl status nginx
```

---

### Step 2: Start Service & Verify Status
Bring the Nginx web server online and check its runtime state:
```bash
# Start Nginx
sudo systemctl start nginx

# Quickly verify active status (Returns 'active' or 'inactive')
systemctl is-active nginx
```

---

### Step 3: Enable Service for Automatic Startup on Boot
Configure Nginx to launch automatically whenever the server boots up:
```bash
# Check if Nginx is configured to start on boot
systemctl is-enabled nginx

# Enable Nginx on system boot
sudo systemctl enable nginx

# Verify it is enabled
systemctl is-enabled nginx
```

---

### Step 4: Restart Service
Apply configuration updates or reload the service state:
```bash
# Restart Nginx
sudo systemctl restart nginx

# Verify it came back online cleanly
systemctl is-active nginx
```

---

### Step 5: Stop & Disable Service
Take Nginx offline and remove it from system startup:
```bash
# Stop Nginx service
sudo systemctl stop nginx

# Verify it is stopped
systemctl is-active nginx

# Disable automatic launch on boot
sudo systemctl disable nginx

# Verify it is disabled
systemctl is-enabled nginx
```

---

### Step 6: Service Masking (Advanced Lock)
Completely lock down a service so it cannot be started manually or by automated scripts:
```bash
# Mask Nginx (symlinks unit file to /dev/null)
sudo systemctl mask nginx

# Attempt to start (Will fail with an error)
sudo systemctl start nginx

# Lift the lock
sudo systemctl unmask nginx

# Start Nginx normally after unmasking
sudo systemctl start nginx

# Confirm service is active
systemctl is-active nginx
```

---

### Step 7: Review Command History
Review all executed commands during your terminal session:
```bash
history
```

---

## 📁 Repository Contents

- `README.md` - Command reference and setup instructions (this file).
- `script.txt` - Complete spoken script and visual directions for the video tutorial.

---

## 🤝 Contributing & Feedback

Feel free to open an issue or pull request if you'd like to suggest improvements or additional `systemctl` tips!su

# 1. Inspect loaded services & check Nginx status
systemctl list-units --type=service
systemctl status nginx

# 2. Start & check active state
sudo systemctl start nginx
systemctl is-active nginx

# 3. Check enabled state & enable on boot
systemctl is-enabled nginx
sudo systemctl enable nginx
systemctl is-enabled nginx

# 4. Apply changes (Restart)
sudo systemctl restart nginx
systemctl is-active nginx

# 5. Stop & Disable
sudo systemctl stop nginx
systemctl is-active nginx
sudo systemctl disable nginx
systemctl is-enabled nginx

# 6. Safety Lock (Masking & Unmasking)
sudo systemctl mask nginx
sudo systemctl start nginx   # (Fails gracefully)
sudo systemctl unmask nginx
sudo systemctl start nginx
systemctl is-active nginx

# 7. Session review
history