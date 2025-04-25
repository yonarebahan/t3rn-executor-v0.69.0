# note isi minimal saldo 10 ETH di masing masing jaringan
**bridge bridge sepolia  ke arb, opt, base dan uni sepolia bisa pake 
https://testnets.relay.link/bridge/base-sepolia?fromChainId=11155111**
**kalo Blast**
sepolia to blast sepolia trasnfer ke 
```
0xc644cc19d2a9388b71dd1dede07cffc73237dca8
```

# ✅ Tahap 1 Install Prerequisites : 
```
sudo apt update && sudo apt upgrade -y && \
sudo apt autoremove
```
# ✅ Tahap 2 Install T3rn Executor Node:
```
cd $HOME && rm -r t3rn && \
mkdir t3rn && cd t3rn && \
curl -s https://api.github.com/repos/t3rn/executor-release/releases/latest | \
grep -Po '"tag_name": "\K.*?(?=")' | \
xargs -I {} wget https://github.com/t3rn/executor-release/releases/download/{}/executor-linux-{}.tar.gz && \
tar -xzf executor-linux-*.tar.gz && cd executor/executor/bin
```
# ✅ Tahap 3 Configure Settings and Environment Required Variables: 
```
export ENVIRONMENT=testnet
export LOG_LEVEL=debug
export LOG_PRETTY=false
export EXECUTOR_PROCESS_BIDS_ENABLED=false
export EXECUTOR_PROCESS_ORDERS_ENABLED=true
export EXECUTOR_PROCESS_CLAIMS_ENABLED=true
export EXECUTOR_MAX_L3_GAS_PRICE=150
```

# ✅ Tahap 4 seting private key wallet
**ganti dulu pake private key mu**
```
export PRIVATE_KEY_LOCAL=EVM-PRIVATE-KEY && \
export ENABLED_NETWORKS='l2rn,arbitrum-sepolia,base-sepolia,blast-sepolia,monad-testnet,optimism-sepolia,unichain-sepolia' && \
export RPC_ENDPOINTS='{
    "l2rn": ["https://t3rn-b2n.blockpi.network/v1/rpc/public", "https://b2n.rpc.caldera.xyz/http"],
    "arbt": ["https://arbitrum-sepolia.drpc.org", "https://sepolia-rollup.arbitrum.io/rpc"],
    "bast": ["https://base-sepolia-rpc.publicnode.com", "https://base-sepolia.drpc.org"],
    "blst": ["https://sepolia.blast.io", "https://blast-sepolia.drpc.org"],
    "mont": ["https://testnet-rpc.monad.xyz"],
    "opst": ["https://sepolia.optimism.io", "https://optimism-sepolia.drpc.org"],
    "unit": ["https://unichain-sepolia.drpc.org", "https://sepolia.unichain.org"]
}' && \
export EXECUTOR_PROCESS_PENDING_ORDERS_FROM_API=true
```

# ✅ Tahap 5 Running your T3rn Executor Node:
```
./executor
```
# Join Channel Airdrop Sambil Rebahan : https://t.me/kingfeeder

# bot check balance 
https://t.me/saldo_t3rn_bot
