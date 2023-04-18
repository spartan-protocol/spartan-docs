## What is a DAO

A Decentralized Autonomous Organization (DAO) places the community participants in control of the platform transparently and programmatically. The power of on-chain smart contracts means that a large number of automated actions within a contract can be set up and voted on, the results of which can be automatically actioned.

### Who makes up the DAO?

"Who makes up the 'majority consensus' you spoke about above?" - If you read up on the [DaoVault staking info,](staking?id=daovault-staking) you will know that only the liquidity providers in the most active Spartan Protocol pools make up the voting weight within the DAO. This means that the people who have influence in these changes are the very people who are likely to be acting in the best interest of the protocol.

### What can the DAO do?

The Spartan DAO can do _ALOT._ Its definitely the most expansive on-chain DAO many users have ever used, giving so much control and trust to the Spartan community to really be able to operate and maintain the protocol now and ongoing. These actions the DAO can perform are triggered via DAO proposals.

---

## DAO Proposals

Anyone can create a DAO proposal at any time, as long as no other DAO proposal is currently active. The proposer simply has to visit the DAO and click a few buttons to select their proposal type and parameters. They will then have to confirm a transaction to initialize the proposal on-chain.

Some gas and a 'new proposal fee' will require payment by the proposer. This fee doesn't go to any middleman, its intention is not rent-seeking, it goes to the reserve which is where all non-owned SPARTA sits waiting to be released via incentives to good peers in the ecosystem. The main reason for this fee is to help resist spamming / griefing and also to ensure the Spartan is sure about this proposal before confirming it. All proposers should seek general consensus from the community on a proposal _prior_ to creating the proposal on-chain, otherwise they will likely have trouble reaching consensus on-chain within the required time period.

### Suggested Proposal Process

Many DAOs these days are mostly off-chain or only have the voting on-chain which is then handed over to a trusted admin/council to actually enact the proposed changes. The reason most projects opt to run the DAO in this way is simply because DAOs are complex and difficult to place on-chain due to the chain-limitations and gas costs. The Spartan Protocol contributors of V1 & V2 worked really hard to ensure they didn't cop out and go the easy route, the entire Spartan DAO is on-chain and automated, _including the functions being actioned following a successful proposal._ There is _no_ reliance on an admin or council of individuals to make the proposal happen once it's successfully approved by majority consensus, any individual can cancel or finalize the proposal permissionlessly.

This design may change in V3 in favour of a less 'on-chain' approach as discussed in the community channels over the past year or so, having this big on-chain beast is great in theory but if its too hard to get it self-sustaining enough to move towards severing the deployer permissions, then its arguably better to explore going fully immutable with a trustless-from-the-start approach for new deploys and user-chosen migrations (effectively how chain-forking works) but of course there are some major nuances there and being a community project thats up to the contributors to shape and decide over the course of V3 development. One thing is for certain, the DAO will at least significantly simplify with the majority of its prior functionality being deprecated with things like the Bond program finalizing.

For now though, there are some deployer permissions throughout the contracts which counter the 'trustless-ness' but can, and are intended to be severed entirely, but not before the DAO weight is distributed and sticky enough. As discussed a lot in the past, the DAO proposals should lean heavily towards ranging from 'impossible to succeed' to 'difficult to succeed' within the parameters of the contracts (ie. shy away from 'easy' leaning factors) to increase the cost and difficulty of malicious attackers. With everything being actionable on-chain, increasing the cost of attack is far more important than simplifying the UX for DAO users.

Outside of these things that we can know in advance and/or read on-chain anytime, there are factors that are dynamic and can lean this difficulty significantly in either direction. For instance, at time of writing, the DAO weight is only worth ~$135k which means someone could theoretically manipulate the a critical (value at risk) DAO proposal to their sole desire for less than ~$100k, but the value at risk is multiples of $100k. So the cost of attack is less than extractable and/or destroyable value. Whilst this kind of attack is not a sure-thing (DAO has been built to allow weight to reactively come defend against such attacks) its still a worry and extra responsibility that the DAO members and community must keep an eye on.

However in these instances (especially when expected; ie. close to genesis or between project phases/versions when weight is migrating or sitting on the sidelines), parameters should be set heavily closer towards 'impossible to succeed' to ensure no funds are at direct risk. As the weight increases to a level where the size and distribution provides good confidence the parameters should be loosened accordingly.

