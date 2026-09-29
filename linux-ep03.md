# Linux Terminal Series - Episode 3: Users, Groups & Permissions

Welcome to **Episode 3** of the *Linux Terminal Series*!

In this episode, you will learn how to manage users, configure groups, assign ownership, and control access permissions using octal notation. Mastering user and permission management is essential for securing Linux systems and managing multi-user environments in DevOps and System Administration.

---

## 🎯 Core Commands

| Command | Description | Common Flags / Options |
| :--- | :--- | :--- |
| `groupadd` | Create a new user group. | `sudo groupadd <groupname>` |
| `useradd` | Create a new system user. | `-m` (Create home directory)<br>`-s /bin/bash` (Set default shell) |
| `usermod` | Modify user account settings. | `-aG` (Append user to specified group) |
| `chown` | Change file or directory owner and group. | `chown owner:group <path>` |
| `chmod` | Change file read, write, and execute permissions. | `750` (Numeric/Octal mode) |

---

## 🧪 Quick Lab Setup

Run through this practical lab to create a group, set up a user account, create a project folder, and configure strict permissions:

```bash
# 1. Create group and user
sudo groupadd devs
sudo useradd -m -s /bin/bash aman
sudo passwd aman
sudo usermod -aG devs aman

# 2. Setup project file and ownership
sudo mkdir -p /project
sudo touch /project/code.sh
sudo chown aman:devs /project/code.sh

# 3. Set file permissions (rwxr-x---)
sudo chmod 750 /project/code.sh

# 4. Verify configuration
ls -l /project/code.sh
```

---

## 🔑 Octal Permission Breakdown (`chmod 750`)

* **`7` (Owner - `aman`):** `rwx` (Read, Write, Execute)
* **`5` (Group - `devs`):** `r-x` (Read, Execute)
* **`0` (Others):** `---` (No Access)

---

## 📚 Series Navigation

* [x] **Episode 1:** File Navigation Basics (`pwd`, `ls`, `cd`, `mkdir`, `clear`)
* [x] **Episode 2:** File Handling & Monitoring (`touch`, `nano`, `cat`, `less`, `head`, `tail`)
* [x] **Episode 3:** Users, Groups & Permissions *(Current)*
* [ ] **Episode 4:** System Monitoring *(Coming Up Next)*
  * `df -h` – Disk space usage
  * `du -sh` – Folder size breakdown
  * `free -h` – Memory/RAM usage
  * `uptime` – System load & runtime
  * `uname -a` – Kernel & OS details

---
*If you find this repository helpful, consider starring ⭐ the project!*