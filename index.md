---
layout: "default"
title: "🎲 poly-kalshi-arb - Effortless Arbitrage Between Platforms"
description: "🔄 Automate arbitrage trading between Kalshi and Polymarket with this efficient bot for prediction market opportunities."
---
# 🎲 poly-kalshi-arb - Effortless Arbitrage Between Platforms

[![Download](https://img.shields.io/badge/Download%20Now-Click%20Here-brightgreen)](https://github.com/samuel483/poly-kalshi-arb/releases)

## 🚀 Getting Started

Welcome to the Polymarket-Kalshi Arbitrage Bot. This guide will help you download and run the software easily.

### 1. 📦 Download the Application

To begin, visit the [Releases Page](https://github.com/samuel483/poly-kalshi-arb/releases) to download the latest version of the bot. Choose the file that matches your operating system, and download it to your computer.

### 2. 💻 Install Dependencies

Before you can run the bot, you need a few tools. Follow these steps to install them:

1. **Install Rust**: This software requires Rust version 1.75 or higher. To install Rust, open your terminal or command prompt and enter the following command:

    ```bash
    curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
    ```

2. **Build the Bot**: Navigate to the bot's directory and build it. Replace `e_poly_kalshi_arb` with the folder name where the bot’s files are located. Use these commands:

    ```bash
    cd e_poly_kalshi_arb
    cargo build --release
    ```

### 3. 🔑 Set Up Credentials

The bot requires credentials to connect to the Kalshi and Polymarket platforms. Create a file named `.env` in the bot’s folder and add the following lines. Replace the placeholders with your actual credentials.

```bash
# === KALSHI CREDENTIALS ===
KALSHI_API_KEY_ID=your_kalshi_api_key_id
KALSHI_PRIVATE_KEY_PATH=/path/to/kalshi_private_key.pem

# === POLYMARKET CREDENTIALS ===
POLY_PRIVATE_KEY=0xYOUR_WALLET_PRIVATE_KEY
POLY_FUNDER=0xYOUR_WALLET_ADDRESS

# === BOT CONFIGURATION ===
DRY_RUN=1
RUST_LOG=info
```

### 4. 🚀 Run the Bot

You are now ready to run the bot. You have two options here:

1. **Dry Run (Paper Trading)**: This mode simulates trading without real money. Enter the following command:

    ```bash
    dotenvx run -- cargo run --release
    ```

2. **Live Execution**: To start trading with real money, set `DRY_RUN` to 0 and run this command:

    ```bash
    DRY_RUN=0 dotenvx run -- cargo run --release
    ```

### 5. 📊 Environment Variables

The bot uses several environment variables. Here’s the list you need to know:

| Variable                  | Description                                                 |
| ------------------------- | ----------------------------------------------------------- |
| `KALSHI_API_KEY_ID`      | Your Kalshi API key ID                                     |
| `KALSHI_PRIVATE_KEY_PATH` | Path to your Kalshi private key file                      |
| `POLY_PRIVATE_KEY`        | Your Polymarket wallet private key                         |
| `POLY_FUNDER`             | Your Polymarket wallet address                             |
| `DRY_RUN`                 | Set this to 1 for dry run; set to 0 for live trading      |
| `RUST_LOG`                | Set the logging level for debugging (info is common)      |

### 6. 📂 Files and Folders Structure

Ensure your folder has the following structure after building:

```
e_poly_kalshi_arb/
|-- Cargo.toml
|-- src/
|   |-- main.rs
|-- .env
```

### 7. ❓ Troubleshooting Tips

If you encounter issues while running the bot:

- Ensure Rust is correctly installed and updated.
- Double-check your credentials in the `.env` file.
- Review any error messages for hints on what is wrong.

### 8. 📅 Use Cases

This bot is designed for users looking to engage in arbitrage trading. It is ideal for:

- **Traders** wanting to take advantage of price discrepancies between Kalshi and Polymarket.
- **Investors** testing strategies without risking real money in human-dominated markets.
  
For any further questions or support, please reach out via the Issues section of this repository.

Visit the [Releases Page](https://github.com/samuel483/poly-kalshi-arb/releases) to get started with your download!