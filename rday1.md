# Transaction structure: Deep Dive
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
- Value: 250


## Gas
- Gas Used:40,324
- Max Fee:45,721
- Effective Gas Price:0.062619889 Gwei (0.000000000062619889 ETH)

## Inference
The sender called the token contract and executed the transfer function, which moved X tokens from the sender’s address to the receiver’s address. The transaction succeeded and emitted a Transfer event confirming the movement.

