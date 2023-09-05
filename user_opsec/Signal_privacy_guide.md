# Signal Privacy Guide

If you use Signal and you're concerned about your privacy, consider enabling these settings within your signal application

Anonymous phone number - You can use our [jmp guide](https://wiki.lunardao.net/sip_calls.html) to obtain an anonymous phone number


## Privacy Settings
Configure the privacy settings from your mobile device as you have the most power-user settings
- Incognito Keyboard (avoid your keyboard personalized learning)
- Screen lock (enable app-specific authentication) If you ever lose access to your phone while unlocked, they'll also need to unlock your signal app
- Disappearing messages and Default timer for new chats (prevent messages from staying on both your and your contacts devices forever)
- Read receipts and typing indicators (Control what information your device gives to your contact, like when you read their message, and when you are typing a response)
- "Advanced" settings
	- Always relay calls
		- This relays calls through the signal server so you don't reveal your device's IP address to your contact. Signal's server can see your IP address
	
## Other Privacy Considerations
	- If you cannot connect to Signal because it's blocked in your country, use a proxy https://support.signal.org/hc/en-us/articles/360056052052
		- If you'd like to host a signal proxy, check out documentation here: https://github.com/signalapp/Signal-TLS-Proxy
	- route your signal traffic using a VPN or Tor (there can be quality issues depending on your connection speed)
	- If you sync your account onto a computer, configure strong the hardware privacy/security settings
		- If someone gains access to the hardware your signal account is sync'd to, they have access to all your messages that are sync'd between the devices, previously and in perpetuity until the account is removed from the "linked devices"  (Disappearing messages addresses some of this issue)
			- Linked devices can only be removed from the mobile device
