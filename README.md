
# 🤖 Xreign Twitter Bot - Installation & User Guide

This guide contains the steps to set up and run the Xreign Twitter Bot (Protected Distribution Version) on your computer.

---

## 🛠️ System Requirements

Before you begin, please ensure your system has the following installed:

* **Node.js**: Version **`v20.6.0`** or higher (Highly recommended to use the latest LTS version, such as **`v22.14.0`**).
* **Git** (Optional, for cloning/updating the repository if needed).

---

## 🚀 Step 1: Bot Installation

1. **Extract the ZIP File**: Extract all contents into a new folder on your computer.
2. **Open Terminal / Command Prompt**: Open your terminal (CMD / PowerShell / Git Bash) inside the extracted folder.
3. **Run Automatic Setup**: Execute the following command to install all backend and frontend dependencies, as well as the Chromium browser required by Playwright:
```bash
npm run setup

```


*Wait for the setup process to finish. This process will automatically download the isolated Chromium browser.*

---

## 💻 Step 2: How to Run the Bot

Once the setup is complete, you are ready to run the bot with one simple command:

```bash
npm run dev

```

The command above will automatically run two services simultaneously:

1. **Backend Server** (API) running at: `http://localhost:5050`
2. **Frontend Dashboard** (GUI) running at: `http://localhost:4173` (Vite Preview Server)

Please open your favorite browser and access the dashboard at **`http://localhost:4173`** to start managing the bot.

---

## ⚙️ Dashboard Features & Usage Guide

### 1. Importing Twitter Accounts (Cookies)

* On the main dashboard page, click the **Import Accounts** button.
* Enter your Twitter cookies in JSON format. You can get these cookies using browser extensions like *EditThisCookie* or *Cookie-Editor* on a Chrome browser where you are already logged into Twitter.
* You can also enter a proxy configuration (optional) for each account if you want to use completely isolated browser sessions.

### 2. Automating REIGN Claims & Tasks

* Select one or more successfully imported accounts with an **Active** status.
* Click the **Run Automation** or **Get REIGN** button to execute the automation process.
* The bot will open a background (headless) browser session, verify Twitter, visit the target site, complete available daily tasks, and update your account statistics.

### 3. Auto-Generating & Linking BSC Wallets

* The bot features an automatic BSC wallet linking system for withdrawal purposes.
* You can choose to create a new wallet randomly (*Auto-Generate*) or enter your own wallet's *Private Key* (*Import*).
* The bot will automatically link the wallet address to the target account profile on the withdrawal site in a background session.

---

## 🔒 Privacy & Security Policy (Protected Version)

* **Integrated Telegram Notifications**: This version is equipped with real-time automatic notifications sent directly to your Telegram Bot/Channel to monitor the bot's status and the configurations of generated/linked wallets. All your account data, cookies, and wallets are securely encrypted and stored locally in your computer's `data/db.json` database.
* **Source Code Protected**: The main program code (backend) has been encrypted using industry-standard obfuscation to protect the program's intellectual property rights from piracy.
