## Spartan Synthetic-Yield Tokens

As the Spartan Protocol liquidity pools growth in depth, they are able to facilitate Synthetic assets (Synths) on-top. Holding a Spartan Synth is kind of like holding the underlying asset, for instance if you forge BNBs, you get the same speculative exposure as holding BNB instead. By forging a synthetic asset in Spartan Protocol, you are essentially going 'long' the underlying asset and 'short' whatever asset you disposed of to acquire it.

## Why Forge a Synth?

"But if it is just like holding the underlying asset, why bother doing it?" - Holding a Synth asset provides extra options and utility in the Spartan ecosystem. For instance, at the moment, when you forge a Synth, it is sent directly to the SynthVault, where it accrues compounding yield constantly. A major advantage here of BNBs over BNB for insstance, is that it is earning more BNBs or SPARTA every day, whereas holding BNB in your wallet does not accrue any yield.

## What About Impermanent Loss?

As discussed in the 'liquidity' section, providing liquidity gives you impermanent loss exposure. Synths however allow you to provide liquidity to a pool with 100% exposure to a single asset, which rules out the impermanent loss scenario.

---

## Listing / Creating a Synth

For a Synthetic asset to be listed / deployed, it must have a deep underlying pool and that pool must be [Curated](/liquidity-pools?id=curated-pools). If the conditions are met, literally anyone has the ability to click a few buttons and deploy the Synthetic asset token contract. Once again, no permissiion is required here, just go ahead and do it Spartan!

## Forge Synths (Mint)

Once a Synth is created/deployed, users are able to swap any listed BSC tokens (BEP20 assets) like BNB, SPARTA or BUSD for the Synth asset via the community DApp. In doing so, there is _no debt position_ for the user to have to maintain, the position is always fully collateralised by the assets disposed of into the pool. If the market moves in one direction or the other, so does the collateral in the pool. Whilst the fees are not exactly the same as a normal swap, the pool is still used to determine the swap rate to and from the Synth asset just like a normal swap of the underlying assets.

> **Synth Caps**
>
> There are Synth-caps in place to limit the amount of Synths that can be minted vs the token-depth of a pool. The dynamic cap gradually adjusts with time, activity and pool depth towards the hard cap to ensure maximum distribution of the tokens.
>
> If you are not able to forge a Synth due to the caps, decrease the size of your forge or come back later to try again.

## Melt Synths (Burn)

Synths are designed to be a longer-term move, similar to providing liquidity, but if you want to exit and swap your Synths back to another BEP20 asset, you are free to do so after removing them from the SynthVault. All of this can be done via the community DApp. You will get the pool's normal swap rate minus some Synth-related fees which scale down as the pool gets deeper.

---

## Guides

- [List / Create Synth Asset _Guide Coming Soon_](/synths?id=guides)
- [Forge Synths](/guides/synths/forge.md)
- [Melt Synths](/guides/synths/melt.md)
