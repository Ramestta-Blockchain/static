# Static server
The private static server for Ramestta Chain.

### How it works?
All files, in this repository, will be served over AWS S3 at `https://static.ramestta.com/<file-path>`.

### Production
Main branch will be automatically deployed. No other action required.

## Package Usage

### Installation
```bash
$ npm i --save @ramesttanetwork/meta
```
### Usage
```javascript
const Network = require("@ramesttanetwork/meta/network")

// define network
const network = new Network("testnet", "v1")

const rama = network.Rama  // all info related to Rama
const Main = network.Main // all info related to Main
const Heimdall = network.Heimdall // all info related to Heimdall

const RootChainABI = network.abi("RootChain")

// use rama js
let rama = new Rama ({
    ramaProvider: Rama.RPC,
    mainProvider: Main.RPC,
    registry: Main.Contracts.Registry,
    ...
    ...
})
```


### Before Publishing
```
npm run minify
```
