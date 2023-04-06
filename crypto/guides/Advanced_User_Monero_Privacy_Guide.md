# Advanced user Monero privacy guide


## What Monero is

*General description of Monero's consensus, security and UTXO based model*  

- Monero follows the UTXO-based model that Bitcoin pioneered and utilizies a few privacy technologies (listed below) implemented into the core protocol. 
<!--- Describe how a tx works---> Transaction outputs are hidden via Ring Signatures. There are 16 possible outputs that are created for the transaction, one real output and 15 false outputs that all look valid to an outside observer. Transaction amounts are hidden via RingCT. Sender and recipient addresses are hidden via Stealth Addresses.
When an XMR transaction occurs, an input is destroyed and 16 outputs are created. 
- Monero uses a Proof of Work consensus with a mining algorithm called [RandomX](https://web.getmonero.org/resources/moneropedia/randomx.html). CPU's are used to mine XMR instead of ASIC.
- Stealth Addresses [Stealth Addresses](https://www.getmonero.org/resources/moneropedia/stealthaddress.html)
- Ring Signatures [Ring Signatures](https://www.getmonero.org/resources/moneropedia/ringsignatures.html)
- Ring CT [Ring CT](https://www.getmonero.org/resources/moneropedia/ringCT.html)


## What Monero is not

Monero is one of the most private cryptocurrencies currently available along with having the largest user-base. Although, Monero focuses on privacy, there are still trade-offs when using Monero. There is a potential concern for the future when using a blockchain that is currently private. As technology advances or breakthroughs occur, a once private transaction may be broken and publicly visible for attackers to trace. For Monero, this isn't currently possible by any known techniques as of today, but this is a risk with using any distributed ledger technology. The largest your anonymity set can be when using monero is the total amount of Monero users.

## Wallets

#### Desktop Wallet

- [Feather Wallet](https://featherwallet.org/): Is a desktop power user wallet that gives greater control over features that many mobile wallets overlook. Ships with same defaults for normal users but can be configured for high or uncommon threat models.


#### Mobile Wallet

- [Monerujo](https://www.monerujo.io/): Include support for Tor nodes, multiple wallets, uses swap service sideshift.ai (doesn't support Tor for sideshift.ai swaps)
- [Anonero](https://gitea.com/ANONERO/ANON/releases): Mandatory Tor, enforced seed passphrase, encrypted backups, and no 3rd party services like exchanges/fiat price/etcetera.


## Monero Nodes

- [XMR Fail](https://monero.fail/): Available public XMR nodes including nodes running over Tor are listed here. You can use this resource to choose online nodes you want your wallet software to connect to.

## Obtaining Monero

- [LocalMonero](https://localmonero.co/) & [AgoraDesk](https://agoradesk.com/)
- [Mining](https://p2pool.io/) - Decentralized monero mining.
- [TradeOgre](https://tradeogre.com/) - Crypto to Crypto centralized exchange that has many different trading pairs that doesn't require Know Your Customer (KYC). 
- [Majestic Bank](https://majesticbank.su/) via onion link:  [https://majestictfvnfjgo5hqvmuzynak4kjl5tjs3j5zdabawe6n2aaebldad.onion/](https://majestictfvnfjgo5hqvmuzynak4kjl5tjs3j5zdabawe6n2aaebldad.onion/). Swap exchange that supports XMR, BTC, BCH, FIRO, LTC, & WOW
- [Trocador](https://trocador.app) via onion link: [http://trocadorfyhlu27aefre5u7zri66gudtzdyelymftvr4yjwcxhfaqsid.onion](http://trocadorfyhlu27aefre5u7zri66gudtzdyelymftvr4yjwcxhfaqsid.onion). Swap exchange aggregator that finds the best rate for instant swap services. The Trocador site then acts as a proxy to complete the swap.

## Atomic Swaps

- [Unstoppable Swap](https://unstoppableswap.net/) GUI. Trustlessly swap BTC to XMR.

## Spending Best Practices

- **Advanced attacks:** Poisoned Outputs Attacks (EAE Attacks)- Avoid posting addresses online or re-using addresses. Use a new subaddress for every transaction. Avoid malicious entites on both sides of your transactions. Reduce the interations with malicious parties that could surveil your transactions. 

- **Janus attack mitigations:** If trying to completely maintain 100% subaddress unlinkability, use different wallet seeds. This is a tradeoff of convenience for privacy. Who is the adersary in this attack? 

## Metadata Considerations | Potential Attack Vectors

- **Network analysis:** Run a full node & keep it running 24/7, you can run a public node that other people can route transactions through, which you can hide among other users routing through this node.
- **Counterparty surveillance:** Counterparty surveillance is about interacting with malicious parties that want to surveill your transactions. This can range from a marketplace that reports transaction info to authorities, in the hope of de-anonymizing users, or it could be a malicous merchant that is collecting on-chain and off-chain data.
- **Churning:** Churning is the act of sending your self funds to create a new ring signature and break the transaction graph. There are pros and cons for churning and there is still discussion if this actually produces the correct outcomes.
- **Remote node considerations related to timing analysis:** If you routinely connect to a remote node when you're going to spend funds, this network data leaks info about your spending habits. 

Many attackers are observing information on-chain but also grab off-chain data.

**Block explorer - transaction and IP address linking:** When using a block explorer, use a hidden service over TOR, I2P, VPN and be sure to Use different browser sessions. The best solution is to run your own node and you can access the information locally.

## Marketplaces

- [Monero market](https://moneromarket.io)  
- [Bitejo](https://bitejo.com)

## VPS provider

- [Kyun](https://kyun.host/)

## Resources

- [Monero project research-lab](https://github.com/monero-project/research-lab/issues/94)
- [Breaking Monero](https://www.monerooutreach.org/breaking-monero/)
- [Monero's marketcap dominance](https://moneroj.net/dominance/)
- [Monero on-chain metrics](https://www.monero.how/)
- [Monero Stack Exchange](https://monero.stackexchange.com/)

