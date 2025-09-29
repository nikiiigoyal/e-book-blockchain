# what is *Ethereum*?

Ethereum is like a single global computer that everyone can use,
stores inofrmation & when people make trancaction or run programs it updates that infromation in a predictble way that everyone agrees on.
Open source, globally decentralized computing infrastructure that executes programs called *smart contracts*. 
It uses a blockchain to synchronize and store the system’s state changes, along with a cryptocurrency called *ether* to meter and constrain execution resource costs.

## how ethereum is diifernt from Bitcoin BlockChian
 
 *State Machine*
**Bitcoin's** blockchain tracks only one thing "Who has how many Bitcoin"
 When someone sends Bitcoin, the scoreboard updates
 That's all it can track

**Ethereum**can track anything : money ,contarcts,data,games,programs.

**key–value tuple**. key - label on the folder
value - whats inside the folder.
Ethereum has memory that stores both code and data, and it uses the Ethereum blockchain to track how this memory changes over time. 

-Normal computer's RAM stores:
Programs currently running
Data being used
Variables and their values

Ethereum's "RAM":

Stores smart contracts (programs)
Stores contract data
Tracks all changes forever
Everyone has the same copy

### Components of Ethereum

P2P network
Ethereum runs on the Ethereum main network, which is addressable on TCP port 30303, and runs a protocol called ÐΞVp2p.

Consensus rules
Ethereum’s consensus rules are defined in the reference specification, the Yellow Paper.

Transactions
Ethereum transactions are network messages that include (among other things) a sender, recipient, value, and data payload.

State machine
Ethereum state transitions are processed by the Ethereum Virtual Machine (EVM), a stack-based virtual machine that executes bytecode (machine-language instructions). EVM programs, called "smart contracts," are written in high-level languages (e.g., Solidity) and converted to bytecode for execution on the EVM.

Data structures
Ethereum’s state is stored locally on each node as a database (usually Google’s LevelDB), which contains the transactions and system state in a serialized hashed data structure called a *Merkle Patricia Tree*.

Consensus algorithm
Proof of work 
Ethereum uses Bitcoin’s consensus model, Nakamoto Consensus, which uses sequential single-signature blocks, weighted in importance by PoW to determine the longest chain and therefore the current state. 

Economic security
Ethereum currently uses a PoW algorithm called *Ethash*, but this will eventually be dropped with the move to PoS at some point in the future.

Clients
Ethereum has several interoperable implementations of the client software, the most prominent of which are Go-Ethereum (Geth) and Parity.

#### Turing Complete
**Turing completeness is the property of a system that means it can solve any computational problem, given enough time and memory.**

**Calculator: Can only do math (not Turing complete)
Your computer: Can run any program - games, browsers, video editors (Turing complete)
Bitcoin: Like a calculator - only handles money transfers (not Turing complete)
Ethereum: Like a full computer - can run any program (Turing complete)
**
**If a programming language has these three capabilities, it is almost certainly Turing complete.**
***Conditional Branching** (`if` statements): The ability to make decisions. "If this is true, do that; otherwise, do something else."
**Unbounded Looping** (`while` or `for` loops): The ability to repeat a set of instructions over and over until a condition is met. This is the "enough time" part.
**Way to Read/Write to Memory** (variables): The ability to store and retrieve data. This is the "enough memory" part.*

Ethereum’s ability to execute a stored program, in a state machine called the Ethereum Virtual Machine, while reading and writing data to memory makes it a Turing-complete system and therefore a UTM. Ethereum can compute any algorithm that can be computed by any Turing machine, given the limitations of finite memory.

problem : Turing-complete systems can run in "infinite loops,","Use excessive memory","attack the world computer"


solution: Ethereum introduces a metering mechanism called *gas*. As the EVM executes a smart contract, it carefully accounts for every instruction (computation, data access, etc.). 
-You pay for gas with ETH
-Set a gas limit when sending a transaction
-If gas runs out, execution stops
Unused gas gets refunded
-Each instruction has a predetermined cost in units of gas. 

