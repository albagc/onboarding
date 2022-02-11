## Ethereum

_Note:_ This page is a cribsheet of the most relevant information. For full documentation, see the [Ethereum Help Pages](https://ethereum.org/en/learn/). 

<br>

### Ether

For the current value vs USD ($), see [here](https://currencio.co/eth/usd/).

<br>

### Consensus mechanisms

Ethereum is moving from proof-of-work (current) to proof-of-stake (new) - see [Test network](#test-networks) section for more details.

**Proof of work (POW)**

> Proof-of-work blockchains are secured and verified by virtual miners around the world racing to be the first to solve a math puzzle. The winner gets to update the blockchain with the latest verified transactions and is rewarded  by the network with a predetermined amount of crypto. 

Advantages include security (hackers would need to possess massive processing power) and robustness. Additionally, increasing value of the crypto results in an increasing incentive for more miners to partake.

Major downside is the speed at which blocks are validated and the huge amount of electrcity required, resulting in a large carbon footprint.

In proof of work, the penalty for miners submitting invalid information, or blocks, is the sunk cost of computing power, energy, and time.

**Proof of stake (POS)**

> In a proof of stake system, staking serves a similar function to proof of work’s mining, in that it’s the process by which a network participant gets selected to add the latest batch of transactions to the blockchain and earn some crypto in exchange. ... [I]n general, proof of stake blockchains employ a network of “validators” who contribute — or “stake” — their  own crypto in exchange for a chance of getting to validate new transaction, update the blockchain, and earn a reward. 

Three steps:
* The network selects a winner based on the amount of crypto each validator has in the pool and the length of time they’ve had it there — literally rewarding the most invested participants. 

* Once the winner has validated the latest block of transactions, other validators can attest that the block is accurate. When a threshold number of attestations have been made, the network updates the blockchain. 

* All participating validators receive a reward in the native cryptocurrency, which is generally distributed by the network in proportion to each validator’s stake. 

There is a minimum amount of crypto that must be staked in order to become a validator (for Ethereum, it is 32ETH, or roughly $100,000). Validators are penalised for being offline or for validating "bad" blocks (process known as **slashing**). **Delegating** involves joining a staking pool run by another user, and so collectively reaching the threshold required to be considered as a validator.

In proof of stake, the validators’ staked crypto funds serve as an economic incentive to act in the network’s best interests.

> Variations of the PoS:
> - Proofs of Storage are simple proving systems to prove that I have possession of some data. A Proof of Data Possession example is: I can prove to you that I have data X, either without revealing data X or if the data is several GB large, in some more succinct way. Then there’s Proof of Retrievability where, not only am I going to prove that I have X, but also that these proofs can be used to reconstruct X in case I’m malicious and want to withhold X from you.
> - Proof of Space: instead of only tokens as stake, stake is in the form of proven storage that determines a miner’s probability of mining a block. In building a decentralized storage network, a proof structure was built in which consensus is achieved through an operation yielding positive social externality: data storage. Proofs of Space are a different type of group where I can guarantee to you that I’m spending a certain amount of storage. If I commit to storing 1 GB, and I generate a random GB then I can prove to you that I’m storing that random GB and not storing some other thing. That lets you use storage space as a Proof of Work.
> - Proof of Spacetime: variation of Proof-of-space where nodes need to proof that a given encoding of the data existed in physical storage continuously over a period of time.
> - Proof of Replication: nodes need to proof that they are storing a unique encoding of the data. It is ultimately a proving system to verify that a storage miner actually has the content they are storing and are not cheating.

**Proof of authority (POA)**

Variation of proof of stake model, where rather than an economic stake, validators stake their reputation. 

Idea is to address the problem inherent to proof-of-stake, where those with the greatest stake are assumed to work in the best interests of the network because they have the most to lose. This is not necessarily the case, as for Person A, 32 ETH might represent all of their holdings, whereas for Person B, it might represent <1%. These persons cannot be expected to act in the same manner.

The POA approach is deisgned to be used with a small number of validators, as the need to prove the identity of each validator makes POA impractical for public blockchains. Also results in greater centralisation that than other models.

<br>


## Modified Merkle Patricia Trie Specification

> Merkle Patricia tries provide a cryptographically authenticated data structure that can be used to store all (key, value) bindings.

This is the approach used by Ethereum to save states. While this is likely beyond the scope of our project, see [here](https://kronosapiens.github.io/blog/2018/07/04/patricia-trees.html) for a nice narrative/easy-to-read description.

<br>

### Test networks

Many different test networks for the Ethereum blockchain exist, and they have different underlying approaches:

* Ropsten (_proof of work_) - see [here](metamask.md#ether-faucets) for a list of faucets for this network.
* Kovan (_proof of authority_)
* Rinkeby (_proof of authority_)
* Goerli (_proof of authority_)
* Kintsugi (_proof of stake_) - note that this network was only formally released in December 2021, and so is not yet available via Metamask by default. See [here](https://etherworld.co/2021/12/20/how-to-join-ethereum-merge-kintsugi-testnet/) details on how to add the Kintsugi testnet to Metamask.

<br>

### Types of account

**External accounts**: controlled by that are controlled by public-private key pairs (i.e. humans). Address is determined by the public key.

**Contract accounts**: controlled by the code stored together with the account. Address is determined at creation, based on the address (public key) of the creator, and the number of transactions sent from the creator's address (also known as the _nonce_).

### Smart contracts

Smart contracts are executed by the Ethereum Virtual Machine (EVM)](#ethereuem-virtual-machine). 

Transactions are messages sent from one account to another, and can contain binary data and Ether. If the target account is a contract account (one that contain code), the code is run and the binary data is used as the input.

_To create a new contract, you must send code that returns the code of the contract you want, rather than just the code of the contract._ This is because when the target account is not set, the transaction creates a new contract by executing the binary data contained in the transaction. The output of this execution is then stored as the code of the contract.

## Ethereuem virtual machine

> The Ethereum Virtual Machine or EVM is the runtime environment for smart contracts in Ethereum. It is not only sandboxed but actually completely isolated, which means that code running inside the EVM has no access to network, filesystem or other processes. Smart contracts even have limited access to other smart contracts.

See [here](https://ethereum.org/en/developers/docs/evm/) for more details.