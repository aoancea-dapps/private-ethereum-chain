# Setup a private ethereum chain
In this series we will test the following techniques:
- create a private chain
- create accounts on the private chain
- send ether between the accounts on the private chain
- launch another node with the genesis block of the private chain
- connect the second node with the first node in the private chain
- import accounts from the first node in the second node - in order to be able to send ether through the second node from one account to the other
- send ether between the accounts on the private chain using the second node

### Frequent commands
- ``geth --datadir ./datadir init genesis.json``
- ``geth --datadir ./datadir account new``
- ``geth --datadir ./datadir console --networkid 2019``
- ``geth --datadir ./datadir console --networkid 2019 --port 20201 --rpc``
- ``geth --datadir ./datadir_new --networkid 2019 --port 30306 --nodiscover console --ipcdisable``
- ``personal.unlockAccount(eth.accounts[0], "password")``
- ``eth.sendTransaction({from:”address”, to:”address”, value: web3.toWei(amount, "ether")})``
- ``admin.addPeer(enode://f7aa5b604056ff77dc561034f12874586b44b4a00e92355e7f750cfb43717ef1d0092f208b08661b209656d09540b11f6d0c6667a611674f7a75b718424d0c9a@[::]:30306?discport=0")``


# Links
- https://medium.com/coinmonks/ethereum-setting-up-a-private-blockchain-67bbb96cf4f1
- https://hackernoon.com/set-up-a-private-ethereum-blockchain-and-deploy-your-first-solidity-smart-contract-on-the-caa8334c343d
- https://ethereum.stackexchange.com/questions/30439/error-unknown-account
- https://www.cryptocompare.com/coins/guides/how-to-do-an-ethereum-transaction-check-your-balance/
