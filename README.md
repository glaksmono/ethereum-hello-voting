# Hello World DApp on Ethereum Blockchain

1. `git clone`
2. `cd ethereum-hello-voting`
3. `npm install ethereumjs-testrpc web3@0.20.1`

```
➜  ethereum-hello-voting git:(master) ✗ ls -l
total 224
-rw-r--r--    1 glaksmono  staff    198 Nov 27 14:37 README.md
-rw-r--r--    1 glaksmono  staff   1595 Nov 25 20:40 Voting.sol
-rw-r--r--@   1 glaksmono  staff   1198 Nov 25 21:06 index.html
-rw-r--r--    1 glaksmono  staff   2218 Nov 25 21:07 index.js
drwxr-xr-x  262 glaksmono  staff   8384 Nov 25 20:40 node_modules
-rw-r--r--    1 glaksmono  staff  96275 Nov 25 20:40 package-lock.json
```

4. `node_modules/.bin/testrpc`

```
EthereumJS TestRPC v6.0.3 (ganache-core: 2.0.2)

Available Accounts
==================
(0) 0xc14ac33b44b17fa025fc289f6c5fb7ffb020a417
(1) 0x09a3f62f6a971c20b5423b53f020b8d979873ee6
(2) 0xf3712eaf41b0d44d831a0372ed79dd85d7d722dd
(3) 0x343fd2dea5d4aae89d0b3a5006407f1d2a98b77a
(4) 0x3d1fe3d96815826b8f5957d5360f279fdee21bbb
(5) 0x21489e7dd629b5beaffc580c087f3e0609e87f85
(6) 0x8aecd29452cf6a033200a6a3daafe878fc7a2d51
(7) 0x772fae51ddf029f6f0a617fd38e6048850c67c34
(8) 0xd245c540075c726693521048a05fa9df3536afe0
(9) 0xb4f9eede8933bb7f8414c49210af9f9aa406c0ad

Private Keys
==================
(0) d8d1f8eebb12f4424b8f088397a9ed5e66a932b120017d9288f8769dfd02b217
(1) 57804165d98921615e8c14b2cdfa9b0822cb717d4f15955fdb9aad9287ae59c7
(2) f147e542e93029a6bca476de6fbcf1279e6cf16430bac92b17dd6da9ead31f6c
(3) 59ad9f1d7d60a14d738877115977b1102d239f7ce23c7eff84a822bc4943b2e4
(4) 722001fa4079002ffdc1c2c3ac5c53c8bb604ec38860b168abcfc9eb45e50578
(5) 2eecae49229ac086e8d9ce32989df16523e350741d286f56a8caff6b8d32bd9d
(6) 29038c01fa4b98cc1b56ae6dac3abdeeb252ecaaa4e8f572ac55b3ba3dc6a9b5
(7) 35c23caa680552ce119f2839fa02ef84976c236cf91ee2a2730e1b135a983153
(8) 184c27eed38667205a87246de2314a2ffadecd691b13d77b6d1a05d99fa038ae
(9) 5624bda2fa52d198ea6ab9be155da642328d11d25fa8f4433c9ceb4a1b229dfc

HD Wallet
==================
Mnemonic:      pattern wall churn exotic barely nothing improve hotel stay finger year squirrel
Base HD Path:  m/44'/60'/0'/0/{account_index}

Listening on localhost:8545
```

5. Run node `node`
6. Compile the code

```
> code = fs.readFileSync('Voting.sol').toString()
> solc = require('solc')
> compiledCode = solc.compile(code)
```

7. Check the contract address

```
> deployedContract.address
'0x9c3602896e302b25a7613c00a46c28b5af8e7916'
```

8. Update `index.js` with the contract address of your localhost

```
// In your nodejs console, execute contractInstance.address to get the address at which the contract is deployed and change the line below to use your deployed address
contractInstance = VotingContract.at('0x9c3602896e302b25a7613c00a46c28b5af8e7916');
```

9. Open `index.html`
