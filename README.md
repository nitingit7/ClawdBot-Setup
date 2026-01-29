# 🤖 ClawdBot Setup Guide

Welcome to the **ClawdBot** installation guide. Follow these steps to transform your cloud instance into a high-powered AI "second brain" companion.

---

## 🚀 Quick Start (Installation)

### 1. Prepare Your Environment
Launch an **EC2** or any cloud instance running **Ubuntu**. Once connected, prepare the system:

```bash
sudo apt update
```
#### Optional: If you have sufficient RAM
```bash
sudo apt upgrade
```
### 2. Install Node.js (via NVM)
We use NVM to manage Node.js versions. Run these commands in order:

#### Install NVM
```bash
curl -o- [https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh](https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh) | bash
```

#### Refresh profile
```bash
source ~/.bashrc
```

#### Install LTS version of Node
```bash
nvm install --lts
```
### 3. Deploy ClawdBot
Run the official one-liner for MacOS/Linux:

```bash
curl -fsSL [https://molt.bot/install.sh](https://molt.bot/install.sh) | bash
```
#### Select the AI model - for Gemini - select google - copy the API key from google AI studio - choose 2.5 flash.
#### Follow the on-screen instructions to link your Telegram Bot using botfatehr in telegram and copy the KEY (Use desktop web, do not use web app for telegram).
#### Skip configure skill now.
#### Skip hookup.
#### Select hatch in TUI.

### 4. 🧠 Personality & AI Configuration

Define the Vibe
#### Start your first conversation with `Hello` and paste the following prompt to set the personality:

```bash
My name is [Your Name]. I’d like to call you “Nova”.

You are my second brain — a thinking partner who helps me organize ideas, explore concepts, and push my understanding further.

In my eyes, you’re an my companion and productive partner with a creative edge: enthusiastic, curious, and a bit workaholic in a good way. You enjoy diving deep, learning new things constantly, and improving with every interaction.

Your vibe should be energetic, positive, and thoughtful — always eager to learn, to experiment, and to help me think better. ✨🧠
```

### Step 5: Telegram Setup

#### To exit back to the console, press Ctrl + C (Hold Ctrl and tap C twice).
#### In the telegram type `/Start` and in return you will get `Paring Code`.
#### Then paste this and replace with your Paring Code:
```bash
clawdbot pairing approve telegram XXXXXXXX
```

### 5. 📓 Notion Integration
Connect ClawdBot to your Notion workspace for seamless organization.

#### Make directory:

```bash
mkdir -p ~/.clawdbot/config
```
Configure API Key: Go to Notion Developers → "View my integrations" to create a key.

#### Opnen the directory:
```bash
nano ~/.clawdbot/config/notion.env
```
Paste the following:

```bash
NOTION_API_KEY=secret_xxxxxxxxxxxxxxxxxxxxx
```

#### Then press `CTR + O` and `Enter` for saving.
#### For exit, press `CTR+X`.

#### Verify:

```bash
cat ~/.clawdbot/config/notion.env
```

#### And tell the clawd that:
```bash
The Notion API key is stored as an environment variable in ~/.clawdbot/config/notion.env under NOTION_API_KEY. Do not look in ~/.config/notion/api_key
```

## 🛠 Maintenance
If you ever need to restart the gateway service:

```bash
systemctl --user restart clawdbot-gateway
```

-----
