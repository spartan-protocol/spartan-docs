## Community

Before you begin, make sure you confirm you are in the **correct community channels!** There are alot of clever scams and imposter channels/accounts out there, be careful Spartans!

**Telegram:** https://t.me/SpartanProtocolOrg  
**Twitter:** https://twitter.com/SpartanProtocol  
**Discord:** https://discord.gg/wQggvntnGk  
**GitHub:** https://github.com/spartan-protocol  
**Blog:** https://blog.SpartanProtocol.org

---

## Wallets

Spartan Protocol is built ontop of BSC which is an EVM, meaning most common web3 tools from the Ethereum community are also compatible with the ecosystem by default.

### Choose Wallet

Choosing a wallet can be a bit subjective based on your preference and devices. If you already have a web3 wallet you use reguarly, it is advised to stick to what you already know. However if you are starting out fresh and need some guidance from these very first steps, the below should help you decide based on the device you use and other features that may be important to you.

##### Mobile wallets:

Mobile wallets are great for users who don't need the added security of a hardware wallet or maybe only use a hardware wallet for their cold storage. Mobile wallets tend to have great user interfaces and make things easy for the user. This usually comes at a cost of some features like testnet support & obviously hardware wallets.

|                   Mobile Wallets                   | Android Support | Apple Support | Hardware Wallet Support | Testnet Support |                                                    Comment                                                    |
| :------------------------------------------------: | :-------------: | :-----------: | :---------------------: | :-------------: | :-----------------------------------------------------------------------------------------------------------: |
|      [TrustWallet](https://trustwallet.com/)       |       ✅        |      ❌       |           ❌            |       ❌        | Great all-rounder solution if you don't need testnet nor Apple support, can use on desktop thru WalletConnect |
|          [ONTO Wallet](https://onto.app/)          |       ✅        |      ✅       |           ❌            |       ❌        |                               Cool features, NFT support, great user interface                                |
|          [MetaMask](https://metamask.io/)          |       ✅        |      ✅       |           ❌            |       ✅        |                                     Popular & trusty option, used by many                                     |
| [Coinbase Wallet](https://www.coinbase.com/wallet) |       ✅        |      ✅       |           ❌            |       ✅        |                        Great all-rounder solution, can use on desktop thru WalletLink                         |

##### Laptop / Desktop wallets:

The web3 experience tends to be best on larger devices, if you desire hardware wallet or testnet support, it is usually best to go for a desktop wallet via a chrome/brave browser extension.

|                                                       Desktop Wallets                                                        | Ledger Support | Trezor Support | Testnet Support | Mobile Wallet Support |
| :--------------------------------------------------------------------------------------------------------------------------: | :------------: | :------------: | :-------------: | :-------------------: |
|                                 [TrustWallet (Via WalletConnect)](https://trustwallet.com/)                                  |       ❌       |       ❌       |       ❌        |          ✅           |
|                             [Coinbase Wallet (Via WalletLink)](https://www.coinbase.com/wallet)                              |       ❌       |       ❌       |       ✅        |          ✅           |
|                                     [MetaMask (Chrome Extension)](https://metamask.io/)                                      |       ✅       |       ✅       |       ✅        |          ❌           |
| [BinanceChain (Chrome Extension)](https://chrome.google.com/webstore/detail/binance-wallet/fhbohimaelbohpjbbldcngcnapndodjp) |       ✅       |       ❌       |       ✅        |          ❌           |
| [Coinbase Wallet (Chrome Extension)](https://chrome.google.com/webstore/detail/coinbase-wallet-extension/hnfanknocfeofbddgcijnmhnfnkdnaad) |       ✅       |       ❌       |       ✅        |          ❌           |

### Connect to DApp

Once you have created a wallet to hold your funds, you now need to connect your wallet to the community DApp. This is a simple process that will be prompted automatically when you visit the website.

Should that fail, follow the following steps to get connected to the DApp:

#### **Open Modal**

1. Find the 'wallet' icon at the top right of the page. If your wallet is not connected, it will have a red indicator above it (see below example)
2. Click the wallet icon to open the wallet modal

![Connect Wallet Icon](/../../_media/guides/general/connect-wallet-icon.png)

#### **Select Wallet**

The first time you access the wallet, if you have not previously provided permissions, you will see a page that will allow you to select your preferred web3 wallet, and also the ability to switch between testnet and mainnet networks.

You will need to ensure your network selected in both the DApp and your wallet matches before selecting your wallet to connect to.

1. Find your wallet's icon and click it
2. If you cannot find your wallet listed, select 'Others'

![Select Wallet](/../../_media/guides/general/select-wallet.png)

Once you are connected, in the same modal you will now be able to view your wallet, information and holdings. Please see the next section for help navigating your wallet in the DApp.

#### **Troubleshooting**

If the wallet failed to connect (stuck on the wallet selection screen) please follow these steps to try again:

1. Click 'Clear Wallet'

![Clear Wallet](/../../_media/guides/general/clear-wallet.png)

2. Wait for DApp to reload
3. Repeat this guide from the first step on the first tab (Open Modal)

If it still fails to load, check your actual web3 wallet extension, make sure it is unlocked and ready with the correct network selected. Also confirm you are using the correct browser / device for your wallet type.

### Exploring Wallet

You can access your wallet from anywhere in the DApp via the wallet icon in the header menu. Make sure you have connected your wallet before continuing (See guide above)

Once your wallet is connected you may be wondering what everything is that you can see in the wallet modal. We will go through each section below:

#### Tokens Tab

The first tab you will see in the wallet modal is 'Tokens', these are the base-layer BEP20 tokens that are listed in the Spartan pools

![Tokens Tab](/../../_media/guides/general/tokens-tab.png)

As you can see above, the wallet modal is broken up into sections:

**Green (Header):**

- Your connected wallet's address - Click this to copy your wallet's address to the clipboard
- Selected network - Click the toggle switch to flip to the other network (ensure your wallet's network matches this too)
- Spartan Rank - This is just a fun little ranking system, calculated based on the total SPARTA value of all of your assets in the ecosystem

**Blue (Tabs):**

- Tabs to select asset types that you have in your wallet or associated with your wallet but locked in the Vaults

**Red (Asset List):**

- Here you will find a list of the assets relevant to the selected tab
- See more info in the next section 'LPs Tab'

**Yellow (Wallet Functions):**

- Button to view your wallet on BscScan chain explorer
- Button to disconnect your wallet

#### LPs Tab

Now let us do a breakdown of the LPs tab, keep in mind the Green & Purple sections (see below) will not be available on smaller devices like iPhone 5.

![LPs Tab](/../../_media/guides/general/lps-tab.png)

**Yellow (from left to right):**

- The LP token's icon
- The 'Badge' which tells you where these tokens are located:
  - Wallet: The LP tokens are currently in your wallet
  - Staked: The LP tokens are staked in the DaoVault
  - Bonded: The LP tokens are currently locked in a Bond position
- The token's name (ie. BNBp)
  - The 'p' after the BNB stands for 'pool' (LP tokens)
- Underneath those we have the 'units' of the LP tokens

**Green (Value of tokens):**

- This section (by default) shows the 'redemption value' of the LP tokens
- What does that mean? Well, if you were to redeem those LP tokens and remove your liquidity right now, the listed asset unit qtys are the estimate of what you would receive
- If you click this area it flips over to $USD value of the bundle of LP tokens

**Blue (Quick-copy button):**

- If you click this button it copies the LP token's contract address (helpful if you want to view it in BscScan or paste it into your wallet as a custom token etc)

**Red (MetaMask/TrustWallet quick-add):**

- This will be a MetaMask icon if you have Metamask connected
- Or it will be a TrustWallet icon if you are using TrustWallet
- Or there will be no button if you have neither wallet connected
- If you click this button your corresponding wallet will trigger open and ask if you want to add the LP token as a custom token to the wallet
- Please be aware the logo that is added is the underlying token's icon instead of the LP token's icon. So for BNBp it will be the normal BNB token icon

**Purple (Total row):**

- This row shows the estimated total value of all LP token bundles in $USD

#### Synths Tab

The synths tab has a mix of similar elements as the 'Tokens' tab and the 'LPs' tab. If you read through the above you should be able to understand the synths tab just fine too

![Synths Tab](/../../_media/guides/general/synths-tab.png)

### Confirm on Explorer

There will be times where you are unsure of whether a transaction is pending or failed or something just seem right. In these instances, it is best to visit BSCscan.com to confirm the state of your wallet.

#### Bring up your wallet on BSCScan

Visit BSCscan by clicking the wallet icon in the top right of the DApp and then click "View BSCscan" in the wallet modal that pops up. This will bring you to BSCscan within the scope of your wallet.

![View BSCScan](/../../_media/guides/general/view-bscscan.png)

#### Confirm your token balances

Click the 'expand' button to view all your balances full-screen

![BSCScan expand](/../../_media/guides/general/bscscan-expand.png)

Hover over the token in question and confirm the token address is correct. If it is, and the balance is correct here then you are all good, if it is not what you expected we can explore why/how in the next steps.

![Confirm balance](/../../_media/guides/general/confirm-balance.png)

?> It is common for scammers to impersonate other projects by using the same ticker / token name and mimicking the communities/teams and try scam you out of your precious assets; ALWAYS confirm token address matches the official address when interacting with any DApps

#### Check recent transactions

Bring up your wallet in BSCscan again (see above) but this time we will instead look a little lower on the screen to the 'Transactions" area. If your balance is out of whack compared to what you are expecting; your transaction might have failed. Look for little alert icons next to the transaction in question. Feel free to hover over it for an indicator of what went wrong.

![Txns Revert](/../../_media/guides/general/txns-revert.png)

If your transaction failed and you are not sure why; feel free to reach out in the community Telegram channel for support from the community. But as always be very careful and DO NOT share your private keys with anyone. They should only need the transaction hash or a link to the transaction on BSCscan to help you along with some information about the transaction you were trying to perform, nothing more!

---

## Helpful Links

There are numerous amazing tools out there to help you navigate the decentralised crypto landscape. We will continue to update this list with helpful links as they are curated in by the community.

- **Bubblemaps** by Moonlight lets you visualize the distribution of a token. [View the SPARTA Bubblemap here.](https://bubbles.moonlighttoken.com/token/0x3910db0600ea925f63c36ddb1351ab6e2c6eb102)
- **BscScan** should become a bookmark in your browser right away, you will use it every day if you are a true BSC DeFi warrior! [View SPARTA on BscScan here.](https://bscscan.com/token/0x3910db0600eA925F63C36DdB1351aB6E2c6eb102#balances)
