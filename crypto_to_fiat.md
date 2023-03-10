# Crypto to Fiat

## Introduction

To be able to improve privacy deposits, transactions, purchases and withdrawal are essential parts. In many places it's still possible to withdraw and pay with cash, ie. via OTC (Over the counter, peer-to-peer crypt to fiat) and for some purchases a card is needed. Payment cards track the users purchased and map out our lives. This compromises our privacy. The focus of this guide is privacy withdrawals. There are grey zones, ie. ways to use CEX like Kucoin in an anonymous way. These are not included as the aim is to improve our knowledge and skills for privacy solutions.

## Considerations 

Do not operate without VPN/TOR (which hides you location, but not necessarily your metadata). To not leak metadata preferrably use NYM or HOPR. Do not use same wallet which you are using for doxxed crypto. 

Every withdrawal to fiat which is not OTC (to paper cash) or non-KYC ATM (to paper cash) is one way or the other KYCed or tracable. The credit card/bank account to which you withdrawing is assigned to a real identity and on-chain data is accessible to anyone.

Privacy is more expensive as the % of conversion/swap fees are higher - usually 2-3% per on chain swap --> DYOR (= Do Your Own Research). Privacy solutions are not mass adopted (yet) and the nation-states and large tradFi players push billions into KYC crypto, while raging a war against anonymity (of any data).

## Questions

1. . Which crypto currency do you want to convert, on which network and with which wallet?
3. What tools of exchanges do you have access to? ( ie. DEX and swaps)
4. What tools of withdraw do you want to use/ which means you have? (OTC, ATM, bity)

Take few minutes, sheet of paper and calculator and sketch the whole process before starting to move money around. This may save time, risk exposure and savings spent on expensive fees or worse on wrongly made transactions.

# Means of Withdrawing

- **$XMR** (Monero) - is the #1 privacy coin at the moment, though there are more and more privacy projects developing alternatives.
- Anonymous withdrawals to cash must be Over the Counter (OTC) or NON-KYC ATMs.
- These services usually take BTC (or ETH or some normie coins) but not XMR, so one has to get to BTC without being connected to the original account.
- With privacy we must be absolutely sure to not connect to any accounts/wallets/IPs we use with doxxed crypto and our identity in general.

# Crypto We Want to Sell and Tools of Exchanging

In case we got paid in USDC/USDT/DAI and wanna cash out - How do we get these to BTC?

## DEX, Bridges, Swaps

**In case of BTC be the coin of the final trade -  Option 1**

- First create a BTC wallet (even a hot one for temporary use). Preferrably [**Electrum on TAILS**](https://electrum.org/#home) (save the seed and password well, ie. in [KeepassXC](https://keepassxc.org/)).
- Monero can ie. be swapped in [Cake wallet app](https://cakewallet.com/).
- In case XMR wasn't the payment method (and BTC is the withdraw method), we need to run our transaction through XMR before getting to the final/"clean" BTC.
- This means to:
1. Swap our coin to XMR. Either using Cake wallet or swaps listed on [getmonero.com](getmonero.com) (on chain BTC-XMR swaps).
2. Send to another XMR wallet to add complexity in case you have been traced.
3. Swap to BTC in Cake Wallet, which you do not use for other payments.

**In case of BTC be the coin of the final trade -  Option 2**

- Your assets to withdraw is in ETH.
- Got through the steps in [Anonymizing assets]().
- Go to [sideshift](https://sideshift.ai/) and swap from ETH to BTC.
- Withdraw via ATM.

**Possibilities:**

1. Run XMR transaction, swap to clean BTC, new TAILS wallet, and use non registered [bity.com](bity.com) transaction (crypto to card) via a friend or a family member.

For this option it's also possible to go through steps in [Anonymizing assets]() and then proceed to [bity.com](bity.com) using ETH.

- This will hide: where did the money come from, what was the total sum, the fact it went directly to you.
- It will reveal: The sum of withdrawal, the BTC address, that someone around you had cash out $ from new BTC wallet.

2. Join local crypto communities/chats, see when someone wants to buy XMR and settle with them.
- Advantage: best price, no fees, no %, no hustle, relativelly secure.
- Reveal: Amount, time and place of the trade to a person who under pressure can reveal these data.

# Step by Step Practical Examples

In this example we aim to get 900E out from an ATM in a private way, starting from Bitcoin.

1. Check where your ATM is, what % fees and static fees it has.
2. Sketch out the whole path of swaps and calulate all the fees.
3. Install new cake wallet and [Monero cli](https://www.getmonero.org/downloads/#cli) (or [GUI wallet](https://www.getmonero.org/downloads/)) on Linux (preferably on TAILS), or make two Cake Wallets.
4. Calculate 900E into USD, add all the fees on the way (ATM, swaps, transactions)
5. Add 1% for volatily (price changes) on top and calculate how much BTC that will be.
6. Swap that BTC to XMR using Cake wallet.
7. Send XMR to another Cake wallet (CLEAN!!! --> this means that the wallet have been set up while protecting IP address and metadata).
8. Swap to BTC.
9. Withdraw from non-KYC ATM, be as low profile as possible (read notes on privacy).

# Note on Privacy

- Remember well what wallets your identity is connected (your phone, Bank Account, MAC, IP, KYC, paying to your family etc)
- If aiming for privacy - use:
  - Non-KYC ATMs
  - All "covid prevention" (glasses, gloves and respirator when withdrawing)
  - Do not walk there with your personal phone in your pocket.
  - Do not swap big amounts of money with a classmate, collegue just because it's cheaper and non KYC - that person is a security risk for your private tx.
- Maybe you don't have a need to always be fully anonymous, but when you do --> Do not act on hope, use excuses or be lazy. Privacy won't be served by the ones who are the most interested in data gathering and transaction monitoring!


