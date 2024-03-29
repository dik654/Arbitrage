# Arbitrage

![image](https://github.com/dik654/Arbitage/assets/33992354/4b4d5235-5915-4a41-ad91-75d0d5fa8f80)

## Introduction
> This repository contains the logic of earning arbitrage profits and distributing profits to investors using the difference in exchange costs between Uniswap V2 pools.
These contracts were written under the foundry framework
Testing and deployment can be done through the following process.

<br/>

## Installation
curl -L https://foundry.paradigm.xyz | bash
foundryup
<br/><br/>

## Test
```bash
cd contract
forge install
forge remappings > remappings.txt

forge clean && forge test --mc ArbitrageMockTest -vv --ffi
forge clean && forge test --mc RewardDistributionMockTest -vv --ffi
forge clean && forge test --mc ArbitrageTest --fork-url https://mainnet.infura.io/v3/<API_KEY> -vv --ffi
forge test --mc RewardDistributionTest --fork-url https://mainnet.infura.io/v3/<API_KEY> -vv --ffi
```

## Deployment
write .env file based on .env.example
```bash
forge clean && forge script script/DeployArbitrageurScript.s.sol:DeployArbitrageurScript --rpc-url https://eth-sepolia.g.alchemy.com/v2/<API_KEY> --sender <PUBLIC_ADDRESS> --ffi --broadcast
forge clean && forge script script/DeployRewardDistributor.s.sol:DeployRewardDistributorScript --rpc-url https://eth-sepolia.g.alchemy.com/v2/<API_KEY> --sender <PUBLIC_ADDRESS> --ffi --broadcast
```
<br>

## License
Distributed under the MIT License. See [License](https://github.com/dik654/Arbitage/blob/main/LICENSE) for more information.
<br><br>

## Contact
If you have any questions, please contact me by email <br/>
> ✉️ ```kimmalee1577@gmail.com```

