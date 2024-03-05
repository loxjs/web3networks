# web3networks

[![Dependency Status][downloads-image]][npm-url]
![Contributors](https://img.shields.io/github/contributors/loxjs/web3networks?label=contributors%20on%20all%20branches)

![ES Version](https://img.shields.io/badge/ES-2021-yellow)
![Node Version](https://img.shields.io/badge/node-18.x-green)

web3networks is a library for managing blockchain networks, allowing you to add networks, query networks, and obtain a list of networks.

## Installation

You can install the package either using [NPM](https://www.npmjs.com/package/@loxjs/web3networks) or using [Yarn](https://yarnpkg.com/package/@loxjs/web3networks)


### Using NPM

```bash
npm install @loxjs/web3networks
```

### Using Yarn

```bash
yarn add @loxjs/web3networks
```

## Getting Started

In web3networks, the data structure for a network is as follows:

```
{
    "chainId": 1,
    // Chain Type
    "chain": "Ethereum",
    // Chain Name
    "name": "Ethereum",
    "rpcUrl": "https://ethereum-rpc.publicnode.com",
    "blockExplorerUrl": "https://etherscan.io/",
    // Whether it is a test network
    "isTest": false,
    // Native currency of the network
    "currency": {
        "name": "ETH",
        "symbol": "ETH",
        "decimals": 18
    },
    // Default configurations for executing transactions on the current network
    "options": {
        // Default gas limit
        "defaultGasLimit": 3000000,
        // Default gas price, in gwei
        "defaultGasPrice": "1",
        // Default gas price multiplier, used to set the gas price of a transaction by
        // multiplying the real-time gas price from the blockchain with this multiplier
        "defaultMultiplierForGasPrice": 1.5
    }
}
```

Usage:

```
const web3networks = require('@loxjs/web3networks')
// Get all networks
const networks = web3networks.list
// Add a new network
web3networks.addNetwork({...})
// Use chainId to get a network
const network = web3networks.getNetworkByChainId(chainId)
```


[npm-url]: https://npmjs.org/package/@loxjs/web3networks
[downloads-image]: https://img.shields.io/npm/dm/@loxjs/web3networks?label=npm%20downloads

