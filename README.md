1. Install Packages

sudo apt-get update && sudo apt-get upgrade -y

sudo apt install screen curl nano  -y
2. Install Rust

 curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
When Prompted, Enter 1 and wait unti installation compelete.
source $HOME/.cargo/env
3. Install Solana CLI:

curl --proto '=https' --tlsv1.2 -sSfL https://solana-install.solana.workers.dev | bash
Close and reopen your Terminal.
solana version
If you get solana: command not found RUN :
echo 'export PATH="/root/.local/share/solana/install/active_release/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
solana --version
4. Switch RPC

solana config set --url https://mainnetbeta-rpc.eclipse.xyz/
Wallet CLI
. Create a CLI wallet
solana-keygen new
Install Bitz
cargo install bitz
Run Bitz Miner
1. Open a screen
screen -S bitz
2. Start Miner
bitz collect
image

Usefull Commands
Check account info:

bitz account
To integrate Node & Backpack address

cat ~/.config/solana/id.json
Claim Bitz to your Node Wallet:

bitz claim
Edit CPU Utilization, Use Ctrl+C, then replace your 8 with your system cores.

bitz collect --cores 8
minimize screen:

Ctrl+A+D
ON/OFF:

screen -r bitz
