## Analyzing a Liquidity Pool

One of the first steps you should take before providing liquidity to a pool (after reading up on what 'providing liquidity' is of course) is to analyze the pool you are considering. The community has built tools for this which will hopefully help you assess whether a pool has shown a history of aligning with your long term goals.

#### 1. Liquidity page in the DApp

Visit the community DApp liquidity page: https://dapp.spartanprotocol.org/liquidity

Or navigate to the liquidity page if you are already in the DApp:  
![Menu liquidity](/../../_media/guides/pools/menu-liquidity.png)

- Open the menu
- Click 'Liquidity'

This can also be achieved via the 'pools' / 'home' page by clicking 'Join' under the specific pool you want to assess:  
![Pools join](/../../_media/guides/pools/pools-join.png)

---

#### 2. Select your assets to assess

Select which asset you want to add as liquidity to the pool, which will filter the view to the relevant pool for the next step  
![Select asset](/../../_media/guides/pools/select-asset.png)

---

#### 3. The 'Metrics' view

Now that you have filtered to the pool you would like to asses, look at the metrics/chart section on the same page.
It might be to the right or below the 'add liquidity' section from the last step depending on the size of your device/screen.  
![Metrics](/../../_media/guides/pools/metrics.png)

Here you will see:

- Internally derived token prices (top left)
- 'Pool/revenue APY' (top right)
- Metrics selection/filtering dropdown options below them
- And an interactive chart at the bottom

---

#### 4. Select the metric

Feel free to click the 'metrics' selection dropdown and select the metric you would like to use to assess the pool

![Click metric](/../../_media/guides/pools/click-metric.png)

Some helpful tips on each metric:

- **'Swap Volume'** tells us how much USD-worth of value has swapped thru the pools. As we know; swaps through the pools are what generates us liquidity providers our yield/revenue, so a consistently high volume is always a good sign of an excellent candidate for providing liquidity
- **'TVL (Depth)'** has a number of effects on the yield potential of a pool. A higher TVL means the pool is more likely to provide a better rate for swappers and therefore more likely the pool will get used via aggregators and therefore lead to more swap volume. It's also worth noting that a higher TVL also means as a liquidity provider you will be sharing the revenue with more liquidity providers. So it's important that more TVL goes into the pools that have higher swap demand than the pool is currently able to serve.
- **'Revenue'** is the direct result of swaps in the pool. This is our 'yield' portion of 'providing liquidity'. If you are in a rush and don't have time to properly assess a pool from a range of metrics, 'Revenue' divided by 'TVL' is a pretty good way of getting a general idea of a pool. This is roughly what the APY figure is calculated via.
- **'Swap Demand'** is a cool arbitrary metric that the community developed to assess the 'Swap Volume' of a pool vs its 'TVL'. You could call it 'TVL-weighted swap volume' if you like. This is helpful for a lot of things, for instance: assessing whether a recently increased TVL has resulted in a dilution of pool yield or not.
- **'Txn Count'** is helpful only really at a higher level, shouldn't put too much weight into assessing a pool's yield generation capabilities based on the number of swaps going thru a pool, volume, revenue, TVL etc are all more important, but this is still a cool figure for assessing pools from less of a 'yield' perspective (these metrics aren't just for people looking to provide liquidity

---

#### 5. Filter the data

Sometimes you want to fine-tune the data or see a longer-term trend, that is where the 'period filter' comes in:

You can scope data to the time period that you find relevant. One month (30 days) is a good overall smoother time period to use to assess a pool, but you can also do 7, 14, 30, 60, or 365 days of data providing the pool has existed for that long.

![Time scope](/../../_media/guides/pools/time-scope.png)

You may also notice something cool:

- The APY figure (top right) will recalculate using the time-scope you have selected to save you from doing the math
- Selecting '1 week' will multiply the figure by 54 for the APY (weeks in a year)
- Selecting '1 month' will multiply by 12 for the APY (months in a year)
- ... etc etc

---

#### 6. Closing comments

This should not be considered 'all I have to do before providing liquidity'. It is just one of many tools at our disposal in the big great open world of blockchain decentralised tools.

Some people are happy to just blindly provide liquidity, others want to see an APY, others want to know how the APY is calculated, others want to see some of the raw data that goes into the APY, others want to see _all_ of the data, and so on.

As Spartans we should strive to want to know what is going on behind the scenes, get our hands dirty, analyze the pools, progress to becoming a Chainalysis master-Spartan!
Don't trust; verify! Always!

[<- Back to Liquidity Guides](/liquidity-pools?id=guides)