As a general rule of thumb, to avoid frustration, do not blindly throw a proposal directly on-chain, it will likely fail to reach consensus without prior discussion + coordination and will almost certainly fail either way due to the tight conditions of the DAO contracts. At best, all you will likely do is spark discussion of the proposal within the community for a cost instead of for free (which in some ways is not so bad...)

All proposals should always be discussed in the community channels off-chain for a significant period and reach at least a positive temperature check prior to being pushed on-chain. Prior to deployer permissions being severed (when correlating with DAO cost of attack being low), parameters have typically been closer to 'impossible to pass' and reactively loosened just prior to a sufficiently discussed off-chain proposal being pushed on-chain.

> ℹ. `Frontend Projects:` If you are integrating proposal functionality, please ensure you show a message directing users to community channels to discuss a new proposal prior to them proposing on chain. Please also pull the 'Cancel Period' & 'Cool-off Period' variables and show them in your interface ideally along with tooltips or links explaining the logic of these variables.

> ℹ. `Frontend Projects:` If the 'Cancel Period' & 'Cool-off Period' are both of equal value to each other, for better UX and user clarity, please make sure the 'new proposal' button state is disabled as this is signal for a 'paused' state, essentially as close as you can get to 'impossible' for a proposal to pass as these parameters get (even though its still possible). It may also make sense in this state to increase the prominency of the message advising users to visit the community channels to discuss/raise any new proposals.

Some more info on the different proposal types in the next section:

### Turn On / Off Emissions

> ℹ. `FLIP_EMISSIONS` Requires: 50% Consensus

Being able to turn the emissions off or on again offers several advantages within the ecosystem. Turning off base emissions would cause Spartan Protocol to have its incentives fade away. This means that there would be less incentive for liquidity providers, potentially leading to reduced total value locked (TVL).

If voted through, the total supply would pause, causing the emissions to cease which would be very good news for longer-term token holders. Although if this happens too early, the TVL will reduce and therefore one would expect the token price would reduce with it, but it is intended and expected for emissions to one day be turned off once the circular revenue is significant enough to feed into itself and continue growing the project on its own.

V3 Notes: There has been recent discussions of the emissions being permanently turned off for V3 which means this proposal likely won't be relevant come V3.

### Burn Synth Premium

> ℹ. `REALISE` Requires: 50% Consensus

Realising the premium of a pool involves working out how much the existing synths are worth and how much the LP tokens held on the Synth contract are worth. If there is a premium amount, it can be burned and therefore attributed to the existing liquidity providers earlier than it would have been if we waited until those Synths were instead melted.

V3 Notes: With derivatives like synths moving to layers above the AMM this proposal is not very relevant even to V2 but definitely not for V3. This sort of thing would be handled by the governing derivative project rather than the AMM.

### Add Pool to Curated

> ℹ. `ADD_CURATED_POOL` Requires: 66.66% Consensus

Adding a pool to the 'Curated' list enables extra features and incentives on top of the pool as explained in the [liquidity section](/liquidity-pools?id=curated-pools) of the documentation. As this is an important decision involving value extraction functions, a majority (66.66%) consensus is required for it to pass.

V3 Notes: Curated pools are not likely to be a thing in V3, with emissions being turned off and existing incentives moving to other less complex layers.

### Remove Pool from Curated

> ℹ. `REMOVE_CURATED_POOL` Requires: 50% Consensus

Conversely, should a Curated pool fail to hold the desire of the community, a proposal can be created to remove the special Curated status and have the pool returned to a regular liquidity pool.

V3 Notes: Curated pools are not likely to be a thing in V3, with emissions being turned off and existing incentives moving to other less complex layers.

### Adjust SynthVault Claim %

> ℹ. `SYNTH_CLAIM ` Requires: 50% Consensus

Here we can regulate the claim percentage of the Reserve that the SynthVault can begin 'harvest' calculations off. If increased; the harvest rewards will be larger. If decreased they will be lower. This proposal has a hard-coded max input of 1500 basis points and a minimum of 0 basis points (which would effectively turn off harvest rewards)

V3 Notes: With derivatives like synths moving to layers above the AMM this proposal is not very relevant even to V2 but definitely not for V3. This sort of thing would be handled by the governing derivative project rather than the AMM.

### Adjust DaoVault Claim %

> ℹ. `DAO_CLAIM` Requires: 50% Consensus

