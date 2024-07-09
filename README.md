# Bitcoin Mining Project

## Overview

This project is a Bitcoin mining program designed to demonstrate how mining works and to participate in the Bitcoin network by solving cryptographic puzzles to secure transactions and create new blocks.

## Features

- Mining algorithm implementation (e.g., SHA-256)
- Network connectivity to the Bitcoin network
- Wallet integration
- Configurable mining settings
## Prerequisites

- [Bitcoin Core](https://bitcoin.org/en/bitcoin-core/) or any other Bitcoin node software
- Python (version 3.6 or higher) or any other required programming language/runtime environment
- Necessary libraries and dependencies (listed below)

## Install dependencies:
For Python:
    pip install
    hashlib install

## Functions and Methods:


**SHA256(text):**
Takes a string text as input and returns its SHA-256 hash.
Uses the sha256 function from the hashlib library to perform the hashing.
mine(block_number, transactions, previous_hash, prefix_zeros):
This function attempts to mine a new block by finding a nonce that results in a hash with a specified number of leading zeros (prefix_zeros).

**Parameters**:
block_number: The number of the block being mined.
transactions: A string representing the transactions included in the block.
previous_hash: The hash of the previous block in the blockchain.
prefix_zeros: The number of leading zeros required in the new hash (i.e., the difficulty level).
The function iterates over possible nonce values (from 0 to MAX_NONCE).
For each nonce, it concatenates the block number, transactions, previous hash, and nonce, then computes the SHA-256 hash of this concatenated string.
If the resulting hash starts with the required number of leading zeros, it prints a success message and returns the new hash.
If no valid nonce is found after MAX_NONCE attempts, it raises an exception.

**Main Block:**
Main Block Execution (if __name__=='__main__'):
Defines a string transactions containing a list of sample transactions.
Sets the mining difficulty (difficulty) to 4 (this value can be changed to make mining harder or easier).
Records the start time using time.time().
Calls the mine function with specific parameters: block number 5, the defined transactions, a given previous hash, and the difficulty level.
Prints the start and end times of the mining process and the time taken to mine the block.
Prints the resulting new hash if mining is successful.

**Usage of Libraries:**
hashlib: Used for computing SHA-256 hashes.
time: Used to measure the time taken for the mining process.

**Constants:**
MAX_NONCE: The maximum number of nonce values to try before giving up on mining a block. Set to a large number (100,000,000,000) to ensure sufficient attempts.

**Notes:**
Increasing the difficulty value makes the mining process harder and more time-consuming, as it requires finding a hash with more leading zeros.
The code simulates the mining process by iterating over possible nonce values and checking if the resulting hash meets the required difficulty criteria.

   
## Acknowledgements
Bitcoin

## Contact
For any questions or issues, please contact us at manohar1434@sasi.ac.in
