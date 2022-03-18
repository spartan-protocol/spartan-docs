## Analyse Your Liquidity Positions

The Spartan community DApp has a cool page to help save you the tough job of logging and calculating all of your liquidity related transactions. Please bear with us as we run through all of this as a 'position' is subjective based on what the user was hoping to achieve (accumulate more USD? accumulate more SPARTA? accumulate more of the underlying assets?)
Each logical scope is covered as best as possible via the DApp so that the user can fully assess how their liquidity is performing in the pools they have selected.

![Nav menu](/../../_media/guides/positions/nav-menu.png)

You can access the 'Positions' page via the navigation menu (bar on the left). Let's walk through the details you can see on the Positions screen, one by one:

![Overview](/../../_media/guides/positions/liq-overview.png)

---

## Overall Position

Before you begin, you will need to press a button to tell the DApp to call the Subgraph and crunch your data for you! If you see 'Generate First' in the DApp then this is probably your first time, make sure your wallet is connected and then click 'Reload'.

![Reload](/../../_media/guides/positions/reload.png)

If you have done this in the past, but have done liquidity related transactions since then, you will need to click the 'Reload' button again to get the fresh data. Note that the Subgraph is usually hours behind, so ideally only visit the Positions page and assess your position if you have not added or removed liquidity recently.

![Blocks](/../../_media/guides/positions/blocks.png)

You can see how far behind the data is by comparing 'Current Block' & 'Last Updated'. Each block is roughly ~3 seconds. So in the example above, the data is ~2,000 blocks behind which is equal to roughly ~6,000 seconds = ~1.7 hours

Keep in mind your 'non realised' positions (Your LP tokens held in wallet or vaults) will always bee up to date/current even if the 'Last Updated' figure is in the past, this is why its very important to verify all this before assessing your positions with datasets from different time periods.

Now that you have loaded your data and confirmed whether it is up to date or not, we can proceed to assess your overall position.

Your 'Overall Position' can be assessed from two different scopes, both of which use internally derived pricing based on the price of the assets (in the pools) at the time when each transaction was realised. Below we see we are currently assessing 'vs Hodl USD' which means our goal is to accrue more USD value. You can click 'Change to:' to change the scope but we will get to that later.

![Scope Change](/../../_media/guides/positions/liq-scope-change.png)

### Overall (vs Hodl USD)

![Overall](/../../_media/guides/positions/liq-overall-usd.png)

#### 'In' type transactions:

- **'Liquidity Added'** is the sum of all liquidity adds you have ever performed into all SpartanV2 pools

> When you add liquidity usually it is in SPARTA + TOKEN but here we show a USD number. This is via the internally derived value of the assets (spot value) in the Spartan pools at the time of each transaction
>
> **Liquidity Added also includes any assets you added via Bond**

#### 'Out' type transactions:

- **'Liquidity Removed'** is the same thing, but it is instead the sum of all liquidity removal transactions. Same deal with it being internally derived at USD price at the time of each transaction
- **'Total Harvest'** is a sum of all SPARTA harvested via the DaoVault. The USD figure is derived at the time of each harvest assuming that you would have converted them to USD straight away in this scope seeing as we are in the 'vs Hold USD' scope
- **'Redemption Value'** is the USD value of all LP tokens attributed to your wallet

> Redemption Value includes all LP tokens that are held in your wallet, staked in your DaoVault or locked in your BondVault

#### Assessed Position:

- We then have a 'Gain vs USD' figure which is simply the sum of all ('Out') transactions minus all ('In') transactions
- This is an assessment of how far ahead you are from adding your liquidity vs holding USD at the start instead. This includes any asset price/value movements, not just yield

#### Other Scopes?

Okay, what if you are a SPARTA OG that just wants to accrue SPARTA and don't care about USD gains? You can now click this button to switch to the 'vs Hold SPARTA' scope:

![Overall](/../../_media/guides/positions/liq-overall-change-scope.png)

### Overall (vs Hodl SPARTA)

![Overall](/../../_media/guides/positions/liq-overall-sparta.png)

#### 'In' type transactions:

- **'Liquidity Added'** is the sum of all liquidity adds you have ever performed into all SpartanV2 pools

> When you add liquidity usually it is in SPARTA + TOKEN but here we show a SPARTA number. This is via the internally derived value of the assets (spot value) in the Spartan pools at the time of each transaction
>
> **Liquidity Added also includes any assets you added via Bond**

#### 'Out' type transactions:

- **'Liquidity Removed'** is the same thing, but it is instead the sum of all liquidity removal transactions. Same deal with it being internally derived at SPARTA price at the time of each transaction
- **'Total Harvest'** is a sum of all SPARTA harvested via the DaoVault. This does not need it's value derived as it is received in SPARTA (our scope)
- **'Redemption Value'** is the SPARTA value of all LP tokens attributed to your wallet

> Redemption Value includes all LP tokens that are held in your wallet, staked in your DaoVault or locked in your BondVault

#### Assessed Position:

- We then have a 'Gain vs SPARTA' figure which is simply the sum of all ('Out') transactions minus all ('In') transactions
- This is an assessment of how far ahead you are from adding your liquidity vs holding SPARTA at the start instead. This includes any asset price/value movements, not just yield

---

## Pool Positions

Your 'Pool Position' can be assessed from two different scopes. The 'vs Hold USD' scope uses internally derived USD prices similar to as explained in the first sections above. The other scope 'vs Hold Units' however does not need to derive any pricing at the time of each transaction as you are comparing to holding those same assets. It does derive a 'current' USD value at the end though to give you yet another scope! OPTIONS!

