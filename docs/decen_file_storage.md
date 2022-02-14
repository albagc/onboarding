## Decentralized file storage
### Context

Today, resources are allocated in a certain url address, hosted in a certain server. This **_location based addressing_** system is centralized, and it exposes the whole file storage online system to the threats related to centralisation: single-point cyberattacks, data monopoly, <a href="https://www.nytimes.com/2020/01/15/world/europe/turkey-wikipedia-access-restored.html" target="_blank"> censorship</a>, etc.

> Useful resources: 
> - <a href="https://www.youtube.com/watch?v=I5M8bXQR9uA" target="_blank"> What is decentralized storage?</a>;
> - <a href="https://www.youtube.com/watch?v=5Vu_jwPjvww" target="_blank">Decentralized Storage Explained</a>;
> - <a href="https://blog.ethereum.org/2014/08/16/secret-sharing-erasure-coding-guide-aspiring-dropbox-decentralizer/" target="_blank">Secret Sharing and Erasure Coding: A Guide for the Aspiring Dropbox Decentralizer</a>;
> - <a href="https://hackernoon.com/swarm-ipfs-and-bigchaindb-comparing-data-storage-and-decentralization-4a2o3wf8" target="_blank">Swarm, IPFS and BigchainDB: Comparing Data Storage and Decentralization</a>