Here we can regulate the claim percentage of the Reserve that the DaoVault can begin 'harvest' calculations off. If increased; the harvest rewards will be larger. If decreased they will be lower. This proposal has a hard-coded max input of 1500 basis points and a minimum of 0 basis points (which would effectively turn off harvest rewards)

V3 Notes: The current incentivized DAO model is not likely to exist in V3, with a lot less need for DAO governance now that token distribution is completed. This incentive will likely move to a permissionless staking platform instead of happening at the AMM level

### Change DAO Proposal Cool off

> ℹ. `COOL_OFF` Requires: 50% Consensus

When a proposal is created, the community will come and vote on whether or not they agree with it. Once a majority has been attained and the proposal reaches enough weight to switch to finalizing status, there is a mandatory window where it needs to stay above 50% consensus otherwise it won't be finalize-able.

This cooling-off period allows the community/DAO time to educate everyone if it's a bad proposal and allows those who oppose it to add liquidity to the pools to get enough weight to vote against it. The community may decide that they want a bigger window for proposals to be voted through, or to make the time shorter if that's what they feel is best for Spartan Protocol.

### Send a SPARTA Grant to a Wallet

> ℹ. `GRANT` Requires: 66.66% Consensus

Being able to vote through a grant is what could be used to encourage the driving force behind any future developments. The vision behind the DAO is that Spartan Protocol continues to be a self-governing community project that does not require any maintenance or upkeep. This means that the project can run indefinitely without any interactions from admins or trusted council members.

Whilst the contributors have always remained active, the community may decide that they want a large upgrade, or to introduce a whole domain of new features which could range from extra deflationary measures or additions that could generate extra revenue streams for Spartan hodlers such as spinning off into gaming / NFTs.

The community can vote through a grant which would allow financial incentives and reward to those involved with any new developments that the community may call for.

This proposal-type has already been testing in the wild with V2 to provide a small grant for marketing purposes thru the last 2021 -> early 2022 months, funding a number of partnerships and opportunities that were previously un-obtainable due to the 'no treasury' aspect of the project.

As this is an important decision involving value extraction functions, a majority (66.66%) consensus is required for it to pass.

### Upgrade DAO Contract

> ℹ. `DAO` Requires: 66.66% Consensus

Changing the DAO contract is a concept that may be of not much use at the moment. However, in order to future proof the Spartan Protocol, there may come a day where a modification or upgrade will need to take place within the DAO itself.

A contract change will allow the contributors to be able to implement changes as the community requests them. This will allow Spartan Protocol to remain fit for use no matter what changes may take place in the future of DeFi.

### Upgrade ROUTER Contract

> ℹ. `ROUTER` Requires: 66.66% Consensus

Another contract change proposal which has to be included to ensure that Spartan Protocol is as future proof as possible. The Router contract is likely to be upgraded many times throughout the years, whether it is to cut out unused features, make existing functions more efficient (save gas) or add new features.

### Upgrade UTILS Contract

> ℹ. `UTILS` Requires: 66.66% Consensus

When V2 launched, a new feeBurn deflationary feature was implemented on every transfer of the SPARTA token. This Utils contract was designed with the intention of making it possible to disable or change that feeBurn, which is exactly what happened in late November 2021, sending us into the next phase of SPARTA token burns where ~37% of the total supply was burned permanently out of the supply to the 0x0dead address! It is unlikely this contract will need to be changed again in the future as it mostly houses 'helper' functions, but nice to know we always can!

### Upgrade RESERVE Contract

> ℹ. `RESERVE` Requires: 66.66% Consensus

The reserve contract is where the emissions are sent before being distributed to the pools or harvested. Just like the DAO contract address, this will most likely never need to be voted through to be changed, however is always best to be safe and make sure we are as future proof as possible.

---

### Bond-related Proposals (Deprecated)

With the token distribution phase of the project coming to a close, a lot of Bond-related proposals are no longer relevant, but live on in the DAO's proposal-history page in the DApp. These Bond proposals included:

- New Bond Allocation: Release a 2M SPARTA allocation available for Bonding.
- List a Bond Asset: The Bond program was only enabled on limited assets as decided by the DAO
- Delist a Bond Asset: The DAO could also propose to remove an asset from being Bond-enabled

---

## Guides

- [Manage or Create Proposal](/guides/dao/manage-proposal.md)
