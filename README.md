# SWARM-Role-TG-Bot-Set-Up-Guide


1️⃣ Install Go
Linux / WSL
cd ~
wget https://go.dev/dl/go1.24.0.linux-amd64.tar.gz
sudo rm -rf /usr/local/go
sudo tar -C /usr/local -xzf go1.24.0.linux-amd64.tar.gz
echo 'export PATH=$PATH:/usr/local/go/bin' >> ~/.bashrc
echo 'export GOPATH=$HOME/go' >> ~/.bashrc
echo 'export PATH=$PATH:$GOPATH/bin' >> ~/.bashrc
source ~/.bashrc
go version

Mac
brew install go

2️⃣ Telegram Bot Set-Up 🤖
(a) Create a Bot

Open 👉 @BotFather

Send /newbot → set name & username

Copy your Bot Token (looks like 1234567:ABC-XYZ...)

(b) Get Chat ID

Send a message to your bot

Visit:

https://api.telegram.org/botYOUR_BOT_TOKEN/getUpdates


Replace YOUR_BOT_TOKEN with your token

Find your chat ID in the result & save it ✅

⚠️ If empty → send a message to your bot first, then refresh

3️⃣ Install & Configure GSwarm
Install
go install github.com/Deep-Commit/gswarm/cmd/gswarm@latest
gswarm --version

Configure

Run:

gswarm


Fill in:

Bot Token (from step 2a)

Chat ID (from step 2b)

EOA Address (from Gensyn dashboard)

4️⃣ Link Discord & Telegram

In Gensyn Discord, go to #swarm-link
→ Run /link-telegram
→ Copy your verification code

In your Telegram bot, type:

/verify {code}


(replace {code} with the one from Discord)

✅ After verification → you’ll automatically get your SWARM Role 🎉
