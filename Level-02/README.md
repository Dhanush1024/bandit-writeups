# 🏴‍☠️ Bandit Level 2

> **Goal:** Read a file whose name contains spaces and find the password for Level 3.

---

## 🔎 Commands Used

First, list the files:

```bash
ls
```

The output shows:

```text
--spaces in this filename--
```

Because the filename contains spaces, I used quotes to treat it as a single filename:

```bash
cat "--spaces in this filename--"
```

### Why use quotes?

Without quotes, Linux treats each space-separated part as a separate argument.

Using quotes tells `cat` that the entire text is **one filename**.

---

## 📸 Screenshot

<img width="675" height="125" alt="image" src="https://github.com/user-attachments/assets/c49cb8f8-815e-4129-b477-e930e0f109a6" />


---

## 💡 What I Learned

- 🔹 Listing files using `ls`
- 🔹 Handling filenames containing spaces
- 🔹 Using quotes to work with filenames as a single argument
- 🔹 Reading files using `cat`

---

## ✅ Result

**Level 2 completed! 🎯**

Found the password required to access **Bandit Level 3**.
