# TCP (Transmission control protocol):-
- It is a Transport layer protocol.
## What TCP does ?
1. `Send data` : 
    - It should be fast enough to send data at an appropriate transmission rate, ie. to utilise the full capacity of the network but it should not be so fast that it causes congetion.
2. `Segment data` :
    - It segments the unsegmented data received from application layer.
    - A segment can also be considered as collection of bytes.
    - If the segmented packets are still big for Network layer then the network layer divides it further into smaller pieces.
3. `Congetion control` :
    - If congetion happens we need to do some congetion control at the Transport layer.
4. `Identify and retransmist message` :
    - TCP is an acknowledgement based protocol. ie. it sends a feedback on the data transmitted that has it reached the receiver or not.

## Application :-
1. `FTP` :
    - Files sent over the network should not get altered/reordered or so and this is made possible using TCP as it resends any data lost during transmission and also ensures data sent is ordered correctly.
2. `SSH` :
    - SSH (Secure Shell) is a network protocol that provides secure remote access and secure communication between two networked devices.
    - It is commonly used for secure login to remote systems and executing commands on remote servers.
    - The SSH protocol typically uses TCP/IP as the underlying transport protocol, but it can also use other transport protocols.
    - `does github uses ssh protocol ?`
        - Yes, GitHub supports the SSH protocol for secure communication between clients and servers. 
        - SSH is commonly used for authenticating and securely accessing remote repositories hosted on GitHub.
        - When using SSH with GitHub, users can generate an SSH key pair on their local machine and add the public key to their GitHub account. This key pair is used for authentication, allowing users to securely push, pull, and interact with repositories on GitHub.
        - It provides an additional layer of security compared to other authentication methods like HTTPS.
3. `Email` :
    - emails also need reliable delivery that is ensured by TCP.
4. `Web browsing` :
    - Http/Https protocols used for browsing also works over the reliable TCP connection only.

## Key Features :-
1. `Connection oriented` :
    - It creates a long term connection b/w the sender and the receiver.
    - The connection remains until 1 oarty terminates the connection.
2. `Full Duplex` :
    - both the sender and receiver can send their messages simutaneously.
3. `Point to Point transmission` :
    - It has exactly 2 endpoints.
    - That means `Broadcasting and Multicasting is not possible using TCP`.
4. `Error Control` :
    - It can detect errors and ask for the fix in the network.
5. `Congestion control` :
    -  It also allows us to control congestion through some mechanism.

## SEGMENT Header :-
- [Segment_header](https://drive.google.com/file/d/1731xtFeqz-8rMqu3rnt8bSpOIyzddNTj/view?usp=drive_link)

## How to establish a TCP connection (3-way Handshake) :-
- To establish a TCP connection we use a `3-way handshake`.
- [3_way_handshake_TCP](https://drive.google.com/file/d/1p3uM1Kgplu9ldxIlieflKNC-brzG0I9P/view?usp=drive_link)