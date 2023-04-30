# Firn Protocol

***Read the update in the end!***

This is a direct copy of two texts posted in LunarDAO [forum](https://forum.lunardao.net/t/investment-proposal-firn-protocol/144?u=ogma). The proposal speaks well for itself.

***LunarDAO note: First [entry](https://forum.lunardao.net/t/investment-proposal-firn-protocol/144), April 25th 2023:***

---
To: LunarDAO Members and Stewards\
From: Captain McAteer, Founder, and Gravning Amundsen, Cofounder\
Date: April 25, 2023\
Regarding: Proposal for investment and partnership opportunities between LunarDAO and Firn
---

We are pleased to present this proposal for investment and partnership between LunarDAO and Firn Protocol. This memorandum outlines several avenues for investment, as well as opportunities for growth which will benefit the DAO as well as Firn. Firn will work closely with the DAO to ensure that this partnership represents the optimal confluence of risk and reward for all involved. These conditions are provisional and subject to change if one or both parties request amendments.

# Avenues of Investment

## OTC Sale

As of April 25, 2023, the DAO’s treasury safe held approximately $19,000 (10.49084 Ether). While our previously discussed minimum token investment was $30,000, we have revised our offer to reflect the change in the DAO’s treasury balance, offering the DAO opportunity to diversify their portfolio during this critical launch phase.

**Minimum Investment to Receive OTC Discount:**

**$10,000 – Discounted 7%**

Note that this offer provides a greater volume-to-discount ratio than the previously discussed $30,000 minimum at a 10% discount. For any amount over $10,000 this discount ratio will scale an additional 3% for every $10,000 purchased, with a maximum discount of 30% at $85,000. This discount represents a composite between the price impact of a market buy, and the remaining percentage of total discount, the resultant figure will be the ­*net discount*. At the date of this proposal the price impact of a $10,000 market buy was 1.56%, the calculated discount applied to this purchase would result in a *net discount* of 5.44% (7% total – 1.56% market = 5.44% net). Firn shall not remove sell-side liquidity at any time between the submission of this proposal and the DAO’s decision. Firn may add sell-side liquidity to cushion against undesirable or erratic price action, in this case the percentage of *net discount* for the DAO would increase. **Any OTC purchase would require $FIRN token to be locked for a period of 12 months by a third-party locking service.**

## Market Purchase

A discounted market purchase may be provided in the case that the terms of the OTC sale are not suitable to the members of the DAO. In this scenario, significant sell-side $FIRN token liquidity will be added to the pool, reducing the price impact of a purchase of a **minimum of $10,000 $FIRN** to **0.56%** from the current 1.56% impact. Price impact is variable and may change between the time of this proposal and the DAO’s decision. If the DAO chooses to perform a market buy, the exact discount applied will be calculated at the time of the purchase, and will be *no less* than 1%, with the discount increasing in an appropriate manner for higher volume purchases. **In the case of a market purchase there will be no locking requirements.**

# Growth Opportunities

We believe that a partnership between LunarDAO and Firn would provide significant upside potential for both parties. Our cutting-edge privacy platform enables unfettered access to private transactions and contract interactions, irrespective of a user’s access to high-speed internet or computational power, truly delivering on the promise of *privacy for all*. The DAO’s commitment to upholding the rights, philosophy, and mission of privacy in the broader sense conform perfectly to the values Firn represents.

## Incentivizing Dao Membership

Firn may offer special airdrops of $FIRN token to LunarDAO members, in an amount proportional to their deposit size in the DAO, as well as their deposit size in Firn. The airdrop amount will be calculated based upon a 1-to-1 deposit-deposit size in LunarDAO and Firn. The minimum deposit size will be 0.5 ETH in both the DAO and Firn, respectively. This will allow DAO members to access the $FIRN airdrop without needing to buy $FIRN token, while also incentivizing growth for the DAO. The specifics of this arrangement will be discussed between Firn and the LunarDAO community once an investment proposal has been accepted.

## Co-Marketing

Tapping into the knowledge, skills, and networks of the Firn and LunarDAO communities will expand the reach of both entities significantly. An investment in Firn will give the DAO a profit incentive to grow our service, not only to increase the fees the DAO will receive from holding token, but the value of the underlying asset itself. Firn will be incentivized to help grow the DAO by working towards future investments and partnerships. Together we believe we can make privacy open and accessible to all.

These offers are only valid for LunarDAO and are not representative of any future offers made to LunarDAO or any other investor. This document does not represent financial advice and is not legally binding. The actions taken by LunarDAO, or any other investor, regarding any form of investment in Firn Protocol are the sole responsibility of the investing party.

Thank you for your consideration,

Captain McAteer - [firnprotocol@proton.me](mailto:firnprotocol@proton.me)

Gravning Amundsen - [gravning_amundsen@proton.me](mailto:gravning_amundsen@proton.me)

---

***LunarDAO note: Second [entry](https://forum.lunardao.net/t/investment-proposal-firn-protocol/144/4?u=ogma) April 25th, few hours later as an answer to provide more info about Firn protocol itself:***

Here is a quick overview of Firn, for a more in depth look into our cryptography and features you can visit [docs.firn.cash](https://docs.firn.cash). You may view our technical whitepaper at [www.firn.link/whitepaper.pdf](https://www.firn.link/whitepaper.pdf).

*Firn* is a state-of-the-art, zero-knowledge privacy utility for Ethereum and EVM-based rollups. Firn supports not just private *payments* , but the private invocation of arbitrary smart contracts. Firn moreover allows deposits and withdrawals of arbitrary *amounts* of Ether, as well as private, peer-to-peer payments (in which the sender's and receiver's identities *and* the amount being transferred are all hidden). In this light, Firn can be viewed as something like a general-purpose private *wallet* for EVM-based blockchains.

**Unlike all other projects in the privacy space, Firn uses an** ***account-based*** **architecture.** In practical terms, this means that Firn's browser-based wallet can retrieve and synchronize your account state extremely efficiently, downloading less than a kilobyte of data in the process. Other projects require data downloads in the megabytes or more, and feature extremely long synchronization times. This latter requirement has proven prohibitive in multiple instances (including *Aztec Connect* , which had an insurmountable bug load and was deprecated, and *Zcash* , which faced a crippling "spam attack"). As privacy projects continue to grow and mature, we believe that our wallet's superior efficiency will prove decisive.

Firn’s [front-end](https://app.firn.cash) is hosted entirely statically on IPFS, and can even be accessed as a [Tor hidden service](http://onion.firn.3th.ws). Firn has no off-chain rollup, and Firn proofs can be generated by the browser entirely unassistedly. Firn’s browser client must only download a few hundred bytes (compared to megabytes in the case of Aztec); it’s completely stateless, and stores nothing locally (unlike Aztec); finally, Firn synchronizes instantly, even on fresh devices. Firn’s liveness depends only on the L1’s liveness. During synchronization and proof-generation, Firn communicates *only* through the selected wallet (whose RPC is controlled by the user), and does *not* initiate any “backdoor” connections to Firn-specific services. (When you actually dispatch a withdrawal or transfer, a one-time zero-knowledge proof gets sent to the Firn relay, which pays gas and forwards it to the blockchain. This proof reveals nothing to the relay. The relay does not collect any IP information.)

---

## Firn Protocol Update

***LunarDAO Note: Updated proposal from [April 30th](https://forum.lunardao.net/t/investment-proposal-firn-protocol/144/6?u=ogma), by Firn builders***

After discussing with Captain McAteer we are prepared to make a significant increase in our offer. 

We would like to move from a 7% discount on $10,000 investment to a simple 50% bonus on any investment over $10,000. The structure will thus be:

* $10,000 investment will receive $15,000 $FIRN
* $50,000 investment will receive $75,000 $FIRN, etc.

This investment proposal represents our dedication to the Lunarpunk community, and the Lunarpunk vision. If the DAO chooses to invest in this extremely generous offer, we expect that LunarDAO will work closely with Firn to grow together, and work for the best interests of both groups. 

All other requirements outlined in the original offer apply to this offer, including the 12 month locking period, and this discount will only apply to an OTC purchase. This is not financial advise.

Thank you
