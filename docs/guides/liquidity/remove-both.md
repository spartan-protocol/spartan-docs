## Removing Liquidity Symmetrically (Both)

Before we begin here; it is important you do your research on AMMs, liquidity pools and providing liquidity. For now, you can start with the [information in our docs on our liquidity pools](/liquidity-pools.md). It is also recommended to assess a pool before providing liquidity, [read about how to analyse pools here](/guides/pools/analyze.md).

Also, make sure you have already created your wallet and connected it to the DApp. This guide assumes you have done the necessary steps to get setup including doing research on how these functions work.

#### 1. Liquidity page in the DApp

Visit the community DApp liquidity page: https://dapp.spartanprotocol.org/liquidity

Or navigate to the liquidity page if you are already in the DApp:  
![Menu liquidity](/../../_media/guides/pools/menu-liquidity.png)

- Open the menu
- Click 'Liquidity'

This can also be achieved via the 'pools' / 'home' page by clicking 'Join' under the specific pool you want to remove from:

![Pools join](/../../_media/guides/pools/pools-join.png)

---

#### 2. Select the 'Remove' tab

If you are sure you want to remove liquidity symmetrically, first select the 'Remove' tab up the top & then ensure the 'Remove Both' tab is selected

![Select asset](/../../_media/guides/pools/remboth-tab.png)
![Select asset](/../../_media/guides/pools/remboth-tab1.png)

---

#### 3. Select your LP tokens to redeem

Select which LP tokens you would like to redeem

![Select asset](/../../_media/guides/pools/remboth-asset.png)

---

#### 4. Input an amount

- Input the amount of the LP tokens you would like to redeem in the pool
- You may click the 'MAX' button next to your balance to use the full amount

![Remove both input](/../../_media/guides/pools/remboth-amount.png)

---

#### 5. Confirm Everything Before Continuing

- Confirm you have inputted and selected everything correctly
- The DApp will estimate an output amount and also list the two input amounts; confirm they look correct before continuing

![Remove both confirm](/../../_media/guides/pools/remboth-confirm.png)

---

#### 6. First-Time Approval

- If this is the first time interacting with the relevant underlying contract (or if the contracts have been upgraded recently) you will need to perform some token approvals before performing the actual transaction
- Approvals/Allowance changing is a standard ERC20 (or BEP20 in this instance) token contract feature that helps prevent accidentally interacting with bogus contracts; you should always confirm the contract you are interacting with is the correct one in a DApp
- It involves a simple on-chain txn that allows your wallet to send a specific amount of a specific token to a specific contract. The contract in this instance is the Spartan Protocol ROUTER contract which handles the routing of funds from the user to the pools and back again
- Click approve and confirm each on your wallet once you have verified this is correct

![Remove both approve](/../../_media/guides/pools/remove-approve.png)

---

#### 7. Perform Liquidity-Remove Transaction

- After approval, the button for the actual transaction should now be visible
- This is a good time to do a final check and verify all the inputs look correct
- Click the 'Remove Both' button and confirm the transaction in your wallet

![Add both txn](/../../_media/guides/pools/remboth-button.png)

---

#### 8. Verify Result

- Once the transaction completes, feel free to click the wallet icon (top right of DApp) and click the 'Tokens' tab to see your fresh tokens in your wallet
- Guide here to: Explore your wallet and held tokens

![Wallet icon](/../../_media/guides/pools/wallet-icon.png)

---

#### 8. Troubleshooting

- If after 'approval' the red button shows up but is disabled or has a different label, please see these reasons:
  - **Check Wallet:** You have not yet connected your wallet to the DApp, follow this guide.
  - **Check Input:** One of your input amounts are not valid; it might be 0 or a negative number. Confirm and fix.
  - **Pool Frozen:** The Curated pool you are trying to remove liquidity from is currently outside it's safe rates. You will need to wait for the pools to rebalance or for the safe ratio to adjust to a safe level.
  - **Check BNB (Gas):** You do not have enough BNB in your wallet to cover the chain gas costs of this txn. Transfer some BNB into your wallet to continue. Also confirm you have the intended wallet connected.
  - **Check Balance:** One of your input amounts are higher than the balance in your wallet; go back and also confirm you have the intended wallet connected.
  - **Unlocks In ##:** This pool is less than 7 days old, you will have to wait until it fully initialises before you can remove liquidity.
  - **I am having some other issue:** No problem; reach out on Telegram to help narrow down the issue and get you back on track!

---

[<- Back to Liquidity Guides](/liquidity-pools?id=guides)
