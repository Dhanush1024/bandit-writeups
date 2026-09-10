# 🏴‍☠️ Bandit Level 5

> **Goal:** Find the file that is human-readable and has a size of 1033 bytes.

---

## 🔎 Commands Used

List the directories:

```bash
ls
```

Search for the required file:

```bash
find -readable -size 1033c
```

The command found:

```text
./maybehere07/./file2
```

Read the file:

```bash
cat maybehere07/./file2
```

The output contains the password for **Level 6**.

### 🔧 `find` Options

| Option | Meaning |
|---|---|
| `find` | Searches for files and directories |
| `-readable` | Finds files that can be read |
| `-size 1033c` | Finds files exactly 1033 bytes in size |
| `c` | Represents bytes |

---

## 📸 Screenshot

<img width="936" height="195" alt="image" src="https://github.com/user-attachments/assets/4fb362ec-4814-438c-9ca2-a1a35e386951" />


---

## 💡 What I Learned

- 🔹 Searching files with `find`
- 🔹 Checking file size
- 🔹 Finding readable files
- 🔹 Using `cat` to read the discovered file

---

## ✅ Result

**Level 5 completed! 🎯**

Found the password required to access **Bandit Level 6**.
