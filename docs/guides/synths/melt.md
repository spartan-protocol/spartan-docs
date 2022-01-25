## Melt Synths (Burn)

Before we begin here, it might help to first do some research on AMMs & the pools. For now, you can start with the information in our docs on our liquidity pools. Synths are quite complex behind the scenes and you may be interested in some of the technical details before proceeding to forge them, [please see the Synths info here.](/synths.md)

Also, make sure you have already created your wallet & connected it to the DApp. This guide assumes you have done the necessary steps to get setup including doing research on how these functions work.

#### 1. Synths page in the DApp

Visit the community DApp synth page: [https://dapp.spartanprotocol.org/synths](https://dapp.spartanprotocol.org/synths)

Or navigate to the synths page if you are already in the DApp:  
![Menu synths](/../../_media/guides/synths/menu.png)

- Open the menu
- Click 'Synths'

---

#### 2. Select synth mode

- This guide is for 'Melting Synths' so make sure the 'Melt Synths' tab is selected

![Select mode](/../../_media/guides/synths/mode-melt.png)

---

#### 3. Select your Synth to sell

- Select which Synth you want to sell
- The Synth selected here will be 'sold' and 'swapped' for the token that you will choose in the next step

![Select input asset](/../../_media/guides/synths/melt-input.png)

---

#### 4. Select a Token to receive

- You will now need to select which token you would like to receive

![Select output asset](/../../_media/guides/synths/melt-output.png)

---

#### 5. Input an amount

- Input the amount of the Synths you would like to sell
- The estimated output amount of the tokens will be calculated for you
- You may click the 'MAX' button next to your balance to use the full amount, but be careful of slippage (always check the rate to make sure you aren't doing a bad trade)

![Melt input](/../../_media/guides/synths/melt-amount.png)

---

#### 6. Confirm Everything Before Continuing

- Confirm you have inputted and selected everything correctly
- The DApp will estimate an output amount and also list the input amount; confirm they look correct before continuing

---

#### 7. First-Time Approval

- If this is the first time interacting with the relevant underlying contract (or if the contracts have been upgraded recently) you will need to perform some token approvals before performing the actual transaction
- Approvals/Allowance changing is a standard ERC20 (or BEP20 in this instance) token contract feature that helps prevent accidentally interacting with bogus contracts; you should always confirm the contract you are interacting with is the correct one in a DApp
- It involves a simple on-chain txn that allows your wallet to send a specific amount of a specific token to a specific contract. The contract in this instance is the Spartan Protocol ROUTER contract which handles the routing of funds from the user to the pools and back again
- Click approve and confirm each on your wallet once you have verified this is correct

![Swap approve](/../../_media/guides/synths/melt-approve.png)

---

#### 8. Perform Melt Transaction

- After approval, the button for the actual transaction should now be visible
- This is a good time to do a final check and verify all the inputs look correct
- Click the 'Melt' button and confirm the transaction in your wallet

![Add both txn](/../../_media/guides/synths/melt-button.png)

---

#### 9. Verify Result

- Congratulations, you just melted your SynthYield tokens!
- Once the transaction completes, feel free to click the wallet icon (top right of DApp) and click the 'Tokens' tab to see your fresh tokens in your wallet
- Guide here to: Explore your wallet and held LP tokens

![Wallet icon](/../../_media/guides/pools/wallet-icon.png)

---

#### 10. Troubleshooting

- If after 'approval' the red button shows up but is disabled or has a different label, please see these reasons:
  - **Check Wallet:** You have not yet connected your wallet to the DApp, follow this guide.
  - **Check Input:** One of your input amounts are not valid; it might be 0 or a negative number. Confirm and fix.
  - **Check BNB (Gas):** You do not have enough BNB in your wallet to cover the chain gas costs of this txn. Transfer some BNB into your wallet to continue. Also, confirm you have the intended wallet connected.
  - **Check Balance:** The input amount is higher than the balance in your wallet; go back and also confirm you have the intended wallet connected.
  - **I am having some other issue:** Reach out on Telegram to help narrow down the issue and get you back on track!

---

[<- Back to Synth Guides](/synths?id=guides)
