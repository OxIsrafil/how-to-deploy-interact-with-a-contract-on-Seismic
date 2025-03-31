# how-to-deploy-and-interact-with-a-contract-on-Seismic

# Guide to Deploy Seismic Devnet Contract

## Pre-Requirements

1.**Install Rust**
```
curl https://sh.rustup.rs -sSf | sh  
. "$HOME/.cargo/env"
```
2. **Verify Installation**
```
rustc --version
```
3. **Install jq
For WSL/Ubuntu**
```
sudo apt install jq
```
#For Mac
```
brew install jq
```

4. **Install sfoundryup**
```
curl -L \
     -H "Accept: application/vnd.github.v3.raw" \
     "https://api.github.com/repos/SeismicSystems/seismic-foundry/contents/sfoundryup/install?ref=seismic" | bash
source ~/.bashrc
```
5. **Run sfoundryup**
```
sfoundryup
```

# NOTE: This Process can take a while to fully download ( 5 to 90 minutes )

**Let's Deploy an encrypted contract**

1. **Clone & Navigate to The Repo**
```
git clone --recurse-submodules https://github.com/SeismicSystems/try-devnet.git
cd try-devnet/packages/contract/
```

2. **Deploy contract**
```
bash script/deploy.sh
```

**This script will generate a dev wallet and promt a Faucet Url, you have to copy that wallet address and take the faucet and then click enter in terminal✅**

**Interact with an encrypted contract 🤖**

1. **Navigate to home directory:**
```bash
cd $home
```
2. **Install Bun**
```
curl -fsSL https://bun.sh/install | bash
```

3. **Install node dependencies**
```
cd try-devnet/packages/cli/
bun install
```
4. **Send transactions**
```
bash script/transact.sh
```

That's all, you just deployed your first contract on SeismicSys & interacted with it. ✅


## if you face any error check their FAQ 
**https://docs.seismic.systems/appendix/devnet**
