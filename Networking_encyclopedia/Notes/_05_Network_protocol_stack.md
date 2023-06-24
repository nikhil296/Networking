# Network Protocol Stack :
1. ***`OSI : (7-layers)`*** 
    1. Application Layer
    2. Presentation Layer
    3. Session Layer
    4. Transport Layer
    5. Network Layer
    6. Data Link Layer
    7. Physical Layer
2. ***`TCP/IP : (5-layers)`*** 
    1. Application Layer : first 3 layers of OSI model is combined into 1 in TCP/IP.
    2. Transport Layer
    3. Network Layer
    4. Data Link Layer
    5. Physical Layer

# We are seeing each layer from sender's perspective :-
## `Application Layer` :-
- email service, chat service, etc.
- Roles :-
    - writing/providing data off to the network.
    - Reading the data from user. (taking input, etc)
    - Contains applications that helps users to interact on the network.(social media apps, etc)
    - error handling and recovering can also be done. (if we are sending some invalid/incomplete data then it can also be handled at this layer only).
- It exists on end systems only.

## `Presentation Layer` :-
- presentation of data. compression, encryption, etc.

## `Session Layer` :-
- User session management.

## `Transport Layer` :-
- Divides bug chunk of data to small chunks and manage those chunks.

## `Network Layer` :-
- How routing of packets will be done over the network.

## `Data Link Layer` :-
- error/flow control, multiplexing and Demultiplexing, handles addressing.

## `Physical Layer` :-
- It comes to wires or wireless medium.

# Network Architectures :-
## Client-Server architecture :-
- It is a 2-level architecture.
    - client side : frontend where user interacts.
    - server side
- It is a process that controls access to a centralised resource or service such as a website/webapp.
- here we have a end-system(client) and a server.
## P-2-P (Peer to Peer) architecture :-
- Here there are mutiple endsystems involved and all these endsystems are connected to each other.
- It is kind of like decentralised in nature.
- every end system helps the other end system to get the resource.
- every end-system can manage the resources at their end.
- eg :- Torrent, etc.
- It is very scalable as, we can see in terms of download torrent is very fast.
- It is not suitable to build applications like facebook, etc.
## Hybrid architecture :-
- Rarely used.
- It is combination of Client-Server architecture & P-2-P (Peer to Peer) architecture.
- the two architectures don't go well together but in system like where we put the torrent on the web we use combination of both.