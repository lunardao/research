Advanced user Monero privacy guide


## Wallets

- Feather Wallet - https://featherwallet.org/
- Monerujo - https://www.monerujo.io/
- Anonero - https://gitea.com/ANONERO/ANON/releases

## Obtaining Monero

- Local Monero - https://localmonero.co/
- Mining

## Spending Best Practices

- Advanced attacks: Poisoned Outputs Attacks (EAE Attacks)- Avoid posting addresses online or re-using addresses. Use a new subaddress for every transaction. Avoid malicious entites on both sides of your transactions. Reduce the interations with malicious parties that could surveil your transactions. 

- Janus attack mitigations - If trying to compleltely maintain 100% subaddress unlinkability, use different wallet seeds. This is a tradeoff of convenience for privacy.

## Metadata Considerations | Potential Attack Vectors
- timing analysis - run a full node. Keep it running 24/7, you can run an open node that other people czn route transactions through, which you can hide among these other people routing through this node.
- counterparty surveillance
- churning (?)
- Remote node considerations

Many attackers are observing information on-chain but also grabs off-chain data

block explorer - transaction and ip address linking - if using a block explorer, use a hidden service over TOR or i2P. When using a block explorer, 

- use tor, VPN, i2p. Use different browser sessions

- best solution, run your own node and you can query the information locally

## Marketplaces

https://moneromarket.io
https://bitejo.com

## Resources

- https://github.com/monero-project/research-lab/issues/94
- Breaking Monero: https://youtube.com/watch?v=n6Bxp0k7Uqg


