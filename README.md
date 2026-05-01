# 🚀 PiLeaker Install Documentation

Simple and structured setup guide for running the Pi Bot with servers, workers, and PM2.

---

## 📌 Overview

This repository contains documentation for:

- ⚙️ Server setup  
- 🧠 Worker configuration  
- 🔄 PM2 process management  
- 🌐 Web dashboard usage  

---

## 📂 Full Documentation

👉 Detailed step-by-step guide is available here:

- **[View Full Installation Guide](./DOC.md)**

---

## ⚡ Quick Start

```bash
apt update
apt install python3.12-venv npm -y

python3 -m venv venv
source venv/bin/activate

npm install pm2 -g
```

---

## 🚀 Run Services

```bash
pm2 start app.py
```

Start workers manually:

```bash
pm2 start index.js --name worker-1 -- Worker1
```

Or using loop:

```bash
for i in {1..10}; do pm2 start index.js --name worker-$i -- Worker$i; done
```

---

## 🌐 Access Panel

Open in browser:

```
http://YOUR-IP:3000
```

---

## 📊 PM2 Commands

```bash
pm2 status
pm2 logs
pm2 restart all
pm2 stop all
pm2 delete all
```

---

## ⚠️ Important Notes

- Always set timezone on each device  
- Do NOT use:
  ```bash
  pm2 start worker-1 worker-2
  ```
- Use proper command with `index.js`  

---

## 🧠 Purpose

This repo is designed for:

- Learning system setup  
- Understanding worker-based architecture  
- Managing scalable processes with PM2  

---

## 👨‍💻 Author

**Sanjeev**

---

## ⭐ Support

If this helped you, consider giving a ⭐ to the repo.
