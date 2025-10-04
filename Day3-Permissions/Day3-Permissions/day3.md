# 📘 Day 3 – Linux Basics: File Permissions & Ownership

## 🎯 Objective

Understand how Linux file permissions work and practice changing them using `chmod`, `chown`, and `chgrp`.

---

## 🖥 Commands Practiced

1. **`ls -l`** – View file permissions

   ```bash
   ls -l file1.txt
   ```

   ✅ Shows permissions, owner, group, file size, and timestamp.

---

2. **`chmod`** – Change file permissions

   * Grant read, write, and execute using numeric values:

     ```bash
     chmod 744 file1.txt
     ```

     ✅ Permissions: Owner = read/write/execute, Group = read, Others = read.

   * Add execute permission:

     ```bash
     chmod +x script.sh
     ```

---

3. **`chown`** – Change file ownership

   ```bash
   sudo chown user:group file1.txt
   ```

---

4. **`chgrp`** – Change group ownership

   ```bash
   sudo chgrp developers file1.txt
   ```

---

## 📂 Practice Example

```bash
mkdir Day3-Permissions
cd Day3-Permissions

# Create a file
touch file1.txt
ls -l file1.txt

# Change permissions
chmod 744 file1.txt
ls -l file1.txt

# Create and run a script
echo "echo Hello Linux" > script.sh
chmod +x script.sh
./script.sh
```

**Output:**

```
Hello Linux
```

---

## ✅ Learning Summary

* Learned how to read and interpret Linux file permissions.
* Practiced changing permissions with `chmod`.
* Understood how to change ownership using `chown` and `chgrp`.
* Created and executed a simple script with proper permissions.