Before you begin, you can select your pool position you would like to assess by clicking the pool icon and making your selection:

![Select](/../../_media/guides/positions/liq-select-pool.png)

### Pool (vs Hold USD)

We will begin with 'vs Hold USD' as it's a little more simple and relatable to the previous two scopes we have already discussed.

![Pool USD](/../../_media/guides/positions/liq-pool-usd.png)

#### 'In' type transactions:

- **'Liquidity Added'** is the sum of all liquidity adds you have ever performed into all SpartanV2 pools

> When you add liquidity usually it is in SPARTA + TOKEN but here we show a USD number. This is via the internally derived value of the assets (spot value) in the Spartan pools at the time of each transaction
>
> **Liquidity Added also includes any assets you added via Bond**

#### 'Out' type transactions:

- **'Liquidity Removed'** is the same thing, but it is instead the sum of all liquidity removal transactions. Same deal with it being internally derived at USD price at the time of each transaction
- **'Redemption Value'** is the USD value of all LP tokens attributed to your wallet

> Redemption Value includes all LP tokens that are held in your wallet, staked in your DaoVault or locked in your BondVault

?> Note: Here we don't take into account 'Harvested' as that cannot really be attributed to a specific pool, so please take that into consideration when assessing your overall position

#### Assessed Position:

- We then have a 'Gain vs USD' figure which is simply the sum of all ('Out') transactions minus all ('In') transactions
- This is an assessment of how far ahead you are from adding your liquidity vs holding USD at the start instead. This includes any asset price/value movements, not just yield

#### Other Scopes?

Okay, what if you want to compare to if you had just held your assets from the start instead of adding them as liquidity? You can now click this button to switch to the 'vs Hold Units' scope:

![Change Scope](/../../_media/guides/positions/liq-pool-change-scope.png)

### Pool (vs Hold Units)

#### --- ASSESS SPARTA SIDE FIRST ---

Let's begin by assessing the first half of this positions scope, the SPARTA side:

![Pool USD](/../../_media/guides/positions/liq-pool-sparta-side.png)

#### SPARTA-side: 'In' type transactions:

- **'Liquidity Added'** is the sum of all SPARTA added during liquidity adds you ever performed into the selected SpartanV2 pool

> This is different to the previous scopes because we are only assessing the SPARTA added first, no internally derived pricing is required, just raw SPARTA!

#### SPARTA-side: 'Out' type transactions:

- **'Liquidity Removed'** is the same thing, but it is instead the sum of all liquidity removal transactions
- **'Redemption Value'** is the SPARTA you would receive from redeeming all LP tokens attributed to your wallet

> Redemption Value includes all LP tokens that are held in your wallet, staked in your DaoVault or locked in your BondVault

?> Note: Here we don't take into account 'Harvested' as that cannot really be attributed to a specific pool, so please take that into consideration when assessing your overall position

#### Assessed SPARTA-half position:

- We then have a 'Gain (SPARTA)' figure which is simply the sum of all ('Out') transactions minus all ('In') transactions

> Remember: this is an assessment of one half of your position (the SPARTA side). You may notice this is actually lower than what you added (this is called impermanent loss) and the other side that we assess next is higher instead (or vice versa)

#### --- ASSESS TOKEN SIDE NEXT ---

We can now move on to assessing the other half of this scope's position, the TOKEN side:

![Pool Token](/../../_media/guides/positions/liq-pool-token-side.png)

#### TOKEN-side: 'In' type transactions:

- **'Liquidity Added'** is the sum of all TOKEN added during liquidity adds you ever performed into the selected SpartanV2 pool

> This is different to the previous scopes because we are only assessing the SPARTA added first, no internally derived pricing is required, just raw TOKEN!

#### TOKEN-side: 'Out' type transactions:

- **'Liquidity Removed'** is the same thing, but it is instead the sum of all liquidity removal transactions
- **'Redemption Value'** is the TOKEN you would receive from redeeming all LP tokens attributed to your wallet

> Redemption Value includes all LP tokens that are held in your wallet, staked in your DaoVault or locked in your BondVault

?> Note: Here we don't take into account 'Harvested' as that cannot really be attributed to a specific pool, so please take that into consideration when assessing your overall position

#### Assessed TOKEN-half position:

- We then have a 'Gain (TOKEN)' figure which is simply the sum of all ('Out') transactions minus all ('In') transactions

> Remember: this is an assessment of one half of your position (the TOKEN side). You may notice this is actually lower than what you added (this is called impermanent loss) and the SPARTA side that we already assessed above is higher instead (or vice versa)

#### --- FINAL ASSESSED GAINS IN USD ---

We can now move onto the 3rd section of assessing this scope's position:

![Pool Token](/../../_media/guides/positions/liq-pool-final-assess.png)

You might be happy to stop at this point now that you know your TOKEN & SPARTA gains in your position. However, it might be hard to be certain at this point whether you are ahead and by how much, especially if your underlying assets have moved in two different directions and you are left with a lot fewer units on one side and a lot more units on the other.

This is where this section comes in. It gives you a current unrealised assessment of both halves of your position in derived USD value.

Quite simply, we get the sum of this:

- 'Gain (SPARTA)' converted to current USD value
- 'Gain (TOKEN)' converted to current USD value

---

[<- Back to Positions Guides](/positions?id=guides)
