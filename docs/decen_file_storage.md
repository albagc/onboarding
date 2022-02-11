## Decentralized file storage
### Context

Today, resources are allocated in a certain url address, hosted in a certain server. This **_location based addressing_** system is centralized, and it exposes the whole file storage online system to the threats related to centralisation: single-point cyberattacks, data monopoly, <a href="https://www.nytimes.com/2020/01/15/world/europe/turkey-wikipedia-access-restored.html" target="_blank"> censorship</a>, etc.

> Useful resources: 
> - <a href="https://ipfs.io/" target="_blank">Install IPFS</a>;
> - <a href="https://hackernoon.com/a-beginners-guide-to-ipfs-20673fedd3f" target="_blank">What is IPFS? - A Beginner's Guide</a>;
> - <a href="https://www.youtube.com/watch?v=I5M8bXQR9uA" target="_blank"> What is decentralized storage?</a>;
> - <a href="https://www.youtube.com/watch?v=5Uj6uR3fp-U&t=112s" target="_blank">IPFS: Interplanetary file storage</a>;
> - <a href="https://www.youtube.com/watch?v=5Vu_jwPjvww" target="_blank">Decentralized Storage Explained</a>;

Some projects implementing a decentralized file storage platfor or system are:
- **Metanet**: it associates a key to each file and a bitcoin address. <a href="https://metanet.mx/" target="_blank"> 🌐 </a> <a href="https://nchain.com/app/uploads/2019/06/The-Metanet-Technical-Summary-v1.0.pdf" target="_blank"> 📃 </a>
- **Maidsafe**: first autonomous data network, formed by farmers (who take care of the netowork) and clients (upload, buy data, etc.). <a href="https://maidsafe.net/" target="_blank"> 🌐 </a>.
- **Filecoin**: <a href="https://filecoin.io/" target="_blank"> 🌐 </a> <a href="https://youtu.be/JgKdBRIyIps" target="_blank"> 📼 </a> <a href="https://docs.filecoin.io/about-filecoin/how-filecoin-works/#the-network" target="_blank"> 📃 </a>.
- **Swarm**: runs on tops of Ethereum's smart contracts infraestructure. <a href="https://www.ethswarm.org/" target="_blank"> 🌐 </a> <a href="https://www.ethswarm.org/The-Book-of-Swarm.pdf" target="_blank"> 📃 </a>.
- **Storj**: separates parts of the file among users of the network, encripting them before sharing and spreading them on the network. <a href="https://www.storj.io/" target="_blank"> 🌐 </a> <a href="https://youtu.be/JgKdBRIyIps" target="_blank"> 📼 </a>.
- **Sia**: <a href="" target="_blank"> 🌐 </a>.
### IPFS
The InterPlanetary File System aims to build a distributed internet. The paradigm changes to a **_content based addressing_**. It is a protocol for decentralized file management created by <a href="https://protocol.ai/" target="_blank">Protocol Labs</a>, publishing the first release in 2015. 
#### How does it work?
When you add a file to IPFS, your file is split into smaller chunks, cryptographically hashed, and given a unique fingerprint called a **_content identifier (CID)_**. This CID acts as an permanent record of your file as it exists at that point in time.

When other nodes look up your file, they ask their peer nodes who's storing the content referenced by the file's CID. When they view or download your file, they cache a copy — and become another provider of your content until their cache is cleared.

A node can pin content in order to keep (and provide) it forever, or discard content it hasn't used in a while to save space. This means each node in the network stores only content it is interested in, plus some indexing information that helps figure out which node is storing what.

If you add a new version of your file to IPFS, its cryptographic hash is different, and so it gets a new CID. This means files stored on IPFS are resistant to tampering and censorship — any changes to a file don't overwrite the original, and common chunks across files can be reused in order to minimize storage costs.

However, this doesn't mean you need to remember a long string of CIDs — IPFS can find the latest version of your file using the **_IPNS_** **_Decentralized Naming System (DNS)_**, and DNSLink can be used to map CIDs to human-readable DNS names.
#### Implementations
Below are a few interesting projects being built on IPFS:
- Akasha, a Next-Generation social network
- Balance3, a triple-entry accounting platform
- BlockFreight, an open network for global freight
- Digix, a platform for tokenizing physical gold
- Infura, an infrastructure provider for DApps
- Livepeer, a decentralized live-video streaming platform
- Origin, a peer-to-peer marketplace for the sharing economy
- uPort, a self-sovereign identity system

It is also being used as a complementary file system for public blockchains and other p2p applications. IPFS is interoperable with smart contracts and blockchain data, so it can add reliable, low-cost storage capacity to the ethereum ecosystem. The attempt to make Ethereum blockchain data natively accessible on IPFS is a separate protocol known as **_IPLD (InterPlanetary Linked Data)_**.

#### Limitations and challenges
Nonetheless, IPFS has still limitations regarding the file availability depends on the availability of nodes. There is **little incentive** for nodes to maintain long term backups of data on the network. Nodes can choose to clear cached data to save space, meaning theoretically files can end up ‘disappearing’ over time if there are no remaining nodes hosting the data. At current adoption levels this isn’t a significant issue but in the long term, backing up large amounts of data requires strong economic incentives. This can be solved by incentivation (see <a href="https://filecoin.io/" target="_blank">Filecoin</a> project, to try to keep the files as long as possible on the network).

> In think it would be worthed to take a look at the <a href="https://explore.ipld.io/#/">IPFS Explorer site</a> as an example of proof of concept implementation.

### SWARM
It is worth to mention Swarm, a protocol part of the Ethereum vision, where <a href="" target="_blank">Ethereum</a> would provide the computational resources, <a href="" target="_blank"> Swarm </a> the storage system and <a href="" target="_blank"> Whisper</a> a messaging layer.

Swarm is implemented as a proof of concept in Geth. To try it we'll need the Go environment as well. Moreover, an Ethereum account is needed. 

#### How does it work?

#### Implementation

#### Limitations and challenges

> **Geth**

We can upload files but without encryption yet. 