Blockchain Resources - Algorand
===============================

https://www.algorand.com

What is Algorand?
-----------------

Algorand is a permissionless, pure proof-of-stake blockchain protocol
that, without forking, provides the necessary security, scalability,
and decentralization for billions of users. [Official
documentation](https://developer.algorand.org/docs/getting-started).


A [video](https://www.youtube.com/watch?v=Lbje18-zxc8&t=8s) overview of Algorand by founder Silvio Micali.


Environment
-----------


Network Configurations
----------------------

There are four types of networks available with various [configuration options](https://developer.algorand.org/docs/node-configuration-settings).

1. [Full archival Mainnet](configuration/archival_node.json) with all transactions and blocks - 2CPU/4Gb/60Gb
2. Default [pruned Mainnet](configuration/default.json) with last 1000 blocks and all account balances -  2CPU/4Gb/5Gb
3. [Testnet](configuration/testnet.json) with [faucet](https://bank.testnet.algorand.network/)
4. [Betanet](https://developer.algorand.org/docs/getting-started-betanet) periodically restarted with new genesis block.

Search in AWS region ***us-east-2*** for public AMIs with name ***Algorand***.

Mainnet nodes take about 40 hours to sync using a 2CPU/4GB (t2.medium) EC2 instance on AWS.  Catch up after 1 week takes about 2 hours.
  

Capabilities
------------

### Wallets

### Transfers

### Tokens

The token standard, *Algorand Standard Asset (ASA)* is part of the
network software with

### Atomic Swaps

### Smart Contracts

In-house, stack-based language [TEAL](https://developer.algorand.org/docs/teal) for smart contracts.  Specific examples:

1. [Escrow]()
2. [Periodic payments]()
3. [DEX]()

### API/CLI

Two APIs are available, [REST]() and [Key management KMD]() as well as
a command line utility.

### SDK

Algorand provides SDKs for
[go](https://developer.algorand.org/docs/go-sdk),
[python](https://developer.algorand.org/docs/python-sdk),
[java](https://developer.algorand.org/docs/java-sdk) and
[javascript](https://developer.algorand.org/docs/javascript-sdk)


