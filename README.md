# TT-Miner 2022.4

- improved defaut hashrates for all variants of ProgPow and KawPow
- printed hashrates is discounting the devfee (printed hashrate = full hashrate - devfee hashrate) - TT-Miner shows what you the miner gets. Please note that most miners show the full hashrate that includes the devfee. For a reliable hashrate comparison use pool-hashrates after some hours/days.
- optimized NiceHash support (ETCHASH, ETHASH, KAWPOW), fast DAG switching
- optimized mining to a QT-wallet, supported by most KawPow coins (known exception: TTM, ARL)
- new algo Sha512256D for Radiant
- new algo EvrProgPow for Evrmore
- new coin RXD(Radiant)
- new coin EVR(Evrmore)
- new coin VTE(VirtualEmpire)
- new coin ETHW(EthereumPOW)
- new coin ETHF(EthereumFair)
- new coin GSPC(GSP Coin)
- new coin LAB(Labyrinth)
- new commandline option: daginfo - prints information about the active dag
- deletes DAG files that are older than 90 days
- deletes DAG files that were used 2 epochs ago




## Mining fees
| Mining | fee |
| - | - |
| Epic Cash | 2.0 % |
| Ghostrider/Mike algo| 2.0 % |
| Radiant/Sha512256D| 2.0 % |
| Solo to Qt-Wallet | 2.0 % |
| all other | 1.0 % |





## Supported Algorithm

| Algorithm | remarks |
| - | - |
| Ethash | includes Etchash(Ethereum Classic) & Ubqhash(Ubiq) |
| KawPow | includes FiroPow(Firo), EvrProgPow(Evrmore) |
| ProgPow | includes ProgPowZ(Zano), vProgPow(VeriBlock) and ProgPow(Veil) |
| Ghostrider | includes Mike |
| SHA512256D ||




## Directly Supported Coins (other coin can be mined by algorithm)

| Coin | Name | Algorithm |
| - | - | - |
| ETC | Ethereum Classic | Etchash |
| CLO | Callisto | Ethash |
| EXP | Expanse | Ethash |
| ETP | Metaverse | Ethash |
| UBQ | Ubiq | Ubqhash |
| FIRO | Firo | FiroPow |
| EVR | Evrmore | EvrProgPow |
| RVN | Ravencoin | KawPow |
| NEOX | Neoxa | KawPow |
| KAW | Kawkaw | KawPow |
| PRCO | Procyon | KawPow |
| SATO | Sato | KawPow |
| ARL | Arielcoin | KawPow |
| HVQ | Hivecoin | KawPow |
| TTM | Titanium | KawPow |
| MEOW | MeowCoin | KawPow |
| REDE | RedeCoin | KawPow |
| VTE | VirtualEmpire | KawPow |
| LAB | Labyrinth | KawPow |
| SERO | Super Zero | ProgPow |
| EPIC | Epic Cash | ProgPow |
| ZANO | Zano | ProgPowZ |
| EVOX | Evoultion | ProgPowZ |
| VBK | VeriBlock | vProgPow |
| VEIL | Veil | ProgPow(Veil) |
| RTM | Raptoreum | GhostRider |
| BTRM | Bitoreum | GhostRider |
| BUT | Butcoin | GhostRider |
| YERB | Yerbas | GhostRider |
| JGC | Jagoan | GhostRider |
| FITA | Theta | GhostRider |
| BBC | Babacoin | GhostRider |
| NAPI | Atanapicoin | GhostRider |
| THOON | Thooneum | GhostRider |
| GSPC | GSP Coin | GhostRider |
| VKAX | Vkax | Mike |
| RXD | Radiant | Sha512256D |




## Supported commandline option

### Basic options
| Option | Information |
| - | - |
| -h [ --help, -? ] | Prints supported options and the commandline format. |
| -no-color [ -nocolor ] | Do not use any color in the screen output. |
| -no-ctrlc [ -noctrlc ] | Disables 'Ctrl-C' monitoring. |
| -no-hashrate [ -nohashrate ] | Do not send hashrate information to the pool. |



### Algo options
| Option | Information |
| - | - |
| -a [ --algo ] arg | Defines the algorithm to use for the primary coin.<br/>Supported algos (values for 'arg'):<br/>ETHASH<br/>ETCHASH<br/>UBQHASH<br/>ProgPow<br/>ProgPowZ<br/>vProgPow<br/>FiroPow<br/>EvrProgPow<br/>KawPow<br/>GhostRider<br/>Mike |
| -aalt [ --algoalt ] arg | Defines the algorithm to use for the alternate coin (primary coin must be 'EPIC'). |