Some projects implementing a decentralized file storage platform or system are:
- **IPFS and Filecoin**: part of the Web3 space, Filecoin is a P2P network to store files including an economic incentive to ensure their readability over time. Filecoin and _**IPFS**_ are complementary protocols for storing and sharing data in the distributed web. Both systems are free, open-source, and share many building blocks, but IPFS alone does not include a built-in mechanism to incentivize the storage of data for other people. This is the challenge Filecoin aims to solve. Filecoin is built on IPFS to create a distributed storage marketplace for long-term storage. Nodes with a large storage capacity can rent their storage to users and get paid for it. It uses the _**Proof of Space-time**_ testing the usable capacity of the hosts.<a href="https://filecoin.io/" target="_blank"> 🌐 </a> <a href="https://youtu.be/JgKdBRIyIps" target="_blank"> 📼 </a> <a href="https://docs.filecoin.io/about-filecoin/how-filecoin-works/#the-network" target="_blank"> 📃 </a>.
- **Ethereum and Swarm**: is a native base layer service of the Ethereum stack. Runs on tops of Ethereum's smart contracts infraestructure and aims to be the DFS of Ethereum's public record as an alternative to an Ethereum always on-chain storage solution. It is integrated with DApps to store and distribute code, data and contents without jamming all the information of the blockchain. <a href="https://www.ethswarm.org/" target="_blank"> 🌐 </a> <a href="https://www.ethswarm.org/The-Book-of-Swarm.pdf" target="_blank"> 📃 </a> (this is Swarm's white paper, a bit lighter read: <a href="https://docs.ethswarm.org/swarm-whitepaper.pdf" target="_blank"> 📃 </a> )
- **The Metanet**: is a layer-2 protocol with the data immutably stored in a blockchain but searched and retrieved in a flexible way. The data is structued in a directed graph with nodes and edges. The nChain project, started in 2008, launched in 2021 <a href="https://kensei.nchain.com/products/" target="_blank">Kensei</a>, an interface that simplifies blockchain development and providing certification of data integrity, linking related documents to form a log and running and verifying code along with the data it uses and produces. <a href="https://nchain.com/" target="_blank"> 🌐 </a> <a href="https://nchain.com/app/uploads/2019/06/The-Metanet-Technical-Summary-v1.0.pdf" target="_blank"> 📃 </a>
- **Maidsafe**: it aims to build the SAFE Network, the world’s first autonomous and decentralised data network. Its architecture accounts with farmers (who take care of the network) and clients (upload, buy data, etc.). The network nodes use _**Proof of Resource**_ to check their availability to store an retrieve data chunks. As an incentive mechanism, _**Safe Network Tokens**_ are used as the internal currency of the Network. The project began in 2006 and the <a href="https://safenetwork.tech/roadmap/" href="_blank">project roadmap</a> with its milestones and status, right now dealing with the development of  The Perpetual Web.<a href="https://maidsafe.net/" target="_blank"> 🌐 </a>, FAQ page <a href="https://safenetwork.tech/faq/">🌐</a>.
- **Storj**: objects uploaded into Storj DCS, are default encrypted, and the network breaks the file into pieces before uploading. Many nodes contain components of one file, meaning that different nodes have encrypted components of the file. The storage architecture utilizes ‘farmers’ and ‘renters.’ Farmers are the hardware providers contributing their storage space to the network. Renters purchase this space using STORJ, the platform’s native currency, and can benefit from a secure and efficient decentralized storage system. Storj utilizes Ethereum smart contracts to work efficiently. The compatibility of STORJ with several wallets is possible as an ERC-20 standard token. The project started in 2014 and <a href="https://www.storj.io/" target="_blank"> 🌐 </a> <a href="https://youtu.be/JgKdBRIyIps" target="_blank"> 📼 </a>.
- **Sia**: this DCS uses _**PoW**_ as the consensus mechanism, as it is closely based on Bitcoin, but trading a different block reward: _**Siacoins (SC)**_. Sia lets you backup any data in a way that only allows you to get to it. Sia software divides files into 20 segments before uploading, targeting their distribution across the world, assuring that no one host represents a single point of failure, reinforcing overall network uptime and redundancy provided by the Reed-Solomon erasure coding, which enables that 10 out of the 30 data chunks can be used to fully recover user's files. Besides, Sia has an open marketplace where anyone can become a host or renter and set their own conditions and pricing. This ensures that even if demand for Siacoin increases and the price surges, natural competition will normalize the prices. Since October 2020, hosts also support SkyDB, which is mutable decentralized database that any application can use. The network itself is not designed for fast on-chain transactions and is only really meant for three things: transacting money, creating payment channels (allowing instant payments between renters and host), and verifying storage contracts<a href="https://sia.tech/" target="_blank"> 🌐 </a>, (white paper) <a href="https://sia.tech/sia.pdf" target="_blank">  📃 </a>.
- **BigchainDB**: is a system specifically designed for BigData Cloud storage. It represents data as assets that can be created or transferred to other users. This asset-centered perspective influences the applications built upon BigchainDB. Assets can be physical objects, digital objects, be shared by multiple/single owners...The key is that these assets are immutable. Ideally, each node in a BigchainDB network is owned and controlled by a different person or organization. The set of people and/or organizations who run the nodes of a BigchainDB network is referred as "BigchainDB consortium". There’s no node that has a long-term special position in the BigchainDB network. All nodes run the same software and perform the same duties. If someone has (or gets) admin access to a node, they can mess with that node (e.g. change or delete data stored on that node), but the BigchainDB network can only be compromised if more than one third of the nodes get compromised. <a href="https://tendermint.com/sdk/" target = "_blank">Tendermint</a> is used for consensus and transaction replication, and Tendermint is Byzantine Fault Tolerant (BFT). <a href="https://www.bigchaindb.com/"> 🌐 </a> ().

> <a href="https://skynet.guide/tech/storage-chains-compared.html#filecoin_3" target="_blank">Storage Chains Compared</a> (this post is from october 2021 and it has some interesting comments, such as critics towards Storj and Filecoin not being really decentralized: "_[...] Storj and Filecoin should immediately be eliminated from this running_. 
> _**Filecoins** issues are:_
>   - _Transfers are egregiously slow due to the seal/unseal process._
>   - _There are conflicts of interest due to conflating miners and storage providers._ 
>   - _PoSt is unproven to actually be resilient against attacks._
>   - _Hardware requirements are stupidly high._
> 
>  _**Storj** just isn’t really a decentralized storage provider. If you’re in the market for distributed storage though, check out Filebase (they’re a storage provider that works both on Sia and Storj for the back end)._
> **Bias disclaimer**⚠️: The author of the post claims :"_Here though, I’m just gonna say what I believe (keep in mind that I’m an active Sia community member and what I’m saying is likely highly biased)._"
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
IPFS offers several APIs for accessing and managing the contents, including a CLI interface, JSON-RPC APIs, and an HTTP interface. JavaScript packages and Go library are available too. Below there are a few interesting projects being built on IPFS:
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
Swarm is a protocol part of the Ethereum vision, where <a href="" target="_blank">Ethereum</a> would provide the computational resources, <a href="" target="_blank"> Swarm </a> the storage system and <a href="" target="_blank"> Whisper</a> a messaging layer.

The primary objective of Swarm is to provide a decentralized and **redundant** store for dapp code and data as well as block chain and state data. Swarm is also set out to provide various base layer services for web3, including node-to-node messaging, media streaming, decentralised database services and scalable state-channel infrastructure for decentralised service economies.

#### How does it work?
Similarly to IPFS, Swarm is a P2P file storage, transfer and retrieval system. Both of them enable the implementation of applications with HTML or JS. However, Swarm's inception within a native Ethereum framework provides it with a built-in incentivation system (which one of the main IPFS drawbacks). The token in which Swarm inventivization is based on, is the BZZ token, an ERC20-compatible token.

Basically, IPFS and Swarm address the same problem, but they differ in the way they provide the solution. For both systems use Merkle Trees to relate all data chunks created and ensure data integrity. However, Swarm also includes the concept is **redundancy**.

Swarm works similarly to Bittorrent, with the same information replicated in several nodes, enabling that when the content is requested, it can be served by the nodes closest to the address of a chunk. This enables the access to a file as long as a single node hosts this piece of data. Hence, highly retrieved files can be asked to be replicated along more nodes of the network, incentivating the replication of highly requested data. This structure also jumps over the directionality needed in the IPFS system, since it does not depend in a ultimate original root node of the Merkle Tree, as IPFS does, which gives Swarm a lower latency time.

Swarm implementation also relies on the **Swarm Accounting Protocol (SWAP)**, which ensures that node operators are motivated to collaborate in routing messages, while simultaneously providing protection against frivolous messaging. Swarm incentives are about ensuring that node operators collaborate.

Users can decide to keep their data private, sell it on data markets, or donate it to research institutions of their choice, amongst many other possibilities.
#### Implementation

Bee is a Swarm client implemented in Go. It’s the basic building block for Swarm Network. Bee provides low level constructs for file storage, feeds, key-value stores and untraceable communication. All the information to implement Swarmd and Bee is very well described in the <a href="https://docs.ethswarm.org/docs/" target="_blank">Swarm Bee web page</a>.


A list of projects implementing Swarm and recipients of a Grant form Ethereum's project, can be found in <a href="https://www.ethswarm.org/ecosystem.html" target="_blank">Grants and ecosystem</a> page on Swarm's official site.
<!--> #### Limitations and challenges <-->