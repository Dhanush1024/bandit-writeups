# 🏴‍☠️ Bandit Level 4

> **Goal:** Find the only human-readable file among the files in `inhere`.

---

## 🔎 Commands Used

List the files:

```bash
ls -l
```

Move into the `inhere` directory:

```bash
cd inhere
```

List the files with details:

```bash
ls -l
```

There are several files named `-file00` to `-file09`.

I checked their contents using:

```bash
cat ./-file0*
```

Most of the files contained unreadable/binary data.

I then checked the readable file:

```bash
cat ./-file07
```

This displayed the password for **Level 5**.

---

## 📸 Screenshot

<img width="927" height="577" alt="image" src="https://github.com/user-attachments/assets/dab6f10f-879e-43d0-995e-478fcfaba040" />


---

## 💡 What I Learned

- 🔹 Using `ls -l` to inspect files
- 🔹 Working with filenames beginning with `-`
- 🔹 Using `./` to specify files
- 🔹 Identifying human-readable file contents
- 🔹 Using `*` as a wildcard

---

## ✅ Result

**Level 4 completed! 🎯**

Found the password required to access **Bandit Level 5**.
