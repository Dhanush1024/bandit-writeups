# 🏴‍☠️ Bandit Level 13 

> **Goal:** Connect to the next level using an SSH private key and retrieve the Bandit 14 password.

---

## 🛠️ Commands Summary

| Command | Description |
| :--- | :--- |
| `ssh-keygen` | Generates a new SSH key pair (public + private) |
| `chmod` | Modifies file permissions (critical for key security) |
| `ssh-copy-id` | Copies your public key to a remote server |
| `ssh -i` | Connects to a server using a specific private key |

---

## 📋 Step-by-Step Instructions

### 1. Generate an SSH Key Pair

Create a secure RSA or Ed25519 key pair on your local machine:

```bash
# Recommended: Modern Ed25519 key
ssh-keygen -t ed25519 -C "your_email@example.com"

# Alternative: Standard RSA key (4096-bit)
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

### 2. Set Critical File Permissions

The SSH client requires private keys to be strictly readable only by the owner. If permissions are too open, SSH will reject the key.

```bash
# Restrict private key permissions
chmod 600 ~/.ssh/id_ed25519

# (Optional) Ensure the .ssh directory itself is secure
chmod 700 ~/.ssh
```

### 3. Copy Public Key to Remote Server

To authenticate without a password, copy your **public key** (`.pub`) to the target server's `authorized_keys` file:

```bash
ssh-copy-id -i ~/.ssh/id_ed25519.pub user@remote_host
```

### 4. Connect Using the Private Key

Use the `-i` flag with `ssh` to specify your private key when connecting:

```bash
ssh -i ~/.ssh/id_ed25519 user@remote_host
```

## 🔎 Command Used

```bash
cat /etc/bandit_pass/bandit14
```
## ScreenShot

<img width="731" height="851" alt="image" src="https://github.com/user-attachments/assets/79a3d1bb-ce40-48aa-b027-bc95249b2cba" />


### How it works

* `cat` → Reads and displays file contents in the terminal.
* `/etc/bandit_pass/bandit14` → The file path storing the password for Bandit Level 14.
