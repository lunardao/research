# Advanced user Monero privacy guide

This is an advanced privacy guide for Monero to inform users with extreme threat models of best privacy practices.

## What Monero is

*General description of Monero's consensus, security and UTXO based model*  

- Monero follows a UTXO-based model that Bitcoin pioneered and includes privacy technologies (listed below) implemented directly into the core protocol.  Monero is built on top of the CryptoNote protocol. There are 0.3 XMR mined per minute. The block subsidy is 0.6 XMR, and the block time between Monero blocks is 2 minutes. Monero has a dynamic block size and a tail emission of 0.6 XMR per block forever. The Monero supply is deflationary.

A Monero transaction occurs by a sum of inputs being consumed and creating an equal sum amount of outputs. During an XMR transaction inputs are destroyed and 16 outputs are utilized. This is called the ring signature. The outputs created from the transaction include one real output and 15 decoy outputs. The decoy outputs are arbitrarily picked from previous transactions on the blockchain. Each of these outputs look valid to an outside observer. The current default ring size is 16 which makes up your anonymity set.

Transaction amounts are hidden via RingCT. Sender and recipient addresses are hidden via Stealth Addresses. 

- Monero uses a Proof of Work consensus with a mining algorithm called [RandomX](https://web.getmonero.org/resources/moneropedia/randomx.html). CPU's are used to mine XMR instead of ASIC.
- [Ring Signatures](https://www.getmonero.org/resources/moneropedia/ringsignatures.html)
- [Ring CT](https://www.getmonero.org/resources/moneropedia/ringCT.html)
- [Stealth Addresses](https://www.getmonero.org/resources/moneropedia/stealthaddress.html)

## What Monero is not

Monero is one of the most private cryptocurrencies currently available along with having the largest user-base. Although, Monero focuses on privacy, there are still trade-offs when using Monero. There is a potential future concern whenever using a blockchain that is "currently" private. As technology breakthroughs occur, a once private transaction may be broken and publicly visible for surveillance software to trace. For Monero, this isn't currently possible by any known techniques, but this is a risk with using any distributed ledger technology. When using Monero, the largest your total anonymity set can be is the total amount of Monero users. Monero does not offer perfect privacy, it offers plausible deniability for its users.

## Spending Best Practices

- **Basic Users:** Most users of Monero don't need to take considerations when using Monero. It works for every day purchases. If there are larger threats to consider such as avoiding sanctions, totalitarian governments, and risk of physical harm, a user should consider these before utilizing Monero. These kinds of attacks are specific in nature and as mentioned previously, do not affect most users. 

## Advanced attacks

**Poisoned Outputs Attack (EAE Attack)**

A *Poisoned Outputs Attacks (EAE Attacks)* consists of two colluding parties on either side of a transaction. The user being surveilled in this attack example is represented by 'A'. The first external party 'E' sends an output to 'A' and monitors the chain for potential paths the output can take. When an output reaches a destination (the second 'E' in the EAE attack) both colluding parties can discover with some degree of certainty the owner 'A'. The more times this occurs, this higher the degree of probabilistic certainty.

A Poisoned Output Attack can be mitigated by several different measures by a user: Do not post addresses online attached to an identity or avoid re-using addresses. Use a new subaddress for every transaction. Avoid malicious parties on both sides of the transactions. Reduce the interactions with potential malicious parties that could surveil the transactions. Use different services to limit the chances of interacting with a service that may surveil the transactions. Use *churning* to add entropy to the transaction.

**Janus attack**

A *Janus Attack* is when a malicious party can discover that different subaddresses are shared by the same Monero seed. This is a specific kind of attack and usually needs off-chain confirmation that funds were received. This is an issue if the user is maintaining separate identities and using separate subaddresses from the same seed, between these separate identities. This would confirm both online identites that the user was keeping separate are actually in control of the same Monero seed. A surveilling attacker can successfully execute a Janus attack if they're able to verify sucessful receipt of funds. This can be from various sources (e.g. user informs reciept of funds, Point of sale system informs receipt of funds, etc.).

A Janus attack can be mitigated by several different measures by a user: Do not confirm receipt of funds. Do not publish or share subaddress publicly. Use different wallet seeds for different identitites. Do not give out subaddresses tied to a real identity including subaddresses from exchanges. Use different Monero seeds if using a subaddress tied to a specific identity. If trying to completely maintain 100% subaddress unlinkability, use different wallet seeds. This comes with a trade-off of convenience for privacy. 

**Churning** 

Churning is the act of sending oneself an entire balance. This creates a new output and helps break the transaction graph. This obscures the output path. There are pros (obscuring output path) and cons for churning(chain bloat, false assumptions) and there is still discussion if this actually produces the correct outcomes. See also *Poisoned Outputs Attacks (EAE Attacks)*. Churning isn't necessary for all users but if done correctly can benefit specific use cases.

**Output consolidation** 

If a user's outputs are being surveilled, and a user consolidates many outputs into a single transaction, with statistical analysis, this increases the likelihood that the transaction was sent by the surveilled user. This works similary to managing UTXO's in bitcoin, but Monero's security assumptions adds more complexity to increase the user's plausible deniability. Use wallets that allow for the user to manage individual outputs (coin control). [Feather Wallet] offers coin control. 

## Metadata Considerations | Potential Attack Vectors

- **Network analysis:** Run a full node & keep it running 24/7, a public node that other people can route transactions through, makes it possible to hide among other users that are using this node.

- **Counter-party surveillance:** Is about interacting with malicious parties that want to surveil your transactions. This can range from a marketplace that reports transaction info to authorities, in the hope of de-anonymizing users, or it could be a malicous merchant that is collecting on-chain and off-chain data. Counter-parties exist on either side of a transaction to a user.

- **Remote node considerations related to timing analysis:** If you routinely connecting to a remote node when sending funds, this network data leaks information about spending habits. 

- **Block explorer - transaction and IP address linking:** When using a block explorer, use a hidden service over TOR, I2P, or VPN and be sure to use different browser sessions. The best solution is to run an own node and access the information locally.

- **Understanding hueristics:** There are heuristics that can be used to conclude further information about a Monero transaction. The more data that a user gives up, which can come from transaction information, transaction partners, network information, metadata, etcetera leads to an increase in the data that can be used in models by surveilling counter-parties. Many attackers are observing information on-chain and off-chain data. The stronger on-chain guarantees for privacy there are, the higher the likelihood that off-chain data will be used to de-anonymize users. 

- **AI and machine learning:** There is concern that the developments in AI and Machine learning will lead to a degradation to Monero security guarantees. The input selection algorithm and spending habits of individuals are two large areas of concern. Following the transaction graph and tracing the spending habits of users create pieces of information that models test for. 

- **Further Developments & Analysis:** Technologicial developments and analysis is an arms race. Analysis gets better with time and this evolution is to discover weaknesses in the current protocol. Monero is not bulletproof but technological developments should make Monero stronger going forward. This includes increasing the ring size while also providing scalability. Monero maintains a strong market share because it accomplishes what it sets out to do in the current environment. See also *Monero project research-lab*


## Wallets

### Desktop Wallet

- [Feather Wallet](https://featherwallet.org/): Is a desktop power user wallet that gives greater control over features that many mobile wallets overlook. It ships with strong defaults for normal users but can be configured for high or uncommon threat models.


### Mobile Wallet

- [Monerujo](https://www.monerujo.io): Includes support for Tor nodes, multiple wallets, uses swap service sideshift.ai (doesn't support Tor for sideshift.ai swaps).
- [Anonero](https://gitea.com/ANONERO/ANON/releases): Mandatory Tor, enforced seed passphrase, encrypted backups, and no 3rd party services like exchanges/fiat price.
- [Monero.com wallet](https://github.com/cake-tech/cake_wallet/releases): Was created by the CakeWallet team. An open source monero only wallet with support for Tor nodes, multiple wallet support, and uses swap service [trocador.app](https://trocador.app).
- [Mysu](hyyps://mysu.dev) via onion link: [http://rk63tc3isr7so7ubl6q7kdxzzws7a7t6s467lbtw2ru3cwy6zu6w4jad.onion/](http://rk63tc3isr7so7ubl6q7kdxzzws7a7t6s467lbtw2ru3cwy6zu6w4jad.onion/). Includes Tor and I2P support, coin control, seed offsets, churning option when selecting UTXOs, and mutli-destination transactions

## Monero Nodes

- [XMR Fail](https://monero.fail/): List of available public XMR nodes including nodes running over Tor. You can use this resource to choose online nodes for your wallet software to connect to.
- [Run a Monero Node](https://github.com/sethforprivacy/sethforprivacy.com/blob/master/content/guides/run-a-monero-node.md): Guide to run an XMR node on a linux virtual private server.
- [Setting up Your Own Node](https://moneroguides.org/tutorials/01x02-setting-up-your-own-node/): Guide to run an XMR node locally.

## Obtaining Monero

- [LocalMonero](https://localmonero.co/) & [AgoraDesk](https://agoradesk.com/).
- [Mining](https://p2pool.io/) - Decentralized Monero mining.
- [TradeOgre](https://tradeogre.com/) - Crypto to Crypto centralized exchange that has many different trading pairs and doesn't require Know Your Customer (KYC) information. 
- [Majestic Bank](https://majesticbank.su/) via onion link:  [https://majestictfvnfjgo5hqvmuzynak4kjl5tjs3j5zdabawe6n2aaebldad.onion/](https://majestictfvnfjgo5hqvmuzynak4kjl5tjs3j5zdabawe6n2aaebldad.onion/). Swap exchange that supports XMR, BTC, BCH, FIRO, LTC, & WOW.
- [Trocador](https://trocador.app) via onion link: [http://trocadorfyhlu27aefre5u7zri66gudtzdyelymftvr4yjwcxhfaqsid.onion](http://trocadorfyhlu27aefre5u7zri66gudtzdyelymftvr4yjwcxhfaqsid.onion). Swap exchange aggregator that finds the best rate for instant swap services. The Trocador site then acts as a proxy to complete the swap.
- [Bisq](https://bisq.network) Decentralized exchange built into an open source desktop application. Bisq routes over Tor by default.  Bitcoin is the base currency but Monero has the largest alt-coin volume traded on Bisq. 

## Atomic Swaps

- [Unstoppable Swap](https://unstoppableswap.net/) GUI. Trustlessly swap BTC to XMR. There is no option to swap from XMR to BTC. The only way an atomic swap from XMR to BTC will after a Monero hard-fork that would enable support for this.

## Marketplaces

- [Monero market](https://moneromarket.io)  
- [Bitejo](https://bitejo.com)
- [Cryptwerk](https://cryptwerk.com/pay-with/xmr/)
- [Accepted Here](https://www.acceptedhere.io/catalog/currency/xmr/)

## VPS provider

- [Kyun](https://kyun.host/)
- [FlokiNet](https://flokinet.is/)

## Resources

- [Open Monero project research-lab Issues](https://github.com/monero-project/research-lab/issues)
- [Monero project researc-lab Open Research Questions](https://github.com/monero-project/research-lab/issues/94)
- [Breaking Monero](https://www.monerooutreach.org/breaking-monero/)
- [Monero's marketcap dominance](https://moneroj.net/dominance/)
- [Monero metrics](https://www.monero.how/)
- [Monero Stack Exchange](https://monero.stackexchange.com/)
- [Zero to Monero: Second Edition](https://www.getmonero.org/library/Zero-to-Monero-2-0-0.pdf)
- [MoneroResearch.info](https://moneroresearch.info/)

