# 🔐 Advanced AES-256 Encryption Tool (Python + Tkinter)

A secure **AES-256 file & folder encryption/decryption tool** with both a **Graphical User Interface (GUI)** and **Command-Line Interface (CLI)**.  
It uses the **PBKDF2-HMAC-SHA256 key derivation** and **AES-GCM encryption** for strong, authenticated encryption.

---

## ✨ Features
- **AES-256 encryption** with a randomly generated salt and nonce for each file.
- **PBKDF2-HMAC-SHA256 key derivation** with 200,000 iterations.
- **Secure authentication** using AES-GCM mode (prevents tampering).
- **Encrypt/Decrypt single files**.
- **Encrypt/Decrypt entire folders** (non-recursive by default).
- **GUI Mode** (Tkinter) for ease of use.
- **CLI Mode** for advanced scripting/automation.
- **Cross-platform** (Windows, Linux, macOS).

---

## 📦 Requirements
- Python **3.7+**
- Required Python packages:
  ```bash
  pip install cryptography
  ```

---

## 🚀 Usage

### **1️⃣ GUI Mode**
Simply run:
```bash
python encryption_tool.py
```
A window will open allowing you to:
- Enter a password
- Select files or folders to encrypt/decrypt
- View status messages

---

### **2️⃣ CLI Mode**

#### **Encrypt a file**
```bash
python encryption_tool.py encrypt -f myfile.txt -p mypassword
```

#### **Decrypt a file**
```bash
python encryption_tool.py decrypt -f myfile.txt.enc -p mypassword
```

#### **Encrypt a folder (non-recursive)**
```bash
python encryption_tool.py encrypt -d myfolder -p mypassword
```

#### **Decrypt a folder**
```bash
python encryption_tool.py decrypt -d myfolder -p mypassword
```

---

## 📂 Output
- Encrypted files are saved with an `.enc` extension.
- Decrypted files are saved with a `.dec` extension.

Example:
```
myfile.txt → myfile.txt.enc → myfile.txt.dec
```

---

## ⚠️ Security Notes
- **Password is never stored** — it's used to derive the encryption key each time.
- If you forget your password, **your data cannot be recovered**.
- Always use a **strong password** (mix of upper/lowercase letters, numbers, symbols).
- AES-GCM provides both confidentiality & integrity — if the file is modified, decryption will fail.

---

## 🛠 Development
- GUI is built using **Tkinter**.
- Encryption is implemented using the [`cryptography`](https://cryptography.io/en/latest/) library.

---

## 📜 License
This project is released under the **MIT License**.

---

**Author:** Adhyan Raghav  