### Coin options
| Option | Information |
| - | - |
| -coin arg | Defines the primary coin to mine.<br/>Supported coins (values for 'arg'):<br/>ETC<br/>CLO<br/>EXP<br/>ETP<br/>UBQ<br/>SERO<br/>EPIC<br/>ZANO<br/>EVOX<br/>VBK<br/>VEIL<br/>FIRO<br/>EVR<br/>RVN<br/>NEOX<br/>ARL<br/>KAW<br/>PRCO<br/>SATO<br/>HVQ<br/>TTM<br/>MEOW<br/>REDE<br/>VTE<br/>LAB<br/>RTM<br/>BTRM<br/>BUT<br/>YERB<br/>JGC<br/>FITA<br/>BBC<br/>NAPI<br/>THOON<br/>GSPC<br/>VKAX |
| -coinalt arg | Defines the alternate coin to mine (primary coin must be 'EPIC'). |



### DAG options
| Option | Information |
| - | - |
| -dag-2mem | Keeps a copy of the created DAG in the host memory.<br/><dl><dt>Advantage:</dt><dd>Can reuse the DAG if required (EPIC-Mining, NICEHASH)</dd><dd>Saves energy since the DAG is created on a single GPU only and then distributed to the other GPUs</dd><dd>You can run the GPU that creates the DAG with different OC settings than the other GPUs</dd><dt>Disadvantage:</dt><dd>Needs hostmemory to keep the DAG</dd></dl> |
| -dag-2disk | Keeps a copy of the created DAG on the disk.<br/><dl><dt>Advantage:</dt><dd>Can reuse the DAG if required (EPIC-Mining, NICEHASH)</dd><dd>Saves energy since the DAG is created on a single GPU only and then distributed to the other GPUs</dd><dd>You can run the GPU that creates the DAG with different OC settings than the other GPUs</dd><dd>Faster start of mining</dd><dt>Disadvantage:</dt><dd>Needs diskspace to keep the DAG</dd></dl> |
| -daginfo | Prints information of the active DAG in the mining statistics |



# Commandline samples
TT-Miner supports the -pool[-o], -user[-u], -pass[-p] notation as well as the more compact -P form. Please replace placeholder with your information:

| Placeholder | meaning |
| - | - |
| \<WALLET\> | Your wallet-id |
| \<WORKER\> | Your worker-id |
| \<USERNAME\> | Your username if required (check EPIC mining & solo mining to Qt-Wallet) |
| \<PASSWORD\> | Your password if required (check EPIC mining & solo mining to Qt-Wallet) |




## Mine ETC on 2miners (TCP-port) (-o,-u format)

| verion | commandline |
| - | - |
| TCP port, -P format | TT-Miner -coin ETC -P \<WALLET\>.\<WORKER\>@etc.2miners.com:1010 |
| TCP port, -o,-u format | TT-Miner -coin ETC -u \<WALLET\>.\<WORKER\> -o etc.2miners.com:1010 |
| SSL port, -P format | TT-Miner -coin ETC -P stratum+ssl://\<WALLET\>.\<WORKER\>@etc.2miners.com:11010 |
| SSL port, -o,-u format | TT-Miner -coin ETC -u \<WALLET\>.\<WORKER\> -o stratum+ssl://etc.2miners.com:11010 |


## Mine RXD on woolypooly (SSL-port) (-P format)

TT-Miner -coin RXD -P ssl://\<WALLET\>.\<WORKER\>@pool.woolypooly.com:3122 




# Mining to NiceHash

### Mine Ethash on NiceHash
TT-Miner offers special handling for mining an algo/pool that frequently changes the required DAG. It is recommended to use the 'dag-2file' commandline option. It will save a DAG - once created - to disk. This will save some time the next time the DAG is required. Please see below one possible commandline to mine ETHASH on NiceHash:<br>
TT-Miner -dag-2disk -daginfo -a ETHASH -P ssl://\<WALLET\>.\<WORKER\>@daggerhashimoto.auto.nicehash.com:443

### Mine Ethash on NiceHash
TT-Miner -dag-2disk -daginfo -a ETCHASH -P stratum+ssl://\<WALLET\>.\<WORKER\>@etchash.auto.nicehash.com:443

### Mine KawPow on NiceHash
TT-Miner -dag-2disk -daginfo -a KAWPOW -P stratum+ssl://\<WALLET\>.\<WORKER\>@kawpow.auto.nicehash.com:443




