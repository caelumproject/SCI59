# [Caelum project] SCI59 Token 

This guide is a quickstart tutorial. A more technical setup will depend on the mining software of your choice.

Mining instructions
---
Please note that the following instructions apply to the **Ropsten testnet version only**.

SCI59 Token details:

- Contract address:   **0xacbaf9715d3d92e2baee463c2189ed8df9ae6a36**
- Total supply:       21,000,000 tokens
- Decimals:           8 Decimals

Contract address:  https://ropsten.etherscan.io/address/0xacbaf9715d3d92e2baee463c2189ed8df9ae6a36

Token tracker:     https://ropsten.etherscan.io/token/0xacbaf9715d3d92e2baee463c2189ed8df9ae6a36

### Step 1: Prepare your Ropsten testnet account ###
- Go to [**MyEtherWallet**](https://www.myetherwallet.com) (MEW).
- In the top right hand corner select **Ropsten (myetherwallet.com)** (a green bar at the bottom will appear telling you you have succesfully connected).
- If not already there, click **New Wallet**
- Enter a password you can remember and click 'Create New Wallet'
- Download & save your Keystore file in a safe space and click 'I Understand. Continue'
- Save your Private Key in a safe space.
- Get your wallet address by clicking on 'View Wallet Info'
- Select 'Private Key' and then enter the private key previously saved then click 'unlock'.
- Go to **https://faucet.ropsten.be/**. Enter your wallet address, click 'Send me test Ether' and the faucet will send a small amount of Ethereum to your account.

### Step 2: Download 0xbtc mining software
It's important to use mining software that supports solo mining for the testnet version. While great performance improvements have been made to the 0xbtc mining software, most latest versions have excluded solo mining due to high difficulty. 

Suggested mining software:

 - Mining-Visualizer (MVis)' TokenMiner (AMD/OpenCL): [https://github.com/mining-visualizer/MVis-tokenminer](https://github.com/mining-visualizer/MVis-tokenminer)
 - COSMiC v3.4 (nVidia/CUDA): [https://bitbucket.org/LieutenantTofu/cosmic-v3/](https://bitbucket.org/LieutenantTofu/cosmic-v3/)
- Original 0xbitcoin miner (CPU) https://github.com/0xbitcoin/0xbitcoin-gpuminer/tree/master/dist/windows

**Carefully read and follow the installation instructions for the  software you have chosen to get started.**

### Step 3: Configure the mining software

This depends on the version you downloaded. All needed parameters are listed below (depending on the software version, you might need to change `config web3provider` with the host and port):

- (RPC) host : http://52.208.46.161
- (RPC) port : 8549
- (MINER) account: your ethereum address generated in step 1
- (MINER) private key: the private key generated in step 1
- (TOKEN) contract/address: **0xacbaf9715d3d92e2baee463c2189ed8df9ae6a36**
- gasprice: 5 gwei

### Step 4: Start the mining software

If you could not change the miner account/private key (depending of software), you might need to enter `accounts list` in the miner terminal. If no account exists, use `accounts new`. Fund the selected address via [https://faucet.ropsten.be/](https://faucet.ropsten.be/)

You should now be mining SCI59 tokens!

![Alt text](https://monosnap.com/image/cwV7mFtb5Wf167TuUDdnsK8RH9uyuQ.png)

Depending on the software, you will see a bunch of transactions appearing on the terminal, along with success messages. This means you successfuly minted a block.

## Becoming A Masternode
---
In order to become a masternode, you must first hold tokens in your account. To see how many tokens you have, you can go to MyEtherwallet.com, view wallet info, and in the bottom left corner select 'Add custom token'.

![Alt text](https://monosnap.com/image/nld75jivvMKGCm0Sd7BFLyZcBxlQ4g.png)

Input the SCI59 token details listed below and then click 'Save'

- Token contract address: **0xacbaf9715d3d92e2baee463c2189ed8df9ae6a36**
- Token Symbol:           SCI59
- Decimals:               8

You should now see your token balance in your account.
**NOTE** During testnet, 1 SCI59 token is enough to become a masternode.

### Step 1:
On MyEtherwallet.com, select the 'Contracts' tab (making sure that you are on **Ropsten network**).

![Alt text](https://monosnap.com/image/5iyvm2yOCkqLcOYNJUQ4HlqYTtI1AF.png)

Next, enter the SCI59 address **0xacbaf9715d3d92e2baee463c2189ed8df9ae6a36** in the contract address field.

Copy paste the code below in the **ABI / JSON Interface**

    [ { "constant": true, "inputs": [], "name": "_own", "outputs": [ { "name": "", "type": "address" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": true, "inputs": [], "name": "name", "outputs": [ { "name": "", "type": "string" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": true, "inputs": [], "name": "TARGET_DIVISOR", "outputs": [ { "name": "", "type": "uint256" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": false, "inputs": [ { "name": "spender", "type": "address" }, { "name": "tokens", "type": "uint256" } ], "name": "approve", "outputs": [ { "name": "success", "type": "bool" } ], "payable": false, "stateMutability": "nonpayable", "type": "function" }, { "constant": true, "inputs": [ { "name": "", "type": "uint256" } ], "name": "masternodes_array", "outputs": [ { "name": "", "type": "address" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": true, "inputs": [], "name": "getMiningDifficulty", "outputs": [ { "name": "", "type": "uint256" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": false, "inputs": [ { "name": "nonce", "type": "uint256" }, { "name": "challenge_digest", "type": "bytes32" } ], "name": "mint", "outputs": [ { "name": "success", "type": "bool" } ], "payable": false, "stateMutability": "nonpayable", "type": "function" }, { "constant": true, "inputs": [], "name": "totalSupply", "outputs": [ { "name": "", "type": "uint256" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": true, "inputs": [], "name": "difficulty", "outputs": [ { "name": "", "type": "uint256" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": true, "inputs": [], "name": "MAX_ADJUSTMENT_PERCENT", "outputs": [ { "name": "", "type": "uint256" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": false, "inputs": [ { "name": "from", "type": "address" }, { "name": "to", "type": "address" }, { "name": "tokens", "type": "uint256" } ], "name": "transferFrom", "outputs": [ { "name": "success", "type": "bool" } ], "payable": false, "stateMutability": "nonpayable", "type": "function" }, { "constant": true, "inputs": [], "name": "rewardEra", "outputs": [ { "name": "", "type": "uint256" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": true, "inputs": [], "name": "decimals", "outputs": [ { "name": "", "type": "uint8" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": true, "inputs": [], "name": "getMiningTarget", "outputs": [ { "name": "", "type": "uint256" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": false, "inputs": [ { "name": "token", "type": "address" }, { "name": "amount", "type": "uint256" } ], "name": "depositToken", "outputs": [], "payable": false, "stateMutability": "nonpayable", "type": "function" }, { "constant": true, "inputs": [], "name": "MINING_RATE_FACTOR", "outputs": [ { "name": "", "type": "uint256" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": true, "inputs": [], "name": "_getNextMasternodeForPayout", "outputs": [ { "name": "", "type": "address" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": true, "inputs": [], "name": "MAX_REWARD_ERA", "outputs": [ { "name": "", "type": "uint256" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": true, "inputs": [], "name": "getMiningReward", "outputs": [ { "name": "", "type": "uint256" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": true, "inputs": [], "name": "getChallengeNumber", "outputs": [ { "name": "", "type": "bytes32" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": true, "inputs": [], "name": "maxSupplyForEra", "outputs": [ { "name": "", "type": "uint256" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": true, "inputs": [ { "name": "", "type": "address" }, { "name": "", "type": "address" } ], "name": "tokens", "outputs": [ { "name": "", "type": "uint256" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": true, "inputs": [], "name": "selectedMasternodeCandidate", "outputs": [ { "name": "", "type": "uint256" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": true, "inputs": [], "name": "baseMiningReward", "outputs": [ { "name": "", "type": "uint256" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": true, "inputs": [], "name": "rewards_Masternodes", "outputs": [ { "name": "", "type": "uint256" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": true, "inputs": [], "name": "rewards_globalReward", "outputs": [ { "name": "", "type": "uint256" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": false, "inputs": [ { "name": "_spender", "type": "address" }, { "name": "_subtractedValue", "type": "uint256" } ], "name": "decreaseApproval", "outputs": [ { "name": "", "type": "bool" } ], "payable": false, "stateMutability": "nonpayable", "type": "function" }, { "constant": true, "inputs": [], "name": "onTestnet", "outputs": [ { "name": "", "type": "bool" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": true, "inputs": [], "name": "tokensMinted", "outputs": [ { "name": "", "type": "uint256" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": true, "inputs": [ { "name": "tokenOwner", "type": "address" } ], "name": "balanceOf", "outputs": [ { "name": "balance", "type": "uint256" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": true, "inputs": [ { "name": "nonce", "type": "uint256" }, { "name": "challenge_digest", "type": "bytes32" }, { "name": "challenge_number", "type": "bytes32" }, { "name": "testTarget", "type": "uint256" } ], "name": "checkMintSolution", "outputs": [ { "name": "success", "type": "bool" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": true, "inputs": [], "name": "epochCount", "outputs": [ { "name": "", "type": "uint256" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": true, "inputs": [], "name": "_MAXIMUM_TARGET", "outputs": [ { "name": "", "type": "uint256" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": true, "inputs": [], "name": "challengeNumber", "outputs": [ { "name": "", "type": "bytes32" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": true, "inputs": [], "name": "symbol", "outputs": [ { "name": "", "type": "string" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": true, "inputs": [], "name": "statistics", "outputs": [ { "name": "lastRewardTo", "type": "address" }, { "name": "lastRewardAmount", "type": "uint256" }, { "name": "lastRewardEthBlockNumber", "type": "uint256" }, { "name": "lastRewardTimestamp", "type": "uint256" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": true, "inputs": [ { "name": "nonce", "type": "uint256" }, { "name": "challenge_digest", "type": "bytes32" }, { "name": "challenge_number", "type": "bytes32" } ], "name": "getMintDigest", "outputs": [ { "name": "digesttest", "type": "bytes32" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": false, "inputs": [ { "name": "token", "type": "address" }, { "name": "amount", "type": "uint256" } ], "name": "withdrawToken", "outputs": [], "payable": false, "stateMutability": "nonpayable", "type": "function" }, { "constant": false, "inputs": [ { "name": "to", "type": "address" }, { "name": "tokens", "type": "uint256" } ], "name": "transfer", "outputs": [ { "name": "success", "type": "bool" } ], "payable": false, "stateMutability": "nonpayable", "type": "function" }, { "constant": true, "inputs": [], "name": "QUOTIENT_LIMIT", "outputs": [ { "name": "", "type": "uint256" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": true, "inputs": [], "name": "rewards_ProofOfWork", "outputs": [ { "name": "", "type": "uint256" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": false, "inputs": [ { "name": "spender", "type": "address" }, { "name": "tokens", "type": "uint256" }, { "name": "data", "type": "bytes" } ], "name": "approveAndCall", "outputs": [ { "name": "success", "type": "bool" } ], "payable": false, "stateMutability": "nonpayable", "type": "function" }, { "constant": true, "inputs": [], "name": "latestDifficultyPeriodStarted", "outputs": [ { "name": "", "type": "uint256" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": false, "inputs": [ { "name": "_spender", "type": "address" }, { "name": "_addedValue", "type": "uint256" } ], "name": "increaseApproval", "outputs": [ { "name": "", "type": "bool" } ], "payable": false, "stateMutability": "nonpayable", "type": "function" }, { "constant": true, "inputs": [], "name": "blocksPerReadjustment", "outputs": [ { "name": "", "type": "uint256" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": true, "inputs": [], "name": "_MINIMUM_TARGET", "outputs": [ { "name": "", "type": "uint256" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": true, "inputs": [ { "name": "tokenOwner", "type": "address" }, { "name": "spender", "type": "address" } ], "name": "allowance", "outputs": [ { "name": "remaining", "type": "uint256" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": true, "inputs": [], "name": "masternode_user_counter", "outputs": [ { "name": "", "type": "uint256" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": true, "inputs": [], "name": "_getNextCandidateINT", "outputs": [ { "name": "", "type": "address" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": true, "inputs": [ { "name": "_address", "type": "address" } ], "name": "isMasternode", "outputs": [ { "name": "", "type": "bool" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": true, "inputs": [], "name": "masternode_epoch", "outputs": [ { "name": "", "type": "uint256" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "constant": true, "inputs": [], "name": "mining_epoch", "outputs": [ { "name": "", "type": "uint256" } ], "payable": false, "stateMutability": "view", "type": "function" }, { "inputs": [], "payable": false, "stateMutability": "nonpayable", "type": "constructor" }, { "payable": true, "stateMutability": "payable", "type": "fallback" }, { "anonymous": false, "inputs": [ { "indexed": true, "name": "from", "type": "address" }, { "indexed": false, "name": "reward_amount", "type": "uint256" }, { "indexed": false, "name": "epochCount", "type": "uint256" }, { "indexed": false, "name": "newChallengeNumber", "type": "bytes32" } ], "name": "Mint", "type": "event" }, { "anonymous": false, "inputs": [ { "indexed": false, "name": "candidate", "type": "address" }, { "indexed": false, "name": "amount", "type": "uint256" } ], "name": "RewardMasternode", "type": "event" }, { "anonymous": false, "inputs": [ { "indexed": false, "name": "token", "type": "address" }, { "indexed": false, "name": "user", "type": "address" }, { "indexed": false, "name": "amount", "type": "uint256" }, { "indexed": false, "name": "balance", "type": "uint256" } ], "name": "Deposit", "type": "event" }, { "anonymous": false, "inputs": [ { "indexed": false, "name": "token", "type": "address" }, { "indexed": false, "name": "user", "type": "address" }, { "indexed": false, "name": "amount", "type": "uint256" }, { "indexed": false, "name": "balance", "type": "uint256" } ], "name": "Withdraw", "type": "event" }, { "anonymous": false, "inputs": [ { "indexed": true, "name": "from", "type": "address" }, { "indexed": true, "name": "to", "type": "address" }, { "indexed": false, "name": "value", "type": "uint256" } ], "name": "Transfer", "type": "event" }, { "anonymous": false, "inputs": [ { "indexed": true, "name": "owner", "type": "address" }, { "indexed": true, "name": "spender", "type": "address" }, { "indexed": false, "name": "value", "type": "uint256" } ], "name": "Approval", "type": "event" } ]

Click '**Access**' to interact with the contract. 

### Step 2
From the dropdown box, select '**Approve**'. By calling the approve method, you will authorise the contract to spend SCI59 tokens on your behalf. This is necessary for the contract to accept deposits and issue withdrawels on your masternode collateral rewards. During testnet, approving 1 SCI59 token is enough.

**NOTE:** The contract will fail if you did not approve it to accept your tokens using the approve call first.

![Alt text](https://monosnap.com/image/bkNUjGW5GrJ6kQCDbsYlJMpaKIr0rC.png)

The **spender** must be set to the contract's own address, since this is the one that will use your tokens as collateral: **0xacbaf9715d3d92e2baee463c2189ed8df9ae6a36**

The **tokens** field must be set to the amount of tokens needed as collateral which, during testnet, is 1 SCI59. Since our contract uses 8 decimals it is therefore **mandatory to append with 8 zeroes**. 1 Token equals **100000000**  (NO decimal points).

Unlock your wallet and confirm and send the transaction. You will receive a confirmation that the transaction has been sent across the network. You can click it to see that status, but generally your transaction will be confirmed at around **2 minutes**.

### Step 3
Select '*allowance*' in the dropdown list. Use your Ethereum address generated at the beginning of the guide as **tokenOwner** and use **0xacbaf9715d3d92e2baee463c2189ed8df9ae6a36** as the spender. The result should see **100000000** 

### Step 4
Now select '*depositToken*' and deposit your token. (**100000000**) using the address **0xacbaf9715d3d92e2baee463c2189ed8df9ae6a36**

### Step 5
In the dropdown box, select **isMasternode** and enter the Ethereum address generated at the beginning of the guide. If the transaction has been confirmed, aa value of **true** should be returned and you are queued for the masternode payouts. If the value is **false** then wait a few more minutes and repeat this step.

Every masternode receives a reward in turn. After some time, you will see that tokens have appeared in your account, depending on your position in the queue. During testnet, this should not take more than every 30 minutes.

**You are now registered as masternode, and will continue to receive rewards until you decide to withdraw your collateral amount of tokens deposited.**

Stop as masternode
---
If for whatever reason you want to stop being a masternode on SCI59, you can do so by repeating the steps in section **Become a masternode**, only replacing the `depositToken` in the dropdown box with the `withdrawToken` function.

This will send your tokens back and remove you from the masternode reward list. Please note that you can only enter as masternode again on the next round.
