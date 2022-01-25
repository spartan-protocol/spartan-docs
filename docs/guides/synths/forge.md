## Forge Synths (Mint)

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

- This guide is for 'Forging Synths' so make sure the 'Forge Synths' tab is selected

![Select mode](/../../_media/guides/synths/mode-forge.png)

---

#### 3. Select your asset to sell

- Select which token you want to sell
- The token selected here will be 'sold' and 'swapped' for the Synth asset that you will choose in the next step

![Select input asset](/../../_media/guides/synths/mint-input.png)

---

#### 4. Select a Synth to receive

- You will now need to select which SynthYield asset you would like to receive

![Select output asset](/../../_media/guides/synths/mint-output.png)

---

#### 5. Input an amount

- Input the amount of the tokens you would like to sell
- The estimated output amount of the Synth token will be calculated for you
- You may click the 'MAX' button next to your balance to use the full amount, but be careful of slippage (always check the rate to make sure you aren't doing a bad trade)

![Mint input](/../../_media/guides/synths/mint-amount.png)

---

#### 6. Confirm Everything Before Continuing

- Confirm you have inputted and selected everything correctly
- You will need to enable a confirmation switch to continue. This is to ensure you realise that these Synth tokens do not go to your wallet; they go to the SynthVault & will be locked for some time before you can remove them to your wallet
- The DApp will estimate an output amount and also list the input amount; confirm they look correct before continuing

![Confirm output](/../../_media/guides/synths/mint-confirm.png)

---

#### 7. First-Time Approval

- If this is the first time interacting with the relevant underlying contract (or if the contracts have been upgraded recently) you will need to perform some token approvals before performing the actual transaction
- Approvals/Allowance changing is a standard ERC20 (or BEP20 in this instance) token contract feature that helps prevent accidentally interacting with bogus contracts; you should always confirm the contract you are interacting with is the correct one in a DApp
- It involves a simple on-chain txn that allows your wallet to send a specific amount of a specific token to a specific contract. The contract in this instance is the Spartan Protocol ROUTER contract which handles the routing of funds from the user to the pools and back again
- Click approve and confirm each on your wallet once you have verified this is correct

![Swap approve](/../../_media/guides/synths/mint-approve.png)

---

#### 8. Perform Forge Transaction

- After approval, the button for the actual transaction should now be visible
- This is a good time to do a final check and verify all the inputs look correct
- Click the 'Forge' button and confirm the transaction in your wallet

![Add both txn](/../../_media/guides/synths/forge-button.png)

---

#### 9. Verify Result

- Congratulations; you just forged some SynthYield tokens! Don't forget to harvest your yield in the SynthVault
- Once the transaction completes, feel free to click the wallet icon (top right of DApp) and click the 'Synths' tab to see your fresh Synth tokens in your wallet
- Guide here to: Explore your wallet and held LP tokens

![Wallet icon](/../../_media/guides/pools/wallet-icon.png)

---

#### 10. Troubleshooting

- If after 'approval' the red button shows up but is disabled or has a different label, please see these reasons:
  - **Check Wallet:** You have not yet connected your wallet to the DApp, follow this guide.
  - **Check Input:** One of your input amounts are not valid; it might be 0 or a negative number. Confirm and fix.
  - **Check BNB (Gas):** You do not have enough BNB in your wallet to cover the chain gas costs of this txn. Transfer some BNB into your wallet to continue. Also, confirm you have the intended wallet connected.
  - **Check Balance:** The input amount is higher than the balance in your wallet; go back and also confirm you have the intended wallet connected.
  - **Synths Disabled:** If the Synths features are not enabled, you will not be able to mint any Synths, visit the Telegram and catch up on the progress
  - **Synth At Capacity:** There are temporary caps/limits to how many synths can exist vs the pool's token depth. This is a dynamic calculation that adjusts every second so feel free to revisit later to try again, or reduce the size of your trade
  - **Pool At Capacity:** There are temporary caps/limits to how much liquidity can be added to each pool. If you would like a pool's caps raised please signal your support on social media using the #OpenTheGates hashtag & $SPARTA & $BNB (or whatever token/pool you are referring to)
  - **Confirm Lockup:** The Synths minted will be sent to the SynthVault & locked for a period of time; you need to confirm you realise this (see image in above steps)
  - **I am having some other issue:** Reach out on Telegram to help narrow down the issue and get you back on track!

---

[<- Back to Synth Guides](/synths?id=guides)
