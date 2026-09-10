# 🏴‍☠️ OverTheWire Bandit — Level 14

## 🎯 Level Goal

The goal of this level is to submit the password of the current level to a service running on **localhost port 30000**.

If the password is correct, the service returns the password for the next level. 🔐

## 💻 Commands Used

```bash
nc localhost 30000
```

## 📝 Steps

### 1. 📂 Check the current directory

```bash
ls
```

There were no visible files to use for this level.

### 2. 🌐 Connect to the service

I used Netcat (`nc`) to connect to port `30000` on the local machine:

```bash
nc localhost 30000
```

### 3. 🔑 Enter the current password

I entered the Bandit 14 password:

```text
aaWecNkG4FhxJQxz07uiwzVP6bJiYS65
```

The server responded:

```text
Correct!
pbLYuZtTg4MgaqfJx8jbA9gKKGqM68A7
```

Therefore, the password for **Bandit Level 15** is:

```text
pbLYuZtTg4MgaqfJx8jbA9gKKGqM68A7
```

## 💡 Key Concept

### 🔌 Netcat (`nc`)

Netcat is a networking utility that can create connections to services using a hostname/IP address and port.

The syntax used was:

```bash
nc <host> <port>
```

In this level:

```bash
nc localhost 30000
```

* `nc` → Netcat 🛠️
* `localhost` → the local machine 💻
* `30000` → the port where the service is running 🚪

## 🏆 Screen Shot

<img width="932" height="417" alt="image" src="https://github.com/user-attachments/assets/fc94d5c6-3eb3-4dd2-9010-9360b4b3b902" />


## 🏆 Result

Successfully obtained the password for **Bandit Level 15**. ✅

**🔐 Next Level Password:**

```text
pbLYuZtTg4MgaqfJx8jbA9gKKGqM68A7
```
