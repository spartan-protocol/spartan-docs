## Staking your Synths into the Synth Vault

Similar to many other protocols, emissions yield is granted to users who lock/stake their tokens.
Spartan Protocol allows users to stake their Synth tokens, such as BNBs or BUSDs, into the Vault, which can be accessed via the nav menu.

![Nav menu](/../../_media/guides/staking/dao-menu.png)

In preparation for staking, you will need to have some Synths, which can be obtained by [forging Synths](/guides/synths/forge). Only [Curated Pools](/liquidity-pools?id=curated-pools) are eligible for emissions yield.

![Overview](/../../_media/guides/staking/synth-overview.png)

---

## Synth Vault Details

![Details](/../../_media/guides/staking/synth-details.png)

In this screen, Spartans can see details about the SynthVault variables and weights.

- **'Min Time'** in the SynthVault, your Synth tokens (and any others of the same type already in the vault) will be locked for a dynamic amount of time (subject to change) but currently, this is set to 1 hour. During this time period, you will not be able to withdraw your Synth tokens from the vault
- **'Eras to Earn'** regulates the harvest claim amounts over a longer time period. This is 30 eras (days) by default and not likely to ever need changing
- **'Vault Claim'** regulates the percentage of the Reserve SPARTA balance that the harvest function will calculate off. The higher this percentage, the higher the SynthVault harvest rewards will be

We then have 'weight' related figures:

- **'Total Weight'** is the total amount of SPARTA value that is currently locked into the SynthVault. This is roughly half of the total spot SPARTA value of all staked Synth tokens
- **'Your Weight'** is the same thing but filtered down to your connected wallet's staked balances
- **'Percent Weight'** is an estimate of what percentage of the total SynthVault weight your wallet represents

Next, we have a 'Harvest All' button, but first some notes on Harvesting:

- Emissions yield is calculated dynamically
- This can be harvested at any time & is not necessarily 'accumulative' as it uses variables that are affected by other users when they add weight or harvest
- That means there are variables that could make your harvestable amount actually go down or up based on what you may have seen earlier
- Whilst the 'ideal' time to harvest is subjective and different person to person, ideally, you should be harvesting at least once per month. Some users harvest more often, like daily for instance
- You should assess the value of your harvest against the costs (gas) and convenience and find a suitable schedule that works for you to come check the DAO proposals and claim your regular harvest
- By default, your harvest will be paid out in the same Synth token and compound straight into the same vault (not your wallet)
- If the Synth is at its cap however, you will instead be paid out in SPARTA to your wallet
- If the pool is at its liquidity cap, you will not be able to harvest until the pool's caps are raised (#OpenTheGates)
- When you harvest, your SynthVault tokens will be locked for the same amount of time as depositing (currently 1 hour) so if you were looking to withdraw urgently, you might have to choose to forfeit your harvestable amount for that SynthVault item

#### Harvesting

You have options here, there is a 'Harvest All' button if you wish to save a little gas & time to harvest all available Synth items with a single singed transaction, or you may choose to harvest an individual item. Some possible reasons to harvest a single item are:

- Having issues with the 'Harvest All' button
- Intend to withdraw one of the items urgently (as explained above, harvesting will lockup your Synths for a period of time (currently 1 hour)
- If you would like to 'Harvest Single' instead of 'All' there is a guide on this a bit later in this page

#### How to Harvest All

- To harvest _all_ items, simply click 'Harvest All' and confirm the prompts in your wallet
- You will need to have some BNB in your wallet to cover the gas costs
- Remember, you will _not_ be able to withdraw any of these Synth items for a period of time after harvesting

![Harvest All](/../../_media/guides/staking/synth-harvest-all-button.png)

---

## Vault Item Details

![Item](/../../_media/guides/staking/synth-item.png)

The items that precede the 'details' tile are each 'Curated' Synth or if you previously deposited a no-longer-curated Synth it should show up here also. You can see:

- **'Balance'** of the respective Synth tokens held in your wallet
- **'Staked'** Synth tokens in the SynthVault attributable to your connected wallet
- **'Harvestable'** amount of tokens estimate to receive if you were to harvest now

#### How to Harvest Single

![Harvest Single](/../../_media/guides/staking/synth-harvest-single.png)

- Each SynthVault item is handled as its own sub-item so you may choose to (or need to if there is an issue with 'Harvest All') harvest an individual position.
- Look for the Curated SynthVault item that you want to harvest
- To harvest a single Synth item, simply click 'Harvest' and confirm the prompts in your wallet
- You will need to have some BNB in your wallet to cover the gas costs

#### How to Deposit

![Deposit](/../../_media/guides/staking/synth-deposit.png)

1. Ensure you hold the Synth tokens in your wallet before trying to deposit them
2. Look for the Curated SynthVault item that you want to deposit into
3. Click 'Deposit'
4. Drag the 'Amount' slider to the desired amount to deposit in the SynthVault
5. Confirm the lockout time period (The Synth tokens being deposited & any of the same type already in the SynthVault will be locked in the SynthVault for a period of time; cannot be withdrawn)
6. If you have not harvested recently; there will be another confirmation here to 'confirm harvest time reset' which means you know that your available harvest will be reset to zero & you will not receive any harvest rewards!
7. If you do not agree with this, feel free to click 'Harvest' to harvest beforehand and wait for that to complete and the warning will disappear before continuing with your deposit
8. If this is your first time interacting with the underlying contract with this token + wallet (or if the contracts have been upgraded recently) you will first have to 'Approve' before continuing the transaction
9. Once all the above is checked, confirmed & valid, feel free to click 'Deposit' and confirm the transaction in your wallet
10. You will need some BNB in your wallet for gas

#### How to Withdraw

![Deposit](/../../_media/guides/staking/synth-withdraw.png)

1. Look for the Curated pool's vault item that you want to withdraw from
2. Click 'Withdraw'
3. If you have not harvested recently; there will be another confirmation here to 'confirm harvest time reset' which means you know that your available harvest will be reset to zero & you will not receive any of those harvest rewards!
4. If you do not agree with this, feel free to click 'Harvest' to harvest beforehand and wait for that to complete, but keep in mind you will then have to wait a period of time (currently 1 hour) before you can withdraw
5. Once all the above is checked, confirmed & valid, feel free to click 'Withdraw' and confirm the transaction in your wallet
6. You will need some BNB in your wallet for gas

---

[<- Back to Staking Guides](/staking?id=guides)
