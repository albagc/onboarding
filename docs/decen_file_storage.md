## Decentralized file storage
### Context

Today, resources are allocated in a certain url address, hosted in a certain server. This **_location based addressing_** system is centralized, and it exposes the whole file storage online system to the threats related to centralisation: single-point cyberattacks, data monopoly, <a href="https://www.nytimes.com/2020/01/15/world/europe/turkey-wikipedia-access-restored.html" target="_blank"> censorship</a>, etc.

> Useful resources: 
> - <a href="https://www.youtube.com/watch?v=I5M8bXQR9uA" target="_blank"> What is decentralized storage?</a>;
> - <a href="https://www.youtube.com/watch?v=5Vu_jwPjvww" target="_blank">Decentralized Storage Explained</a>;
> - <a href="https://blog.ethereum.org/2014/08/16/secret-sharing-erasure-coding-guide-aspiring-dropbox-decentralizer/" target="_blank">Secret Sharing and Erasure Coding: A Guide for the Aspiring Dropbox Decentralizer</a>;

Some projects implementing a decentralized file storage platform or system are:
- **Metanet**: it associates a key to each file and a bitcoin address. <a href="https://nchain.com/" target="_blank"> 🌐 </a> <a href="https://nchain.com/app/uploads/2019/06/The-Metanet-Technical-Summary-v1.0.pdf" target="_blank"> 📃 </a>
- **Maidsafe**: first autonomous data network, formed by farmers (who take care of the netowork) and clients (upload, buy data, etc.). <a href="https://maidsafe.net/" target="_blank"> 🌐 </a>.
- **Filecoin**: <a href="https://filecoin.io/" target="_blank"> 🌐 </a> <a href="https://youtu.be/JgKdBRIyIps" target="_blank"> 📼 </a> <a href="https://docs.filecoin.io/about-filecoin/how-filecoin-works/#the-network" target="_blank"> 📃 </a>.
- **Swarm**: runs on tops of Ethereum's smart contracts infraestructure. <a href="https://www.ethswarm.org/" target="_blank"> 🌐 </a> <a href="https://www.ethswarm.org/The-Book-of-Swarm.pdf" target="_blank"> 📃 </a> (this is Swarm's white paper, a bit lighter read: <a href="https://docs.ethswarm.org/swarm-whitepaper.pdf" target="_blank"> 📃 </a> )
- **Storj**: separates parts of the file among users of the network, encripting them before sharing and spreading them on the network. <a href="https://www.storj.io/" target="_blank"> 🌐 </a> <a href="https://youtu.be/JgKdBRIyIps" target="_blank"> 📼 </a>.
- **Sia**: <a href="" target="_blank"> 🌐 </a>.
### IPFS
The InterPlanetary File System aims to build a distributed internet. The paradigm changes to a **_content based addressing_**. It is a protocol for decentralized file management created by <a href="https://protocol.ai/" target="_blank">Protocol Labs</a>, publishing the first release in 2015. 
> Useful resources: 
> - <a href="https://ipfs.io/" target="_blank">Install IPFS</a>;
> - <a href="https://hackernoon.com/a-beginners-guide-to-ipfs-20673fedd3f" target="_blank">What is IPFS? - A Beginner's Guide</a>;
> - <a href="https://www.youtube.com/watch?v=5Uj6uR3fp-U&t=112s" target="_blank">IPFS: Interplanetary file storage</a>;
#### How does it work?
When you add a file to IPFS, your file is split into smaller chunks, cryptographically hashed, and given a unique fingerprint called a **_content identifier (CID)_**. This CID acts as an permanent record of your file as it exists at that point in time. The structure in which IPFS's sharing schema is based, splitting the chunks of information of a single document, is a _**Merkle Tree**_, a _**Directed Acyclic Graph (DAG)**_ containing the relations between CIDs. Upon this structure, versioned file systems or apps can be built.

When other nodes look up your file, they ask their peer nodes who's storing the content referenced by the file's CID. When they view or download your file, they cache a copy — and become another provider of your content until their cache is cleared. A node can pin content in order to keep (and provide) it forever, or discard content it hasn't used in a while to save space. This means each node in the network stores only content it is interested in, plus some indexing information that helps figure out which node is storing what.

