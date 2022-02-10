## Decentralized file storage
### Context

Today, resources are allocated in a certain url address, hosted in a certain server. This **_location based addressing_** system is centralized, and it exposes the whole file storage online system to the threats related to centralisation: single-point cyberattacks, data monopoly, <a href="https://www.nytimes.com/2020/01/15/world/europe/turkey-wikipedia-access-restored.html" target="_blank"> censorship</a>, etc.

### IPFS
The InterPlanetary File System aims to build a distributed internet. The paradigm changes to a **_content based addressing_**. It is a protocol for decentralized file management created by <a href="https://protocol.ai/" target="_blank">Protocol Labs</a>, publishing the first release in 2015. 

One file X has a specific **hash** $H_X$. When user A wants file X, it requests it to the IPFS network. The file Y arrives, and user A, knowing on beforehand the (X,$H_X$) pair, checks if $H_Y = H_X$.

Files are stored into IFPS objects, which can contain data and links, so that big files can be splitted into different linked IFPS objetcs. 

This means as well that the created object is immutable, since the hash will depend on the data stored in that moment. When a file is updated, a commit is applied to the file object, updating the versioning history in all the network, but making the last commit the available one.

Nonetheless, IFPS has still limitations regarding the file availability depends on the availability of nodes, but they can go offline. This can be solved by incentivation (see Filecoin project, to try to keep the files as long as possible on the network).

> Useful resources: 
> - <a href="https://www.youtube.com/watch?v=I5M8bXQR9uA" target="_blank"> What is decentralized storage?</a>;
> - <a href="https://www.youtube.com/watch?v=5Uj6uR3fp-U&t=112s" target="_blank">IPFS: Interplanetary file storage</a>;
> - <a href="https://www.youtube.com/watch?v=5Vu_jwPjvww" target="_blank">Decentralized Storage Explained</a>;
### Projects
- Metanet: it associates a key to each file and a bitcoin address. 
- Maidsafe: first autonomous data network, formed by farmers (who take care of the netowork) and clients (upload, buy data, etc.).
- Filecoin: 
- Swarm: runs on tops of Ethereum's smart contracts infraestructure. 
- Sia: 
- Storj: separates parts of the file among users of the network, encripting them before sharing and spreading them on the network.
### SWARM
It is worth to mention Swarm, a protocol part of the Ethereum vision, where <a href="" target="_blank">Ethereum</a> would provide the computational resources, <a href="" target="_blank"> Swarm </a> the storage system and <a href="" target="_blank"> Whisper</a> a messaging layer.

Swarm is implemented as a proof of concept in Geth. To try it we'll need the Go environment as well. Moreover, an Ethereum account is needed. 

> **Geth**

We can upload files but without encryption yet. 