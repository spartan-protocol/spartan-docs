## Adding Liquidity Asymmetrically (Add Single)

Before we begin here; it is important you do your research on AMMs, liquidity pools and providing liquidity. For now, you can start with the [information in our docs on our liquidity pools](/liquidity-pools.md). It is also recommended to assess a pool before providing liquidity, [read about how to analyze pools here](/guides/pools/analyze.md).

Also, make sure you have already created your wallet and connected it to the DApp. This guide assumes you have done the necessary steps to get setup including doing research on how these functions work, important to make sure you know what 'adding liquidity' is and how it affects you. It is not to be confused with what is generally regarded as 'staking', they are vastly different things.

#### 1. Liquidity page in the DApp

Visit the community DApp liquidity page: https://dapp.spartanprotocol.org/liquidity

Or navigate to the liquidity page if you are already in the DApp:  
![Menu liquidity](/../../_media/guides/pools/menu-liquidity.png)

- Open the menu
- Click 'Liquidity'

This can also be acheived via the 'pools' / 'home' page by clicking 'Join' under the specific pool you want to assess:

![Pools join](/../../_media/guides/pools/pools-join.png)

---

#### 2. Select the 'Add Single' tab

If you are certain you want to add liquidity one-sided (add asymmetrically) then ensure you have that tab selected

![Add single tab](/../../_media/guides/pools/addsingle-tab.png)

---

#### 3. Select your assets to add

Select which asset you want to add as liquidity to the pool along with SPARTA

![Select asset](/../../_media/guides/pools/addsingle-select.png)

---

#### 4. Select/confirm the pool to add to

- If you selected SPARTA in the last step you will also have to select which pool you want to add the SPARTA to
- If you selected an asset other than SPARTA it is still a good idea to at least now confirm the auto-selected pool is correct and everything looks correct

![Select pool](/../../_media/guides/pools/addsingle-poolselect.png)

---

#### 5. Input an amount

- Input the amount of the selected asset you would like to add to the pool
- You may click the 'MAX' button next to your balance to use the full amount
- If you are adding BNB, be conscious of leaving some BNB behind for gas in future txns

![Add single input](/../../_media/guides/pools/addsingle-input.png)

---

#### 6. Confirm Everything Before Continuing

- Confirm you have inputted and selected everything correctly
- There may be a requirement to confirm a switch if the pool is new or some other similar situation
- The DApp will estimate an output amount and also list the two input amounts; confirm they look correct before continuing

![Add single confirm](/../../_media/guides/pools/addboth-confirm.png)

---

#### 7. First-Time Approval

- If this is the first time interacting with the relevant underlying contract (or if the contracts have been upgraded recently) you will need to perform some token approvals before performing the actual transaction
- Approvals/Allowance changing is a standard ERC20 (or BEP20 in this instance) token contract feature that helps prevent accidentally interacting with bogus contracts; you should always confirm the contract you are interacting with is the correct one in a DApp
- It involves a simple on-chain txn that allows your wallet to send a specific amount of a specific token to a specific contract. The contract in this instance is the Spartan Protocol ROUTER contract which handles the routing of funds from the user to the pools and back again
- Click approve and confirm each on your wallet once you have verified this is correct

![Add single approve](/../../_media/guides/pools/addboth-approve.png)

---

#### 8. Perform Liquidity-Add Transaction

- After approval, the button for the actual transaction should now be visible
- This is a good time to do a final check and verify all the inputs look correct
- Click the 'Add Single' button and confirm the transaction in your wallet

![Add single txn](/../../_media/guides/pools/addsingle-txn.png)

---

#### 9. Verify Result

- Congratulations! You just joined the pools!
- Once the transaction completes, feel free to click the wallet icon (top right of DApp) and click the 'LPs' tab to see your fresh new LP tokens in your wallet
- Guide here to: Explore your wallet and held LP tokens

![Wallet icon](/../../_media/guides/pools/wallet-icon.png)

---

#### 10. Troubleshooting

- If after 'approval' the red button shows up but is disabled or has a different label, please see these reasons:
  - **Check Wallet:** You have not yet connected your wallet to the DApp, follow this guide.
  - **Check Input:** One of your input amounts are not valid; it might be 0 or a negative number. Confirm and fix.
  - **Check BNB (Gas):** You do not have enough BNB in your wallet to cover the chain gas costs of this txn. Transfer some BNB into your wallet to continue. Also confirm you have the intended wallet connected.
  - **Check Balance:** One of your input amounts are higher than the balance in your wallet; go back to step 4 and also confirm you have the intended wallet connected.
  - **Slip Too High:** This is a feature to protect you from performing a liquidity-add with very high slippage. Check the pool depths and size of your liquidity add and consider adding a safer amount.
  - **Pool At Capacity:** There are temporary caps/limits to how much liquidity can be added to each pool. If you would like a pool's caps raised please signal your support on social media using the #OpenTheGates hashtag and $SPARTA and $BNB (or whatever token/pool you are referring to)
  - **Confirm Lockup:** The pool you are entering was created less than 7 days ago; you need to confirm you realise your liquidity will be locked in this pool until the pool is at least 7 days old (see image in step 5)
  - **Confirm Freeze:** The Curated pool you are adding liquidity to is currently outside its safe ratio. This means that liquidity cannot be removed from this pool. Consider whether you might need to remove your liquidity for an emergency but if you are happy to continue check the confirm button.
- I am having some other issue: No problem; reach out on Telegram to help narrow down the issue and get you back on track!

---

[<- Back to Liquidity Guides](/liquidity-pools?id=guides)
