# 🏴‍☠️ Bandit Level 7

> **Goal:** Find the file owned by `bandit7`, belonging to group `bandit6`, and read its contents.

---

## 🔎 Commands Used

Search the filesystem:

```bash
find / -user bandit7 -group bandit6 -type f -size 33c
```

The search found:

```text
/var/lib/dpkg/info/bandit7.password
```

Read the file:

```bash
cat /var/lib/dpkg/info/bandit7.password
```

The output contains the password for **Level 7**.

---

## 📸 Screenshot

<img width="637" height="222" alt="image" src="https://github.com/user-attachments/assets/f90aa67f-bd4c-4da2-974d-9a060d2d83de" />


<img width="616" height="1002" alt="image" src="https://github.com/user-attachments/assets/a2ead56c-ae72-4fcb-8259-6351d6bccfe6" />


---

## 💡 What I Learned

- 🔹 Searching files using `find`
- 🔹 Filtering by user and group
- 🔹 Working with file permissions
- 🔹 Reading a specific file using `cat`

---

## ✅ Result

**Level 7 completed! 🎯**

Found the password required to access **Bandit Level 8**.
