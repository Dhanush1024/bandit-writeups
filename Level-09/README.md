# 🏴‍☠️ Bandit Level 9

> **Goal:** Find the password hidden among readable strings in `data.txt`.

---

## 🔎 Command Used

```bash
strings data.txt | grep "="
```

### How it works

- `strings data.txt` → Extracts readable text from the file.
- `|` → Sends the output to the next command.
- `grep "="` → Searches for lines containing `=`.

The output reveals the password for **Level 10**.

---

## 📸 Screenshot

<img width="502" height="236" alt="image" src="https://github.com/user-attachments/assets/509848be-0059-45ed-9149-148e43df946a" />


---

## 💡 What I Learned

- 🔹 Extracting readable text with `strings`
- 🔹 Searching text using `grep`
- 🔹 Combining commands with `|`
- 🔹 Finding useful information inside binary data

---

## ✅ Result

**Level 9 completed! 🎯**

Found the password required to access **Bandit Level 10**.
