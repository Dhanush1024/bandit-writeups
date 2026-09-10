# 🏴‍☠️ Bandit Level 6

> **Goal:** Find a file owned by `bandit7`, belonging to group `bandit6`, with a size of 33 bytes.

---

## 🔎 Command Used

```bash
find / -user bandit7 -group bandit6 -type f -size 33c
```

### What it means

| Option | Meaning |
|---|---|
| `find /` | Search from the root directory |
| `-user bandit7` | File must be owned by `bandit7` |
| `-group bandit6` | File must belong to group `bandit6` |
| `-type f` | Search only for regular files |
| `-size 33c` | File must be exactly 33 bytes |

The search produced many **Permission denied** messages, but eventually found:

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

<img width="886" height="396" alt="88ee5f6c-5f8f-4f9c-96ba-b61ad6abaf1f" src="https://github.com/user-attachments/assets/e25d1bc1-e4a3-4264-b48f-32535b0a4bc0" />

<img width="827" height="857" alt="a9f8e3a4-ebd5-4b96-b3db-029c5aaf3c91" src="https://github.com/user-attachments/assets/e9f3c92d-7395-437b-9a94-a80fe90c0e63" />

<img width="622" height="661" alt="bcf20222-d6ad-446f-8f35-a31427af4c25" src="https://github.com/user-attachments/assets/9c478545-c5d1-4b88-a4a8-97f190ca7c73" />


---

## 💡 What I Learned

- 🔹 Searching the entire filesystem with `find`
- 🔹 Filtering files by owner and group
- 🔹 Filtering files by size and type
- 🔹 Understanding `Permission denied` messages

---

## ✅ Result

**Level 6 completed! 🎯**

Found the password required to access **Bandit Level 7**.
