# 🏴‍☠️ Bandit Level 1

> **Goal:** Read a file whose name is `-` and find the password for Level 2.

---

## 🔎 Commands Used

```bash
ls -l
```

Lists the files with detailed information.

The output shows a file named:

```text
-
```

Since `-` is normally interpreted as an option, we specify the file using its path:

```bash
cat ./-
```

### Why `./-`?

- `./` means **current directory**
- `-` is the filename
- Together, `./-` tells Linux to read the file named `-`

---

## 📸 Screenshot

<img width="710" height="107" alt="image" src="https://github.com/user-attachments/assets/2db27309-bae6-40c7-bfe5-12acf082b39a" />


---

## 💡 What I Learned

- 🔹 Using `ls -l` to view detailed file information
- 🔹 Handling filenames beginning with `-`
- 🔹 Using `./` to specify a file in the current directory
- 🔹 Reading files with `cat`

---

## ✅ Result

**Level 1 completed! 🎯**

Found the password required to access **Bandit Level 2**.
