## Staking

Everything discussed so far might seem quite technical and different to what you consider to be DeFi. That's because _it is_ different to what most consider to be DeFi. For DeFi projects to be sustainable and last more than months or years, it has to be more than just pumping some inflationary token out to people as an incentives without those incentives actually helping bootstrap or fuel some sort of sustainable revenue. Often the approach is just for users to lock assets into a contract that does not even utilize those assets to generate any revenue. Removing tokens from the ciurculating supply is great, but it does nothing to create a sustainable, long term path forward for the protocol or any individuals.

So it should now be clear that is why it was important to discuss those revenue sources first (see [liquidity](/liquidity-pools?id=revenue-potential), [swapping](/swap?id=swapping-trading-assets) and [Synths](/synths?id=spartan-synthetic-yield-tokens)) to show you that Spartan Protocol is here for the long term, working on sustainable ways to have the pools incentivise themselves. Having said that, it is also important to bootstrap liquidity in the growth stages in a controlled and non-degen manner. That is where 'Staking' comes in. The Reserve contract holds a bunch of not-yet-circulating SPARTA and controls their distribution to pools and Spartans by the Protocol's incentive functions. By locking up staking-enabled assets within the protocol's vaults, you will be able to earn extra yield and be incentivized further to stay in the pools.

### Why Stake?

Staking usually involves a user locking up a layer-one asset such as BNB or SPARTA into a smart contract to temporarily remove them from the circulating supply. The problem with this is it doesn't utlize those assets to generate revenue (unsustainable; dependent on inflation) nor does it really provide the protocol or pools with any tangible advantages. With Spartan Protocol's DeFi contracts, only the second-layer assets are able to be staked for yield or governance weight. This means that for anyone to extract incentives from the protocol, they have to show their commitment and provide utility to the ecosystem first.

---

## Staking Features

### DaoVault Staking

Spartans have the option to stake [Curated](/liquidity-pools?id=curated-pools) LP tokens in the DaoVault to generate SPARTA yield every second which can be harvested directly to their wallet whenever the user calls the harvest function from the community DApp. Another very important side-effect of staking in the DaoVault is that it gives you percentage-weight in the DAO governance of the protocol. That means the very people who are supplying the protocol with its most important utility (the liquidity) are the ones who vote to shape the future of the protocol.

### SynthVault Staking

By staking your Synths in the SynthVault (this happens by default when you forge a Synth) you are exposed to compounding yield in the form of the same Synth (ie. BNBs) by default. If the Synth being harvested is capped however, you will receive SPARTA to your wallet instead.

### What is the BondVault?

The BondVault holds the time-locked LP tokens of Spartans who participated in the Bond token distribution program. If you are one of those users, your position/s will show up here and you will be able to claim your unlocked LP tokens to your wallet which are then free for you to do with as you please (Stake in DaoVault, remove liquitity etc)

The Bond program was retired when the SPARTA token distribution phase was ended and remaining distribution (~37% of the supply at the time) was burned to the 0x0dead address permanently.


---

## DApp Features

### What is the Vault APY

The yield that users receive from the vaults is not set/fixed nor predictable. All we can do is look at historic performance and provide some general guides/assumptions about the future. 

Here is a general overview of how the DApp calculates the history-based APY estimations for staking in the vaults:
- **Yield** = Last 30 days total globally Harvested (in SPARTA value)
- **Depth** = Current global SPARTA weight in the Vault

With those two variables it is pretty simple:
- **APR** = (Yield * 12) / Depth
- **APY** = APR * weekly compounding (it actually compounds every time you harvest, so a week has been chosen as the average harvest rate for this estimation)

So what we are doing is using the last 30 days total Harvested amount (in SPARTA value), then multiplying it by 12 to make a full year of estimated yield then scaling it down by the amount of SPARTA staked in the Vault.

---

## Guides

- [DaoVault Staking](/guides/staking/dao-vault.md)
- [SynthVault Staking](/guides/staking/synth-vault.md)
- [Claim from BondVault](/guides/staking/bond-vault.md)
