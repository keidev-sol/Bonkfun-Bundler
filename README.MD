# 🐶 Bonk.fun Multi-Wallet Bundle Trading Bot
##
---

## 🚀 Features
- Dynamic multi-wallet bundling (2 → 50+ wallets)
- Atomic one-block execution for token creation + buys
- Jito relayer integration with MEV protection
- Raydium SDK v2 swap execution
- Priority compute unit pricing for faster confirmations
- Modular and scalable codebase
---

## 📸 Sample Bundles (Jito Explorer)
| Wallets | Example |
| ------: | :------ |
| 2 | [🔗 View](https://explorer.jito.wtf/bundle/56ac378f193c9b90a4b6d2c52096a2d783653f300c343d59976691b2a6fcb184) |
| 9 | [🔗 View](https://explorer.jito.wtf/bundle/8116172ad6bea279b6873020ac412eb36c9777b311b96ab38c58204637166bf1) |
| 12 | [🔗 View](https://explorer.jito.wtf/bundle/eb6d075d4f3e065d5e127ec76c328e00e08d3608ee858a15fa13a21c8f922d98) |
---

## ⚙️ How It Works
1. Create token (BONK-style)
2. Prepare swap transactions across multiple wallets
3. Bundle into a single atomic block
4. Submit via Jito relayer
5. Confirm all-or-nothing execution
---

## ⚙️ Configuration
Set these variables in your `.env` file:

`PRIVATE_KEY, RPC_ENDPOINT, TOKEN_NAME, TOKEN_SYMBOL, DESCRIPTION, TOKEN_SHOW_NAME, TOKEN_CREATE_ON, TWITTER, TELEGRAM, WEBSITE, FILE, VANITY_MODE, SWAP_AMOUNT, DISTRIBUTION_WALLETNUM, JITO_FEE, BUYER_WALLET, BUYER_AMOUNT`

➡️ See `constants/constants.ts` for the full list and details.
---

## 🛠️ Scripts & Usage
| Action | Yarn Command | npm Command | Description |
| ------ | ------------ | ----------- | ----------- |
| Start main process | `yarn start` | `npm run start` | Token creation, distribution, automation |
| Gather & close wallets | `yarn gather` | `npm run gather` | Collect funds, close wallets |
| Close LUTs | `yarn close` | `npm run close` | Close address lookup tables |
| Check status | `yarn status` | `npm run status` | Wallet & transaction status |
---

## 🗂️ Project Structure
- **index.ts** — Main entry (token creation, distribution, automation)  
- **src/** — Core logic & utilities  
- **gather.ts** — Gather/close wallets  
- **closeLut.ts** — Close LUTs  
- **status.ts** — Status checks  
- **constants/** — Environment & constants  
- **executor/** — Transaction execution (Jito/legacy)  
- **utils/** — Helper functions  

---


## ⚡ Performance Tuning
```ts
ComputeBudgetProgram.setComputeUnitPrice({
  microLamports: 200_000, // High priority
});

---

## 📬 Contact  
For **MEV bot consulting, custom strategy development, or private collaboration**, feel free to connect.  

- **Telegram** → [@Kei Novak](https://t.me/Kei4650)
- **X (Twitter)** → [@Kei Novak](https://x.com/kei_4650)  

---