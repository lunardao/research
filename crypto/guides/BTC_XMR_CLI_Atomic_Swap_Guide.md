#####Running unstoppableswap-GUI over TOR



####How to add a new provider to the public registry
  
##Other potential topics: How to swap only using the CLI: COMIT Swap CLI    
  
- Download latest binary **swap** release for your system[https://github.com/comit-network/xmr-btc-swap/releases](https://github.com/comit-network/xmr-btc-swap/releases)    
-   
- To verify is an ASB is online: ./swap list-sellers --rendezvous-point /dns4/discover.unstoppableswap.net/tcp/8888/p2p/12D3KooWA6cnqJpVnreBVnoro8midDL9Lpzmg8oJPoAGi7YYaamE

  
To initate a swap, input this command:
- *swap buy-xmr --change-address <bitcoin-change-address> --receive-address <monero-receive-address> --seller <seller> --tor-socks5-port <tor-socks5-port>
*  
<bitcoin-change-address>: input a bitcoin address you control that will act as a refund address
<monero-receive-address>: this is the address which you'll receive your swapped XMR to
<seller>: this is the rendezvous point argument, It is the address of the rendezvous point you want to use to discover ASBs. It must include a peer ID part. Here is an example: */dns4/discover.unstoppableswap.net/tcp/8888/p2p/12D3KooWA6cnqJpVnreBVnoro8midDL9Lpzmg8oJPoAGi7YYaamE*
  

  
###Privacy tips: 
--monero-daemon-address: input a monero daemon that you trust or your own monero daemon, following this format <host>:<port>  
  
--electrum-rpc: input an electrum rpc url trusted party or your own electrum server to prevent surveillance of your transaction 
  
##How to become a Market Maker  
  
- Download latest binary **asb** release [https://github.com/comit-network/xmr-btc-swap/releases](https://github.com/comit-network/xmr-btc-swap/releases)  


####Rendezvous points and providers

https://xmrswap.me/#providers  
  
https://unstoppableswap.net/
  
swap list-sellers --rendezvous-point /dnsaddr/rendezvous.coblox.tech/p2p/12D3KooWQUt9DkNZxEn2R5ymJzWj15MpG6mTW84kyd8vDaRZi46o  - Not Live
  
swap list-sellers --rendezvous-point /dns4/rendezvous.xmr.radio/tcp/8888/p2p/12D3KooWN3n2MioS515ek6LoUBNwFKxtG2ribRpFkVwJufSr7ro7   - Not live
  
  
swap list-sellers --rendezvous-point /dns4/discover.unstoppableswap.net/tcp/8888/p2p/12D3KooWA6cnqJpVnreBVnoro8midDL9Lpzmg8oJPoAGi7YYaamE  
  
swap list-sellers --rendezvous-point /dnsaddr/xmrswap.me/p2p/12D3KooWEKJYMDstzF4i8V4LqH8xfUYRQv4p6uyA3uisKp4HaQtP
  
swap list-sellers --rendezvous-point /dns4/xmrswap.loki/tcp/9942/p2p/12D3KooWCcFVKnFf2u1c4t47fiHLNKSnC4g6wh2i7nkczjwYRWG3  
  
swap list-sellers --rendezvous-point /onion3/xmrswapnme3snsgr2oydj2fmgao2l7acpyzncwnacmi5i5vbgnqby4id:9941/p2p/12D3KooWMFQrFiecB72zbCPWbHWiN7K2U7QAxMit8  
    git 