If you add a new version of your file to IPFS, its cryptographic hash is different, and so it gets a new CID. This means files stored on IPFS are resistant to tampering and censorship — any changes to a file don't overwrite the original, and common chunks across files can be reused in order to minimize storage costs. However, this doesn't mean you need to remember a long string of CIDs — IPFS can find the latest version of your file using the **_IPNS_** **_Decentralized Naming System (DNS)_**, and DNSLink can be used to map CIDs to human-readable DNS names.


#### Implementations
Below are a few interesting projects being built on IPFS:
- **Akasha**, a Next-Generation social network;
- **Balance3**, a triple-entry accounting platform;
- **BlockFreight**, an open network for global freight;
- **Digix**, a platform for tokenizing physical gold;
- **Infura**, an infrastructure provider for DApps;
- **Livepeer**, a decentralized live-video streaming platform;
- **Origin**, a peer-to-peer marketplace for the sharing economy;
- **uPort**, a self-sovereign identity system.

It is also being used as a complementary file system for public blockchains and other p2p applications. IPFS is interoperable with smart contracts and blockchain data, so it can add reliable, low-cost storage capacity to the Ethereum ecosystem.

>The attempt to make Ethereum blockchain data natively accessible on IPFS is a separate protocol known as **_IPLD (InterPlanetary Linked Data)_**.

#### Limitations and challenges
Nonetheless, IPFS has still limitations regarding the file availability, which depends on the availability of nodes. There is **little incentive for nodes to maintain long term backups of data** on the network. Nodes can choose to clear cached data to save space, meaning theoretically files can end up "disappearing" over time if there are no remaining nodes hosting the data. At current adoption levels this isn’t a significant issue but in the long term, backing up large amounts of data requires strong economic incentives. This can be solved by incentivation (see <a href="https://filecoin.io/" target="_blank">Filecoin</a> project, to try to keep the files as long as possible on the network).

> In think it would be worthed to take a look at the <a href="https://explore.ipld.io/#/">IPFS Explorer site</a> as an example of proof of concept implementation.

### Swarm
It is worth to mention Swarm, a protocol part of the Ethereum vision, where <a href="" target="_blank">Ethereum</a> would provide the computational resources, <a href="" target="_blank"> Swarm </a> the storage system and <a href="" target="_blank"> Whisper</a> a messaging layer.

The primary objective of Swarm is to provide a decentralized and **redundant** store for dapp code and data as well as block chain and state data. Swarm is also set out to provide various base layer services for web3, including node-to-node messaging, media streaming, decentralised database services and scalable state-channel infrastructure for decentralised service economies.

#### How does it work?
Similarly to IPFS, Swarm is a P2P file storage, transfer and retrieval system. Both of them enable the implementation of applications with HTML or JS. However, Swarm's inception within a native Ethereum framework provides it with a built-in incentivation system (which one of the main IPFS drawbacks). The token in which Swarm inventivization is based on, is the BZZ token, an ERC20-compatible token.

Basically, IPFS and Swarm address the same problem, but they differ in the way they provide the solution. For IPFS, **splitting** and **directionality** are key aspects of its strategy, whereas for Swarm, the key concept is **redundancy**. 

Swarm works similarly to Bittorrent, with the same information replicated in several nodes. This enables the access to a file as long as a single node hosts this piece of data. Hence, highly retrieved files can be asked to be replicated along more nodes of the network, incentivating the replication of highly requested data. This structure also jumps over the directionality needed in the IPFS system, since it does not depend in a ultimate original root node of the Merkle Tree, as IPFS does, which gives Swarm a lower latency time.

Swarm implementation also relies on the **Swarm Accounting Protocol (SWAP)**, which ensures that node operators are motivated to collaborate in routing messages, while simultaneously providing protection against frivolous messaging. Swarm incentives are about ensuring that node operators collaborate.

Users can decide to keep their data private, sell it on data markets, or donate it to research institutions of their choice, amongst many other possibilities.
#### Implementation

Bee is a Swarm client implemented in Go. It’s the basic building block for Swarm Network. Bee provides low level constructs for file storage, feeds, key-value stores and untraceable communication. All the information to implement Swarmd and Bee is very well described in the <a href="https://docs.ethswarm.org/docs/" target="_blank">Swarm Bee web page</a>.


A list of projects implementing Swarm and recipients of a Grant form Ethereum's project, can be found in <a href="https://www.ethswarm.org/ecosystem.html" target="_blank">Grants and ecosystem</a> page on Swarm's official site.
<!--> #### Limitations and challenges <-->