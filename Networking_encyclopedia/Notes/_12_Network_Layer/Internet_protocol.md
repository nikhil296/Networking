# Internet Protocol (IPv4):-
- It is a network Layer protocol.
## Design of IP was based on following assumptions :-
- It should provide an unreliable connectionless service.
    - `Reason` : So that all packets sent over a network are not bound to follow the same fixed path from source to destination, and they can follow different paths. 
- Must have fixed 32-bit address.
    - `X_(8-bits).Y_(8-bits).Z_(8-bits).W_(8-bits)` : ie. 4-octets.
- IP host should be able to exchange variable length packets.

## Address assignment :-
1. `FCFS (first come first serve)` :-
- This is a naive method to assign Ip address to each host on FCFS basis. So if a host from Belgium comes first it gets an IP = '2.3.4.5' then a Host from India coming next to it will get IP = '2.3.4.6'.
- we can see here that all the routers have to maintain/remember specific routes to all the hosts in order to deliver the packets correctly.
- Since, there will be `2^32 = 10^9 (approx)` hosts so it is not feasible to maintain so many routes thus the method is inefficient.

2. `Subnetting` :-
- In this method routers maintain routes to only `Blocks of addresses` and not towards individual hosts.
- For this blocks of IP addresses are assigned to ISP's.
- The ISP assign sub block of the assigned address space in an hierarchical manner. These sub-blocks are called as `Subnets`.
    ### Subnet :-
    - A typical subnet groups all the hosts that are part of same enterprise.
    - An enterprise network is typically composed of several LAN's interconnected by routers.
    - A small block of Ip address from the enterprise block is usually assigned to a LAN.
    - Ip address has two parts - `[IP_address] = [Subnet_IP] + [Host_IP]` 
    - `[Subnet_IP] is in (higher order bits)`.
    - `[Host_IP] is in (lower order bits)`.

# Address Classes :-


## Classful Addressing :-
- The IP addresses were distributed in `5 classes namely {A, B, C, D, E}`.
- `Class A` :
    - The 1st bit is always `0`.
    - So, it has `2^31` Ip addresses(50%).
    - The `1st Octet --> X_(8 bits) = represents Network ID`. Therefore `2^7 = 128` total network ID in class A.
    - The rest of the bits represent host. ie. `2^24 host ID's`.
    - `Masking` :
        - It helps us to get the network ID from any IP address.
        - To get the network ID we need to do Bitwise AND with given mask class.
        - For class A mask is - `255.0.0.0`
    - Range of IP addresses in class A is `{0.0.0.0  to  127.255.255.255}`.
    - The IP `{X.0.0.0 for net ID}, {X.255.255.255 for Broadcat ID}` are reserved IP's.
    - Therefore, total unique hosts we can have in class A is = `2^24 - 2`.
- `Class B, C, D, E` :
    - The 1st bit always `1`.
    - So, the remaining 2^31 Ip addresses are distributed among the mentioned 4 classes.
    1. `Class B` :
        - 1st 2 bits are fixed as `(1, 0)`.
        - 1st & 2nd octet are for Network ID,  while 3rd and 4th octet for Host ID.
        - `Total network ID = 2^6  *  2^8 = 2^14  ( as 1st 2 bits are fixed as "10")`.
        - `Total Host ID = 2^16 9last 2 octets`.
        - `X.Y.0.0` represent Network ID, `X.Y.255.255` represents Broadcast ID.
        - `Total unique hosts = 2^16 - 2`.
        - `Default mask = 255.255.0.0`.
    2. `Class C` :
        - 1st 3 bits fixed as `(1, 1, 0)`.
        - `Total IP addrs = 2^29`.
        - 1st, 2nd & 3rd IP fixed for network. `Total Netword ID = 2^21  (1st 3 bits are fixed)`.
        - `Total hosts = 2^8`.
        - `Default mask = 255.255.255.0`.
    3. `Class D` :
        - 1st 4-bits fixed. (1, 1, 1, 0).
        - `Total IP address = 2^28`. All of which are used for `Multicasting` purpose.
        - No network or host reserved for specific purpose.
    4. `Class E` :
        - 1st 4 bits are (1, 1, 1, 1).
        - Reserved for `Military purpose`.
        - range : {240 to 255}.
- Disadvantages of Classful addressing :
    - Wastage of IP addresses.
    - Maintainance and time consuming.
    - More prone to error.

## Classless Addressing :-
- No class, `only Blocks`.
- Notation : `X.Y.Z.W/n`
- here `n` represents that the `1st n-bits` in the mask will be set (or 1) and rest unset(or 0).

# IPv6 :-
- Work started in 1996, basic protocol published in 1998.
- `128-bit address`.
- seperated in 2 parts, `Subnet Prefix` & `Host Suffix`.
- `uses 8 blocks/octets of 16-bit each. can be represented using Hexadecimal numbers.`
- If a block has only zeros we can omit them using `::`.
- use `[]` brackets in URL.
- eg:- ***` http://[2001:470:806d:1::9]:80`***.
- `80` is the port that http always uses.