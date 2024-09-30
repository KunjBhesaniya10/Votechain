#  Votechain
The project aims to implement __E-Voting System__ with help of **<u>Blockchain technology</u>**.

Blockchain is decentralized digital ledger that maintain records such as transactions or other important informations such that they remain immutable and transparent to whole network. Blockchain is chain of Blocks which are linked to their previous Blocks by cryptography technique known as Hashing.

The Blocks contain index,hash of previous block,nonce,Transactions/Infos,Timestamp, merkle tree etc. The first block is known as __genesis block__ which don't have previous hash value. This block is generated by Blockchain's owners and it have special hash value to make it distinguishable from other blocks. On this block, the whole blockchain is generated. The Blockchain network has many _nodes_ of which some are _miners_. The minor node create Blocks,generate it's hash and broadcast it to network and they get incentives after doing so. To prevent network from one party domination in terms of computational power, each Block's hash has conditions which is needed to produce a valid block and the diffculty is adjusted according to generation of blocks over given timeline. 

**<u>Proof of Work</u>** used in Bitcoin system - the system puts condition on hash of the block that it must have some no. of preffix 0's. for example if difficulty is 4 then hash must be of the type "0000xxxxxxxxxxx".

On producing valid Block, the _miner_ broadcast it to the network. Each other nodes get notified about the new block and they validate the block by checking the proof of work and other infos. If 51% of the nodes gives validation then the block is appended in blockchain. This is known as __consensous algorithm__.

Let us see Why it is hard to tamper some info's stored in blockchain ? If someone tries to change the info present in block, the hash value of that block changes and this will change hash of all the blocks present in chain after that block. To propagate the changes 51% of the network must need to agree which is impossible. Also, the infos present in blocks are encrypted with security keys and only owner can access the info.

The case where 2 Blocks of same index are released in system, The chain branches out into two chains. The longest of the two is consider as valid blockchain as more computational power is spended to make that chain. Then, the system discards the second branch. This is known as __longest chain rule__.

Blockchain along with Cryptography is helpful in creating e-voting system. This will ensure the anonymity and security of votes with no chances of tampering. The vote can be stored in blocks which are encrypted and decrypted only at the time of counting. The anonymity can be preserved by applying hashing along with other cryptography techniques to create voter_id. reverese engineering the voter info from hash is difficult. Also, while verification of vote, It is checked whether there is vote with given hashed_id in previous votes stored in blockchain. 



The repository has several files -
### 1. [Blockchain.py](https://github.com/KunjBhesaniya10/SOC-24-Votechain/blob/main/Blockchain.py) - 

- Blockchain class

### 2. [election.py](https://github.com/KunjBhesaniya10/SOC-24-Votechain/blob/main/election.py) -

- Vote class
- Voter class
- Election class

### 3.[Block.py](https://github.com/KunjBhesaniya10/SOC-24-Votechain/blob/main/Block.py) -
- Block class
### 4. [util.py](https://github.com/KunjBhesaniya10/SOC-24-Votechain/blob/main/util.py) -
- contain utility functions.

### 5. [flow_chart](https://github.com/KunjBhesaniya10/SOC-24-Votechain/blob/main/flow_chart.pdf) -
- describes sequence of function calls.
## Prerequisites

Before running the project, ensure you have the Crypto library installed. You can install it using pip with the following command:

```bash
pip install pycryptodome

