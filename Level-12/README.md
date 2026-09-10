# 🏴‍☠️ Bandit Level 12

> **Goal:** Convert a hexdump back to its original form and extract multiple layers of compressed and archived data to find the password for Level 13.

---

## 🛠️ Commands Summary

| Command | Description |
| :--- | :--- |
| `cd` | Navigate into a directory |
| `ls` | List directory contents (`-l` for long format, `-a` for hidden, `-h` for human-readable sizes) |
| `file` | Identify the file type/format |
| `tar` | Extract files from a TAR archive |
| `mv` | Rename or move files |
| `bzip2` | Decompress `.bz2` compressed files |
| `gzip` | Decompress `.gz` compressed files |

---

## 📋 Quick Walkthrough

### 1. Extract First Archive (TAR)
```bash
cd /tmp/tmp.sgxjhJL3oz
file data.tar
tar -xf data.tar
```

### 2. Decompress Second Archive (BZIP2)

Identify `data6.bin`, rename it with a `.bz2` extension so `bzip2` can process it, and decompress the file:

```bash
file data6.bin
# Output: data6.bin: bzip2 compressed data

mv data6.bin data6.bz2
bzip2 -d data6.bz2
file data6
# Output: data6: POSIX tar archive
```

### 3. Extract Third Archive (TAR)

Identify `data6`, verify its archive format, and extract its contents to uncover the next compression layer:

```bash
file data6
# Output: data6: POSIX tar archive (GNU)

tar -xf data6
ls -l
# Output: data8.bin
```

### 4. Decompress Final Archive (GZIP) & Read Password

Identify `data8.bin`, rename it with a `.gz` extension, decompress it using `gzip`, and output the contents:

```bash
file data8.bin
# Output: data8.bin: gzip compressed data

mv data8.bin data8.gz
gzip -d data8.gz

file data8
# Output: data8: ASCII text

cat data8
```

## 📸 Screenshot

<img width="931" height="982" alt="image" src="https://github.com/user-attachments/assets/51741154-2871-452b-bde9-ad36cbc8a433" />

## 💡 What I Learned

* **Hexdump Reversal (`xxd`)**: Learned how to convert raw hex dumps back into binary data using `xxd -r`.
* **Magic Numbers over Extensions (`file`)**: Discovered that Linux file extensions can be arbitrary or misleading; the `file` command checks internal "magic numbers" to accurately identify real file types.
* **Archive & Compression Formats**: Gained hands-on experience identifying and unpacking common Linux compression types:
  * **GZIP**: Decompressed using `gzip -d <filename.gz>`.
  * **BZIP2**: Decompressed using `bzip2 -d <filename.bz2>`.
  * **TAR**: Extracted using `tar -xf <filename>`.
* **Strict File Extension Requirements**: Learned that utilities like `gzip` and `bzip2` strictly require standard file extensions (`.gz`, `.bz2`) to run correctly, requiring `mv` to prepare files before decompression.
* **Temporary Workspaces (`/tmp`)**: Experienced working inside temporary system directories (`/tmp`) when working on write-restricted user environments.



