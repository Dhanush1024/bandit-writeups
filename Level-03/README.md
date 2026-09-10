# 🏴‍☠️ Bandit Level 3

> **Goal:** Find the hidden file inside the `inhere` directory and read the password for Level 4.

---

## 🔎 Commands Used

First, list the directory:

```bash
ls -l
```

The output shows a directory named:

```text
inhere
```

Move into it:

```bash
cd inhere
```

Then list **all files**, including hidden files:

```bash
ls -al
```

This reveals the hidden file:

```text
...Hiding-From-You
```

Read the file:

```bash
cat ...Hiding-From-You
```

The output contains the password for Level 4.

---

## 📸 Screenshot

<img width="800" height="435" alt="image" src="https://github.com/user-attachments/assets/13273c8f-734a-47cf-8462-43b75c32f17c" />


---

## 💡 What I Learned

- 🔹 Using `cd` to navigate directories
- 🔹 Using `ls -al` to display hidden files
- 🔹 Understanding hidden files in Linux
- 🔹 Reading files using `cat`

---

## ✅ Result

**Level 3 completed! 🎯**

Found the password required to access **Bandit Level 4**.
