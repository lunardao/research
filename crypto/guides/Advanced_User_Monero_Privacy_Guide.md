# Advanced user Monero privacy guide


## What Monero is

*General description of Monero's consensus, security and UTXO based model*  

- Monero follows a UTXO-based model that Bitcoin pioneered and utilizies a few privacy technologies (listed below) implemented into the core protocol.  Monero is built on top of the CryptoNote protocol. There are 0.3 XMR mined per minute. The block subsidy is 0.6 XMR, and the block time between monero blocks is 2 minutes. Monero has a dynamic block size and a tail emission of 0.6 XMR per block forever. The Monero supply is deflationary.

A Monero transaction occurs by a sum of inputs being consumed and creating an equal sum amount of outputs. During an XMR transaction inputs are destroyed and 16 outputs are utilized. This is called the ring signature. The outputs created from the transaction include one real output and 15 decoy outputs. The decoy outputs are arbitrarily picked from previous transactions on the blockchain. Each of these outputs look valid to an outside observer. The current default ring size is 16 which makes up your anonymity set

Transaction amounts are hidden via RingCT. Sender and recipient addresses are hidden via Stealth Addresses. 

- Monero uses a Proof of Work consensus with a mining algorithm called [RandomX](https://web.getmonero.org/resources/moneropedia/randomx.html). CPU's are used to mine XMR instead of ASIC.
- Stealth Addresses [Stealth Addresses](https://www.getmonero.org/resources/moneropedia/stealthaddress.html)
- Ring Signatures [Ring Signatures](https://www.getmonero.org/resources/moneropedia/ringsignatures.html)
- Ring CT [Ring CT](https://www.getmonero.org/resources/moneropedia/ringCT.html)


## What Monero is not

Monero is one of the most private cryptocurrencies currently available along with having the largest user-base. Although, Monero focuses on privacy, there are still trade-offs when using Monero. There is a potential future concern whenever using a blockchain that is "currently" private. As technology breakthroughs occur, a once private transaction may be broken and publicly visible for surveillance software to trace. For Monero, this isn't currently possible by any known techniques, but this is a risk with using any distributed ledger technology. When using Monero, the largest your total anonymity set can be is the total amount of Monero users. Monero does not offer perfect privacy, it offers plausible deniability for its users.

## Spending Best Practices

- **Basic Users:** Most users of Monero don't need to take in considerations when using Monero. It works for every day purchases. If there are larger threats to consider such as avoiding sanctions, totalitarian governments, and risk of physical harm, a user should take these potential attacks into consideration. These kinds of attacks are specific in nature and as mentioned previously, do not affect most users. This is an advanced privacy guide for Monero to inform users of best privacy practices.

- **Advanced attacks:** 
*Poisoned Outputs Attacks (EAE Attacks)* - A Poisoned output attack consists of two colluding parties on either side of a transaction. The user being surveilled is represented by 'A'. The first external party 'E' sends an output to 'A' and monitors the chain for potential paths the output can take. When an output reaches a destination (the second 'E' in the EAE attack) both parties can decide with some degree of certainty the owner 'A'. The more times this occurs, the higher the degree of probabilistic certainty increases.

 Avoid posting addresses online or re-using addresses. Use a new subaddress for every transaction. Avoid malicious parties on both sides of your transactions. Reduce the interations with potential malicious parties that could surveil your transactions. Use different services to limit the chances of you interacting with a service that may surveil your transactions.

*Janus Attacks* - <!---describe what a janus attack is and mitigations---> If trying to completely maintain 100% subaddress unlinkability, use different wallet seeds. This is a trade-off of convenience for privacy. Who is the adversary in this attack? 

## Metadata Considerations | Potential Attack Vectors

- **Network analysis:** Run a full node & keep it running 24/7, you can run a public node that other people can route transactions through, which you can hide among other users routing through this node.
- **Counterparty surveillance:** Counterparty surveillance is about interacting with malicious parties that want to surveill your transactions. This can range from a marketplace that reports transaction info to authorities, in the hope of de-anonymizing users, or it could be a malicous merchant that is collecting on-chain and off-chain data.
- **Churning:** Churning is the act of sending your self funds to create a new ring signature and break the transaction graph. This obscures the outputs being created. There are pros and cons for churning and there is still discussion if this actually produces the correct outcomes. See also *Poisoned Outputs Attacks (EAE Attacks)* 

- **Remote node considerations related to timing analysis:** If you routinely connect to a remote node when you're going to spend funds, this network data leaks info about your spending habits. 

Many attackers are observing information on-chain but also grab off-chain data.

**Block explorer - transaction and IP address linking:** When using a block explorer, use a hidden service over TOR, I2P, VPN and be sure to Use different browser sessions. The best solution is to run your own node and you can access the information locally.

- **Understanding Hueristics:** There are heuristics that can be used to conclude further information about a Monero transaction. The more data that a user gives up, which can come from transaction information, transaction partners, network information, metadata, etc. leads to an increase in the statistical analysis by surveilling counter-parties.

- **Further Developments & Analysis:** There are developments that are constantly taking place. Technologicial develop and analysis is an arms race. Analysis gets better with time and this evolution is to discover weaknesses in the current protocol. Monero is not bulletproof but technological developments should make Monero stronger going forward. This includes increasing the ring size while also providing scalability.

- **AI and machine learning:** There is concern that the input selection algorithm and spending habits of individuals may be traceable using tools like Artificial Intelligence or machine learning.


## Wallets

#### Desktop Wallet

- [Feather Wallet](https://featherwallet.org/): Is a desktop power user wallet that gives greater control over features that many mobile wallets overlook. It ships with strong defaults for normal users but can be configured for high or uncommon threat models.


#### Mobile Wallet

- [Monerujo](https://www.monerujo.io/): Includes support for Tor nodes, multiple wallets, uses swap service sideshift.ai (doesn't support Tor for sideshift.ai swaps)
- [Anonero](https://gitea.com/ANONERO/ANON/releases): Mandatory Tor, enforced seed passphrase, encrypted backups, and no 3rd party services like exchanges/fiat price.


## Monero Nodes

- [XMR Fail](https://monero.fail/): List of available public XMR nodes including nodes running over Tor. You can use this resource to choose online nodes you want your wallet software to connect to.

## Obtaining Monero

- [LocalMonero](https://localmonero.co/) & [AgoraDesk](https://agoradesk.com/)
- [Mining](https://p2pool.io/) - Decentralized monero mining.
- [TradeOgre](https://tradeogre.com/) - Crypto to Crypto centralized exchange that has many different trading pairs and doesn't require Know Your Customer (KYC) information. 
- [Majestic Bank](https://majesticbank.su/) via onion link:  [https://majestictfvnfjgo5hqvmuzynak4kjl5tjs3j5zdabawe6n2aaebldad.onion/](https://majestictfvnfjgo5hqvmuzynak4kjl5tjs3j5zdabawe6n2aaebldad.onion/). Swap exchange that supports XMR, BTC, BCH, FIRO, LTC, & WOW
- [Trocador](https://trocador.app) via onion link: [http://trocadorfyhlu27aefre5u7zri66gudtzdyelymftvr4yjwcxhfaqsid.onion](http://trocadorfyhlu27aefre5u7zri66gudtzdyelymftvr4yjwcxhfaqsid.onion). Swap exchange aggregator that finds the best rate for instant swap services. The Trocador site then acts as a proxy to complete the swap.

## Atomic Swaps

- [Unstoppable Swap](https://unstoppableswap.net/) GUI. Trustlessly swap BTC to XMR. There is no option to swap from XMR to BTC. The only way this will be possible is with a Monero hard-fork.


## Marketplaces

- [Monero market](https://moneromarket.io)  
- [Bitejo](https://bitejo.com)

## VPS provider

- [Kyun](https://kyun.host/)

## Resources

- [Monero project research-lab](https://github.com/monero-project/research-lab/issues/94)
- [Breaking Monero](https://www.monerooutreach.org/breaking-monero/)
- [Monero's marketcap dominance](https://moneroj.net/dominance/)
- [Monero metrics](https://www.monero.how/)
- [Monero Stack Exchange](https://monero.stackexchange.com/)
- [Zero to Monero: Second Edition](https://www.getmonero.org/library/Zero-to-Monero-2-0-0.pdf)

