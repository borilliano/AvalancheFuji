
# AvalancheFuji

**Auto Avalanche Fuji Faucet Request**

## Overview

AvalancheFuji is a Python automation script that helps developers and testers automatically request AVAX testnet tokens from the [Chainlink Faucet](https://faucets.chain.link/) for the Avalanche Fuji testnet. This tool saves time and effort during smart contract development and testing on the Avalanche Fuji network.

## Features

- Automates the process of requesting AVAX testnet tokens.
- Uses browser automation to interact with the Chainlink Faucet.
- Simple and easy to use.

## Prerequisites

- Python 3.7 or higher
- [pip](https://pip.pypa.io/en/stable/)
- [pyppeteer](https://github.com/pyppeteer/pyppeteer) Python package

## Installation

Clone this repository:

```bash
git clone https://github.com/borilliano/AvalancheFuji.git
cd AvalancheFuji
```

Install dependencies:

```bash
pip install pyppeteer
```

## Usage

1. Open `ava,py` and replace `0xYourFujiWalletAddress` with your Avalanche Fuji testnet wallet address.
2. Run the script:

```bash
python ava,py
```

The script will launch a browser, navigate to the Chainlink Faucet, and attempt to request AVAX testnet tokens for your address.

## Notes

- **Wallet Connection:** This script does **not** automate connecting a wallet extension (like MetaMask). For full automation, consider Node.js with Puppeteer and dappeteer.
- **Selectors:** If the faucet website changes, you may need to update the selectors in `ava,py`.
- **Responsible Use:** Please use this tool responsibly and do not abuse public testnet faucets.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

