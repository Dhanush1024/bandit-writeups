# 🏴‍☠️ Bandit Level 0

> **Goal:** Connect to the Bandit server and find the password for Level 1.

---

## 🔐 SSH Connection

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

### What it means

| Part | Meaning |
|---|---|
| `ssh` | Secure remote connection |
| `bandit0` | Level 0 username |
| `bandit.labs.overthewire.org` | Bandit server |
| `-p 2220` | Connect using port 2220 |

---

## 🔎 Finding the Password

First, list the files:

```bash
ls
```

Output:

```text
readme
```

Then read the file:

```bash
cat readme
```

The file contains the **password for Level 1**.

---

## 📸 Screenshot

<img width="911" height="475" alt="image" src="https://github.com/user-attachments/assets/b69af594-2b46-41e4-b2fd-8e6fc1d5e04f" />.

<img width="940" height="232" alt="image" src="https://github.com/user-attachments/assets/6bf5e0c6-f552-4940-872a-fe989b385236" />


---

## 💡 What I Learned

- 🔹 Connecting to a remote server using **SSH**
- 🔹 Using `ls` to list files
- 🔹 Using `cat` to read files
- 🔹 Understanding SSH ports

---

## ✅ Result

**Level 0 completed! 🎯**

Found the password required to access **Bandit Level 1**.
