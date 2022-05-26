# Transactions.

## Table Of Contents
* [Definition](#definition)
* [Gas]
## Transactions
- An Ethereum transaction refers to an action initiated by an externally-owned account.
- Transactions, which change the state of the EVM, need to be broadcast to the whole network.
- Any node can broadcast a request for a transaction to be executed on the EVM; after this happens.
- A miner will execute the transaction and propagate the resulting state change to the rest of the network.
- Transactions require a fee and must be mined to become valid.
- A submitted transaction includes the following information:
  1. recipient – the receiving address (if an externally-owned account, the transaction will transfer value. If a contract account, the transaction will execute the contract code).
  2. signature – the identifier of the sender. This is generated when the sender's private key signs the transaction and confirms the sender has authorized this transaction.
  3. value – amount of ETH to transfer from sender to recipient (in WEI, a denomination of ETH).
  4. data – optional field to include arbitrary data.
  5. gasLimit – the maximum amount of gas units that can be consumed by the transaction. Units of gas represent computational steps.
  6. maxPriorityFeePerGas - the maximum amount of gas to be included as a tip to the miner.
  7. maxFeePerGas - the maximum amount of gas willing to be paid for the transaction (inclusive of baseFeePerGas and maxPriorityFeePerGas).


## Resources