# Mining Solo to a Qt-Wallet
To use your Qt-Wallet for solo mining you need to create/configure a config file. The config file is a textfile that must contain following information:
You need \<USERNAME\> and \<PASSWORD\> in the commandline of TT-Miner to get access to the Qt-Wallet.
Please change rpcallowip to match your network configuration. It defines IPs that may connect to the wallet.<br/>

rem -- FILE START -- do not add this line to your config file!<br/>
automintoff=1<br/>
rpcuser=\<USERNAME\><br/>
rpcpassword=\<PASSWORD\><br/>
rpcbind=0.0.0.0<br/>
rpcallowip=192.168.41.0/24<br/>
server=1<br/>
listen=1<br/>
gen=1<br/>
miningaddress=\<WALLET\><br/>
rem -- FILE END -- do not add this line to your config file!<br/>


## Then start your Qt-Wallet with the option to use this new configuration file:<br/>
neoxa-qt -conf=filename.conf<br/>


## Mine NEOX Solo to Qt-Wallet
Please use the USERNAME and PASSWORD information from your config file that you use to start your wallet.<br/>
TT-Miner -coin neox -P http://\<USERNAME\>:\<PASSWORD\>@\<IP-TO-YOUR-QT-WALLET\>:9766




## Not supported Solo to Qt-Wallet
Some project modified the format of the RPC protocol so that TT is not able to establish a connection to the wallet for solo mining. Please find below a list of known project that do not work:
- Arielcoin(ARL)
- Titanium(TTM)

If you see any addition project that modified the RPC protocol so that solo mining is not supported pßülease let me know.




# Mining EPIC
You have the choice to mine EPIC either directly to the local node, or to one of the EPIC mining pools. Since EPIC is alternating the active algo you can mine something else if EPIC uses RandomX or Cuckoo.


## Sample command lines to mine just EPIC to a local node
TT-Miner -coin EPIC -P <SOME_ID>.<SOME_WORKER>@127.0.0.1:3416

## Sample command lines to mine just EPIC on fastepic.eu
TT-Miner -coin EPIC -P ssl://\<YOUR_KEYBASE_ID\>.\<YOUR_WORKER_NAME\>:\<YOUR_PASSWORD\>@fastepic.eu:3416

## Sample command lines to mine just EPIC on 51pool.online
TT-Miner -coin EPIC -P \<YOUR_ID\>#\<YOUR_WORKER_NAME\>:\<YOUR_PASSWORD\>@51pool.online:4416


## Mining EPIC with an alternate coin
To use TT for mining EPIN and an alternate coin you just ne4ed to add the additional information for the alternate. In most cases that would be the information for the coin or algo and the information required to access the pool (wallet/worker/password/server). To add these additional information please append 'alt' to the commandline option. So find the details in the table below:

| option | normal | alternate |
|-|-|-|
|pool|-o or -pool|-oalt or -poolalt|
|password|-p or -pass|-palt or -passalt|
|wallet|-u, -user or -wallet|-ualt, -useralt or -walletalt|
|coin|-coin|-coinalt|
|algo|-a or -algo|-aalt or -algoalt|
|server|-P|-Palt|

Please see the samples below on how to setup mining EPIC and an alternate coin


## Sample command lines to mine EPIC to a local node and ETC as alternate coin on 2miners
TT-Miner -coin EPIC -P <SOME_ID>.<SOME_WORKER>@127.0.0.1:3416 -coinalt ETC -Palt stratum+ssl://\<YOUR_ETC_WALLET_ID\>.\<YOUR_ETC_WORKER\>@etc.2miners.com:11010

## the same goes for all other combination - here an example to mine EPIC on fastepic and RVN on flypool.org as alternate coin
TT-Miner -coin EPIC -P ssl://\<YOUR_KEYBASE_ID\>.\<YOUR_WORKER_NAME\>:\<YOUR_PASSWORD\>@fastepic.eu:3416 -coinalt RVN -Palt ssl://\<YOUR_RVN_WALLET_ID\>.\<YOUR_RVN_WORKER\>@stratum-ravencoin.flypool.org:3443

## mine EPIC on pool51.online and RXD on woolypooly as alternate coin
TT-Miner -coin EPIC -P <YOUR_USER_ID\>#\<YOUR_WORKER_NAME\>:\<YOUR_PASSWORD\>@51pool.online:4416 -coinalt RXD -Palt ssl://\<YOUR_RXD_WALLET_ID\>.\<YOUR_RXD_WORKER\>@pool.woolypooly.com:3122


