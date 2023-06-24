# BTC --> XMR Atomic Swap Guide  
  
This is a guide using Comit-network's [unstoppableswap-gui](https://github.com/UnstoppableSwap/unstoppableswap-gui/releases)    
    
Swaps currently only work one direction as of June 2023, Bitcoin --> Monero. There is no atomic swap for the other direction, XMR --> BTC. This is due to a technical constraint from the Monero side. There is ongoing research into this topic.


- Download the unstoppableswap-gui[https://github.com/UnstoppableSwap/unstoppableswap-gui/releases](https://github.com/UnstoppableSwap/unstoppableswap-gui/releases) release for your system 

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
- Your unstoppableswap-gui client will communicate the fee with the market maker, then you will receive a Bitcoin deposit address. Send Bitcoin to this deposit address. 
    - You are given a range that the market maker will accept, you can send any amount between this range
    - Your bitcoin will need to reach 2 confirmations, after 2 confirmations the market maker then locks up their Monero.
    - The Monero is locked up for 10 confirmations. Then the market maker has the BTC deposited to their address
    - After the market maker funds are deposited, you're XMR is deposited in the wallet address you provided before.
- After the designated amount of confirmations, you now have XMR in your wallet!  


### Enhanced privacy and tips:   
- In the *Help* menu, enable tor by selecting *START TOR*
- Use your own Electrum Server or a trusted party's server
- Use coin control when using bitcon, and always use an address thats never been used for the *Bitcoin refund address*  
- You can find swap providers here:
    - https://xmrswap.me/#providers 
    - https://unstoppableswap.net/

