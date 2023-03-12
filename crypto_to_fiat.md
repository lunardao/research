# Crypto to Fiat

## Introduction

This guide is focused on how to withdraw crypto to cash in an anonymous way, which will include ATM and OTC. There might be other solutions out there which we encourage the community to share with each other on the [forum](forum.lunardao.net). 

Banks are fundamental for economic surveillance. Payment cards track purchases and map out our lives. Not our keys, not our cash - which means that money in the bank is imaginary funds which can be frozen or taken away. This compromises our privacy as well as our autonomy. 

There are grey zones in regards to withdrawals, ie. ways to use CEX like Kucoin in an anonymous way. These are not included as the aim is to improve our knowledge and skills for privacy solutions and CEX is centralized, non reliable and counter-intuitive to anyone who seek to develop sovereignty.

## Considerations 

Here are some things to keep in mind before starting.

- It is preferred to start these operations on [Tails](https://tails.boum.org/) or in a [Virtual machine](https://wiki.lunardao.net/virtualbox_whonix.html). If so, the second point below is not needed.
- If using a regular OS --> Do not operate without hiding IP address and metadata. Use for example [NYM](https://nymtech.net/), [HOPR](https://hoprnet.org/) or https://lokinet.org/.
- If nothing else, use VPN, such as [ProtonVPN](https://protonvpn.com/download) or [Mullvad VPN](https://mullvad.net/en/pricing/) (remember that VPNs hides location, but not necessarily metadatabut. The VPN provider can observe your origination point) or use [Tor browser](https://www.torproject.org/download/).
- Do not use same wallet which you are using for doxxed crypto. 

Every withdrawal to fiat which is not OTC (to paper cash) or non-KYC ATM (to paper cash) is one way or the other KYCed or traceable. The credit card/bank account to which you are withdrawing is assigned to a real identity and on-chain data is accessible to anyone.

Privacy is more expensive as the % of conversion/swap fees are higher - usually 2-3% per on chain swap --> DYOR (= Do Your Own Research). Privacy solutions are not mass adopted (yet) and the nation-states and large tradFi players push billions into KYC crypto, while waging a war against anonymity (of any data).

## Questions

1. Which crypto currency do you want to convert to, on which network and with which wallet?
3. What types exchanges do you have access to? ( ie. DEX and swaps)
4. What tools of withdrawal do you want to use? Which means do you have? (OTC, ATM, bity)

Take few minutes and a sheet of paper. Sketch the whole process before starting to move money around. This may save time, risk exposure and savings spent on expensive fees or worse on wrongly made transactions.

# Means of Withdrawing

- **$XMR** (Monero) - is the #1 privacy coin at the moment, though there are more and more privacy projects developing alternatives.
- Anonymous withdrawals to cash must be Over the Counter (OTC, peer-to-peer) or NON-KYC ATMs.
- These services usually take BTC (or ETH or some normie coins) but not XMR, so there is a need to exchange or swap BTC without being connected to the original account.
- To remain private and anonymous we must be absolutely sure to not connect to any accounts/wallets/IPs we use with doxxed crypto and our identity in general.

# Crypto We Want to Sell and Tools of Exchanging

In case we got paid in USDC/USDT/DAI and want to cash out - How do we get these to BTC?

## DEX, Bridges, Swaps

**In case BTC is the coin for the final trade -  Option 1**

- First, create a BTC wallet (even a hot one for temporary use). Preferrably [**Electrum on TAILS**](https://electrum.org/#home) (save the seed and password well, ie. in [KeepassXC](https://keepassxc.org/)).
- Monero can be swapped in [Cake wallet app](https://cakewallet.com/).
- In case XMR wasn't the payment method (and BTC is the currency for withdrawal), we need to run our transaction through XMR before getting to the final/"clean" BTC.
- This means to:
1. Swap our coin to XMR. Either using Cake wallet or swaps listed on [getmonero.com](getmonero.com) (on chain BTC-XMR swaps). <!--- .. The swap services mentioned on getmonero.org are not good swap services, you can mention services like majesticbank.sc , trocador.app, fixedfloat.com, or https://stealthex.io/) --->
2. Send to another XMR wallet to add complexity in case you are being tracked. <!--- .. It would be good to suggest sending to an xmr thats not connected to the same node, or send to an XMR address you control that you are using on your own node --->
3. Swap to BTC in Cake Wallet, which is not used for other payments.

**In case BTC is the coin for the final trade -  Option 2**

- The assets for withdrawal is in ETH.
- Got through the steps in [Anonymizing assets](https://wiki.lunardao.net/anonymizing_assets.html).
- Go to [sideshift](https://sideshift.ai/) and swap from ETH to BTC. <!--- .. Id suggest something like trocador.app (Which has an onion address) or fixedfloat.com --->
- Withdraw via ATM. [List of BTC ATMs](https://coinatmradar.com/countries/) <!--- .. Is it easy to withdraw cash from a crypto ATM, or are there restrictions on size --->

**Possibilities:**

1. **Bity to family or friend**  
Run XMR transaction, swap to clean BTC, new TAILS wallet, and use non registered [bity.com](bity.com) transaction (crypto to card) via a friend or a family member. <!--- .. I think this description can be expanded upon more, it doesn't seem like there's enough detail --->

For this option it's also possible to go through steps in [Anonymizing assets](https://wiki.lunardao.net/anonymizing_assets.html) and then proceed to [bity.com](bity.com) using ETH.

- This will obscure: Where the money originated, what was the total sum, and the fact it went directly to you.
- It will reveal: The sum of withdrawal, the BTC address, that someone around you cashed out $ from new BTC wallet.

2. **Join local crypto communities/chats**  
See when someone wants to buy XMR and settle with them.
- Advantage: best price, no fees, no %, no hustle, relativelly secure.
- Reveal: Amount, time and place of the trade to a person who under pressure can reveal these data.

3. **OTC exchange**  
Find out who is doing OTC exchanges where you live. This usually cost 1-3% fee for withdrawal. The accepted currencies can vary. The benefit is that the OTC exchanger doesn't want to reveal thier customers as this is their source of income. The negative part is that the only base of trust is monetary, though minimum information can be shared.

# Step by Step Practical Examples

In this example we aim to get 900E out from an ATM in a private way, starting from Bitcoin.

1. Check where your ATM is, what % fees and static fees is included.
2. Sketch out the whole path of swaps and calculate all the fees.
3. Install new cake wallet and [Monero cli](https://www.getmonero.org/downloads/#cli) (or [GUI wallet](https://www.getmonero.org/downloads/)) on Linux (preferably on TAILS), or make two Cake Wallets connected to two different nodes.
4. Calculate 900E into USD, add all the fees on the way (ATM, swaps, transactions)
5. Add 1% for volatily (price changes) on top and calculate how much BTC that will be. <!--- .. depending on length of time, price change can be larger than 1% --->
6. Swap that BTC to XMR using Cake wallet.
7. Send XMR to another Cake wallet (CLEAN!!! --> this means that the wallet has been set up while protecting IP address and metadata).
8. Swap to BTC.
9. Withdraw from non-KYC ATM, be as inconspicuous as possible (read notes on privacy).

# Note on Privacy

- Remember well what wallets your identity is connected to: your phone, Bank Account, MAC, IP, KYC, paying to your family etc. It would be best to label all of your wallets
- If aiming for privacy - use:
  - Non-KYC ATMs
  - All "covid prevention" (glasses, gloves and respirator when withdrawing)
  - Do not walk there with your personal phone in your pocket.
  - Do not swap big amounts of money with people close to you such as a classmate or colleague just because it's cheaper and non KYC - that person is a security risk for your private tx.
- You don't always have a need to be fully anonymous, but when you do --> Do not act on hope, use excuses or be lazy. Privacy won't be served by the ones who are the most interested in data gathering and transaction monitoring!

# Resources

- ### See [**Privacy tools**](https://wiki.lunardao.net/list_privacy_tools.html) section about *Virtual payment cards* for anonymous payments cards to which the user can deposit crypto.

- ### See [**Privacy projects**](https://wiki.lunardao.net/crypto_privacy_projects.html) section on *P2P Trading platforms* about local BTC and Monero exchanges.

- ### [List of BTC ATMs](https://coinatmradar.com/countries/)


<!--- notes: Suggest for XMR using cake wallet with tor nodes, or Monerujo wallet (which by default uses TOR only)
 Consider using Trocador.app or Majestic Bank for swap services as well, they've got hidden services --->