-Run out of gas, program stops,
-Expensive operations cost more gas
-Attackers must pay for their attacks

##### Ethereum currency unit - Ether
1 ether = 1,000,000,000,000,000,000 *wei* (that's 18 zeros)
Wei is the smallest unit.
All calculations internally happen in wei, even though we usually think in ether.


**Wallets**
A wallet is software that:

Manages your private keys (keeps them secure)
Shows your account balance
Helps you send transactions
Critical point: The wallet doesn't actually hold your money - your money exists on the blockchain. The wallet just holds the keys to access it.

###### Types of Accounts
Two Types of Accounts 
**Externally Owned Accounts (EOAs)**
*Think of these as personal bank accounts:*

Has a private key (like bank PIN) - whoever controls this controls the account
Can initiate transactions - can send money or interact with contracts

**Contract Accounts**
  *Like as automated bank accounts with built-in rules:*

No private key - instead, they're controlled by code (smart contracts)
Cannot initiate transactions - they can only respond when someone else contacts them
Have their own Ethereum address - can send ether to them
Run programs when contacted - like a vending machine that executes code when you insert coins.
.
**zero address** - The zero address is a special address that tells the Ethereum blockchain that you want to register a contract.

###### Ethereum Clients

Think of Ethereum clients like different *web browsers* (Chrome, Firefox, Safari, Edge):

They're all different software made by different companies
They're written in different programming languages
But they all display the same websites correctly
They all follow the same rules (web standards like HTML, CSS)

Similarly, Ethereum clients are different programs that all:

Connect to the same Ethereum network
Follow the same rules
Can talk to each other
Let you interact with Ethereum
Some real-world etheruem Networks -Geth (Go Ethereum) - Written in Go language,
Nethermind - Written in C#, Besu - Written in Java,
Erigon - Written in Go (optimized version)

**Real-world scenario: You could run Geth on your computer, your friend runs Nethermind, and you'd both see the exact same blockchain data and could send transactions to each other!**

###### Ethereum Networks
Different Versions of the Same Game

-They all follow similar rules, but have slight differences. Players on one version usually can't play with players on another.
Real Ethereum Networks:

Ethereum - The main network (like the original Minecraft)
Ethereum Classic - A split from Ethereum (like a modded version)
Musicoin, Ubiq, Expanse - Specialized versions for specific purposes

Why they exist: Each network made small changes for different purposes.


###### Types of Nodes - Different Ways to Participate
1. Full Node
Analogy: Owning a Complete Restaurant
You have:

Full kitchen (validates all transactions)
Complete menu history (entire blockchain)
Can serve anyone (help other nodes)

Advantages:
You verify everything yourself (maximum trust)
Help keep Ethereum decentralized
Can read blockchain data anytime, even offline

Disadvantages:

 Expensive (300 GB+ storage)
 Takes days to set up initially
 Needs constant maintenance


2. Testnet Node
Analogy: Playing with Monopoly Money
Testnets are like practice versions of Ethereum:
Real Networks:

Ropsten - Most like real Ethereum
Kovan - Faster, controlled by specific people
Rinkeby - Another practice network

What's different:
Advantages
Money is free (get test ETH from "faucets")
Much smaller (75 GB instead of 300 GB)
Syncs faster
Perfect for learning!

Real Example:
Want to test deploying a smart contract?
Mainnet: Costs real money ($20-$100)
Testnet: Completely free!

Disadvantages:
Can't test with "real" security (no hackers trying to steal worthless tokens)
Doesn't experience real network congestion.


3. Local Blockchain (Ganache)
Analogy: Playing a Single-Player Video Game
Ganache is like having your own private Ethereum:

Only you exist on it
You start with free test accounts already loaded with ETH
Instant transactions (no waiting)
Reset anytime

Advantages
good for Learning programming
Testing contracts privately
Debugging without costs

Disadvantages:
Not realistic (no other users)
Can't test how your app handles network congestion