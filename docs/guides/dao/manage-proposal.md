## Creating & Managing Proposals

If you have LP tokens locked in the DaoVault, you will likely have weight that you can use to vote in SPARTA's DAO proposals. On the DAO page in the DApp, you will be able to view and manage the current proposal and see the previous proposals.
[Read more about DAO proposals here](/dao?id=dao-proposals) before voting or creating a proposal.

![Nav menu](/../../_media/guides/dao/nav-menu.png)

To have weight in the DAO, you will need to have some Liquidity Pool tokens, which can be obtained by [adding liquidity](/guides/liquidity/add-both). Only [Curated Pools](/liquidity-pools?id=curated-pools) are eligible for DAO weight. These LP tokens will also have to be [staked in the DaoVault.](/guides/staking/dao-vault)

Let's walk through the details you can see on the DAO proposal screen, one by one.

![Overview](/../../_media/guides/dao/dao-overview.png)

---

## DAO Details

![Details](/../../_media/guides/dao/dao-details.png)

In this screen, Spartans can see:

- **'Proposal Count'** - the total amount of proposals submitted by the community so far.
- **'Dao Running'** - whether the DAO is currently 'running' or not (DAO can be disabled in certain cases)
- **'Cool-off Period'** - the amount of time an open proposal will have to wait between reaching consensus and being finalise-able
- **'Cancel Period'** - the amount of time a proposal can be open for before it can be cancelled. This doesn't necessarily mean a proposal will automatically cancel after this period, someone will still have to manually cancel it via the interface (see more info later in this guide)
- **'Total Weight'** - the total amount of DAO weight held in the vaults

And then we have two buttons:

- **'Add Weight'** - click this to be directed to the DaoVault screen where you can stake Curated LP tokens to have additional weight in the DAO proposals
- **'New Proposal'** - click this to bring up a modal to be able to submit a new DAO proposal for the community to consider

### Create a New Proposal

Keep in mind you will not be able to create a new proposal if there is already an existing open proposal. Also, there is a fee to create a proposal that goes to the Reserve contract and is circulated back to the ecosystem peers.
For a proposal to have a chance at succeeding it should be discussed & reach some general consensus in the community channels _before_ being proposed via the interface/protocol, so don't create a new proposal unless you are sure, you could potentially waste your time & money by not discussing with the community first.

**1.** Read up on each proposal type first  
**2.** Propose it (off-chain in the social channels) to the community for long form discussion & debate  
**3.** Once general consensus seems to be in support of it off-chain and you are sure you want to proceed, continue:  
**4.** Click on 'New Proposal'

![New Proposal Button](/../../_media/guides/dao/new-proposal.png)

**5.** Select your desired proposal type from the list

![Select Proposal Type](/../../_media/guides/dao/new-proposal-type.png)

**6.** Based on the selected 'type' of proposal, there may be an address that needs to be selected and/or an input that needs to be filled out in the correct format

![Proposal Inputs](/../../_media/guides/dao/proposal-inputs.png)

**7.** You will then need to confirm that you know you are about to pay a 'new proposal' fee in SPARTA (no-one can recover this fee even if you make a mistake, so be careful!)

![Proposal Fee](/../../_media/guides/dao/proposal-fee.png)

**8.** Then click the 'Confirm' button & confirm the transaction in your wallet

#### Troubleshooting:

If the submit button is disabled, here are the explanations for each state:

- **'Existing Proposal'** - this means there is already an existing 'open' proposal (there can only be one active/open proposal at a time)
- **'Approve SPARTA'** - this means you have not yet approved SPARTA with the DAO contract, you will need to click this and approve the transaction before you can continue (approval to spend the SPARTA proposal fee)
- **'Check BNB (Gas)'** - you need to have some BNB in your wallet to cover the gas costs
- **'Check Wallet'** - your wallet is not connected to the DApp, check and confirm before continuing
- **'Global Freeze'** - you will not be able to create a proposal during a global freeze, you will have to wait for the pools to balance before continuing

---

## Proposal Item Details

![Proposal Item Details](/../../_media/guides/dao/item-details.png)

Here, we see the details of the current open proposal (if we are still on the 'Open' tab):

