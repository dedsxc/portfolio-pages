# How to Run a Blockchain Node on Your Laptop 🚀

Running a blockchain node on your laptop is a fantastic way to explore the world of blockchain and understand how these networks function. This guide explains blockchain in simple terms, provides the hardware requirements, and walks you through setting up a node on your MacBook.


## What is a Blockchain? 🤔

A blockchain is a network of computers that work together to maintain a large, shared database. This database, often called a "ledger" keeps a permanent record of every transaction made on the network. 

For example, in the Ethereum blockchain, you can use websites like [Etherscan.io](https://etherscan.io) to view all transactions. If Alice sends money to Bob, the transaction will be recorded. However, instead of seeing "Alice" and "Bob," you’ll see their **public addresses**, which look like a string of characters (e.g., `0xAB12...DEF3`). This design keeps the system **transparent** but also **private** since it doesn’t reveal personal identities.

The blockchain’s structure ensures:
1. **Security**: Data is cryptographically secured and tamper-proof.
2. **Transparency**: Anyone can verify transactions.
3. **Decentralization**: No single entity controls the database; it's distributed across many computers.

This is why blockchains are so popular for cryptocurrencies, as well as other use cases like smart contracts, voting systems, and supply chain tracking.

Blockchains are the foundation of **decentralized finance (DeFi)**, which is different from traditional, centralized finance (CeFi). In centralized finance, banks or institutions control your money and act as intermediaries for transactions. In decentralized finance, no single entity controls the system. Instead, smart contracts (or in simple term, an application running on blockchain) automatically manage transactions, allowing anyone with an internet connection to participate without relying on middlemen.

DeFi provides transparency and global access, while CeFi offers simplicity and trusted customer support. Both have their strengths, but DeFi gives people more direct control over their assets.


## Prerequisite Hardware 💻

To run a blockchain node, your laptop needs to meet certain hardware requirements:

- **Processor**: A multi-core processor like an Intel i5 or Apple M1/M2 is sufficient for lightweight nodes.
- **Memory (RAM)**: At least 8GB, though 16GB is ideal for better performance.
- **Storage**: Blockchain nodes require significant storage. For example:
  - Bitcoin: ~500GB+
  - Ethereum: ~1TB+
  Use an external SSD if your internal storage is limited.
- **Internet Connection**: A stable connection with no data caps is crucial, as nodes regularly sync data.

## Run a Blockchain Node on Your MacBook 🛠️

Here’s a step-by-step guide to running an Ethereum node (as an example):

1. Install Homebrew

Homebrew is a package manager for macOS. Open your terminal and install it:
~~~bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
~~~

2. Install Ethereum client 
~~~bash
brew install erigon
~~~

3. Start the ethereum node

The following command will launch the ethereum blockchain node and will save the data in `data` directory.
~~~bash
erigon --internalcl --prune=hrtc --datadir=data --http.addr="0.0.0.0" --http.api=eth,web3,net,debug,trace,txpool
~~~

4. Interact with the node when it is ready
~~~bash
curl -X POST http://localhost:8545 -H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_blockNumber","params":[],"id":1}'
~~~

Et voila, that's it! Welcome to the world of decentralized finance!