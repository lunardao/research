---
title: Mel Project
author: serinko
date: March 2023
abstract: A quick introduction to Mel project (former Themelio). L1 network with focus on off-chain composability of decentralized light-weight apps without relying on web2/3 or the smart contract model. 
---

# Mel Project

**Website:** [melproject.org](https://melproject.org/en/)\
**Production stage:** mainnet beta, possible to [run a node](https://docs.melproject.org/developer-guides/run-a-full-node), [develop a protocol](https://docs.melproject.org/developer-guides/gibbername)\
**Founder:** Eric Tung ([@nullchinchilla](https://nullchinchilla.me)); also founder of Geph\
**Backers:** Polychain Capital\

Mel project is a new name for Themelio. At the time of writing the website is very new, for a full documentation see https://docs.themelio.org/. The [vision](https://melproject.org/en/#vision) of Mel project is to build off-chain composable apps with a minimal on-chain interaction to achieve censorship resistance and decentralization. 

**Focus of Mel Project**

1. Censorship resistance
2. Decentralized trust/Zero trust
3. User-aligned incentives

## Problem

Large blockchains and smart contract ecosystems with complex protocols, governance and heavy clients. Difficult composability between on-chain and off-chain. Scalable and modular blockchains as well as L2 on traditional blockchains are not addressing the questions of security and over-complexity. At the same time non-DeFi dApps (Tor, I2P etc) are not adopted nor use blochain.

Cryptocurrencies are too volatile or oracle-based fiat stablecoins.

## Solution

**Computing**

Build apps accessed by non-blockchain programs, trustless light clients connected to minimal blockchain *"that distills blockchains' incentive-based trust: an immutable, credibly neutral, "code-is-law" engine that liberates us from contentious human governance."* (as described in the projects [vision](https://melproject.org/en/#vision)). The off-chain dApps (protocols, programs, anonymity & privacy solutions) would leverage Mel as a web 3 component not as a platform.

**Finances**

MEL is aimed to become a stable and trustless cryptocurrency. Based on a primitive without oracles, a protocol-internal mechanism deriving its value from computation time. Mel project calls this *"trustless sound money"* and has a well documented description in their [docs](https://docs.melproject.org/concepts/melmint).

![Matrix of trustless light clients](https://lh4.googleusercontent.com/nFaHg6RtvtYZ1KY056l_SPLlzLVwpRsR8rXJ2-eCL8EdQf2oRO50ikgBEuit83N5aXWiln7UfTvjvVBxAo4Xx1aLKU2vJvXNC4FTf_9dwJjrBXtJ_brvgFP_vRhXWKUi-tty52nS1tneyXty8MCDn_3kXA=s2048)

# Mel Project & Lunarpunk Mission

Mel Project is not a privacy first crypto, neither does not try to portray self as such. However Mel brings interesting answers on often forgotten question of network decentralization, security and privacy. Based on Unix philosophy of light, local clients plugging together into a composable model Mel breaks the currecnt paradigm of overcomplexed on-chain apps. 

## Use Case

Crypto frontends are censorship free and not spying users's metadata.  

The light clients can be a foundation of private communication. As modern internet encryption requires quering third parties for verification, connections established through tls leaks information to Google, Amazon etc. This is because of a trusted intermediary sending a public key associated with a domanin name. The intermediary can be replaced with blockchain allowing for a p2p encrypted connection.  

The light clients can be embedded in the browser, run as a daemon, or embedded in the kernel, or as hardware so that the blockchain can become a truly decentralized root of trust. This is only possible if the light client is stable and governance free. As the system only needs to trust the light client, and the client can validate the entire state up to the current height with minimal memory, it's possible to run that client anywhere: phones, raspberry pi's, tiny computer chips, etc.

With a trustworthy light client it's possible to validate a self-signed certificate issued on chain. The simplest example of this is a claim to a name like `lunardao.mel` that maps to a public key and externally routable address like a `.onion`, traditional TLD like `.com`, an IP, or anything else. When a user wants to connect to `lunardao.mel` they first do a lookup on chain, save the cert, route themselves to the address, then verify the cert against the domain. 

## Caveats

Wallets can be hacked. If the owner of `lunardao.mel` is hacked, or tricked into transferring ownership, then the client's will be "trustlessly" phished. This is similar to a traditional Certificate Authority hack with the CA containing only one cert. Taking a note from CA's it might be beneficial to consider a counter measure for such an instance, like introducing an external Certificate Revocation List, trusted 3rd party NFT revocation, and/or UTXO hardening schemes like multisig.

# Conclussion

Privacy, anonymity and p2p distribution has many layers. Connecting different links to cover all of them is a way for people to be properly shielded. Mel project is not the most outspoken privacy advocate out there, neither the team doesn't promote the lunarpunk vision per se. However their work towards p2p distribution and private network future is sincere and dedicated. The team brings unique solutions whih shall be explored, discussed and supported. 


# Mel Community

Mel has linux vibes when it comes to their philosophy, approach and tools. The team has been always responsive when help was needed, both via their platforms and DMs with the devs. There is no shill of another moon-coin, neither overly self-centric marketing, one can see that building has been the main focus of the dev oriented team. 

**Community Platforms**

* [Forum](https://forum.melproject.org/)
* [Telegram](https://t.me/mel_project)
* [Discord](https://discord.gg/qfg35paESn)
* [Twitter](https://twitter.com/melproject_org)

