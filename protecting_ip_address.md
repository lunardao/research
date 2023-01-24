
* protocol for how to check what information can be seen about you. (IP leaks)

# VPN

User --> Server --> Page (communication encrypted)

- VPN changes the user location, but doesn't protect metadata

- VPN leaking metadata: os, browser, screen resolution, type of computer?, list of plug-ins, time zone, color depth, list of fonts, cookies

# TOR

- Creating generic fingerprint so the user cannot be indentified via metadata
- functioning like many VPNs/nodes
- centralization


# Threat model

**Three main ways to attack**

- Block all traffic like tor and chinese wall. (note: The exit node is recognizable, which means that it is not possible to go to certain pages when using Tor)

- Take over 80% and taint the paquets. (Note: How likely is this?)

- Take over 100% (corrupting or backdoor in node operators) and sniffing the whole traffic and keeping all encryption keys).

**Risk with using TOR**

there are a number of known risks using tor.
1) it's mostly funded by US govt.  
2) exit/entry nodes can be fradulent (since it's free to set up these - any number of them)  
3) metadata fingerprinting still happens

# Safing

Whitepaper: https://safing.io/files/whitepaper/Gate17.pdf

This is similar to Tor, so instead of opening 1 onion routed path, you open as many as you have apps, using the exit node that is closer to the service you want to reach. The per app approach is very similar to what Nym enables. Nym has a 1 route per packet approach which is more generic.

- If you hack safing, like any VPN, you can have the list of their customers

- The network is proprietary, which makes it more vulnerable to corruption.

- Too much trust need to be put in Safing.

Contributors: huxian, alexis, 

# Difference between TOR and I2P

- Differences in the threat model and the out-proxy design.

- Tor takes the directory-based approach - providing a centralized point to manage the overall 'view' of the network, as well as gather and report statistics, as opposed to I2P's distributed network database and peer selection.

- TOR: More resistant to state-level blocking due to TLS transport layer and bridges

- TOR: Designed and optimized for exit traffic, with a large number of exit nodes

- TOR: Centralized control reduces the complexity at each node and can efficiently address Sybil attacks

The I2P/Tor outproxy functionality does have a few substantial weaknesses against certain attackers - once the communication leaves the mixnet, global passive adversaries can more easily mount traffic analysis. In addition, the outproxies have access to the cleartext of the data transferred in both directions, and outproxies are prone to abuse, along with all of the other security issues we've come to know and love with normal Internet traffic.

- I2P: Designed and optimized for hidden services, which are much faster than in Tor

- I2P: Distributed

- I2P: peer-to-peer

- I2P: Designed and optimized for hidden services, which are much faster than in Tor

- I2P: Tunnels in I2P are short lived, decreasing the number of samples that an attacker can use to mount an active attack with, unlike circuits in Tor, which are typically long lived.


# How lokinet is different from TOR

source: https://lokinet.org/faq

While Tor and Lokinet are both onion routers, they are very different at both the protocol and infrastructure levels.

Tor relies on a network of volunteer-operated relays and a set of central directory authorities, and this infrastructure introduces a number of weaknesses and limitations. Because Tor’s circuit moderation is bandwidth-weighted, you are much more likely to use high-bandwidth nodes than low-bandwidth ones, meaning that a large percentage of Tor’s 7000+ nodes are underutilised due to having insufficient bandwidth. Additionally, Tor relies on a limited set of directory authorities. When these directory authorities are compromised or suffer from technical issues, the stability of the entire Tor network suffers because the network is unable to agree on what the node set is or the roles of nodes in the network (whether they were guard nodes, exit nodes, relays, etc.).

Instead of relying on volunteers, Lokinet leverages the Oxen Service Node Network. Because Oxen’s service node operators are required to provide high-quality nodes — and are actively incentivised to do so — Lokinet’s relay network is consistent and reliable. Lokinet also inherits the market-based Sybil attack resistance of the Oxen blockchain, increasing Lokinet’s security against such attacks.

Instead of Tor’s system of central directory authorities, Lokinet stores the state of the service node network on the blockchain. Every service node has access to this list, and comes to a consensus on it, making Lokinet significantly more decentralised than Tor.

Lokinet is also more versatile than Tor — Tor operates on the transport layer and is only able to carry TCP traffic, while Lokinet operates on the network layer, meaning it can onion-route any IP-based protocol: TCP, UDP, ICMP, etc. This means Lokinet can be used for much more than just web browsing — it can also handle things like media streaming and video conferencing.

# How is Lokinet different from VPNs

Like a VPN, you can use Lokinet to improve the privacy and security of your online browsing. However, Lokinet offers additional benefits above a VPN.

When you use a VPN, your VPN provider is able to collect information about you, such as your IP and the websites you are trying to access.

Lokinet provides additional privacy and protection by being decentralised and onion-routed. Thanks to Lokinet’s decentralisation, no individual node (or server) used by Lokinet has complete information about you, so your privacy cannot be compromised. Onion routing also provides additional security.

Lokinet also allows you to access SNApps, which are hidden, secure, and private websites only accessible using Lokinet.

# How Safing is different from VPNs

https://safing.io/blog/2022/09/06/spn-vs-vpns/

# How Safing is different from TOR

https://safing.io/blog/2020/01/22/how-the-spn-compares-to-tor/


# NYM in comparison with VPNs and TOR

https://blog.nymtech.net/vpns-tor-i2p-how-does-nym-compare-8576824617b8?gi=7eddb2d753e7




















