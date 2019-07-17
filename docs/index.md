# Welcome to Token Swap CLR-ERC20 to BNB
# BNB
## How to Run Full Node
### Install Git LF
Please go to [https://git-lfs.github.com/](https://git-lfs.github.com/) and install git lfs.

### Download Binary with Git LFS
`git lfs clone https://github.com/binance-chain/node-binary.git`

`cd node-binary/fullnode/{network}/{version}`

### Initialize Home Folder
First you need to choose a home folder (i.e. ~/.bnbchaind) for Binance Chain.

You can setup this by:

`mkdir ~/.bnbchaind`

`mkdir ~/.bnbchaind/config`

### Configuration
Put `app.toml`, `config.toml` and `genesis.json` from 

`node-binary/fullnode/{network}/{version}/config/ into $HOME/config`

### Starting Node
Start the full node according to the platform.

Replace the platform variable with `mac` `windows` or `linux` in the following command:
`./{{platform}}/bnbchaind start --home $HOME`

### System Requirements to Run a Full Node
System must meet certain requiremetns to run a full node

* Desktop or laptop hardware running recent versions of Mac OS X, Windows, or Linux.
* 500 GB of free disk space, accessible at a minimum read/write speed of 100 MB/s.
* 4 cores of CPU and 8 gigabytes of memory (RAM).
* A broadband Internet connection with upload/download speeds of at least 1 megabyte per second
* Your full node has to run at least 4 hours per 24 hours in order to catch up with Binance Chain More hours will be better, run your node *  * continuously for best results.

## Full Node CLI Commands
### Create New Key (Account)
You can use `add` to create a new key

MainNet `./bnbcli keys add <Key-name>`

Testnet `./tbnbcli keys add <Key-name>`

### List Keys (Accounts)

MainNet `./bnbcli keys list`

Testnet `./tbnbcli keys list`

### Account Info
You can query the account info with the following command 

On MainNet: `./bnbcli account <your-address> --chain-id Binance-Chain-Tigris --node https://dataseed5.defibit.io:443 --indent --trust-node`


On TestNet: `./tbnbcli account <your-address> --trust-node --chain-id=Binance-Chain-Nile --node=data-seed-pre-2-s1.binance.org:80`

`NOTE: Please note that the amount is boosted by e^8 for the decimal part.`

### BNB Transfer
Sent Tokens

MainNet: `./bnbcli send --from from-key-name --to to-address --amount 200000000:BNB --chain-id Binance-Chain-Tigris --node  https://dataseed5.defibit.io:443 --json --memo "Test transfer"`

TestNet: `./tbnbcli send --from from-key-name --to to-address --amount 200000000:BNB --chain-id=Binance-Chain-Nile --node=data-seed-pre-2-s1.binance.org:80 --json --memo "Test transfer"`

`NOTE: Please note that the amount is boosted by e^8 for the decimal part.`

### Token Creation (Issue)
`Issue` is a transaction used to create a new asset. Anyone can issue a new token with fee paid `(500 BNB fee)`. After issuing, the token would appear in the issuer's account as free balance.

MainNet:

To issue a ABC mintable token with total-supply 1 billion

`./bnbcli token issue --token-name <token-name> --total-supply 100000000000000000 --symbol ABC --mintable --from <key or address>  --chain-id Binance-Chain-Tigris   --node  https://dataseed5.defibit.io:443 --trust-node`

To issue a ABC non-mintable token with total-supply 1 billion

`./bnbcli token issue --token-name <token-name> --total-supply 100000000000000000 --symbol ABC --from <key or address>  --chain-id Binance-Chain-Tigris   --node  https://dataseed5.defibit.io:443 --trust-node`

TestNet:

To issue a ABC mintable token with total-supply 1 billion

`./tbnbcli token issue --token-name <token-name> --total-supply 100000000000000000 --symbol ABC --mintable --from <key or address> --chain-id=Binance-Chain-Nile --node=data-seed-pre-2-s1.binance.org:80 --trust-node`

To issue a ABC non-mintable token with total-supply 1 billion

`./tbnbcli token issue --token-name <token-name> --total-supply 100000000000000000 --symbol ABC --from <key or address> --chain-id=Binance-Chain-Nile --node=data-seed-pre-2-s1.binance.org:80 --trust-node`


# ERC20
In progress
