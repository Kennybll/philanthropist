# PhilanthropistCoin

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

## Wallet - Windows Only - Mac/Linux To Come

For the wallet to work correctly you must have philanthropistcoin from the base folder running (up above).

Go to into the wallet directory and run:

```npm install```
```npm run build```

Then go into the wallet/dist folder and run:

```npm install```
```npm run electron```

The programs are then under wallet/dist/Staging/(your computer type).

Then double click on PhilanthropistCoin.exe.