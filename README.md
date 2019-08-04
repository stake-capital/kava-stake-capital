# kava-stake-capital
All things Kava &amp; Stake Capital

# Documentation 

https://medium.com/kava-labs/kava-testnet-2-guide-b9f5a8294d80

# Install Kave

# Run Kava into System Service

Create `kava-system-service.sh` from https://github.com/stake-capital/kava-stake-capital/blob/master/kava-system-service.sh

And Run `./kava-system-service.sh`

# Status and Logs 

Status: `kvcli status`
Output:
```
{"node_info":{"protocol_version":{"p2p":"7","block":"10","app":"0"},"id":"aafd0790e2abdffa44852eb33f9864904affbaa5","listen_addr":"18.196.186.121:26656","network":"kava-testnet-2000","version":"0.32.1","channels":"4020212223303800","moniker":"Stake Capital","other":{"tx_index":"on","rpc_address":"tcp://0.0.0.0:26657"}},"sync_info":{"latest_block_hash":"9B39905E74FB6DAE001F1D0E1AA15966509935E0804B9E8A03ED0BAA856E1E01","latest_app_hash":"9317731FE2CB444425C4D75C2C6C0447F53FAC6BC8D193F4460E892A2B297F0D","latest_block_height":"54910","latest_block_time":"2019-08-04T14:55:11.153650319Z","catching_up":false},"validator_info":{"address":"C3194A2BAD4A58B99806430EA1A04723C65566E9","pub_key":{"type":"tendermint/PubKeyEd25519","value":"JKslFt686HR6esjX7e67819v/GbV6DEJAWSavRRneKA="},"voting_power":"10000"}}
```

Wallet information: `kvcli q account $(kvcli keys show -a kava-wallet-1) --trust-node`
```
kvcli q account $(kvcli keys show -a kava-wallet-1) --trust-node
|
  address: kava1hfj6n07rt7qh7gsh75eerhh5mwccdfqauj9ugx
  coins:
  - denom: ukava
    amount: "90000000000"
  pubkey: kavapub1addwnpepqtnfum5kj8a3ryx89jlfd4pnuak6xvac5857e6kk5sjpj36z6y75xlc6l04
  accountnumber: 98
  sequence: 1
```

Voting power: `curl localhost:26657/status|grep -i voting`
Output: `
``curl localhost:26657/status|grep -i voting
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1109  100  1109    0     0  1083k      0 --:--:-- --:--:-- --:--:-- 1083k
      "voting_power": "10000```

