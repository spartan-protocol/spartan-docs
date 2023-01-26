## API

API Info (Get swap quotes, supply, tokenomics, TVL, pool information etc). Follow the link to our docs inside the API's GitHub repo:

https://github.com/spartan-protocol/spartan-api/blob/main/v1docs.md

---

## Aggregator Integration Guide

Welcome fellow DeFi projects and aggregators! If you are interested in integrating with the Spartan Protocol AMM our community is always on hand and ready to help through the process, but please find below some crucial steps to get started.

#### Integrate Swap Quoting

If you are a front-end project or similar looking to get a quote for swapping between two assets via the SPv2 pools, follow along to integrate swap quoting either directly via a SpartanSwap Utility smart contract (this is the best option for trust and uptime reasons) or via the SpartanProtocol API (this is the more convenient option)

A note on WBNB & BNB handling: You can either enter the BNB (`0x0000000000000000000000000000000000000000`) address or the WBNB (`0xbb4CdB9CBd36B01bD1cBaEBF2De08d9173bc095c`) address and the same WBNB pool will be utilised correctly to return you the sazme result whether using the smart contract call or the API.

##### Via SpartanSwap Utils Smart Contract

To get a quote for a swap via the SpartanSwap Utils contract you will only need a few things:
- An RPC and provider object to static call web3/smart contracts (you do not need a signer object as this is a read-only call)
- Token contract address for the input token (address string)
- Token contract address for the output token (address string)
- WEI units of the input token you want to swap (wei string)

Build the contract object (see ethers.js) with your provider/rpc + the SpartanSwap Utils contract address + ABI:
- SSUtils Address: `0xB7B3216A199893aC00486Fe30439A8F4388fF4C9`
- BSCScan Link: https://bscscan.com/address/0xB7B3216A199893aC00486Fe30439A8F4388fF4C9#code
- ABI Link: https://api.bscscan.com/api?module=contract&action=getabi&address=0xB7B3216A199893aC00486Fe30439A8F4388fF4C9

Call the swap quote function:
`SSUtilsContractObject.getSwapOutput(inputAddress,outputAddress,inputUnitsWei)`

Don't forget: the input is in WEI so for `1.0` BNB units input you would enter: `1000000000000000000`
The return is *also* in WEI. So don't forget to convert WEI->UNITS for the end user.

##### Via Spartan Protocol API

To get a quote for a swap via the SpartanProtocol API you will only need a few things:
- Token contract address for the input token (address string)
- Token contract address for the output token (address string)
- WEI units of the input token you want to swap (wei string)

Call the endpoint with your desired inputs as URL params. The following example will quote for swapping 1.0 USDT to BUSD:
`https://api.spartanprotocol.org/api/v1/swapQuote?inputAddr=0x55d398326f99059fF775485246999027B3197955&outputAddr=0xe9e7CEA3DedcA5984780Bafc599bD69ADd087D56&inputUnits=100000000000000000000`

Don't forget: the input is in WEI so for `1.0` USDT units input you would enter: `1000000000000000000`
The return is *also* in WEI as a string type. So don't forget to convert WEI -> UNITS for the end user along with any desired number-formatting.

API endpoint documentation: https://github.com/spartan-protocol/spartan-api/blob/main/v1docs.md

#### Integrate Swap Functionality

If you are a swap aggregator or any project looking to be able to utilise the Spartan Protocol V2 AMM pools to perform swaps, follow along to get integrated today!

##### Derive Current Router Address

The Router and DAO contracts can be replaced by DAO proposals, hence you should ideally derive the current Router address via our source of truth: the SPARTA token contract. Follow these few calls to ensure you are deriving the current permissioned Router address.

1. SPARTA Token Address:
   `0x3910db0600eA925F63C36DdB1351aB6E2c6eb102` - (We will refer to this contract as `SPARTA` now)

2. With the SPARTA token address, we can perform a static call of:
   `SPARTA.DAO()` to derive the current DAO contract address - (We will refer to this contract as `DAO` now)

3. With the DAO token address, we can perform a static call of:
   `DAO.ROUTER()` to derive the current Router contract address - (We will refer to this contract as `ROUTER` now)

We are now in a position to interact with the pools with confidence that we are using the permissioned router

##### Perform a Swap

With the Router address now derived, the easiest way to perform a swap through the pools is to call:  
`ROUTER.swapTo(uint256 inputAmount, address fromToken, address toToken, address member, uint256 minAmount)`

- `inputAmount` = the wei units amount that the user is looking to sell (aggregators: or the partial amount if performing a split-route swap)
- `fromToken` = the token address of the token being 'swapped from' / 'sold'
- `toToken` = the token address of the token being 'swapped to' / 'bought'
- `member` = the wallet address that will be receiving the output of the swap (where the funds go after the swap, aggregators: this will probably be your own referring router address)
- `minAmount` = you can input a wei units amount here, if the output is lower than this amount, the transaction will revert

##### Example

Swap 1 BNB for BUSD and send to user, revert if the output is less than 300 BUSD

- 1 unit = `1000000000000000000`
- BNB address = `0x0000000000000000000000000000000000000000`
- BUSD address = `0xe9e7CEA3DedcA5984780Bafc599bD69ADd087D56`
- User address = `0x588f82a66eE31E59B88114836D11e3d00b3A7916`
- 300 units = `300000000000000000000`

`ROUTER.swapTo(`  
 `1000000000000000000,`  
 `0x0000000000000000000000000000000000000000,`  
 `0xe9e7CEA3DedcA5984780Bafc599bD69ADd087D56,`  
 `0x588f82a66eE31E59B88114836D11e3d00b3A7916,`  
 `300000000000000000000`  
`)`

##### Reference

`DAO.ROUTER()` - https://github.com/spartan-protocol/spartanswap-contracts/blob/master/contracts/Dao.sol#L621  
`ROUTER.swapTo()` - https://github.com/spartan-protocol/spartanswap-contracts/blob/master/contracts/Router.sol#L214  
`POOLFACTORY.getPool()` - https://github.com/spartan-protocol/spartanswap-contracts/blob/master/contracts/poolFactory.sol#L124

---

## Smart contracts

Please find below some important notes divided up by contract scope for the curious Spartans and developers looking to integrate.
For projects looking to fork or explore our ideas in their own project, we live and breath open source and welcome you to both fork and integrate in our community and ask questions.

We only want to see things get built and continue to innovate the decentralised, open source world, so reach out and let us know what you are working on.

##### Base contract

_Coming Soon_

##### BondVault contract

_Coming Soon_

##### DAO contract

_Coming Soon_

##### DaoVault contract

_Coming Soon_

##### FallenSpartans contract

_Coming Soon_

##### PoolFactory contract

_Coming Soon_

##### Reserve contract

_Coming Soon_

##### Router contract

_Coming Soon_

##### SynthFactory contract

_Coming Soon_

##### SynthVault contract

_Coming Soon_

##### Utils contract

_Coming Soon_
