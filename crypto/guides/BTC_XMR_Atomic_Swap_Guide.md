# BTX --> XMR Atomic Swap Guide  
  
This is guide using Comit-network's [unstoppableswap-gui](https://github.com/UnstoppableSwap/unstoppableswap-gui/releases)    
    
Swaps currently only work one direction as of June 2023. Bitcoin --> Monero. There is no atomic swap for the other direction, XMR --> BTC. This is due to a technical constraint from the Monero side. There is ongoing research into this topic.
  
- Download the unstoppableswap-gui release for your system [https://github.com/UnstoppableSwap/unstoppableswap-gui/releases](https://github.com/UnstoppableSwap/unstoppableswap-gui/releases)  

- After downloading the latest release, you'll be greeted with the swap menu.  <!--- sadar: insert pic of swap menu ---> 
- Here you can choose your swap provider.
    - Parameters to consider when choosing a swap provider
        - Network (Mainnet or Testnet)
        - Uptime
        - History
        - Exchange rate
        - Maximum/minimum swap amount
- After choosing your swap provider and inputting the amount of Bitcoin you'd like to swap, select **SWAP**  
 <!--- sadar: insert pic of BTC/XMR entry fields pic ---> 
- Input the XMR address that you'd like to receive to.
- Input a BTC address that you'll receive a refund to (this refund is only there if something goes wrong during the trade, all bitcoin will be returned to the BTC address)
- Select **Start Swap**
- Your client will communicate the fee with the market maker, then you will receive a Bitcoin deposit address. Send Bitcoin to this address. 
    - You are given a range that the market maker will accept, you can send any amount between this range
    - Your bitcoin will need to reach 2 confirmations before the market maker locks up their Monero
    - The Monero is locked up for 10 confirmations before the market maker can withdraw their BTC
    - After the market maker is allowed to withdraw their new BTC, you're XMR is deposited in the wallet address you provided before.




####How to add a new provider to the public registry
  
##Other potential topics: How to swap only using the CLI: COMIT Swap CLI    
  
- Download latest binary **swap** release for your system[https://github.com/comit-network/xmr-btc-swap/releases](https://github.com/comit-network/xmr-btc-swap/releases)

  
##How to become a Market Maker  
  
- Download latest binary **asb** release [https://github.com/comit-network/xmr-btc-swap/releases](https://github.com/comit-network/xmr-btc-swap/releases)  

  
  
swap list-sellers --rendezvous-point /dnsaddr/rendezvous.coblox.tech/p2p/12D3KooWQUt9DkNZxEn2R5ymJzWj15MpG6mTW84kyd8vDaRZi46o  - Not Live
  
swap list-sellers --rendezvous-point /dns4/rendezvous.xmr.radio/tcp/8888/p2p/12D3KooWN3n2MioS515ek6LoUBNwFKxtG2ribRpFkVwJufSr7ro7   - Not live
  
swap list-sellers --rendezvous-point /dns4/eratosthen.es/tcp/7798/p2p/12D3KooWAh7EXXa2ZyegzLGdjvj1W4G3EXrTGrf6trraoT1MEobs 
  
/dns4/discover.unstoppableswap.net/tcp/8888/p2p/12D3KooWA6cnqJpVnreBVnoro8midDL9Lpzmg8oJPoAGi7YYaamE  
  
/dnsaddr/xmrswap.me/p2p/12D3KooWEKJYMDstzF4i8V4LqH8xfUYRQv4p6uyA3uisKp4HaQtP
  
/dns4/xmrswap.loki/tcp/9942/p2p/12D3KooWCcFVKnFf2u1c4t47fiHLNKSnC4g6wh2i7nkczjwYRWG3