Perfect ✅ Tariq — here’s your **Day 7 Git Branching & Merging Documentation** file.
Save this as:
📄 `Day7-GitBranching/challenge.md`

---

# 🌿 Day 7 Challenge – Git Branching & Merging

## 🎯 **Objective**

Learn how to create, switch, and merge branches in Git to manage new features and collaborate efficiently.

---

## 📘 **Step 1: Open Your Git Project**

Navigate to your Git project directory:

```bash
cd Git-Challenge
```

---

## 📘 **Step 2: Create a New Branch**

Create a new branch for your feature:

```bash
git branch feature-update
```

List all branches:

```bash
git branch
```

✅ **Example Output:**

```
* main
  feature-update
```

---

## 📘 **Step 3: Switch to the New Branch**

```bash
git checkout feature-update
```

Now you are working inside the **feature-update** branch.

---

## 📘 **Step 4: Make and Commit Changes**

```bash
echo "New feature added in feature-update branch" >> project.txt
git add project.txt
git commit -m "Added new feature in feature-update branch"
```

---

## 📘 **Step 5: Switch Back to Main Branch**

```bash
git checkout main
```

Check the content of your file:

```bash
cat project.txt
```

➡ You won’t see the new feature line yet since it exists only on the feature branch.

---

## 📘 **Step 6: Merge Feature Branch into Main**

```bash
git merge feature-update
```

✅ **Example Output:**

```
Updating 4b2f1e3..c9d2b5f
Fast-forward
 project.txt | 1 +
 1 file changed, 1 insertion(+)
```

Now confirm the merge:

```bash
cat project.txt
```

✅ You’ll see the newly added feature text.

---

## 📘 **Step 7: Delete the Feature Branch**

After merging:

```bash
git branch -d feature-update
```

---

## 📘 **Step 8: Push the Updated Code to GitHub**

```bash
git push origin main
```

✅ Your GitHub repo is now updated with the merged content.

---

## 🧠 **Bonus Challenge – Handle Merge Conflicts**

1. Create another branch and modify the same line in `project.txt` in both branches.
2. When merging, you’ll get a conflict message.
3. Open the file showing conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`), fix manually, then run:

   ```bash
   git add project.txt
   git commit -m "Resolved merge conflict"
   git push
   ```

---

## 🧩 **Key Commands Summary**

| Command                  | Description                            |
| ------------------------ | -------------------------------------- |
| `git branch <name>`      | Create a new branch                    |
| `git checkout <branch>`  | Switch between branches                |
| `git merge <branch>`     | Merge a branch into the current branch |
| `git branch -d <branch>` | Delete a branch                        |
| `git push origin main`   | Push merged changes to GitHub          |

---

## ✅ **Day 7 Summary**

By completing this challenge, you have:

* Created and switched branches
* Merged feature branches into main
* Practiced conflict resolution
* Updated your GitHub repository
