# PhilanthropistCoin

Anyone and everyone who loves cryptocurrency can help the world.

PhilanthropistCoin is a javascript coin, wallet, and block explorer. It was forked from naive-coin.

Every time someone mines a block they get 50 PhilanthropistCoins. But an extra 50 PhilanthropistCoins goes to a "charity" address where nonprofits/charities can request funds from.

Currently the code only supports transactions. Soon I will make a way for users to vote where the "charity" funds go.

The current algorithm is POW (Proof of Work). This will stay the same, but I will also add in DPOS (Delegated Proof of Stake). That addition will allow for the voting.

The idea came from a mix of bitshares and wanting to help the world. Bitshares created a funding system to fund their workers all by the users voting for them. The funds came in the beginning. Then users can vote to where the funds can go. I want that but where users can vote what charities/nonprofits to help.

## Installation (Daemon)

> You must have [Nodejs Installed](https://nodejs.org/en/download/)

```
npm install
npm start
```

##### Get blockchain
```
curl http://localhost:49028/blocks
```

##### Start mining blocks
```
curl -X POST http://localhost:49028/mineBlock
``` 

##### Stop mining blocks
```
curl -X POST http://localhost:49028/stopMineBlock
``` 

##### Send transaction
```
curl -H "Content-type: application/json" --data '{"address": "04bfcab8722991ae774db48f934ca79cfb7dd991229153b9f732ba5334aafcd8e7266e47076996b55a14bf9913ee3145ce0cfc1372ada8ada74bd287450313534b", "amount" : 35}' http://localhost:49028/sendTransaction
```

##### Query transaction pool
```
curl http://localhost:49028/transactionPool
```

##### Mine transaction
```
curl -H "Content-type: application/json" --data '{"address": "04bfcab8722991ae774db48f934ca79cfb7dd991229153b9f732ba5334aafcd8e7266e47076996b55a14bf9913ee3145ce0cfc1372ada8ada74bd287450313534b", "amount" : 35}' http://localhost:49028/mineTransaction
```

##### Get balance
```
curl http://localhost:49028/balance
```

#### Query information about a specific address
```
curl http://localhost:49028/address/04f72a4541275aeb4344a8b049bfe2734b49fe25c08d56918f033507b96a61f9e3c330c4fcd46d0854a712dc878b9c280abe90c788c47497e06df78b25bf60ae64
```

##### Add peer
```
curl -H "Content-type:application/json" --data '{"peer" : "ws://localhost:49029"}' http://localhost:49028/addPeer
```
#### Query connected peers
```
curl http://localhost:49028/peers
```

## Wallet
For the wallet to work correctly you must have the daemon from the base folder running (up above).

Go to into the wallet directory and run:

```
npm install
npm start
```

And go to http://localhost:49030/

Your private key is at the basefolder/node/wallet/private_key

## Blockchain Explorer

The official explorer is at http://144.76.63.8/