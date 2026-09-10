# 🏴‍☠️ OverTheWire Bandit — Level 15

## 🎯 Level Goal

The goal of this level is to submit the password of the current level to a service running on **localhost port 30001** using **SSL/TLS encryption**.

If the password is correct, the service returns the password for the next level.

## 💻 Commands Used

```bash
openssl s_client -connect localhost:30001
```

## 📝 Steps

### 1. 🔐 Connect to the SSL service

I used `openssl s_client` to establish a secure SSL/TLS connection to port `30001` on the local machine:

```bash
openssl s_client -connect localhost:30001
```

The connection was successfully established:

```text
CONNECTED(00000003)
```

The server was using **TLS 1.3**:

```text
Protocol: TLSv1.3
Cipher    : TLS_AES_256_GCM_SHA384
```

The certificate was self-signed, which is expected for this challenge.

### 2. 🔑 Enter the current password

After the SSL connection was established, I entered the Bandit 15 password:

```text
pbLYuZtTg4MgaqfJx8jbA9gKKGqM68A7
```

The server responded:

```text
Correct!
kS0Hf0u5HiXFwKMKFqXvPdOTNGGa0X8V
```

Therefore, the password for **Bandit Level 16** is:

```text
kS0Hf0u5HiXFwKMKFqXvPdOTNGGa0X8V
```

## 💡 Key Concept

### 🔒 SSL/TLS with OpenSSL

`openssl s_client` is a command-line tool used to connect to SSL/TLS-enabled services and inspect secure connections.

The syntax used was:

```bash
openssl s_client -connect localhost:30001
```

* `openssl` → OpenSSL command-line toolkit 🛠️
* `s_client` → Creates an SSL/TLS client connection 🔐
* `-connect` → Specifies the server and port to connect to 🌐
* `localhost` → The local machine 💻
* `30001` → The port running the SSL/TLS service 🚪

### 🔍 Important Observation

The output showed:

```text
Verify return code: 18 (self-signed certificate)
```

This means the server certificate was **self-signed** rather than signed by a trusted Certificate Authority.

The connection itself was still successfully established using **TLS 1.3**.

## Screen Shot

<img width="837" height="1007" alt="image" src="https://github.com/user-attachments/assets/e34f80cd-1771-4fb5-b4bc-0bb06d4d5169" />


## 🏆 Result

Successfully obtained the password for **Bandit Level 16**. ✅


