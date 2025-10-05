# 📘 Day 4 – Linux Basics: Process Management

## 🎯 Objective

Learn how to view, manage, and control processes running in Linux using process-related commands.

---

## 🖥 Commands Practiced

### 1. **`ps`** – Show Active Processes

Displays currently running processes in the current terminal session.

```bash
ps
```

To list all processes on the system:

```bash
ps aux | less
```

---

### 2. **`top`** – Real-Time Process Monitoring

Shows a dynamic view of system performance (CPU, memory usage, running processes).

```bash
top
```

➡ Press `q` to quit the `top` command.

---

### 3. **`htop`** – Interactive Process Viewer (Optional)

A more advanced and user-friendly version of `top`.

```bash
sudo apt install htop -y
htop
```

---

### 4. **`kill`** – Terminate a Process

Use to stop a running process by its **PID (Process ID)**.

```bash
ps aux | grep sleep
kill <PID>
```

✅ Replaces `<PID>` with the process ID you want to stop.

---

### 5. **`jobs`, `bg`, `fg`** – Manage Background/Foreground Tasks

Run processes in the background and bring them back to the foreground.

```bash
sleep 100 &
jobs
fg %1
```

---

## 📂 Practice Example

```bash
mkdir Day4-ProcessManagement
cd Day4-ProcessManagement

# Create a simple process script
echo "sleep 100" > process.sh
chmod +x process.sh

# Run the script in the background
./process.sh &

# Check active processes
ps
jobs

# Terminate the process
ps aux | grep sleep
kill <PID>
```

**Expected Output Example:**

```bash
[1] 1234
$ ps
PID  TTY      TIME     CMD
1234 pts/0    0:00     sleep 100
```

After running `kill <PID>`, the process ends.

---

## ✅ Learning Summary

* Learned how to **view and monitor running processes** (`ps`, `top`, `htop`).
* Understood **background & foreground job control** (`jobs`, `bg`, `fg`).
* Practiced **terminating a process** safely using `kill`.
* Gained a deeper understanding of how Linux manages multitasking.

---

👉 **Next Step (Day 5): Git Basics — version control, commits, and repositories.**

---
