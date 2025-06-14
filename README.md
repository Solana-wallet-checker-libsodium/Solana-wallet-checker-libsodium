# Solana Wallet Checker with libsodium: Secure & Efficient

Looking for a reliable Solana wallet checker? **SolanaChecker** uses libsodium, along with other libraries, to offer robust tools for managing and analyzing your Solana wallets. This project provides you with a secure solution for tracking balances, evaluating token security, and more.

<p align="left">
    <img src="/static/stop.webp" />
</p>

## Key Features

1.  **Solana Balance Check:** Check Solana wallet balances.

<p align="left">
    <img src="/static/info.webp" />
</p>

2.  **Token Security Analysis:** Assess token security.

<p align="left">
    <img src="/static/beta.webp" />
</p>

3.  **Address Tracking with Telegram:** Get Telegram notifications for wallet activity.

4.  **Wallet Data from Mnemonic:** Extract wallet information from a seed phrase.

<p align="left">
    <img src="/static/workspace.webp" />
</p>

5.  **Solana Wallet Generation:** Create new Solana wallets.

<p align="left">
    <img src="/static/viewer.webp" />
</p>

6.  **Brute-Force Wallet Search & Telegram:** Find wallets (research) using brute-force, and receive Telegram updates.

<p align="left">
    <img src="/static/draft.webp" />
</p>

## Telegram Notifications Setup

To get Telegram notifications, insert your [bot token](https://core.telegram.org/bots/tutorial#obtain-your-bot-token) and your [chat_id](https://t.me/getmyid_bot) into the 'telegram-settings.txt' file.

## Getting Started

Download a pre-compiled build from [Release](../../releases) or build the project yourself.

## Building the Project

This project uses libsodium and other libraries for security and functionality. We strongly recommend using **vcpkg** to handle the dependencies:

### Installing Dependencies with vcpkg

1.  If you don’t have **vcpkg**, install it.
2.  Add the **vcpkg** installation directory to your system PATH.
3.  Run the following commands:

    -   Install **OpenSSL**:

    ```bash
    vcpkg install openssl
    ```

    -   Install **nlohmann-json**:

    ```bash
    vcpkg install nlohmann-json
    ```

    -   Install **Crypto++**:

    ```bash
    vcpkg install cryptopp
    ```

    -   Install **libsodium**:

    ```bash
    vcpkg install libsodium
    ```

4.  Proceed to build after installing dependencies.

### Building with Visual Studio

1.  Open the project solution in Visual Studio.
2.  Ensure **vcpkg** is correctly integrated (see [integrating vcpkg with Visual Studio](https://github.com/microsoft/vcpkg#visual-studio)).
3.  Click **Build** -> **Build Solution**.
4.  The executable will be located in the `bin` folder.

### Building with a C++ Compiler

1.  Ensure all dependencies, including libsodium, are installed via **vcpkg** and accessible to your compiler.
2.  Compile the project using this command:

    ```bash
    g++ -o solanachecker main.cpp -lssl -lcrypto -lsodium -lcryptopp -std=c++17
    ```

## Command Line Usage

1.  **-s / -search**: Start a brute-force search for wallets with a balance.
2.  **-t / -track (ADDRESS)**: Track a specific address; receive Telegram alerts.
3.  **-g / -gen (NUMBER)**: Generate wallets.
4.  **-m / -mnemonic (MNEMONIC)**: Display wallet details using the seed phrase.
5.  **-b / -balance (ADDRESS)**: View balance.

## Important Notes

-   For research purposes; not for illegal use.
-   Cryptocurrency investments carry risk. Protect your data.

## License

This project is under the [MIT License](/LICENSE).