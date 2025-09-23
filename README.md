# 🐝 SWARM Role & Telegram Bot Set-Up Guide  

This guide explains how to install **Go**, set up a **Telegram bot**, and configure **GSwarm** to link your Gensyn node with Discord & Telegram.  

---

## 1️⃣ Install Go

### Linux / WSL
```bash
cd ~
wget https://go.dev/dl/go1.24.0.linux-amd64.tar.gz
sudo rm -rf /usr/local/go
sudo tar -C /usr/local -xzf go1.24.0.linux-amd64.tar.gz
echo 'export PATH=$PATH:/usr/local/go/bin' >> ~/.bashrc
echo 'export GOPATH=$HOME/go' >> ~/.bashrc
echo 'export PATH=$PATH:$GOPATH/bin' >> ~/.bashrc
source ~/.bashrc
go version


2️⃣ Telegram Bot Set-Up 🤖
(a) Create a Bot

Open 👉 @BotFather

Send /newbot and follow instructions

Copy your Bot Token (looks like: 123456:ABC-xyz...)

(b) Get Your Chat ID

Send a message to your bot

Open in browser:

https://api.telegram.org/botYOUR_BOT_TOKEN/getUpdates


(replace YOUR_BOT_TOKEN with your actual token)

Copy your Chat ID from the response ✅

⚠️ If result is empty ({"ok":true,"result":[]}), send another message to your bot and refresh.

3️⃣ Install & Configure GSwarm
Install
go install github.com/Deep-Commit/gswarm/cmd/gswarm@latest
gswarm --version

Configure
gswarm


Fill in:

Bot Token (from step 2a)

Chat ID (from step 2b)

EOA Address (from Gensyn Dashboard)

4️⃣ Link Discord & Telegram

In Gensyn Discord, go to #swarm-link

Run /link-telegram

Copy your verification code

In your Telegram bot, type:

/verify {code}


(replace {code} with the one from Discord)

✅ Once verified, you’ll automatically receive your SWARM Role 🎉

✅ Summary

Install Go

Create Telegram Bot & get Chat ID

Install & configure GSwarm with token, chat ID, and EOA

Link Discord + Telegram → get your SWARM Role


---

When you paste this into your `README.md` and commit → GitHub will automatically display **copy buttons** on all the `bash` and code snippets.  

👉 Do you want me to also prepare a **combined repo README** (with both BlockAssist + SWARM guides linked together)?


