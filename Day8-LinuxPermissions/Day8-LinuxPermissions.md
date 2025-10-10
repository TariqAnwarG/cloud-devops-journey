📄 `Day8-LinuxPermissions/challenge.md`

---

# 🧠 Day 8 Challenge – Linux File Permissions & User Management

## 🎯 **Objective**

Master Linux commands to control file permissions, manage ownership, and handle user accounts.
These skills are crucial for system administration, DevOps, and cloud security roles.

---

## 📘 **Step 1: Create a Working Folder**

```bash
cd ~
mkdir linux-day8
cd linux-day8
```

---

## 📘 **Step 2: Create Sample Files**

```bash
touch permission_demo.txt
ls -l
```

✅ **Example Output:**

```
-rw-r--r-- 1 tariq tariq 0 Oct 5 15:30 permission_demo.txt
```

---

## 📘 **Step 3: Understand Permission Structure**

Example:
`-rw-r--r--`

| Section | Symbol | Description                  |
| ------- | ------ | ---------------------------- |
| Type    | `-`    | Regular file (d = directory) |
| Owner   | `rw-`  | Owner can read & write       |
| Group   | `r--`  | Group can read only          |
| Others  | `r--`  | Others can read only         |

---

## 📘 **Step 4: Change Permissions (chmod)**

### 1️⃣ Add execute permission for owner:

```bash
chmod u+x permission_demo.txt
```

### 2️⃣ Remove read permission for others:

```bash
chmod o-r permission_demo.txt
```

### 3️⃣ Check updated permissions:

```bash
ls -l
```

✅ **Output Example:**

```
-rwxr----- 1 tariq tariq 0 Oct 5 15:35 permission_demo.txt
```

---

## 📘 **Step 5: Change Ownership (chown)**

### 1️⃣ Create a test user:

```bash
sudo useradd testuser
sudo passwd testuser
```

### 2️⃣ Change file ownership:

```bash
sudo chown testuser:testuser permission_demo.txt
```

✅ Verify ownership:

```bash
ls -l
```

---

## 📘 **Step 6: User Management Commands**

| Command                   | Purpose                               |
| ------------------------- | ------------------------------------- |
| `sudo useradd <username>` | Add new user                          |
| `sudo passwd <username>`  | Set password for user                 |
| `sudo deluser <username>` | Delete user                           |
| `whoami`                  | Show current user                     |
| `su <username>`           | Switch to another user                |
| `groups`                  | Show current user's group memberships |

---

## 📘 **Step 7: Secure Folder with Restricted Access**

```bash
mkdir secure_folder
chmod 700 secure_folder
ls -ld secure_folder
```

✅ Only the **owner** can read, write, or execute inside the folder.

---

## 🧠 **Bonus Task – Create and Run a Script**

```bash
echo "echo 'Hello, Tariq! Linux permissions mastered!'" > hello.sh
chmod +x hello.sh
./hello.sh
```

✅ **Output:**

```
Hello, Tariq! Linux permissions mastered!
```

---

## ✅ **Day 8 Summary**

You learned how to:

* View and modify file permissions
* Change file and directory ownership
* Create and manage users
* Secure files using `chmod` and `chown`
* Execute shell scripts with custom permissions
