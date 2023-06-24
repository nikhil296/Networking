# Bit Torrent :-
- It is a `peer-to-peer file sharing protocol`. A bit torrent client is an application that uses this protocol.
- It follows a hybrid architecture instead of P2P.
- Data is downloaded & uploaded directly to and by `peers`. This can be done simultaneously.
- Allows easy exchange of large files.
- A torrent client can request files from multiple clients in parallel.
- Big file is divided into small chunks of data is called `pieces`.
- `If a client downloads a piece successfully, then bit-torrent tells other clients in the network that a particular client has downloaded the piece of data and so if anyone in the network needs that piece, the client who has the downloaded data can now be used a source for other peers in the network.`
- The above collection of collaborating clients are called as ***`Swarms`***.

## Torrent file :-
- Client joins a swarm by downloading a (.Torrent) file that tells the following info.
    - It gives a info about the size of the pieces and how they are interacting to the client.
    - Gives information about a very special type of client clalled as `Tracker`.
    - `The tracker acts as a server that tracks who is participating in the network.`
- when client joins a swarm, it requests a list of clients from the traker and starts communication with these clients over TCP (initially as a `Leecher (The one who is benefitting/downloading from the network)`).
- when the size of swarm increase we can use something like trackerless torrents(that uses Distributed Hash tables).
    - It is a distributed coordination mechanism, such that some part of client info is tored in one node while some in another so on and so forth.
    - Information on swarm is distributed accross many nodes.

## What exactly Bit torrent does ?
- It breaks the files into N pieces :-
    - For throughput, pieces are large : 256kb-1mb.
    - For latency, broken into subpieces.
    - This is to ensure that TCP stream transferring the file is long lined enough that its congestion window can grow to reasonable size.
- Piecews also ensure integrity :-
    - Torrent contains SHA-1 hash of every piece, so if any corrupted piece comes the SHA-1 hash is not matched and thus piece is rejected.

## Why Bit torrent is so successful ?
1. `TFT (tit-for-tat policy)` :-
    - The peers who contribute can download faster. This creates an incentive to send pieces to only those peers.
    - Intitally most peers are in `choked state` and then current peer checks the download rate of all the peers connected to the `seeders`.
    - Then the `top P peers` according to their download and upload rate are chosen.
    - Now, the entire uplink capacity bandwidth is distributed equally among these top P peers eventhough some might not even need that much bandwidth.
    - The resolution to this problem is `BIT TYRANT`.
2. `BIT-TYRANT` :-
    - throughput is increased by 70%.
    - we can preferentially give access to a particular peer apart from the top P peers.
    - It ensures that each peer uses uplink capacity exactly equal to just what they need.
    - It gives room for new peers to be added to the newtwork.