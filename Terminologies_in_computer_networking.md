## Protocols :
- Set of rules and regulations to perform some task.

## Network Protocols :
- Set of rules and regulations setup to communicate and share information over a network.
- eg :- HTTP, UDP, TCP, SMTP, etc.

## Packets :
- In order to share data, we cannot send the entire big chunk of data over the network. So we divide the data in smaller chunks, these chunks are called as packets.
- Having smaller chunks of data makes the overall network more managable, reusable and fast so that we can leverage the whole capacity of the network.

## Address :
- Sending messages/data over the internet requires the destination details. This detail that uniquely identifies the end system(or client system) is called as `address`.
- This address can be of a computer, tablet, mobile phone, etc.

## Ports :
- Any machine could be running many network applications, in order to distinguish between these apps for receiving messages/data, we use ports.
- If IP-Address tells us about the computer then port tells us about the particular app un that computer for which the data is meant to be.
- Ports help us to get the packet to a specific process on the Host.
- Ports were formally known as port numbers.
- Every process has a `16-bit` port number. Range is `0 - 2^16 = 65535`.
- `0 - 1023 = well known ports` : 
    - These ports are reserved for specific appliations.
    - If a packet belongs to a port that falls under this range then definitely the use ase is already defined atleast by the protocols.
    - eg :- { port - 80 belongs to HTTP }, { port - 443 belongs to HTTPs }, etc.
- `1024 - 49152 = Registered ports` :
    - They are used by specific potentially propietery apps/process that are known but not system defined.
    - Any third party applications can use these ports. 
    - Like HTTP, SMTP, etc are known to the end machine or system but what system does not know is that there can be a MongoDb server, or NodeJs server, etc. so these are known but not system defined.
    - eg:- { Sql Server uses port = 1433 }, { MongoDb Server uses port = 27017 }, etc.
    - we an change these range, like if tomorrow we decide to run our MongoDb server in port = 3000 then we have to specify to all aaplication that are consuming this mongo server that instead of 27017 port 3000 is where the Mongo server is running.
- `49153 - 65535 = Dynamic ports` :
    - These are ports for future purpose.

## Socket :
- **`{ IP-Address + Port } == Socket`** : the combination of Ip address and port is called as an socket.