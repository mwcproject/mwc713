# MWC713

MWC713 is:

- a wallet for MWC.

   [MWC](https://github.com/cgilliard/mwc-node) is a blockchain-powered cryptocurrency that is an implementation of the MimbleWimble protocol, forked from mwc, with a focus on privacy and scalability. In MimbleWimble, transactions are interactive, requiring the Sender and Recipient to interact over a single round trip in order to build the transaction.

- a fork of the wallet713 wallet for MWC.

   mwc713 makes it easy to store, send and soon also swap mwcs seamlessly through a single interface. Built on top of the standard MWC wallet reference implementation, mwc713 extends its functionality to improve usability and reduce friction. 

- integrated with the mwcmq messaging relay.

   For better privacy and usability, the mwcmq messaging relay allows the steps to build transactions (partial transactions, or "slates") to be routed via the relay, protecting the user from exposing their IP address, and with no impact to the safety of their funds.

<p align="center">
  <img width="600" src="demo.svg">
</p>

## Features

* **Get up and running fast.** Download a pre-compiled binary (or build yourself). We run a node for you (or run your own). 
* **Everything in one interface.** Listen, send and receive using the same instance of the wallet.
* **Use your public key as your address.** mwcmq relies on public/private keypairs that are derived from your wallet seed to authenticate yourself and receive your messages.
* **SSL & End-to-end encryption.** All mwcmq traffic uses SSL and messages are end-to-end encrypted. Nobody beyond the intended recipient can read the contents of your transaction slates. (Note: Windows SSL support is not functional yet)
* **Process transactions easily.** Send to a recipient's mwcbox profile and it takes care of itself. No need to deal with IP addresses, port forwarding, or manual file transfers.
* **Receive transactions while you are offline.** Transactions persist, waiting for you to fetch them the next time you come online.
* **Contacts.** No need to keep track of mwcmq addresses account names. Add addresses to contacts stored locally on your machine, and sending 10 mwc becomes as easy as `send 10 --to @alice`.
* **Remain in full control.** Only you have access to your private keys and your wallet balance, only you can read or sign your own transactions.

## Status

Running on mainnet. Under heavy development. Contributions are welcomed.

## Roadmap

* Multi-sig support.
* P2P Atomic Swaps with Bitcoin directly from within the wallet.
* Transaction aggregation with other users before broadcasting to the network.
* Privacy enhancements.
* Graphical User Interface on Mobile, Desktop and Web.

...and much more. We are only getting started!

## Getting started

* To get up and running, see the [setup documentation](docs/setup.md).
* For specific functionality, see the [usage documentation](docs/usage.md).

## Privacy considerations

* **The relay does not store data.** mwcbox does not store any data on completed transactions by design, but it would be possible for the relay to do so and as a result build a graph of meta-data activity between mwcbox addresses.

* **Your IP is your responsibility.** When you communicate with the mwcbox relay service, you are exposing your IP to the relay. You can obfuscate your real IP address using services such as a VPN and/or TOR or i2p.

## License

Apache License v2.0.
