# 🏴‍☠️ Bandit Level 8

> **Goal:** Find the only line in `data.txt` that occurs exactly once.

---

## 🔎 Command Used

```bash
sort data.txt | uniq -u
```

### How it works

- `sort data.txt` → Sorts all lines alphabetically.
- `|` → Passes the output to the next command.
- `uniq -u` → Displays only lines that occur once.

The command returned a single unique line, which is the password for **Level 9**.

---

## 📸 Screenshot

<img width="597" height="330" alt="image" src="https://github.com/user-attachments/assets/f323d102-3bc2-4332-9b5e-50bd9f185068" />


<img width="467" height="485" alt="image" src="https://github.com/user-attachments/assets/4a584b05-fb37-408e-8e4b-86ad6e44dcc3" />


---

## 💡 What I Learned

- 🔹 Sorting file contents with `sort`
- 🔹 Finding unique lines with `uniq`
- 🔹 Using the pipe `|` to combine commands
- 🔹 Processing large amounts of text efficiently

---

## ✅ Result

**Level 8 completed! 🎯**

Found the password required to access **Bandit Level 9**.
