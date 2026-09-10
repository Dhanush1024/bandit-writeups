# 🏴‍☠️ Bandit Level 11

> **Goal:** Decode the ROT13-encoded text to find the password for Level 12.

---

## 🔎 Command Used

```bash
tr 'A-Za-z' 'N-ZA-Mn-za-m' < data.txt
```

### How it works

- `tr` → Translates characters from one set to another.
- `A-Za-z` → Selects uppercase and lowercase letters.
- `N-ZA-Mn-za-m` → Applies the ROT13 character mapping.
- `< data.txt` → Uses `data.txt` as the input.

The encoded text:

```text
Gur cnffjbeq vf ...
```

is decoded into:

```text
The password is ...
```

---

## 📸 Screenshot

<img width="697" height="150" alt="image" src="https://github.com/user-attachments/assets/affa9b07-e61d-4eaf-a43d-774e167d3e8a" />


---

## 💡 What I Learned

- 🔹 Understanding ROT13 encoding
- 🔹 Using `tr` for character translation
- 🔹 Redirecting file input using `<`
- 🔹 Decoding text from the Linux terminal

---

## ✅ Result

**Level 11 completed! 🎯**

Decoded the password required to access **Bandit Level 12**.
