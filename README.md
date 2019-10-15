Yeti is currently pre-alpha. This means that not only is the code not well tested, but it isn't even funtional yet. We would love help testing and code review and hope to have something usable reasonably trustworthy within a few weeks.


Yeti is a script that installs bitcoin core and then walks the user through setup of cold storage solution that has the following advantages:

- Private keys are never on any device with a channel to an Internet connected device except through QR codes. Solutions that use removable media or a USB cable to connect to a device connected to the internet could be used to send keys to an attacker. Because the only data that leaves device with private keys does so through QR codes all data can be easily verified and is very limited. We believe this is the smallest possible attack surface.
- A 3 of 7 multisig addresses is used for bitcoin storage. This allows up to 4 keys to be lost without losing bitcoin and requires 3 locations to be compromised by an attacker to lose funds. This prioritizes recovery and redundancy and we believe accidental loss is the most likely way for users to lose their bitcoin.
- Generic computing hardware is used. Hardware sold specifically for bitcoin storage requires trusting everyone from manufacturing to shipping to fail to realize the opportunity available to modify the hardware in order to steal bitcoin. 
- Minimal software beyond bitcoin core. Bitcoin core is far and away the most trustworthy bitcoin software. Unfortunately it doesn’t yet provide a user friendly interface for establishing a multisig address using an offline device or display and accept private keys in a human transcribable format. As bitcoin core adds these features we will reduce the Yeti code that provides these features now. Eventually we hope Yeti will be entirely unnecessary and only trusting bitcoin core will be required.
- Open source and easily audited. One of the reasons bitcoin core is trustworthy is that it is the most scrutinized software. This makes it the least likely to contain a critical security flaw that hasn’t been identified and fixed. Yeti will never be as trustworthy, but by minimizing the amount of code and primarily using python scripts and console commands and a tiny amount of JavaScript the effort required to verify that Yeti is performing as expected is minimized.
- Usable for non-technical users. By following simple instructions users with moderate computer literacy can use Yeti. This is important because trusting someone to help you establish your cold storage solution introduces considerable risk.
- Private. Unlike many popular hardware and software wallets that transmit your IP address and bitcoin balance to third party servers, Yeti uses a bitcoin core full node. This means nothing is shared beyond what is required to create a bitcoin transaction. Yeti also uses Tor.

While we believe Yeti provides the best balance of security, ease of use and cost when storing significant sums of bitcoin, it has the following disadvantages that might not be expected:

- Cost. You will need two computers and two external hard drives. If you need to purchase all of these items it should cost less than $500 USD, but this is not an insignificant expense.
- Time. To complete setup you will need to invest 4 hours spread over the course of 1-2 weeks. This time includes writing down security words, copying files and scanning QR codes. 
