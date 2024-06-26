# Votechain
This project aims to devlope a secure voting system based on blockchain technology using Python. This system is secure, decentralized and do not require any third party.
It will be almost impossible to manipulate the votes casted by this system.
## Plan
A voter ID will be provided to all the eligible voters along with a unique public key(public key is anonymous) and a unique private key(private key is private and should not be shared with anyone). When a voter will caste vote, a function named sign() will generate a signature based on voter's private key and a message containing voter ID and the candidate the voter has voted for. The Private key ensures that no one else can produce that signature and the message ensures that signature produced everytime will be different, making it impossible for anyone to reuse it. After this a function named verify() will verify the validity of vote using that message, signature and public key. <br>
SHA256 is a cryptographic hash function which returns a 256-bit number when applied on a string, this number is called its hash. It is almost impossible to trace back the string using its hash, the only way is guessing the string. The newly casted votes will be added to a block. This block will also contain timestamp, hash of previous block and nonce. Nonce is a number which should be found by computers(by trial and error) such that the hash of the block will start with a particular number of zeroes and the process of finding nonce is called mining. <br>
In this manner block start linking and forms a blockchain. If any block is manipulated then its hash will change and it will change hash of all subsequent blocks, rendering the whole blockchain invalid. This algorithm of creating blocks and validation of blockchain is called proof of work.<br>
In this way this Votechain system will work.<br>
## Checkpoint
The implementation plan for Votechain is built, and the required classes are initiallized. The following files are uploaded:<br>
block.py: contains the 'block' class for creating and managing individual blocks in the blockchain<br>
blockchain.py: contains the 'blockchain' class for managing chain of blocks and handling vote mining<br>
