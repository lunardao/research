Advanced user Monero privacy guide


## What Monero is

- General description of Monero's consensus, security and UTXO based model. Monero follows the UTXO-based model that Bitcoin pioneered. Monero utilizies a few privacy technologies implemented into the core protocol.
- Monero uses Proof of Work consensus. CPU's are used to mine XMR instead of ASIC


- Stealth Addresses
- Ring Signatures
- Ring CT
## What Monero is not

Monero is one of the most private cryptocurrencies currently available along with having the largest user-base. Though, there are trade-offs when using Monero. There is still a risk when using a public blockchain that is currently private. As technology advances or breakthroughs occur, a once private transaction may be broken and publicly visible for attackers to trace. For Monero, this isn't currently possible by any known techniques as of today, but this is a risk with using any public distributed ledger technology.
## Wallets

- Feather Wallet - [https://featherwallet.org/](https://featherwallet.org/) - Feather Wallet is a desktop power user wallet that gives greater control over features that many mobile wallets overlook. 

- Monerujo - [https://www.monerujo.io/](https://www.monerujo.io/)
- Anonero - [https://gitea.com/ANONERO/ANON/releases](https://gitea.com/ANONERO/ANON/releases)


## Monero Nodes
- XMR Fail - [https://monero.fail/](https://monero.fail/)
## Obtaining Monero

- Local Monero - [https://localmonero.co/](https://localmonero.co/)
- Mining - https://p2pool.io/

## Atomic Swaps
- Unstoppable Swap GUI **Bitcoin to Monero** - [https://unstoppableswap.net/](https://unstoppableswap.net/)


## Spending Best Practices

- Advanced attacks: Poisoned Outputs Attacks (EAE Attacks)- Avoid posting addresses online or re-using addresses. Use a new subaddress for every transaction. Avoid malicious entites on both sides of your transactions. Reduce the interations with malicious parties that could surveil your transactions. 

- Janus attack mitigations - If trying to completely maintain 100% subaddress unlinkability, use different wallet seeds. This is a tradeoff of convenience for privacy. Who is the adersary in this attack? 

## Metadata Considerations | Potential Attack Vectors

- Timing analysis - run a full node. Keep it running 24/7, you can run an open node that other people can route transactions through, which you can hide among these other people routing through this node.
- Counterparty surveillance - counterparty surveillance is going to be about interacting with potential malicious parties that want to surveill your transactions (it could be a marketplace that reports transaction info to authorities, in the hope of de-anonymizing users).
- Churning: churning is the act of sending your self funds to create a new ring signature and break the transaction graph. 
- Remote node considerations related to timing analysis: if you routinely connect to a remote node when you're going to spend funds, this network data leaks info about your spending habits. 

Many attackers are observing information on-chain but also grabs off-chain data.

Block explorer - transaction and IP address linking: if using a block explorer, use a hidden service over TOR or I2P. When using a block explorer: 

- Use TOR, VPN, I2P. Use different browser sessions.

- **Best solution:** run your own node and you can query the information locally.

## Marketplaces

[https://moneromarket.io](https://moneromarket.io)
[https://bitejo.com](https://bitejo.com)

## Resources

- [https://github.com/monero-project/research-lab/issues/94](https://github.com/monero-project/research-lab/issues/94)
- Breaking Monero: [https://youtube.com/watch?v=n6Bxp0k7Uqg](https://youtube.com/watch?v=n6Bxp0k7Uqg)
- https://moneroj.net/dominance/ Monero on-chain metrics
- https://www.monero.how/ Monero on-chain metrics

