# Cryptologic BE Challenge
> Backend application writen in Nodejs/Typescript with simple REST architecture. Implemented the ethers.js library to manage the RPC connection, fetch transactions data and utils.

### Contains:
1. RPC Connection to Avalanche EVM C-Chain
2. Local MongoDB connection
3. Middlewares on endpoint routes

### Endpoints Description:
- GET: transaction from RPC by txHash and contract detail `/api/detail/:txHash`

- POST: save transaction fetched from RPC to the DB `api/transaction/` \
    Body json example:
    ```
    {
        "txHash": 0x508217c172c3cfe006ee9ca5bef621ba11a359461bacfc0494f1449a7d00f443
    }
    ```
- GET: get transaction by txHash with _decode BigNumbers_ `api/:txHash`]
  
- GET: get all saved transactions from the DB with _decode BigNumbers_ `api/transaction/get-all`
  
- GET: get ABI from server `/contract/abi`
  
- GET: get ABI from server `/contract/bytecode`
  
### Packages
1. Ethers
2. Express
3. MongoDB
4. ts-node
___

## Challenge

✅ Use web3.js or ethers.js proper methods to fetch transaction data details

✅ Fetch and save main contract ABI and bytecode and save them into a file and database

✅ Understand and parse the event log to show in a básic REST response the decoded events and its parameters

✅ Create a basic REST endpoint that once queried saves the parsed data into a MongoDB document.

✅ Create a basic REST endpoint to get the previously saved data.

### Must have:

✅ Basic error handling

✅ Basic README file

✅ Basic explaination of the work done

### Extra points:

❌ unit testing

✅ Docker build

___

## Setup
To run this project you can use Yarn or Docker:
### Yarn
```
yarn install
yarn start
```
### Docker
```
docker-compose build
docker-compose up
```

### TODO
- Error handling when RPC doesnt responds
- unittest

> Original repository with commit history: [https://github.com/nsalto/cryptologic_challenge]



