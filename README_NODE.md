https://bnbsmartchain.com/how-to-run-a-fullnode-on-binance-smart-chain/

https://www.youtube.com/watch?v=Bvh-ZRIi_jk

### Start a validator node
## generate the consensus key and input the password
geth account new --datadir ./node
echo {your-password} > password.txt
geth --config ./config.toml --datadir ./node --syncmode snap -unlock {your-validator-address} --password password.txt  --mine  --allow-insecure-unlock  --cache 18000




## start a full node
geth --config ./config.toml --datadir ./node  --cache 18000 --rpc.allow-unprotected-txs --txlookuplimit 0