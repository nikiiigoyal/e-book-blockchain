*Blockchain*: A chain of blocks containing transaction records, secured by cryptography
*Cryptocurrency*: Digital money (like Bitcoin or Ether)
*Decentralized*: No single authority controls it - it's distributed across many computers
*Node*: A computer that participates in the blockchain network
*Transaction*: Transfer of value or data between accounts
*Smart Contract*: Self-executing code stored on the blockchain

Ethereum-Specific Terms:

*Ether*(ETH): Ethereum's native cryptocurrency
*Gas*: Fee paid to execute operations on Ethereum
*EVM* (Ethereum Virtual Machine): The "computer" that runs smart contracts
*DApp*: Decentralized Application - apps built on blockchain
*Web3*: The vision of a decentralized internet
*Bytecode*: Machine language the EVM understands
*Key-Value Store*: Way of organizing data
*Merkle Patricia Tree*: Data structure for efficient storage



# Bitcoin : Digital cash

Traditional Money Problems:

If you want to send $100 to someone in another country, you need a bank
The bank keeps a record: "John sent $100 to Mary"
You have to trust the bank to not lose your money or lie about transactions
Banks charge fees and can take days to process.

**Bitcoin's Solution:
Instead of one bank keeping records, thousands of computers around the world keep the same record book (ledger). It's like having 1000 accountants all watching each other to make sure no one cheats!**

## why cryptocurrency is called 'DIgItAl GoLD'

-Limited supply (only 21 million will ever exist)
-Difficult to "mine" (create new ones)
-Stores value over time
-No government controls it

### what is BLOCKCHAin technology

there are several blocks each block has - *Data,Hash(unique no.),PreviousHash(hash of connected block)*
*Genesis block* : 1st block in blockchain(do not have previos hash)

### Components of a Blockchain

The components of an open, public blockchain are (usually):

-A peer-to-peer (P2P) network connecting participants and propagating transactions and blocks of verified transactions, based on a standardized *"gossip" protocol*

Messages, in the form of transactions, representing state transitions

*consensus rules*: Rules everyone agrees to follow

*A state machine* that processes transactions according to the consensus rules -Keeps track of current state: who owns what, what programs are running

A chain of cryptographically secured blocks that acts as a journal of all the verified and accepted state transitions -Permanent record of everything that happened

*Consensus algorithm* that decentralizes control over the blockchain, by forcing participants to cooperate in the enforcement of the consensus rules -Proof-of-Work

-Reward-A game-theoretically sound incentivization scheme (e.g., proof-of-work costs plus block rewards) to economically secure the state machine in an open environment 

One or more open source software implementations of the above *("clients")*

When someone says "blockchain," ask them:

Is it open? (Can anyone join?)
Is it public? (Can anyone see the transactions?)
Is it decentralized? (No single company controls it?)
Is it censorship-resistant? (Can't be shut down?)

Many companies create "private blockchains" that are basically just fancy databases. True blockchains like Bitcoin and Ethereum are open to everyone and controlled by no one.