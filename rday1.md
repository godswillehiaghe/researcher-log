## 1.TRASACTION STRUCTURE: TYPE; TRANSFER
Tool: Etherscan's "raw input" tab
Activity: Tracing one token transfer and decoding its input data using Etherscan’s decoder.

## Observation:
- Hash:   0x605c83c6b8de4e2c1827003194def36da1344eefe7b2cc1a5568dcb809e0ff99
- Block:  24321727
- Status: success

## Participants
- Sender:         0xE3bEa3F81e775B90299Aded86502176E0338d479
- Receiver:       0x08633E0cf3A77e308B9ce4a7eE1001f07Fda37A9
- Token Contract: 0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48(Circle: USDC Token)

## Execution
- Function:      transfer(address, uint256 value)
- Raw Input(hex):0xa9059cbb00000000000000000000000008633e0cf3a77e308b9ce4a7ee1001f07fda37a900000000000000000000000000000000000000000000000000000000000000fa
- Decoded Input(Input Parameters):
    - to:0x08633E0cf3A77e308B9ce4a7eE1001f07Fda37A9
    - amount:250


## Logs Evidence
- Event: Transfer (index_topic_1 address from, index_topic_2 address to, uint256 value)
- From:  0xE3bEa3F81e775B90299Aded86502176E0338d479
- To:    0x08633E0cf3A77e308B9ce4a7eE1001f07Fda37A9
- Value: $250


## Gas
- Gas Used:40,324
- Gas Max:45,721
- Effective Gas Price:0.062619889 Gwei (0.000000000062619889 ETH)

## Inference
The sender called the token contract and executed the transfer function, which moved X tokens from the sender’s address to the receiver’s address. The transaction succeeded and emitted a Transfer event confirming the movement.









## 2.TRASACTION STRUCTURE: TYPE; SWAP
Tool: Etherscan's "raw input" tab
Activity: Tracing token swap on a certain DEX(Uniswap V2 Router)

## Transaction Overview
- Transaction Hash: 0x260df459d831b01c129e222af20c3fabd1b6a89383be8fd4c30ef64534e8c018
- Block Number:     24330148  
- Status:           success

## Participants
- Sender: 0x994609D5FF23548D5E02c93EeC5337bAe4420Dc6
- DEX Router/Receiver: 0x7a250d5630B4cF539739dF2C5dAcb4c659F2488D (Uniswap V2: Router2)
- Pool Contracts(Token Contracts): 0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2(WETH). 0x8272877AcC4953A7baCEcAc44c0A30C64411AAc0(PENGUIN)

## Transaction Details
- Function Called:  swapExactETHForTokensSupportingFeeOnTransferTokens(uint256 amountOutMin, address[] path, address to, uint256 deadline)
- Input Parameters:
  - amountOutMin: 0(No protection against slippage) 
  - Path(Tokens): WETH → PENGUIN
  - To(Receiver): 0x994609D5FF23548D5E02c93EeC5337bAe4420Dc6
  - Amount: 0.16834444437026252 ETH → 186,941.437080422 PENGUIN

## Logs Evidence
- Event: Swap
- Value: $459.30
- Token In: WETH
  - From: 0x7a250d5630B4cF539739dF2C5dAcb4c659F2488D
  - To:   0x722ce988665ACAfd2d5187f8Ea9ADADeF50b17F6
  - Amount: 0.16834444437026252 
- Token Out:PENGUIN
  - From: 0x722ce988665ACAfd2d5187f8Ea9ADADeF50b17F6
  - To:   0x994609D5FF23548D5E02c93EeC5337bAe4420Dc6
  - Amount: 186,941.437080422

## Gas Information
- Gas Used: 132,644
- Gas Max:  1,000,000
- Effective Gas Price: 0.044837813 Gwei (0.000000000044837813 ETH)

## What Happened (Plain Explanation)
The user sent 0.168344 ETH to the Uniswap V2 Router.
The router wrapped the ETH into WETH, routed it through the PENGU–WETH liquidity pool, and executed a swap.
In return, the user received 186,941.437 PENGU tokens directly into their wallet.

No minimum output was enforced, meaning the user accepted any price, which exposes them to slippage risk.

