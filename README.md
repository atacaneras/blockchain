# Simple Blockchain Implementation in Python

This repository contains a basic implementation of a blockchain in Python. The purpose of this project is to demonstrate the fundamental concepts of a blockchain without relying on additional libraries.

## Features

- Blocks: The Block class represents a single block in the blockchain. It contains a timestamp, data, previous hash, and its own hash. The calculate_hash() method uses the SHA-256 algorithm to hash the block's contents.
- Blockchain: The Blockchain class manages the chain by storing blocks and providing methods for adding blocks and validating the chain. The chain is initialized with a genesis block (the first block in the chain).
- Validation: The is_chain_valid() method checks the integrity of the blockchain by iterating through the chain and verifying the hashes and previous hashes of each block.

## Usage

To use this blockchain implementation, follow these steps:

1. Clone the repository:
```
git clone https://github.com/your-username/blockchain-python.git
```
2. Import the necessary classes:
```
from blockchain import Block, Blockchain
```
3. Create an instance of the Blockchain class:
```
my_blockchain = Blockchain()
```
4. Add blocks to the blockchain using the add_block() method:
```
my_blockchain.add_block(Block(datetime.datetime.now(), "Transaction 1", ""))
my_blockchain.add_block(Block(datetime.datetime.now(), "Transaction 2", ""))
my_blockchain.add_block(Block(datetime.datetime.now(), "Transaction 3", ""))
```
5. Check the validity of the blockchain using the is_chain_valid() method:
```
print("Is the blockchain valid?", my_blockchain.is_chain_valid())
```
The method will return True if the blockchain is valid or False if it has been tampered with.

Feel free to modify the code or add additional functionality as needed. This implementation serves as a starting point to understand the basic structure and validation of a blockchain.

## Limitations

- This implementation is simplified for learning purposes and may not include all the features and optimizations found in real-world blockchain systems.
- It does not include concepts like proof-of-work, consensus algorithms, or transaction verification, which are essential in practical blockchain implementations.
- Use this implementation for educational purposes and experimentation rather than for production environments.

Please refer to the code comments for more detailed explanations of the implementation.

## License

This project is licensed under the MIT License.
