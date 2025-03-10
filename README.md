# Tading Bot

Stock Market Trading Bot

📌 Overview

This is a fully autonomous AI-powered trading bot that analyzes stock market data, executes trades using Alpaca API, and sends trade notifications via Twilio. The bot is designed to trade stocks from the S&P 500 and ASX 200 markets using machine learning, news sentiment analysis, and technical indicators.

🚀 Features

✅ Automated Trading - Executes buy/sell trades based on AI predictions.✅ Sentiment Analysis - Fetches financial news and determines sentiment impact.✅ Market Trend Analysis - Avoids trading in downtrending markets.✅ Dynamic Trade Allocation - Adjusts trade sizes based on volatility (VIX index).✅ Live & Paper Trading - Supports both real and simulated trading via Alpaca API.✅ Google Cloud Deployment - Runs 24/7 on Google Cloud VM.✅ Profit & Loss Tracking - Logs trades and tracks PnL over time.✅ SMS Alerts - Sends trade notifications using Twilio.

🔧 Installation & Setup

1️⃣ Clone the Repository

# Install Git if not already installed
sudo apt install git -y

# Clone this repository
git clone https://github.com/YOUR_GITHUB_USERNAME/YOUR_REPO_NAME.git
cd YOUR_REPO_NAME

2️⃣ Install Dependencies

pip3 install -r requirements.txt

3️⃣ Set Up API Keys (DO NOT SHARE THESE!)

Create a .env file to securely store your API keys:

touch .env
nano .env

Then, add the following keys:

ALPACA_API_KEY=your-alpaca-api-key
ALPACA_SECRET_KEY=your-alpaca-secret-key
NEWS_API_KEY=your-newsapi-key
TWILIO_ACCOUNT_SID=your-twilio-sid
TWILIO_AUTH_TOKEN=your-twilio-auth-token
TWILIO_PHONE_NUMBER=your-twilio-number
USER_PHONE_NUMBER=your-phone-number

Save the file (CTRL + X, then Y, then ENTER).

4️⃣ Run the Trading Bot

python3 your_script.py

This will start the bot in live trading mode. Ensure your Alpaca account is correctly set up.

📊 Running in Paper Trading Mode

If you want to test the bot without real money, set Alpaca to paper mode in .env:

BASE_URL=https://paper-api.alpaca.markets

Run the bot again:

python3 your_script.py

🚀 Deploying on Google Cloud (24/7 Trading)

1️⃣ Launch a Virtual Machine (VM) on Google Cloud

Go to Google Cloud Console and create a Compute Engine VM.

Choose Ubuntu 22.04 LTS as the operating system.

Use at least e2-standard-2 (2 vCPUs, 8GB RAM) for best performance.

2️⃣ Connect to Your VM

Once the VM is running, connect via SSH:

ssh your-user@your-vm-ip

3️⃣ Keep the Bot Running 24/7

To keep the bot running even after you close SSH, use screen:

sudo apt install screen -y
screen -S trading-bot
python3 your_script.py

Press CTRL + A + D to detach and keep the bot running in the background.

🛠️ Troubleshooting & Logs

Check Trade Logs

If something goes wrong, check the log file:

tail -f trade_log.txt

Reconnect to the Running Bot

If you used screen, reconnect with:

screen -r trading-bot

Stop the Bot

To stop the bot, use:

pkill -f your_script.py

⚠️ Important Disclaimers

Trading involves risks. Use this bot responsibly.

This bot does NOT guarantee profits. Market conditions change, and losses can occur.

Always test in paper trading mode before live trading.

📞 Support & Contact

For any issues or questions, open a GitHub issue or contact the repo owner. 🚀


