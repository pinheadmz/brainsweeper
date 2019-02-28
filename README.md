# Brainwallet sweeper

### Never enter a password or private key into an online computer!

### Web browsers are insecure environments for cryptography!

### [Brainwallets](https://en.bitcoin.it/wiki/Brainwallet) are a terrible idea and you could lose money!

### This tool is for entertainment purposes only! Use at your own risk!

![screenshot](https://raw.githubusercontent.com/pinheadmz/brainsweeper/master/brainsweeper_demo1.gif "demo")

This webapp uses the [bcoin library](https://github.com/bcoin-org/bcoin), browserified and bundled
with [bpkg](https://github.com/chjj/bpkg). It fetches blockchain data from the
[Blockstream.info API](http://blockstream.info).

Usage:

- Enter the brainwallet passphrase

- The app will take the SHA256 digest of the phrase and use it as a private key

- Three address types are derived: Legacy Compressed, Legacy Uncompressed, and native SegWit

- UTXO are requested from the API for those addresses

- Enter the destination address you want to sweep the Bitcoin funds to

- Using the bcoin library, a transaction is constructed from the UTXO and the destination
address. The TX is signed with the private keys derived from the brainwallet phrase

- The TX is output in raw hex, and can be pushed to the Bitcoin network via the API
by clicking the button at the bottom.