- **Title** - this represents the 'type' of proposal
- **Subtitle** - shows the (#) ID of the proposal followed by the 'status' of the proposal
- Then we have the variables of the specific proposal
- **'Can Cancel'** - this is a countdown timer of when the proposal is able to be cancelled (by anyone who presses the 'Cancel' button and confirms the txn + pays the gas
- **'Your Votes'** - this will show you whether you have voted in support of the proposal or not. If you have voted in support of the proposal, it will show the amount of DAO SPARTA weight you are contributing in support of the proposal (this is dynamic and will vary over time)
- **'Total Votes'** - this shows the current consensus level in support of the proposal:
  - **'Minority'** means 16.66%+ of all DAO weight is in support of the proposal
  - **'Quorum'** means 50.00%+ of all DAO weight is in support of the proposal
  - **'Majority'** means 66.66%+ of all DAO weight is in support of the proposal
- The progress bar underneath is a visual representation of that same consensus % as described above

Then we have 5 possible buttons to 'manage' the proposal as a user:

- **'Add Vote'** - to signal your support for a proposal (vote in support of a proposal)
- **'Remove Vote'** - if you previously voted in support of the proposal, you can 'remove' your support/vote if you have changed your mind (if you have not voted, it is the same as voting 'against' or 'not in support' of a proposal. So if you _do not_ want a proposal to go through, simply do not vote at all (abstain from voting to help prevent a proposal)
- **'Poll Votes'** - if a proposal has reached a sufficient level of consensus, the 'Poll Votes' button will be enabled and anyone can click it & pay the gas to push the proposal to the next stage
- **'Finalise'** - if a proposal has already been pushed to the next stage, the 'Poll Votes' button will instead change to a disabled 'Finalise' button. This button will only become enabled if the proposal still has 'Quorum' level of consensus after the cool-off period (See previous section for more info)
- **'Cancel'** - the final button is to cancel the proposal. This can only be done if the proposal has been active for at least the entire duration of the current 'Cancel Period' (See previous section for more info)

<!-- tabs:start -->

#### **Add Vote**

If you agree with a proposal and want to vote in support of it, you should click 'Add Vote' & go through the steps:

![Add Vote](/../../_media/guides/dao/add-vote.png)

1. Click 'Add Vote'
2. Confirm the transaction in your wallet (be aware this will cost you BNB gas)

?> If you make a mistake or change your mind after voting, you can 'Remove Vote' any time afterwards as long as the proposal is still open (see next tab)

#### **Remove Vote**

If you change your mind on a proposal and want to remove your in support of it, you should click 'Remove Vote' & go through the steps:

1. Click 'Remove Vote'
2. Confirm the transaction in your wallet (be aware this will cost you BNB gas)

?> If you make a mistake or change your mind again, you can 'Add Vote' any time afterwards as long as the proposal is still open (see previous tab)

#### **Poll Votes**

If the proposal has reached its required consensus / support from the DAO members, it can be pushed to the next stage by anyone. To do so:

![Poll Votes](/../../_media/guides/dao/add-vote.png)

1. The 'Poll Votes' button should only be enabled if the proposal's consensus requirements have been met. If it is active and you want to push it to the next stage, start by clicking 'Poll Votes'
2. Confirm the transaction in your wallet (be aware this will cost you BNB gas)

?> Once the transaction finalises on-chain, you will notice the button label will change to 'Finalise' and will be temporarily disabled, see the next tab for more info on finalising a proposal

#### **Finalise**

If the proposal has been in the finalising stage for longer than the cool-off period and still has above Quorum consensus, the 'Finalise' button will be enabled and anyone can attempt to do the honours of finalising the proposal. To do so:

1. Click the 'Finalise' button
2. Confirm the transaction in your wallet (be aware this will cost you BNB gas)

?> If you do not agree with the proposal you might be able to cancel it if it is taking long to reach consensus, for more info on that see the next tab

#### **Cancel**

If the proposal doesn't have consensus support, or has been taking too long to reach it, or maybe was not properly proposed off-chain before being submitted on-chain, there may be an opportunity for anyone to cancel it. As discussed earlier on this page, if a proposal has been open for longer than the 'Cancel Period', _anyone_ can choose to cancel the proposal. The cancel button should only be enabled if this condition is met. If you want to cancel it, do the following:

![Cancel](/../../_media/guides/dao/add-vote.png)

1. Click the 'Cancel' button
2. Confirm the transaction in your wallet (be aware this will cost you BNB gas)

<!-- tabs:end -->

---

## Proposal Type Info

![Type Info](/../../_media/guides/dao/type-info.png)

The final tile/section shows some general information about the current open proposal and what it means if the proposal goes through.

There may be a button the 'View in Docs' underneath it, be sure to read up on all available information before supporting a proposal, don't forget you are helping make major decisions in an important protocol!

---

## View Past Proposals

The tabs up the top of this page also allow you to view past proposals whether they were successful proposals or not.

![Past Proposals Tabs](/../../_media/guides/dao/past-props-tabs.png)

'Completed' - shows us every successful proposal in the DAO's history
'Failed' - shows us every proposal that didn't meet consensus in time and was therefore cancelled by a Spartan

Each past-proposal item will show most of the details attributed to that proposal along with the date that it was submitted on-chain.

![Past Proposals](/../../_media/guides/dao/past-props.png)

---

[<- Back to Dao Guides](/dao?id=guides)
