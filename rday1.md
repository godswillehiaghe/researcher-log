# Transaction structure: Deep Dive
Tool: Etherscan's "raw input" tab
Activity: Tracing one token transfer and decoding its input data using Etherscan’s decoder.

## Observation:
- Hash:   0xf4e1f4d445499bd3adf4b3a7fa78fd6f8163ad208db29e998c24f7e37984ea5e
- Block:  23882967
- Status: success

## Participants
- Sender:         0x4846e84A1B7EE15F61e75c91634A3d715Df2EB07
- Receiver:       0xF5042e6ffaC5a625D4E7848e0b01373D8eB9e222 (relay router)
- Token Contract: Dexswap(relay:router)
    - Router Contract:      0x
    - Token In;0x...(USDC):
    - Token Out;0x...(ETH):

## Execution
- Function:       multicall((address,bool,uint256,bytes)[], address, address)
- Raw Input(hex):
- Decoded Input:
    - to:
    - amount:

## Gas
- Gas Used:
- Max Fee:
- Effective Gas Price:

## Inference
