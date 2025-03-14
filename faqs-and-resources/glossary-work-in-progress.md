# Glossary

## Common Terms

***

<details>

<summary>Satoshi's (Sats)</summary>

A satoshi is 1/100 millionth of a Bitcoin. In the Lightning Network, a satoshi is further divisible into 1000 pieces ([millisatoshi](https://docs.lightning.engineering/community-resources/glossary#millisatoshi)). It is named after Bitcoin's creator, [Satoshi Nakamoto](https://docs.lightning.engineering/community-resources/glossary#satoshi-nakamoto).

</details>

<details>

<summary>mSats</summary>

mSats are each 1/1000 (a thousandth) of a satoshi. A satoshi is the smallest unit for bitcoin, but lightning can transact with even smaller units while channels are open. The amount is [rounded down](https://github.com/lightningnetwork/lnd/blob/master/lnwire/msat.go#L22-L24) to the nearest satoshi when the channel is closed and broadcast to the blockchain to adhere to bitcoin's limit.

</details>

<details>

<summary>Payment</summary>

A payment is a transaction that occurs on the lightning network. Payments are routed through lightning payment channels and are not recorded in the bitcoin blockchain.

_Credit: bitcoin.design_

</details>

<details>

<summary>Signature</summary>

Since a [private key](https://bitcoin.design/guide/glossary/#private-key) can be used to prove that the holder controls a specific address, it can therefore authorize transactions from the address. This is called a digital signature.

<img src="../.gitbook/assets/image (14).png" alt="https://bitcoin.design/assets/images/guide/glossary/signature.jpg" data-size="original">

One of the most important activities of the Bitcoin network is to verify that signatures are valid.



_Credit: bitcoin.design_

</details>

<details>

<summary>Public Key</summary>

A bitcoin address’ public key can be derived from the private key. The address itself is a hash of the public key.

</details>

<details>

<summary>Private Key</summary>

Every Bitcoin address has a public key and a corresponding private key, together they are called a keypair. If you have access to both the public and private key, you effectively control the funds in the address. As with HD wallets there are also keypairs that control _branches_ in the hierarchical tree of the wallet, and at the very top is the extended keypair (x-pub and x-prv for short) that control all the addresses in the wallet.

The private key is a 64 hexadecimal (or 256 if described in binary 1’s and 0’s) character string generated by the encryption algorithm. They look something like this in hexadecimal form:

`5KYZdUEo39z3FPrtuX2QbbwGnNP5zTd7yyr2SC1j299sBCnWjss`

Or for the extended private key:

`xprv9zrji5mK3nb4RbuR2ZYFtyzK3gn78KnEzkNP4ZxwwPPwcgQQVZqnjTMAGxmmM3jpmfsthQUtfD9iYPvnaqwejCjcyEswLqEhX4LPKNFUXT5`

_Credit: bitcoin.design_

</details>

<details>

<summary>The Lightning Network</summary>

The [lightning network](https://lightning.network/) extends bitcoin with payment channels to increase transaction speed and lower costs. It is becoming widely adopted and accepted as the preferred way to scale bitcoin.



_Credit: bitcoin.design_

</details>

<details>

<summary>Lightning Invoices</summary>

Users of the lightning network use a lightning invoice to request a payment. It is defined by [BOLT 11](https://github.com/lightningnetwork/lightning-rfc/blob/master/11-payment-encoding.md) and includes an amount to be paid, destination of the payment, and an optional message. Unlike bitcoin addresses, lightning invoices expire after a set amount of time. By default, this is set to 60 minutes.

_Credit: bitcoin.design_

</details>

<details>

<summary>Passphrase</summary>

A passphrase can be added to the [recovery phrase](https://bitcoin.design/guide/glossary/#recovery-phrase) for extra security. Technically, all recovery phrases have a passphrase. If it’s not set by the user, an empty string (“”) will be used by default. Using the recovery phrase with or without the user-defined passphrase will recover two DIFFERENT wallets. Passphrases are sometimes called the password, the extra word, or the 13th/25th word.

_Credit: bitcoin.design_

</details>

<details>

<summary>Custodial Wallet</summary>

A custodial wallet is a wallet wherein the user’s private keys are held by a third party, such as an exchange. The third-party has full control over the user’s funds, while the user only has permission to send and receive bitcoin.

The third party is responsible for providing a backup to the wallet in case the user forgets their login information. A custodial wallet is subject to the security practices of the third party, which reduces the user's responsibility, but creates an increased risk to the seed phrase and the keys stored by the wallet if the third party is hacked.

</details>

<details>

<summary>Non-Custodial Wallet</summary>

Non-custodial wallets give the user full control over their funds and the associated private keys. By using a non-custodial wallet, a user is their own bank; they can initiate transactions and are responsible for the security of their wallet, including the protection of their seed phrase, which can be used to restore their wallet if it’s lost or compromised.

</details>

<details>

<summary>Faraday </summary>

Faraday is analytics software developed by Lightning Labs that can help identify [liquidity needs](https://docs.lightning.engineering/community-resources/glossary#liquidity-management) and profitable channels in a [Lightning node](https://docs.lightning.engineering/community-resources/glossary#lightning-network-node).

</details>

<details>

<summary>Gossip Network</summary>

The Lightning gossip network is used to broadcast information about channels and peers.

</details>

<details>

<summary>Invoice </summary>

To receive Lightning payments, the recipient typically issues an invoice containing information such as a [public key](https://docs.lightning.engineering/community-resources/glossary#public-key), [payment hash](https://docs.lightning.engineering/community-resources/glossary#payment-hash), or an invoice amount and label. Invoices are defined in[ BOLT 11](https://www.bolt11.org/).

</details>

<details>

<summary>Keysend </summary>

Keysend allows users of the Lightning Network to send funds to a node's public key.

</details>

<details>

<summary>Watchtower </summary>

A watchtower consists of a client and a server. The client will share information relevant to [channel breaches](https://docs.lightning.engineering/community-resources/glossary#channel-breach) with the server, which will intervene in case they observe a breach on-chain. Watchtowers are needed in case the client is offline and unable to observe the breach themselves.

</details>

<details>

<summary>Transaction ID</summary>

The transaction ID (txid) is the hash of a Bitcoin transaction. Channels are identified by the transaction ID of their funding transaction.

</details>

<details>

<summary>Taproot Assets</summary>

A Taproot-powered protocol for issuing assets on Bitcoin that can be transferred over the Lightning Network for instant, high-volume, low-fee transactions.

Taproot Assets (formerly Taro) is a new Taproot-powered protocol for issuing assets on the Bitcoin blockchain that can be transferred over the Lightning Network for instant, high-volume, low-fee transactions. At its core, Taproot Assets taps into the security and stability of the Bitcoin network and the speed, scalability, and low fees of Lightning.

Overview of Taproot Assets:

1. Allows assets to be issued on the Bitcoin blockchain
2. Leverages taproot for privacy and scalability
3. Assets can be deposited into Lightning channels
4. Assets can be transferred over the existing Lightning Network



</details>

<details>

<summary>Peer-to-Peer Network</summary>

A peer-to-peer network is any system not relying on a leader, in which connections are made directly between peers without intermediaries.

</details>

<details>

<summary></summary>



</details>





## FAQ’s - Lightning Network&#x20;

***

<details>

<summary>How many Satoshi’s (Sats) are in one Bitcoin?</summary>

Each of the 21 million units of Bitcoin that will ever exist can be broken down further into 100,000,000 satoshis.

</details>

<details>

<summary>Why do Lightning Invoices Expire?</summary>

Why do invoices expire? If invoices had no expiry, recipients would likely run into memory/storage issues as the number of locally stored preimages grows with each payment attempt.

_Credit: bitcoin.design_

</details>

<details>

<summary>What is a Lightning Network channel?</summary>

A Lightning Network channel is a peer-to-peer payment channel that enables instant and low-cost transactions between two parties.

</details>

<details>

<summary>How do I open a Lightning Network channel?</summary>

Open a channel by sending a small amount of Bitcoin to another node or wallet, which serves as a deposit for the channel.

</details>

<details>

<summary>Do I need to run a Lightning Network node to use the network?</summary>

Nope, you don't need to run a node to use the Lightning Network. You can simply use a lightning wallet app to send and receive payments.

</details>

<details>

<summary>What is a "channel reserve" and how does it affect my onboarding experience?</summary>

Channel reserve is the amount of Bitcoin required to open a payment channel. Higher reserves can make it harder to find nodes and open channels.

</details>

<details>

<summary>What should I do if my Lightning transaction fails while trying to pay someone?</summary>

Lightning Network transactions can fail for a few common reasons. The most frequent one is usually just not having enough funds in your channel to cover the payment. Make sure you've got enough money in the account you're sending from and don't forget to factor in the network fees (\~2% of the total amount you are trying to send).

Another common issue is the transaction not being able to find a route to the recipient's Lightning node. If that happens, just try again a few minutes later.

The Lightning Network is still evolving, so some failed transactions are normal. But those two things - insufficient funds and routing problems - tend to be the main culprits when a Lightning payment doesn't go through.

</details>

<details>

<summary></summary>



</details>



## FAQ's Lightning Network Wallets&#x20;

***



<details>

<summary>What Are Some Popular Lightning Network Wallets?</summary>

Some popular Lightning Network wallets include:&#x20;

* [Blue Wallet](https://bluewallet.io/)
* [Blink](https://www.blink.sv/)
* &#x20;[Muun](https://muun.com/)&#x20;
* [Wallet of Satoshi](https://www.walletofsatoshi.com/)
* [ Zeus Wallet](https://zeusln.com/)
* [Breez](https://breez.technology/)

</details>

<details>

<summary>Are Lightning Wallets the Same as Bitcoin Wallets?</summary>

No, they're not quite the same.

A Bitcoin wallet stores your Bitcoin and conducts transactions directly on the main Bitcoin network. However, with a Lightning wallet, transactions are performed on top of the Bitcoin network using specialized channels between two parties. These channels enable off-chain transactions that Bitcoin itself doesn't track. Only the opening and closing of these channels are recorded on the Bitcoin network.

In summary, while both wallets involve Bitcoin, a Lightning wallet leverages additional channels to facilitate faster and more scalable transactions.

</details>

<details>

<summary>What is the difference between a Non-custodial &#x26; Custodial wallet?</summary>

<mark style="background-color:red;">**Non-custodial Wallet:**</mark>\
A non-custodial wallet gives you full control over your private key and recovery phrase. This means that you are the only one who can initiate transactions, ensuring that your funds can only be accessed with your direct action. However, it's important to remember that if you forget or lose your recovery phrase, the wallet makers cannot help you regain access to your funds.

<mark style="background-color:orange;">**Custodial Wallet:**</mark>\
On the other hand, a custodial wallet takes a slightly different approach. In this type of wallet, you don't have direct control over the recovery phrase. Instead, you typically sign in with your email and password. In a custodial wallet, you have to trust the wallet makers to secure your recovery phrase and your Bitcoin. Essentially, the wallet makers technically have control over your funds. Many exchanges provide custodial wallets as part of their services.

To sum it up, non-custodial wallets give you complete control, while custodial wallets require you to trust the wallet makers to secure your funds. It's important to understand the difference and choose the option that aligns with your preferences and level of trust.

</details>

<details>

<summary>What's The Difference Between a <mark style="color:yellow;">Hot Wallet</mark> vs <mark style="color:blue;">Cold Wallet</mark></summary>

_<mark style="color:yellow;">Hot</mark>_ and _<mark style="color:blue;">cold</mark>_ describes a wallet in terms of being connected to the internet. Where a <mark style="color:yellow;">hot</mark> wallet is connected to the internet, a <mark style="color:blue;">cold</mark> wallet is not.&#x20;

The idea is that a <mark style="color:blue;">cold</mark> wallet is less susceptible to third-party theft over the internet. Most software wallet applications would be seen as <mark style="color:yellow;">hot</mark> (although some can be used just for signing on a device not connected to the internet), and most hardware wallet applications would be seen as <mark style="color:blue;">cold</mark> (although they are sometimes connected for signing purposes).

</details>

<details>

<summary></summary>



</details>



## Lightning Bounties FAQ's

***

<details>

<summary>What's Lightning Bounties?</summary>

Lightning Bounties is a Web3 Bug Bounty Platform tailored to open-source developers and the Lightning Network. We provide a platform for developers, bug bounty hunters, and ethical hackers to discover and report bugs, vulnerabilities, and security issues within Lightning Network applications and protocols.

Lightning Bounties offers an opportunity for the Lightning community to proactively address potential security threats and ensure the overall safety and integrity of the network.

The platform facilitates the responsible disclosure of vulnerabilities and rewards individuals for their efforts in identifying and reporting security issues, ultimately contributing to the ongoing improvement and stability of the Lightning network.

Through Lightning Bounties, participants can engage in a collaborative effort to bolster the security of the Lightning ecosystem, and contribute to a safer and more reliable network for all users.

</details>

<details>

<summary>Who Typically Uses Lightning Bounties?</summary>

Lightning Bounties caters to two primary groups: **developers** and **organizations**.

**Developers** can showcase their skills, earn Bitcoin, and contribute to the growth of web3 technology.

**Organizations** can tap into a talented pool of developers to improve the quality and security of their software projects.

</details>

<details>

<summary>Why Do I Have To Link My GitHub Account To Use Lightning Bounties?</summary>

**Linking your GitHub account to Lightning Bounties is necessary for several reasons:**

<img src="../.gitbook/assets/image (18).png" alt="" data-size="original">



**TLDR**: _Linking your GitHub account streamlines bug hunting, promotes collaboration, and ensures proper reward distribution._

</details>

<details>

<summary></summary>



</details>

