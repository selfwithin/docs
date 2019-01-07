<div class="welcome-card">
  <div class="title">Welcome to</div>
  <img src="img/welcome.svg" width="458">
  <div class="call-to-action">Feel free to navigate through any section of interest, or start by clicking in our most visited sections bellow.</div>

  <div class="call-to-action-links">
    <a href="#" class="link">What is Peercoin?</a>
    <a href="#" class="link">PoS vs PoW</a>
    <a href="#" class="link">Minting vs Mining</a>
  </div>
</div>

---

# Introduction to Peercoin

Hello, and welcome to the Peercoin Documentation website. We hope to help you understand more about this coin, its philosophy and technologies that runs behind it. Before getting too technical, we invite you to dive a little bit into the history of Peercoin, learning why it was created, and the purposes behind it.

## Peercoin Genesis: 2012

Since the creation of Bitcoin (Nakamoto 2008), Proof-of-Work has been the predominant design of peer-to-peer cryptocurrency. The concept of Proof-of-Work has been the backbone of mining and security model of Nakamoto’s design. In 2012, Sunny King and Scott Nadal proposed an alternative form of consensus that was both more secure, but also energy efficient.  Proof-of-Work, however is subject to centralized mining, large amounts of power consumption, and majority attacks.  Centralized mining comes about due to the increased profits and production from large scale mining operations.  Proof-of-Stake sought to provide sustainability and improved security through energy efficient staking and time-based confirmations (coin age).  Instead of electricity and computing power, time could be used as a verification method that would prevent many of the issues plaguing Proof-of-Work consensus.  Proof-of-Stake guards the blockchain, keeping users safe, while dynamic Proof-of-Work mining provides economic competition and maintains a balance in distribution.  Dynamic mining and staking allow for around 1% inflation a year, making it extremely practical for long term use.

Since its first block in 2012, Peercoin has remained one of the most energy effective, secure, and size effective blockchains in existence. Many projects have been created using Proof-of-Stake or derivatives, and all can be traced back to Peercoin's original model. Off-chain transactions are extremely compatible with Proof-of-Stake, meaning future developments and scaling will be easy to develop and deploy with Peercoin.

## Peercoin University

(University Summary here)

---


# Comparison with other blockchain networks

Peercoin is best compared with its sibling - Bitcoin; however in the following table we'll show how it bodes against something vastly different like Ethereum. Peercoin was invented as response to increasing doubts on Bitcoin's PoW consensus model with regards to its increasing centralization and conflict of interests between miners. Peercoin can be understood as a Proof-of-Stake clone of Bitcoin, though that is an oversimplification as Peercoin differs vastly - especially when it comes to economics and incentives of the system.
Major differences between the two are the fee market, ie. the absence of it in Peercoin and Peercoin's dedication to continual token distribution via PoW block rewards while the Bitcoin's distribution rate (also PoW block rewards) is reduced geometrically every four years until it becomes zero.

## Consensus algorithm

Peercoin is secured by Proof-of-Stake type of consensus. Proof-of-Work uses energy as a scary resource to verify transactions, while Proof-of-Stake uses time as a scare resource measured in "coin age".  Once a transaction has reached an age of thirty (30) days, these coins become eligible for minting.  With a high enough coin, a new block will be minted, with minting being determined by fixed probability functions.  After minting, a portion of will be given back to the minter, and their coins will again begin the thirty (30) day maturation process, giving other minters the opportunity to mint blocks.  As a note, after ninety (90) days, a transaction reaches its maximum maturity and minting probability is at its highest.  This minting can be done by simple low energy computers, such as a raspberry pi, making the process energy efficient when compared to Proof-of-Work power consumption, further increasing the possibility of decentralization.

Another benefit of Peercoin's Proof-of-Stake mechanism is its monetary cost of attack.  With pure Proof-of-Work, and individual can attempt to generate and verify faulty blocks without holding the Proof-of-Work coin or even a majority of the coin supply. Peercoin requires the  malicious individual to hold Peercoin with a coin age of thirty (30) days minimum, as well as being required to hold a majority sum of the Peercoin supply, increasing their risk massively.  This makes such an attack economically unviable. The requirement of those verifying the blockchain to hold a portion of the supply means investors are protected from malicious outside sources who hold no coins.  Those who hold Peercoin and use the network, share interest in the security of the chain.

## Distribution

Peercoin is continually distributed via PoW block rewards. At the time of writing there is 24,828,480.19 PPC issued with annual inflation of 2.3%.
The `MAX_MONEY` variable in the Peercoin source code is nothing but a placeholder.
There is no final number of Peercoins issued, while inflation is steadily diverging toward fixed 1%.
Peercoin PoW block reward is product of network Proof-of-Work hashrate. The higher the network hashrate, the lower the block reward.
This mechanism effectively pegging the issuance of Peercoins to the development of SHA256 asic miners. Reasoning behind this decision is that it's expected that development of SHA256 miners represent the level of advancement of general cryptocurrency scene, at least that is something that is visible to the blockchain and can be encode in algorithm.

Proof-of-Work reward formula is:  `difficulty == (9999 / (mint per block)) ** 4`

Proof-of-Work coin mint rate is a function of difficulty, for every 16x in difficulty mint rate is halved.

## Fee market

The fee market provides a mechanism to decide which transactions have priority over the others, and to create economic incentives for the transaction validators who usually claim the fees as rewards. Transaction fees are claimed by the block miner in both Bitcoin and Ethereum economic systems. This provides the miners the incentive to validate and include transactions in the blocks they mine. If Alice wants her transaction to be included in the next block, she should set transaction fee higher and pay more then other network users, ie. outbid them. It is presumed that miners, as rational subjects, will first include transactions which carry the most Bitcoin value. If Alice pays a transaction fee which is under the average fee at the time she might wait for several blocks (or hundreds of blocks) to see her transaction included and confirmed. So, it is obvious that the fee market serves as the incentive for miners to process and include the transactions in the blocks they mine.
With Bitcoin's block size limit set to 1MB there exists an artificial upward pressure on the price of transaction fees - incentivizing miners to validate the transactions. This is especially important as Bitcoin's economy is expected to run on transaction fees alone when the block subsidies eventually stop.

Peercoin's fees are fixed at 0.01 PPC per kb and are burned. This is equivalent to paying the transaction fee to each Peercoin holder in proportion to their Peercoin holdings since the fee decreases the total supply of Peercoins. This property eliminates the need for a fee market on Peercoin's network and allows every transaction to get included in the very next block. Peercoin retains the 1MB block size limit as it is based on the Bitcoin code, but it has no intricate need to keep it. The block size limit will definitely be increased as Peercoin's network grows in usage. Peercoin developers have already hinted that Peercoin will feature a dynamic block size in the near future.
Due to these economic properties of Peercoin a question arises: Why do Peercoin miners bother processing the transactions?

From a spectator looking at this from a Bitcoin oriented perspective the answer is that Peercoin block miners want to process transactions so they allow Peercoins to be burned - thus making their own stake in the network more valuable.
However when the intricacies of PoS are learned it is understood that with Peercoin minters (PoS miners) include transactions because it doesn't cost much to include them, while producing empty blocks reduces the value of the blockchain, and therefore of their stake. The burned fees are not really an argument as the effect on their holdings is negligible.
Bitcoin miners always start off mining an empty block, otherwise they lose the time it takes to validate the transactions and signatures, as time is money on the Bitcoin network. Only after they have validated the txns to include and have computed the merkle root, they start mining blocks with txns.
While for PoS, the time advantage is negligible as you can still use the stake hash of a few seconds ago. (hrobeers, 30.08.2017)

## Block size limit and block time spacing

Bitcoin features the 1MB block size limits which serves to place the upward pressure on the transaction fee price, Peercoin copies this parameter from the Bitcoin but it's economic model does not depend on scarcity of the block space.
Bitcoin and Peercoin generate a block every 10 minutes while Ethereum generates a block every 12 seconds. Considering this and the block size limit of 1MB, Bitcoin and Peercoin have a transaction per second (TPS) of about seven tps and Ethereum of about 25 tps.

<table>
<thead>
<tr>
<th>Features</th>
<th>Bitcoin</th>
<th>Peercoin</th>
<th>Ethereum</th>
</tr>
</thead>
<tbody>
<tr>
<td>Main use-case:</td>
<td>p2p financial transactions / store of value</td>
<td>p2p financial transactions / store of value</td>
<td>Turing complete smart contracts</td>
</tr>
<tr>
<td>Consensus algorithm:</td>
<td>PoW</td>
<td>PoS</td>
<td>PoW</td>
</tr>
<tr>
<td>Active since:</td>
<td>2009</td>
<td>2012</td>
<td>2015</td>
</tr>
</tr>
<tr>
<td>Distribution method:</td>
<td>PoW block reward</td>
<td>PoW block reward / PoS block reward</td>
<td>Initial Coin Offering / PoW block reward</td>
</tr>
<tr>
<td>Distribution:</td>
<td>Limited, until 21M tokens exist in the system.</td>
<td>Unlimited.</td>
<td>Unlimited.</td>
</tr>
</tr>
<tr>
<td>Transaction fee:</td>
<td>Fee market (~390 satoshis/byte)</td>
<td>Static 0.01 PPC/kb (~0.2 Btc satoshis/byte)</td>
<td>Fee market (~23 Gwei/byte)</td>
</tr>
<tr>
<td>Estimated transaction bandwidth:</td>
<td>7 tx/sec</td>
<td>7 tx/sec</td>
<td>25 tx/sec</td>
</tr>
<tr>
<td>Block time:</td>
<td>10 minutes</td>
<td>10 minutes</td>
<td>12 seconds</td>
</tr>
<tr>
<td>Block size:</td>
<td>1MB</td>
<td>1MB</td>
<td>Dynamic</td>
</tr>
<tr>
<td>Extra transaction data size limit:</td>
<td>80 Byte<br />(OP_RETURN)</td>
<td>80 Byte<br />(OP_RETURN)</td>
<td>Dynamic<br />(5 gas / byte)</td>
</tr>
<tr>
<td>Topology:</td>
<td>Public blockchain</td>
<td>Public blockchain</td>
<td>Public blockchain</td>
</tr>
</tbody>
</table>
Table 1. Comparison of Crypto currency attributes
(prices of transactions at the time of writing)

---


# Important Links

## Official Sites

- [Peercoin.net](https://peercoin.net/)
- [GitHub](https://github.com/peercoin/)
- [Foundation](https://peercoin.net/foundation.html/)

## Forums

- [Peercointalk](https://talk.peercoin.net/)
- [Reddit](https://www.reddit.com/r/peercoin/)
- [Bitcointalk Thread](https://bitcointalk.org/index.php?topic=101820.0)

## Chats

- [Discord](https://discord.gg/XPxfwtG)
- [Telegram](https://www.reddit.com/r/peercoin)

## Social Media

- [Facebook](https://www.facebook.com/Peercoin/)
- [Twitter](https://twitter.com/PeercoinPPC)
- [LinkedIn](https://www.linkedin.com/company/the-peercoin-foundation/)

## News

- [Team Updates](https://talk.peercoin.net/c/official-updates)

## Blog

- [Medium](https://medium.com/peercoin)

## Tools

### Block Explorers

Mainnet

- [BitInfoCharts](https://bitinfocharts.com/peercoin/explorer/)
- [Chainz.CryptoID](https://chainz.cryptoid.info/ppc/)
- [Mintr](https://mintr.peercoinexplorer.net/)
- [CoinExplorer](https://www.coinexplorer.net/PPC)
- [PeerExplorer](https://explorer.peercoin.net/)

Testnet

- [PeerExplorer](https://testnet-explorer.peercoin.net/)
- [Chainz.CryptoID](https://chainz.cryptoid.info/ppc-test/)

### Other

- [Inflation](https://www.peercoinexplorer.net/inflation/)
- [Mempool](https://www.peercoinexplorer.net/mempool/)
- [Energy Statistics](https://www.peercoin.site/#energytable)
- [Testnet Faucet](https://faucet.peercoinexplorer.net/)

---


# The Peercoin Foundation

The Peercoin Foundation was publicly announced on May 13, 2018.<sup>[5.1](#footnote-5.1)</sup>

## Mission

The Foundation was established with the simple mission of promoting and supporting the continued education, development, and overall progression of the Peercoin project. It seeks to empower future Peercoin team members by providing the tools necessary to perpetuate Peercoin's long standing reputation for bringing world-first innovations to the Blockchain.<sup>[5.2](#footnote-5.2)</sup>

## Funding

To accomplish its mission The Foundation raises funds from donations to the multi-signature address: `p92W3t7YkKfQEPDb7cG9jQ6iMh7cpKLvwK`<sup>[5.2](#footnote-5.2)</sup>

## Board of Directors

The Foundation is controlled by a Board of Directors. The membership is not known at this time.

## Footnotes

<a id="footnote-5.1">5.1</a>: https://talk.peercoin.net/t/update-15-the-peercoin-foundation-is-now-open-for-business/

<a id="footnote-5.2">5.2</a>: https://peercoin.net/foundation

---


# Purchase

## How to buy Peercoin

There are many ways to buy Peercoin, although it may depend on your previous exchange access or location.
You should have a Peercoin wallet set up previously to making a purchase so that you have a place to store your Peercoin.

### Fiat gateways

In order to purchase Peercoin directly with a bank wire or debit card, there are several options for direct purchase, although these primarily support European wire transfers and purchases.  If you want to directly purchase with a card or bank transfer, you can use the following sites:

#### The Rock Trading
https://www.therocktrading.com/
TheRockTrading offers SEPA direct deposits and offers Peercoin directly on the platform, while offering no trading fees on PPC.

### AnycoinDirect
https://anycoindirect.eu/en/buy-peercoin
Supports EUR

#### LiteBit
https://www.litebit.eu/en/buy/peercoin
Supports EUR

#### Livecoin.net
https://www.livecoin.net/
Supports both USD/RUR/EUR deposits

If you are in the US, the above websites may not be available.  You must use an exchange that accepts you must buy a cryptocurrency like Bitcoin and transfer it to an exchange that lists Peercoin, which will be discussed at a later time.

#### Coinbase

https://coinbase.com
CoinBase is one of the most popular broker sites and is arguably the most commonly used for US based citizens.

#### Gemini

https://gemini.com
Gemini also offers fiat purchasing options for Bitcoin with bank wire options.

#### OkCoin

https://www.okcoin.com/lang/en-US/
Offers fiat deposits by wire to buy Bitcoin and other common coins.

It is strongly recommended to purchase Bitcoin as it has the most traded pairs for the exchanges that list Peercoin which will be discussed in the section below.  Once you have made a purchase, send those coins over to your chosen exchange and make your purchase of Peercoin.

There are other websites that can be used to buy Bitcoin with a debit or credit card, and there are a plethora of guides available on these sites.  We suggest you find a reputable site with low fees and a large number of positive user reviews over time.

## Exchanges

If you already own cryptocurrency, the section about fiat gateways can be skipped since you most likely already have one.  Below is a list of exchanges which support Peercoin and where it can be traded actively.  Send your coins there and you will be able to purchase Peercoin.

### PPC/BTC Pairs

#### Bittrex

https://bittrex.com/Market/Index?MarketName=BTC-PPC

#### Cryptopia

https://www.cryptopia.co.nz/Exchange?market=PPC_BTC

#### HitBTC

https://hitbtc.com/PPC-to-BTC

#### Livecoin

https://www.livecoin.net/

#### Poloniex

https://poloniex.com/exchange#btc_ppc

#### The Rock Trading

https://www.therocktrading.com/en/offers/PPCBTC

#### Tux Exchange

https://bx.in.th/BTC/PPC/

____________

Each exchange comes with a variety of fees both in trading and withdrawals and user experience may vary.  As always, use strong passwords, 2FA, and cold storage as needed.

Once you have made your purchase, you can withdraw your coins to the wallet you have chosen.

---


# Official client implementation

Once you install official Peercoin client from peercoin.net, you’ll have access to three executables: peercoind, peercoin-qt, and peercoin-cli.

## Peercoin Wallet

`peercoin-qt` provides a combination full Peercoin network client and wallet. Peercoin-qt is highly portable application written in QT5 framework.
From the Help menu, you can access a console where you can enter the RPC commands so power-user features are still available.

## peercoind

`peercoind` provides a full peer which you can interact with through JSON-RPC interface on port 9904 (902 for testnet).

For more information on how to use the JSON-RPC interface see the [json-rcp-api-reference article](./006-json-rpc-api-reference.md)

## peercoin-cli

`peercoin-cli` allows you to send JSON-RPC commands to running instance of `peercoind` from the command line.
For example:
> peercoin-cli help

> peercoin-cli getinfo

All three programs get settings from peercoin.conf in the Peercoin application directory:

> Windows: %APPDATA%\Peercoin\

> OSX: $HOME/Library/Application Support/PPCoin/

>Linux: $HOME/.peercoin/

To use `peercoind` and `peercoin-cli`, you will need to add a RPC password to your peercoin.conf file. Both programs will read from the same file if both run on the same system as the same user, so any long random password will work:

> rpcpassword=change_this_to_a_long_random_password

You should also make the peercoin.conf file only readable to its owner.
On Linux, Mac OSX, and other Unix-like systems, this can be accomplished by running the following command in the Peercoin application directory:

> chmod 0600 peercoin.conf

# Peercoin Core Wallet

## Overview

![Wallet Overview](../img/wallet.png)

### Windows Installation

To install on Windows, you can find the download files here: https://peercoin.net/download.  Once download is complete, extract the contents of the folder.  Depending on if your system is x32 or x64 bits, choosing the relevant folder.  Run the peercoin-win_setup.exe and you will be guided through the installation process.  Once finishes, the client can be launched by running "peercoin-qt.exe" from the appropriate folder.

### Debian Installation

As of April 2018, Peercoin has official Debian repository hosted at `repo.peercoin.net`.
Repository is serving .deb packages for latest Debian stable, for amd64 and armhf hardware architectures.
Repository offers two packages, `peercoin-qt` which is official graphical client for the Peercoin network and `peercoind` which is a daemon client for the network.
In the future repository may host other Peercoin-related packages.

### Mac Installation

To install for MacOS, you can find the download files here: https://peercoin.net/download.  Once the download is complete, extract the contents of the folder.  Inside the extracted folder, double click the "Peercoin-Qt.dmg" file to open the client.

#### Adding the GPG key

`wget -O - https://repo.peercoin.net/peercoin.gpg.key | sudo apt-key add -`

#### Adding the repository in the sources

`sudo sh -c "echo 'deb http://repo.peercoin.net stretch main' >> /etc/apt/sources.list.d/peercoin.list"`

`sudo apt update`

#### Installing the packages

`sudo apt install peercoin-qt`

### Debian/Ubuntu Package Compilation Guide

If you want a more in-depth guide on the compilation of the client for a variety of systems, [more can be found here](004-compiling-packages-for-debian.md)
____________

## General Notes

### Wallet Encryption

When a wallet is first generated, it will be unencrypted.  In order to encryt the wallet, one must go to Settings > Encrypt Wallet.  The client will then prompt the user for a password which will then be used to verify transactions and unlock the wallet for minting in the future.  It is important to make sure this password is remembered as losing access means losing access to any coins held in that wallet.  A wallet must be encrypted in order to participate in minting.

### Backups

It is strongly recommended that a backup of the wallet.dat is made and kept in a separate location in the event of hardware failure or similar disaster.  Choosing File > Backup Wallet, will present the user with the option of where to export this file.

____________

## Wallet Overview

From this tab you can see the "Available", "Pending", and "Total" balance of your Peercoin wallet.  On the right side, you can see your "Recent transactions" as well which will show the most recent transactions that have come into the wallet recently.

### Send

![Send Tab](../img/send.png)

The send tab is used to send Peercoin.  The "Pay To" section is where a target address can be entered.  If you wish to label the address for future use, such as an exchange, you may add it to your address book.  Amount determines the quantity of Peercoin which will be sent in the transaction.  If the wallet is encrypted, the secure password must be entered before the send transaction can be finalized.

### Receive

![Recieve Tab](../img/recieve.png)

The Receive tab lists all wallet addresses attached to the Peercoin client.  Generating a new address is as simple as clicking the "New Address" button at the bottom of the screen.  The "Sign Message" button can also be used to verify ownership of a wallet.  [There is a tutorial on signing messages with the Peercoin client here.](014-SigningMessages.md)  The example addresses have been removed from the image for privacy sake.

### Transactions

![Transactions Tab](../img/transactions.png)

The Transactions tab gives a full history of recent transactions that have come in and out of the wallet since its creation.  It will list the Date, Type, Address, and Amount.  This information can be exported as a .csv using the "Export" button on the bottom right of the screen.  The amounts have been removed from the image for privacy sake.

### Minting

![Peercoin staking](../img/staking.png)

The Minting tab is the fifth option and from here, you can see the coin age of your transaction.  The Address, Age, Balance, CoinDay, and MintProbability, are also displayed.  Until the transaction reaches 30 days of age, it will be displayed in red, with a CoinDay of 0.  In the picture above, you can see a transaction that is red and is not eligible for staking due to it only having a an Age of 49.  In the next 30 days, it has a probability of minting of roughly 54.94%.  In 4 days, that transaction will become eligible for minting and change to green color.  You can use the "Display minting probability within:" drop-down menu to estimate the probability of minting during the next period.  Once the 30 day period has passed, and the transaction has become eligible for minting, go to Settings > Decrypt Wallet for Minting Only, and enter your wallet password.  If you have not already encrypted your wallet, you will be asked to do so.  Once the wallet has been unlocked for minting, leaving it running will allow for minting to occur.  Making a transaction from that wallet will disrupt the coin age and the maturation process will have to be repeated.  Sending more coins will not disrupt the coin age.

If you are interested in calculating the rough time until minting takes place, you can use this calculator: http://poscalculator.peercointalk.org/

Once minting occurs, the initial batch of coins will have their coin age reset, and the coins earned from minting will remain locked for 520 blocks, or roughly 3 days.  After this period, the coins will be available in the wallet.  As a note, you do not need to leave your wallet running 24/7, as the time spent staking does not increase the probability of minting taking place, as the highest coin age will always take precedence.  Holding longer also does not increase the minting reward.

### Addresses

![Addresses](../img/addresses.png)

Addresses is the final tab and displays the addresses saved to the Address Book from the Send tab.  This is handy for managing repeat use addresses such as exchanges.  The example address has been removed from the image for privacy sake.

____________

## Creating a New Address

Creating a new address is very simple.  Navigate to the "Receive" tab and select the "New Address" button.  A window with a "Label" and "Address" field will appear.  Enter the name you want in the "Label" field.  You will be able to change this later.  Leave the "Address" field blank.  Click "Ok" to continue.  If you have already encrypted your wallet, you will need to enter your wallet password.

![New Address Window](../img/newaddress.png)

![New Address Created](../img/newaddress2.png)

You can see the new address now available.  If you want to change the name of the label of the address, double click the name and you will be able to enter a new one.

_________________________________________

## Sending Peercoin

If you want to send Peercoin, navigate to the "Send" tab.  We are going to send some Peercoins to the address we created above.  This page has three fields: "Pay To", "Label", and "Amount".  Paste the address you want to send Peercoins to into the "Pay To" field.  Make sure to verify that this address is correct.  If you already have a label for this wallet, it will automatically fill in the "Label" field.  If not, you can write your own in and it will be saved in your address book (Under the "Address" tab).  In the amount field, insert the number of Peercoins you would like to send.  There is a drop down menu which allows you to determine if you want to send in denominations of "Peercoins", "MilliPeercoins", "MicroPeercoins".  Make sure that you have enough to pay for the transaction fee.  When everything is finalized, press the "Send" button to confirm the transaction.  You will be prompted to confirm the transaction and must enter your wallet password to verify the transaction.  Once this is completed, you can view the transaction under the "Transactions" tab.

![Sending Peercoin](../img/sendingpeercoin.png)

_________________________________________

# Using the multisig

You can access multisig graphic interface in latest builds of Peercoin-qt. Open Peercoin-qt, click on File - Multisig. Now you see Multisig interface.

![Peercoin-qt multisig](../img/multisig.png)

## How to create a multisig address using QT wallet

In this example, we'll go over creating 2/3 multisig address.
On your screen you see two tables, each containing "Public key", "Address" and "Label".

1) First click "+ Add public key" button, this will make three input fields. Then enter number 2 in the "Required signatures" field.

2) In the first table, we will first make input in "Address field". You can click book-like icon on the right side to load address from your address book. When you do so, other fields will be auto-populated.

3) Your partners will need to do the same and copy their entries to you. When you exchange information properly make final check to reduce chance of error and finally click on "Create multisig address" button.

4) Now multisig address is created, confirm that all of you got the same address.

5) Finally click "Add address to wallet" in lower right to have it listed in your address book.

That is it, now you have your 2/3 multisig address.

## Creating a multisig address using the command line interface (debug console)

The multisig address is generated with the complete public keys of the participants.

**Alice:**

validateaddress "mw2pj33HMhRfRkKtceHcyKpPiGYkPdD4SM"

    {
      "isvalid" : true,
      "address" : "mw2pj33HMhRfRkKtceHcyKpPiGYkPdD4SM",
      "ismine" : true,
      "isscript" : false,
      "pubkey" : "02c16ff447129fae7374d97212cf9fcd88a744da87ff2985869065cd6d17ee5c0b",
      "iscompressed" : true,
      "account" : "Alice"
    }


**Bob:**

validateaddress "mkLNecFNeiJgKjw6492nqDiQfKQs1JnLmE"

     {
       "isvalid" : true,
       "address" : "mkLNecFNeiJgKjw6492nqDiQfKQs1JnLmE",
       "ismine" : true,
       "pubkey" : "025cc4b319284aabcdaef6e9a18af0bb73ac5d4b9f2556a214f30686b0173b316e",
       "iscompressed" : true,
       "account" : "Bob"
     }


**Charlie:**

validateaddress "mm8Fwn92RU8zvJmH7TCpaYL3v4PTyjN4xd"

    {
      "isvalid" : true,
      "address" : "mm8Fwn92RU8zvJmH7TCpaYL3v4PTyjN4xd",
      "ismine" : true,
      "isscript" : false,
      "pubkey" : "033ba42c942ff7e7fcf42ff604d6ef6c51826f9eea3a04308379c2ade98fb9e703",
      "iscompressed" : true,
      "account" : "Trent"
    }

createmultisig 2 '["02c16ff447129fae7374d97212cf9fcd88a744da87ff2985869065cd6d17ee5c0b", "025cc4b319284aabcdaef6e9a18af0bb73ac5d4b9f2556a214f30686b0173b316e", "033ba42c942ff7e7fcf42ff604d6ef6c51826f9eea3a04308379c2ade98fb9e703"]'

    {
      "address" : "2N582fRZZZm9hL4RH4sguG9SDDLZhu7eeng",
      "redeemScript" : "522102c16ff447129fae7374d97212cf9fcd88a744da87ff2985869065cd6d17ee5c0b21025cc4b319284aabcdaef6e9a18af0bb73ac5d4b9f2556a214f30686b0173b316e21033ba42c942ff7e7fcf42ff604d6ef6c51826f9eea3a04308379c2ade98fb9e70353ae"
    }

_________________________________________

## How to spend from the multisig address

Reference Peercoin client is not capable of indexing the multisig addresses and showing their balance because multisig addresses can be owned by keys which are not part of the wallet (friends, family, backup). Thus the procedure to spend the funds from the multisig is a bit more complicated, more "low level" then usual.

In the "Spend Funds" tab of the multisig dialog, on the left there is "Inputs" table. You need to provide with the [UTXO](https://en.wikipedia.org/wiki/Unspent_transaction_output) you want to spend. That is, the `txid` and output index. On the right side there is "Outputs" table, where the desired outputs will be placed. Please note that you have to include the change output and deduct the tx fee (0.01 PPC per kB).

After that is set, click on the "Create Transaction" button bellow, and copy the resulting hash to your peers for further signing.
Finally paste the hash of fully signed raw transaction into "Sign Transaction" box bellow and click send.

![Peercoin-qt multisig spending](../img/multisig-spend.png)


### Spending from the multisig via command line interface

Bob creates a transaction to spend the coins that Alice sent to the multisig address.
The transaction will have 360 PPC (Alice's coins) as input and 359.99 PPC as output (because of the mandatory 0.01 PPC transaction fee; the transaction won't be accepted by the network without it).


**Bob:**

getrawtransaction "0ef16552d0dadaa150da34cfbc5380e82d59b5f328f967fb72104c43a1b99f74" 1

    {
      "hex" : "01000000197f5a530105a302fe97c3ab33581486fdb39296e8728d2dac7b06324a62ab83515c30d9d8000000006b4830450221008054ee73403f401b2c10acdaed1e51e5345d35fb24574719d8a01203934c6e3202204d97e79ccdae05713b18d85e36896e3bd7a1a0636bd207a493779ca6a7c148c4012102c16ff447129fae7374d97212cf9fcd88a744da87ff2985869065cd6d17ee5c0bffffffff02f0591b2c000000001976a9149f99f0ec7288694065243d32bea766bf9a8d602188ac002a75150000000017a914824524d69e3c8f2ea66e39af89727bc0e8d3de4b8700000000",
      "txid" : "0ef16552d0dadaa150da34cfbc5380e82d59b5f328f967fb72104c43a1b99f74",
      "version" : 1,
      "locktime" : 0,
      "vin" : [
        {
          "txid" : "d8d9305c5183ab624a32067bac2d8d72e89692b3fd86145833abc397fe02a305",
          "vout" : 0,
          "scriptSig" : {
            "asm" : "30450221008054ee73403f401b2c10acdaed1e51e5345d35fb24574719d8a01203934c6e3202204d97e79ccdae05713b18d85e36896e3bd7a1a0636bd207a493779ca6a7c148c401 02c16ff447129fae7374d97212cf9fcd88a744da87ff2985869065cd6d17ee5c0b",
            "hex" : "4830450221008054ee73403f401b2c10acdaed1e51e5345d35fb24574719d8a01203934c6e3202204d97e79ccdae05713b18d85e36896e3bd7a1a0636bd207a493779ca6a7c148c4012102c16ff447129fae7374d97212cf9fcd88a744da87ff2985869065cd6d17ee5c0b"
          },
          "sequence" : 4294967295
        }
      ],
      "vout" : [
        {
          "value" : 739.99000000,
          "n" : 0,
          "scriptPubKey" : {
            "asm" : "OP_DUP OP_HASH160 9f99f0ec7288694065243d32bea766bf9a8d6021 OP_EQUALVERIFY OP_CHECKSIG",
            "hex" : "76a9149f99f0ec7288694065243d32bea766bf9a8d602188ac",
            "reqSigs" : 1,
            "type" : "pubkeyhash",
            "addresses" : [
              "mv4r9a4FXuDgSA5GaFtLGC9W5Db3XJUrLD"
            ]
          }
        },
        {
          "value" : 360.00000000,
          "n" : 1,
          "scriptPubKey" : {
            "asm" : "OP_HASH160 824524d69e3c8f2ea66e39af89727bc0e8d3de4b OP_EQUAL",
            "hex" : "a914824524d69e3c8f2ea66e39af89727bc0e8d3de4b87",
            "reqSigs" : 1,
            "type" : "scripthash",
            "addresses" : [
              "2N582fRZZZm9hL4RH4sguG9SDDLZhu7eeng"
            ]
          }
        }
      ],
      "blockhash" : "05a7088c02f589ca91beb52ea9667955f7ee10a2433e56f2e11a058c2273bb70",
      "confirmations" : 2,
      "time" : 1398439709,
      "blocktime" : 1398439709
    }

createrawtransaction '[{"txid" : "0ef16552d0dadaa150da34cfbc5380e82d59b5f328f967fb72104c43a1b99f74", "vout" : 1, "scriptPubKey" : "a914824524d69e3c8f2ea66e39af89727bc0e8d3de4b87", "redeemScript" : "522102c16ff447129fae7374d97212cf9fcd88a744da87ff2985869065cd6d17ee5c0b21025cc4b319284aabcdaef6e9a18af0bb73ac5d4b9f2556a214f30686b0173b316e21033ba42c942ff7e7fcf42ff604d6ef6c51826f9eea3a04308379c2ade98fb9e70353ae"}]' '{"mub5ke5cWP4nZW2VDgtAkFGA7UzSVhwese" : 359.99}'

    0100000062815a5301749fb9a1434c1072fb67f928f3b5592de88053bccf34da50a1dadad05265f10e0100000000ffffffff01f0027515000000001976a9149a59a69866c7668acdd2b36491cfc18229d2348988ac00000000


#### First signature of the transaction

Bob signs the new transaction with the private key associated to the public key he used to create the multisig address and sends the result to Alice.


**Bob:**

dumpprivkey "mkLNecFNeiJgKjw6492nqDiQfKQs1JnLmE"

    cTxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxo5

signrawtransaction "0100000062815a5301749fb9a1434c1072fb67f928f3b5592de88053bccf34da50a1dadad05265f10e0100000000ffffffff01f0027515000000001976a9149a59a69866c7668acdd2b36491cfc18229d2348988ac00000000" '[{"txid" : "0ef16552d0dadaa150da34cfbc5380e82d59b5f328f967fb72104c43a1b99f74", "vout" : 1, "scriptPubKey" : "a914824524d69e3c8f2ea66e39af89727bc0e8d3de4b87", "redeemScript" : "522102c16ff447129fae7374d97212cf9fcd88a744da87ff2985869065cd6d17ee5c0b21025cc4b319284aabcdaef6e9a18af0bb73ac5d4b9f2556a214f30686b0173b316e21033ba42c942ff7e7fcf42ff604d6ef6c51826f9eea3a04308379c2ade98fb9e70353ae"}]' '["cTxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxo5"]'

    {
      "hex" : "0100000062815a5301749fb9a1434c1072fb67f928f3b5592de88053bccf34da50a1dadad05265f10e01000000b40047304402201dfd957507d6b48b777a6f5c31d85fb8d00513b79c55dbd902c7f6dee90bc4cc0220773f05b481a9dbbc3153cb832acd994caef0d569de49d3b4a125b5f1e637836c014c69522102c16ff447129fae7374d97212cf9fcd88a744da87ff2985869065cd6d17ee5c0b21025cc4b319284aabcdaef6e9a18af0bb73ac5d4b9f2556a214f30686b0173b316e21033ba42c942ff7e7fcf42ff604d6ef6c51826f9eea3a04308379c2ade98fb9e70353aeffffffff01f0027515000000001976a9149a59a69866c7668acdd2b36491cfc18229d2348988ac00000000",
      "complete" : false
    }


#### Second signature of the transaction

Let's imagine that Alice refuses to sign the transaction.
Bob sends the transaction with one signature to Trent and asks him to validate it. Let's imagine that Trent decides that the transaction is legitimate.
Trent signs the transaction with the private key associated to the public key he used to create the multisig address.


**Charlie:**

dumpprivkey "mm8Fwn92RU8zvJmH7TCpaYL3v4PTyjN4xd"

    cPxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxis

signrawtransaction "0100000062815a5301749fb9a1434c1072fb67f928f3b5592de88053bccf34da50a1dadad05265f10e01000000b40047304402201dfd957507d6b48b777a6f5c31d85fb8d00513b79c55dbd902c7f6dee90bc4cc0220773f05b481a9dbbc3153cb832acd994caef0d569de49d3b4a125b5f1e637836c014c69522102c16ff447129fae7374d97212cf9fcd88a744da87ff2985869065cd6d17ee5c0b21025cc4b319284aabcdaef6e9a18af0bb73ac5d4b9f2556a214f30686b0173b316e21033ba42c942ff7e7fcf42ff604d6ef6c51826f9eea3a04308379c2ade98fb9e70353aeffffffff01f0027515000000001976a9149a59a69866c7668acdd2b36491cfc18229d2348988ac00000000" '[{"txid" : "0ef16552d0dadaa150da34cfbc5380e82d59b5f328f967fb72104c43a1b99f74", "vout" : 1, "scriptPubKey" : "a914824524d69e3c8f2ea66e39af89727bc0e8d3de4b87", "redeemScript" : "522102c16ff447129fae7374d97212cf9fcd88a744da87ff2985869065cd6d17ee5c0b21025cc4b319284aabcdaef6e9a18af0bb73ac5d4b9f2556a214f30686b0173b316e21033ba42c942ff7e7fcf42ff604d6ef6c51826f9eea3a04308379c2ade98fb9e70353ae"}]' '["cPxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxis"]'

    {
      "hex" : "0100000062815a5301749fb9a1434c1072fb67f928f3b5592de88053bccf34da50a1dadad05265f10e01000000fdfd000047304402201dfd957507d6b48b777a6f5c31d85fb8d00513b79c55dbd902c7f6dee90bc4cc0220773f05b481a9dbbc3153cb832acd994caef0d569de49d3b4a125b5f1e637836c014830450220576a38baba9c821a5dbfce6be50825322995041a052f8a76016928ee2741b542022100e95dcefd049628e8c422ee584eb1c3feab3d00f7111a29a16f40353ff7de9648014c69522102c16ff447129fae7374d97212cf9fcd88a744da87ff2985869065cd6d17ee5c0b21025cc4b319284aabcdaef6e9a18af0bb73ac5d4b9f2556a214f30686b0173b316e21033ba42c942ff7e7fcf42ff604d6ef6c51826f9eea3a04308379c2ade98fb9e70353aeffffffff01f0027515000000001976a9149a59a69866c7668acdd2b36491cfc18229d2348988ac00000000",
      "complete" : true
    }


#### Send the signed transaction to the network

The transaction has the two required signatures, anyone can send it to the network.

sendrawtransaction "0100000062815a5301749fb9a1434c1072fb67f928f3b5592de88053bccf34da50a1dadad05265f10e01000000fdfd000047304402201dfd957507d6b48b777a6f5c31d85fb8d00513b79c55dbd902c7f6dee90bc4cc0220773f05b481a9dbbc3153cb832acd994caef0d569de49d3b4a125b5f1e637836c014830450220576a38baba9c821a5dbfce6be50825322995041a052f8a76016928ee2741b542022100e95dcefd049628e8c422ee584eb1c3feab3d00f7111a29a16f40353ff7de9648014c69522102c16ff447129fae7374d97212cf9fcd88a744da87ff2985869065cd6d17ee5c0b21025cc4b319284aabcdaef6e9a18af0bb73ac5d4b9f2556a214f30686b0173b316e21033ba42c942ff7e7fcf42ff604d6ef6c51826f9eea3a04308379c2ade98fb9e70353aeffffffff01f0027515000000001976a9149a59a69866c7668acdd2b36491cfc18229d2348988ac00000000"

    fea9875ccac102897ff128c868027a05e3d2f9057569529c8e5e94f8d641bc47

# How To Sign a Message Using the Peercoin Client

First, check that the address you want to use is loaded up into the wallet of your Peercoin client.  You can use the standard client found [here](https://peercoin.net/download).  The list of your addresses can be found using the receive tab.

![1](https://talk.peercoin.net/uploads/default/original/2X/3/3a72b5afa078a4d7b24cfaa7e2a5a303014ec6c6.jpeg)

Once you are satisfied that the address is in the wallet (you can even copy it to your clipboard if you like), open up the 'Sign message...' option of the 'File' menu.

![2](https://talk.peercoin.net/uploads/default/original/2X/3/3709984353eb778d29e1a91704b170b702383e59.jpeg)

At this point, you should be on the 'Sign Message' tab where you can paste in the address you want to use, either via your clipboard or by clicking on the address book button.

![3](https://talk.peercoin.net/uploads/default/original/2X/3/3b6c44045c17aab2a7694b571812d960da105975.jpeg)

Now you can type your message into the big blank box.  It might be best to copy and paste this text from a plaintext source in order to avoid any formatting issues.  When you are done, hit the 'Sign Message' button.

![4](https://talk.peercoin.net/uploads/default/original/2X/a/abc4f6835c2841fbd763f9985dcd15034005db50.jpeg)

If it completed its function correctly, it will display in green 'Messaged signed.'  Copy the signature using the convenient button.

![5](https://talk.peercoin.net/uploads/default/original/2X/8/8728853e3d051ebf766435752b6102ffcd8f960c.jpeg)

Just to be sure everything worked correctly, you can validate your signature.  Go to the 'Verify Message' tab and fill in all the fields.  If everything looks good, and it comes back with a green 'Message verified.' then you can share with anyone your signature, message, and address and they should be able to verify it just the same.

![6](https://talk.peercoin.net/uploads/default/original/2X/1/1f6ed2c60c32921af99e1c59cc27eb4124caaffa.jpeg)

Congratulations, you have now cryptographically signed and verified a message!


# Hardware Wallets

## Stakebox

![stakebox](https://talk.peercoin.net/uploads/default/original/2X/8/8581bbbb551a82aea92598a5aa93c4144e387317.png)


Stakebox is a project by Peercoin Foundation and PiSupply to deliver cost and power efficient, user friendly set-top box able to run a blockchain node.
Stakebox is a plug and play Pi with the Peercoin wallet pre-installed.What is need is a keyboard and monitor to plug in to and you are ready to go.

*StakeBox is a brand by Pi Supply, which is a world leading distributor of Raspberry Pi mini computers.*


### Installation

Beside ordering a pre-installed Stakebox from [PiSupply website](https://www.stakebox.org/products/peercoin-stakebox) you can also make one yourself.

What do you need:

* Raspberry Pi (2 or newer)
* image downloaded from files.peercoin.net
* an SD card (4GB +)
* some spare time

Download the image from files.peercoin.net, use the [Etcher](http://etcher.io/) to load it to the SD card.

Now follow the guide: https://www.stakebox.org/blogs/learn/getting-started-with-peercoin-stakebox.

## Ledger Peercoin Tutorial

### Ledger Live

If you wish to store Peercoin on the Ledger Nano or Ledger Blue, this tutorial will guide you through using the Ledger Live program

Open the Ledger Live program and enter your password to unlock the wallet.  In order to store Peercoin, we first need to add the Peercoin wallet application to the Ledger device.  If this is the first time you are using a Ledger device, you will have to install the Bitcoin app first.  Follow the same steps to add the Bitcoin app, then do the same process for the Peercoin application.  Select Manager from the sidebar and make sure your device is connected, unlocked, and allows access when prompted by the Ledger Manager.

![Ledger Live main screen](../img/ledgerman_main.JPG)

Once this is done, you will be presented with a variety of apps that can be added.  Type in "Peercoin" to find the Peercoin app.  Click the "Install" button and you will be asked to confirm this on your Ledger device.  After a moment, the app will be done installing.  Click "Okay" to proceed.

![Manager](../img/ledgerman_manager.JPG)

![Installing](../img/ledgerman_installing.JPG)

Once this is finished, the Peercoin app is now installed on your Ledger device.  Now we need to add an actual wallet account which we can do by clicking "Portfolio" to return to our starting screen.  Once you are on the main screen, click the "+" by the Accounts tab to add a new asset.

![Ledger Live main screen](../img/ledgerlive_main.JPG)

This will open the menu where you can search for the asset account you would like to add.  Input "Peercoin" and click continue.  You will have to unlock your Ledger again and navigate to the Peercoin app.  To open it, press both buttons on the Ledger Nano device simultaneously.  Once this is done, Ledger Live will sync and you will have the option to name the newly created account.

![Which Asset do you want to add?](../img/ledgerlive_select.JPG)

![Adding Peercoin](../img/ledgerlive_select2.JPG)

Click continue until everything is finalized and completed.  You now have the Peercoin app, and the account added to your Ledger product and wallet.

## Peercoin Paper Wallet Guide

You can find the source code for this wallet here: https://github.com/peercoin/peercoin-address-generator/

If you are interested in generating a paper wallet for holding your Peercoin, this guide will walk you through the process.  First, navigate to this address: https://paperwallet.peercoin.net/

![Paper Wallet Home Screen](../img/paperwallet_mainscreen.JPG)

To being, click the large green Start button.  This will begin the wallet generation process.  In order to ensure randomness, you will be asked to move your mouse cursor around for a period until a wallet address is generated.  This movement of the mouse adds entropy to the generation of an truly random address

![Swipe finger for randomness](../img/paperwallet_random.JPG)

![Keep Swiping](../img/paperwallet_keepswiping.JPG)

Once you have moved the mouse enough, the wallet will be generated and you will be presented with the public and private key for the new wallet.

![Finished!](../img/paperwallet_finished.JPG)

To export the wallet, click the green share icon on the left side of the QR code.  You will then be presented with the options displayed below.

![Saving Options](../img/paperwallet_savingoptions.JPG)

*Save .txt locally
   *This option will download the wallet as a text file.*
*Copy address/priv. key to clipboard
   *This option will copy the address/priv. key to a clipboard where it can be pasted.  Make sure your system is clean and secure before exposing this information to potential threats like keystroke loggers.*
*Send via email
   *This option will allow you to send the wallet information via email.*
*Save JSON data will
   *This option will download the wallet information in JSON format.*
*Paper Wallet (print)
   *This option will open a print dialogue from which the wallet can be printed or saved as a PDF.  Paper wallets provide physical security and backups for Peercoins that are to be left in cold storage.*

This concludes the tutorial on the paper wallet generator.  This platform provides extra security for those who wish to keep their Peercoin in a safe and physical location.

#  Unofficial client implementations

## Coinomi

https://www.coinomi.com/

## Coinspot

https://www.coinspot.com.au

## CoinVault

https://www.coinvault.io/

## Cryptonator

https://www.cryptonator.com/

## HolyTransaction

https://holytransaction.com/

## Ledger

https://www.ledger.com/

## Magnum

Airdrop focused wallet

https://magnumwallet.co

## UberPay

http://uberpay.io/

---


# PeerAssets

> PeerAssets offers the framework that enables communities and organizations to issue and transact with blockchain assets.

PeerAssets is a Peercoin in-house developed blockchain token protocol. At the time of writing PeerAssets is tailored to work with the Peercoin blockchain, however there are plans to port the technology to other blockchains like Bitcoin and allow for cross-chain compatibility. PeerAssets is as minimalist as possible, seeking to find the most efficient and affordable method for a blockchain to support tokenization.
PeerAssets transactions are standard Peercoin transactions, relayed by the standard nodes and processed by miners as any other transaction. Unlike many similar protocols ([Omni](http://www.omnilayer.org/), [CounterParty](http://counterparty.io/)), PeerAssets does not use so called "auxilary" tokens (Omni and XCP respectively), it only uses blockchain's native currency which is used to pay transaction fees. PeerAssets protocol does not require hard nor soft fork of the host network, but it requires development of a PeerAssets aware client. PeerAssets is also inspired by the original idea of "Colored Coins" and uses OP_RETURN to write data on the blockchain, but offers some optimizations to reduce amount of data written in the OP_RETURN and reducing blockchain bloat.
PeerAssets enables easy querying of the blockchain for relevant transactions via the use [P2TH](http://peerassets.github.io/P2TH/), which allows development of very light clients and does not mandate the use of resource intense blockchain-parsing nodes which are common with competing protocols.

PeerAsset protocol based assets can be utilized to represent any type of asset like bonds or equity. PeerAssets can also represent real life objects, and by doing so confirm their existence on the blockchain.

PeerAssets was invented in 2016, and the whitepaper was released in April, 2016 by `peerchemist`.

### Nomenclature

PeerAssets uses a somewhat different phrasing to describe the protocol and it's interactions. In PeerAssets terminology assets are named “decks” and each transaction on the deck is called a “card”. Decks and cards are types of transactions parsed by the PeerAsset client to understand the bigger picture and calculate the cards balances and thus the state of the deck.

`Deck - asset`

`Card - individual token`

## Transaction types

PeerAssets protocol has four elemental transaction types:

* **Deck spawning transaction**

Creates a new token at a given Peercoin address. Asset is described by:
* token name,
* descriptive metadata,
* how divisible the token is (number of decimals),
* the deck issue mode.

Deck issue modes can be understood as light smart contracts, speaking in modern crypto jargon as they allow great flexibility when defining rules of token supply.

* **Card issue transaction**

Creates new tokens of `deck` at given Peercoin address.

* **Card burn transaction**

Destroys tokens and removes them from the supply.

* **Card transfer transaction**

Standard p2p token transaction, transfer a token from the address where they reside to a new address.

## Tools

### pacli

This command line program is useful as companion utility during PeerAssets development and testing. It is built for console usage via intuitive and easy to learn set of commands. It stores the privkey in OS's native keystore, which is automatically unlocked upon logging into active user session.

github: https://github.com/PeerAssets/pacli

### pypeerassets

Official Python implementation of the PeerAssets protocol.

github: https://github.com/PeerAssets/pypeerassets

### papi

PeerAssets API provider, implemented using pypeerassets.

github: https://github.com/PeerAssets/papi

deployed: https://papi.peercoin.net/api/v1/decks

## Wallets

### chizukeki

(work in progress)

A light, cross-platform Peercoin wallet with baked-in support for the PeerAssets.

code: https://github.com/peerassets/chizukeki

deployed: https://peerassets.github.io/chizukeki/

## Future plans & research

The PeerAssets project has adopted [RFC](https://en.wikipedia.org/wiki/Request_for_Comments) schema of sharing new ideas and establishing standards like the Peercoin project.
RFC's are submitted on the PeerAssets [github repo](https://github.com/PeerAssets/peerassets-rfcs) and peer-reviewed, after which code experimentation and final implementation proceeds.

There is a number of interesting RFC which are currently discussed, such as:

[PeerAssets Alias/Proof-of-identity protocol specification](https://github.com/PeerAssets/peerassets-rfcs/blob/master/0003-peerassets-alias-poid-protocol-specification.md)

> Extension of PeerAssets protocol specifies using singlet PeerAsset deck to alias the Peercoin address with any UTF-8 string with added secondary functionality of using descriptive information contained in the PeerAssets token to allow proof-of-identity verification of the privkey owner.

[PeerAssets on-chain voting protocol specification](https://github.com/PeerAssets/peerassets-rfcs/blob/master/0005-on-chain-voting-protocol-proposal.md)

> PeerAssets on-chain voting protocol. Aim is to deliver a standardized way to organize and operate peer-to-peer voting and opinion polls in fully decentralized and trustless fashion. Both vote and poll initialization and counting must be done in completely decentralized and trustless fashion without dependency on 3rd party services.

[PeerAssets Data Audit Protocol](https://github.com/PeerAssets/peerassets-rfcs/blob/master/0009-data-audit.md)

> The primary purpose of this protocol is to record cryptographic hashes of successive revisions of single-file documents in a public blockchain, in a manner which enables thin clients to easily query and verify document histories. Such histories inherit useful properties from the underlying blockchain, namely immutability and massive replication, and can therefore serve as proofs of existence.

## Articles
[Whitepaper](http://peerassets.github.io/WhitePaper/)

[PeerAssets deck issue modes](https://medium.com/peercoin/peerassets-deck-issue-modes-c419f38f7800)

[The benefits of PeerAssets](https://medium.com/peercoin/the-benefits-of-peerassets-77bad7693925)

[[Tutorial] PeerAssets Peer to Peer (p2p) Transactions](https://talk.peercoin.net/t/tutorial-peerassets-peer-to-peer-p2p-transactions/8640)

[[Tutorial] Basic Deck Creation with PeerAssets](https://talk.peercoin.net/t/tutorial-basic-deck-creation-with-peerassets/8639)


# Bootstrapping

## What is it?

> In computer technology the term (usually shortened to booting) usually
> refers to the process of loading the basic software into the memory of
> a computer after power-on or general reset, especially the operating
> system which will then take care of loading other software as needed.<sup>[9.1](#footnote-9.1)</sup>

For Peercoin it means loading all of the block chain history from a special
file containing a snapshot of block data.

This special file, named `bootstrap.dat`, allows the Peercoin client to
sync from your hard drive instead of the internet. Using a
`bootstrap.dat` file is faster and reduces stress on the Peercoin network to sync new nodes.

## How do I make a `bootstrap.dat`?

Any synced client has the ability to make a `bootstrap.dat` file. Assuming
you're running linux you can do the following to manufacture your own.
First, shutdown your client. Allow it to cleanly exit so we know the block
data is settled.

Now, navigate to the directory `~/.peercoin/blocks` in your terminal and
notice the files named `blk00000.dat`, `blk00001.dat`, `blk00002.dat`, etc.
These are the raw block data files that can be combined to form the
`bootstrap.dat`!

The command:
> cat blk*.dat > bootstrap.dat

will produce the `bootstrap.dat`.
The file is often then compressed (zip'ed, tar/gzip'ed) and shared.

The same process can be executed on Microsoft Windows (7+):

> CD C:\Users\<my_user>\AppData\Roaming\Peercoin

> COPY /b blk0001.dat+blk0002.dat bootstrap.dat

Or on OS X:

> cd "~/Library/Application Support/Peercoin/"

> cat blk*.dat > bootstrap.dat


On linux and OS X you can create hash of the bootstrap:

> sha256 bootstrap.dat

## How do I use a `bootstrap.dat`?

Assuming you're on linux and you haven't started the Peercoin client before.

Make the directory `~/.peercoin` if it doesn't exist and then move the
`bootstrap.dat` into the `~/.peercoin` directory.

Start the Peercoin client. You should see the status `Importing blocks from disk...` if the client has found the `bootstrap.dat` and is using it to
sync the block chain.

## Where can I download a `bootstrap.dat`?

We've put some recent copies on our [file server](https://files.peercoin.net) :)

* [Mainnet bootstrap.dat.zip](https://files.peercoin.net/download/peercoin_mainnet_2018_08_06_bootstrap.dat.zip) SHA256 `66c494e0c2a4c78ba19f14a3781ca77f1b8b16f3833fb85c10959ee991764a4c` | [torrent](https://files.peercoin.net/download/peercoin_mainnet_2018_08_06_bootstrap.dat.zip.torrent) | [magnet](magnet:?xt=urn:btih:9fc1f0d09a6598ae96ba5d8b9ac5caca0ae92402&dn=peercoin%5Fmainnet%5F2018%5F08%5F06%5Fbootstrap.dat.zip&tr=udp%3A%2F%2Fpublic.popcorn-tracker.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.ilibr.org%3A80%2Fannounce&tr=http%3A%2F%2Fatrack.pow7.com%2Fannounce&tr=http%3A%2F%2Fbt.henbt.com%3A2710%2Fannounce&tr=http%3A%2F%2Fmgtracker.org%3A2710%2Fannounce&tr=http%3A%2F%2Fmgtracker.org%3A6969%2Fannounce&tr=http%3A%2F%2Fopen.touki.ru%2Fannounce.php&tr=http%3A%2F%2Fp4p.arenabg.ch%3A1337%2Fannounce&tr=http%3A%2F%2Fpow7.com%3A80%2Fannounce&tr=http%3A%2F%2Fretracker.krs-ix.ru%3A80%2Fannounce)
* [Mainnet bootstrap.dat.tar.gz](https://files.peercoin.net/download/peercoin_mainnet_2018_08_06_bootstrap.dat.tar.gz) SHA256 `bac807186735347e2c7ccbfecb3d91045de32246258a7ba3e3d0a9c2a10b8ff0` | [torrent](https://files.peercoin.net/download/peercoin_mainnet_2018_08_06_bootstrap.dat.tar.gz.torrent) | [magnet](magnet:?xt=urn:btih:77f1c5352e9eca71e9f4f1e31487e7d13900a335&dn=peercoin%5Fmainnet%5F2018%5F08%5F06%5Fbootstrap.dat.tar.gz&tr=udp%3A%2F%2Fpublic.popcorn-tracker.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.ilibr.org%3A80%2Fannounce&tr=http%3A%2F%2Fatrack.pow7.com%2Fannounce&tr=http%3A%2F%2Fbt.henbt.com%3A2710%2Fannounce&tr=http%3A%2F%2Fmgtracker.org%3A2710%2Fannounce&tr=http%3A%2F%2Fmgtracker.org%3A6969%2Fannounce&tr=http%3A%2F%2Fopen.touki.ru%2Fannounce.php&tr=http%3A%2F%2Fp4p.arenabg.ch%3A1337%2Fannounce&tr=http%3A%2F%2Fpow7.com%3A80%2Fannounce&tr=http%3A%2F%2Fretracker.krs-ix.ru%3A80%2Fannounce)
* [Testnet bootstrap.dat.zip](https://files.peercoin.net/download/peercoin_testnet_2018_08_06_bootstrap.dat.zip) SHA256 `1312aaaf0d8466b6f7006bac60a5cad4daf36e1241f791924e45bc5959ff2452` | [torrent](https://files.peercoin.net/download/peercoin_testnet_2018_08_06_bootstrap.dat.zip.torrent) | [magnet](magnet:?xt=urn:btih:c70afb5100953362b45df75133e01bf1f9466e04&dn=peercoin%5Ftestnet%5F2018%5F08%5F06%5Fbootstrap.dat.zip&tr=udp%3A%2F%2Fpublic.popcorn-tracker.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.ilibr.org%3A80%2Fannounce&tr=http%3A%2F%2Fatrack.pow7.com%2Fannounce&tr=http%3A%2F%2Fbt.henbt.com%3A2710%2Fannounce&tr=http%3A%2F%2Fmgtracker.org%3A2710%2Fannounce&tr=http%3A%2F%2Fmgtracker.org%3A6969%2Fannounce&tr=http%3A%2F%2Fopen.touki.ru%2Fannounce.php&tr=http%3A%2F%2Fp4p.arenabg.ch%3A1337%2Fannounce&tr=http%3A%2F%2Fpow7.com%3A80%2Fannounce&tr=http%3A%2F%2Fretracker.krs-ix.ru%3A80%2Fannounce)
* [Testnet bootstrap.dat.tar.gz](https://files.peercoin.net/download/peercoin_testnet_2018_08_06_bootstrap.dat.tar.gz) SHA256 `15f0e40a7e99083b2ed27c78d37d0f201fd6c744537cf643925d0aae84395896` | [torrent](https://files.peercoin.net/download/peercoin_testnet_2018_08_06_bootstrap.dat.tar.gz.torrent) | [magnet](magnet:?xt=urn:btih:eb2a70e90285ca847be47b2f96e36e5cdec4580e&dn=peercoin%5Ftestnet%5F2018%5F08%5F06%5Fbootstrap.dat.tar.gz&tr=udp%3A%2F%2Fpublic.popcorn-tracker.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.ilibr.org%3A80%2Fannounce&tr=http%3A%2F%2Fatrack.pow7.com%2Fannounce&tr=http%3A%2F%2Fbt.henbt.com%3A2710%2Fannounce&tr=http%3A%2F%2Fmgtracker.org%3A2710%2Fannounce&tr=http%3A%2F%2Fmgtracker.org%3A6969%2Fannounce&tr=http%3A%2F%2Fopen.touki.ru%2Fannounce.php&tr=http%3A%2F%2Fp4p.arenabg.ch%3A1337%2Fannounce&tr=http%3A%2F%2Fpow7.com%3A80%2Fannounce&tr=http%3A%2F%2Fretracker.krs-ix.ru%3A80%2Fannounce)

## Footnotes

<a id="footnote-9.1">9.1</a>: https://en.wikipedia.org/wiki/Bootstrapping


# Proof-of-Stake

>Peercoin uses both the Proof-of-Work and Proof-of-Stake algorithms. The PoW algorithm is used to spread the distribution of new coins. Up to 99% of all Peercoins is created with PoW. Proof-of-Stake is used to secure the network: The chain with longest PoS coin age wins in case of a blockchain split-up.

`Minting`, as it is called in Peercoin to make a proof-of-stake block, is based on metrics of an unspent transaction.
If we take a look at the number one spot of the rich list, transaction c7293fc60c80bdcc374775d1f0734e0766465b905bae1a312fe487793be3b8f7 has among others the following characteristics:

* The transaction appeared in block 376161 at timestamp 1531750952 (Unix time).
* The transaction in the block has an offset of 383 bytes. It is the third transaction in the block. The size of the first two transactions in the block are respectively 78 and 224 bytes.
* The transaction timestamp is 1531750624.
* The second recipient (index 1) received 1786301.06651300 Peercoins which, at the moment, is still unspent.

These metrics, along with two more data points serves as a basis to calculate a hash for POS minting:

* a future timestamp X (in Unix time notation) in which the stake could win;
* a block modifier that was set by the network 1830080 seconds (~21 days) earlier than X.

Every 6 hours the network calculates a new block modifier to be used for POS minting.

The win in proof-of-stake minting, the calculated hash is compared to the current difficulty minus the coinage. The chances of finding a stake therefor improves when either the coin age increases or when the difficulty of the network decreases.

## Peercoin minting behaviour

* The Minting process can only start after 30 days of coinage.
* Minting coin age is maxed out after 90 days. Which means that after 90 days the only variable left in PoS is the current difficulty.
* Minting is predictable and not random. For a given transaction, you can calculate the maximum network PoS difficulty over time for your transaction to be able to mint a PoS block.
* Whenever this PoS difficulty is higher than the current network PoS difficulty your Peercoin client can mint a PoS block.
* PoS blocks can be rejected (orphans) if several people mint a PoS block within a given window (2 hours also called timedrift). Only one (the chain with longest coin age) will be accepted.
* Minting splits the transaction in two if coin age < 90 days.
* PoS block reward is 1% annually. This 1% is a factor of your coin age, and is not maxed out.
* A transaction that just staked has its coins locked for 520 confirmations (3-4 days).
* Merging transactions, spending coins, etc. burns coinage (resets it to 0).
* The PoS reward is directly added to your transaction which staked (if this transaction is split in two because coinage < 90 days, the reward is equally distributed to both resulting transactions).

## Peercoin v0.5 Proof-of-Stake protocol

![Peercoin PoS diagram](../img/pos-diagram.svg)

## Qualities of Proof-of-Stake Consensus

### Efficient
The use of Proof-of-stake mining in Peercoin is efficient because network security is not dependent on the use of massive amounts of electrical energy (proof-of-energy-burn). Instead minters invest their coins and time to emulate the PoW process. This is done by simply opening up their wallet app, sending coins to their address and letting them sit there while they are occasionally selected by the protocol to mint the next block. This process is both energy and cost efficient.

### Aligning interests
Because coin owners also produce new blocks in Proof-of-Stake, this means security providers and users of the network are ultimately the same group of people. No longer is there a separate group of security providers who only care about making profit and are not financially tied to the network itself. All security providers must own a stake in the network through ownership of Peercoin. As everyone has similar financial interests in the long-term future of the network this leads to much less conflict between factions with different ideas about how the blockchain should develop and evolve.

### User governance
Because users in Peercoin have the ability to produce blocks they also have the power to influence and determine the future direction of the network. User governance goes hand in hand with the PoS consensus mechanism. Peercoin is the very first blockchain capable of allowing its protocol rules to be governed directly by its users.

### Global network
As a direct consequence of the resource efficient consensus mechanism the number of people capable of participating in the race to create new blocks is significantly expanded. In addition to this security providers are also no longer drawn to geographical locations with cheap electricity. Due to the cost efficiency of operating a proof-of-stake node minting nodes can be set up anywhere in the world. This allows Peercoin to maximize its level of decentralization and achieve global security from minting users all around the world.

### Network security is price independent
Unlike proof-of-work where miners are completely dependent on the market price of a blockchain's native token to ensure profitability, Peercoin contains no such price dependency. Proof-of-stake minters are compensated as motivation to provide consistent security, however since this process is so inexpensive to perform minters actually have the ability to voluntarily operate a minting node without compensation if they want. Even without compensation from the network, the process of minting helps to secure the blockchain and along with it a stakeholder's overall investment. The ability to decide which version of the protocol to run also gives a minter the opportunity to make their voice heard concerning future upgrades to the network. These are two important reasons a stakeholder may have to want to run a node for free, however, compensation is automatically provided which makes it even better to participate. Running a proof-of-work mining node without compensation is just not possible due to the requirement of being profitable enough in order to afford the associated costs of participating. However, since 2012 it has been proven that Peercoin is capable of sustaining its network security even during the lowest periods of demand where market price was close to zero. If the network is capable of surviving extremely stressful conditions like these then it is likely to survive any challenges the market may present it with in the future.

### Higher Resistance to Censorship
As explained above, the efficiency of proof-of-stake results in a blockchain network that can easily be secured by people all over the world who hold some amount of Peercoin. This globally decentralized security makes the Peercoin network incredibly difficult to censor and shut down. This is similar to downloading files through a bittorrent network. In bittorrent network, many people around the world operate nodes where they hold a full copy of the file that others are trying to download. Pieces of the file are downloaded from different nodes until the full file has finished downloading. If a government were to deem this file sharing illegal and attempt to shut down the torrent network, they would be forced to target every single node on the network no matter where they happen to exist in the world. Even then, there is nothing stopping more torrent nodes from being created that share the same file. As long as one node exists that shares the file, it can be downloaded and spread to others.

Peercoin works in a similar way where minting nodes that process transactions can be operated from anywhere in the world as long as the minter has access to a computer, minimal electricity, some amount of Peercoin and an internet connection. Geographical decentralization of minting nodes makes it incredibly difficult to shut down the Peercoin network, but when the number of nodes around the world expands to thousands or even tens of thousands then it essentially becomes impossible to censor. In systems like these, individual nodes are usually called peers. Together they act as a peer-to-peer network. This is where Peercoin obtained its name. It was originally introduced by Sunny King as ppcoin, which stood for peer-to-peer coin. Shortly after it was renamed to Peercoin.


# Mining

>Peercoin uses both the Proof-of-Work and Proof-of-Stake algorithms. The PoW algorithm is used to spread the distribution of new coins. Up to 99% of all peercoins is created with PoW. Proof-of-Stake is used to secure the network: The chain with longest PoS coin age wins in case of a blockchain split-up.

Peercoin uses the hashcash double iterated SHA-256 algorithm for [Proof-of-Work mining](https://en.bitcoin.it/wiki/Proof_of_work). This means that any hardware that can mine Bitcoin can mine Peercoin as well.

To mine Peercoin, you need a mining software. Below is a list that is not official endorsed but have been found to have a decent reputation.

* [BFGMiner](http://bfgminer.org/)
* [CGMiner](https://github.com/ckolivas/cgminer)
* [EasyMiner](https://easyminer.net/)

There are others, but this list can be used as a starting place.  Each will request pool or solo information and should come with the related support.

## Peercoin Mining Profitability

If you want to calculate the profitability of mining Peercoin, you can use this website: https://www.coinwarz.com/calculators/peercoin-mining-calculator

## Mining Confirmations

Once a block has been mined, 520 blocks must be passed for the mining to be confirmed. This is roughly 3.61 days of time.

---


# Compiling

## Compiling packages for Debian and Ubuntu

As Peercoin is made to run on range of platforms, from Amazon's server to low powered Raspberry Pi Debian is perfect OS platform for deploying Peercoin nodes as it is renowned for multitude of supported hardware architectures as well as security and stability.

For compilation of Debian packages we will be using `pbuilder` which is a automatic Debian Package Building system for personal development workstation environments.<sup>[3.1](#footnote-3.1)</sup> pbuilder aims to be an easy-to-setup system for auto-building Debian packages inside a clean-room environment, so that it is possible to verify that a package can be built on most Debian installations. The clean-room environment is achieved through the use of a base chroot image, so that only minimal packages will be installed inside the chroot.

The following tutorial is written for the Ubuntu or Debian host, precisely Ubuntu 17.10 which is last stable version of Ubuntu at the time of writing.

## Prepare the tooling

`sudo apt install pbuilder qemu-user-static ubuntu-keyring debian-archive-keyring`

We'll also need keyring for the Raspbian, which a Debian fork made for the Raspberry Pi platform, so we can compile packages for this ARM based mini-pc platform.

> wget http://archive.raspbian.org/raspbian/pool/main/r/raspbian-archive-keyring/raspbian-archive-keyring_20120528.2_all.deb

> sudo dpkg -i raspbian-archive-keyring_20120528.2_all.deb

Now, set up the conf file for the pbuilder.

`touch .pbuilderrc`

> gedit .pbuilderrc

Paste the following:

```
#!/bin/sh

set -e

PBUILDERSATISFYDEPENDSCMD="/usr/lib/pbuilder/pbuilder-satisfydepends-apt"

if [ "$OS" == "debian" ]; then
    MIRRORSITE="http://ftp.no.debian.org/debian/"
    COMPONENTS="main contrib non-free"
    DEBOOTSTRAPOPTS=("${DEBOOTSTRAPOPTS[@]}"
        "--keyring=/usr/share/keyrings/debian-archive-keyring.gpg")
    : ${DIST:="wheezy"}
    : ${ARCH:="amd64"}
    if [ "$DIST" == "wheezy" ]; then
        #EXTRAPACKAGES="$EXTRAPACKAGES debian-backports-keyring"
        OTHERMIRROR="$OTHERMIRROR | deb $MIRRORSITE wheezy-backports $COMPONENTS"
    fi
elif [ "$OS" == "raspbian" ]; then
    MIRRORSITE="http://ftp.acc.umu.se/mirror/raspbian/raspbian/"
    COMPONENTS="main contrib non-free"
    DEBOOTSTRAPOPTS=("${DEBOOTSTRAPOPTS[@]}"
        "--keyring=/usr/share/keyrings/raspbian-archive-keyring.gpg")
    : ${DIST:="wheezy"}
    : ${ARCH:="armhf"}
elif [ "$OS" == "ubuntu" ]; then
    MIRRORSITE="http://no.archive.ubuntu.com/ubuntu/"
    COMPONENTS="main restricted universe multiverse"
    DEBOOTSTRAPOPTS=("${DEBOOTSTRAPOPTS[@]}"
        "--keyring=/usr/share/keyrings/ubuntu-archive-keyring.gpg")
else
    echo "Unknown OS: $OS"
    exit 1
fi

if [ "$DIST" == "" ]; then
    echo "DIST is not set"
    exit 1
fi

if [ "$ARCH" == "" ]; then
    echo "ARCH is not set"
    exit 1
fi

NAME="$OS-$DIST-$ARCH"

if [ "$ARCH" == "armel" ] && [ "$(dpkg --print-architecture)" != "armel" ]; then
    DEBOOTSTRAP="qemu-debootstrap"
fi
if [ "$ARCH" == "armhf" ] && [ "$(dpkg --print-architecture)" != "armhf" ]; then
    DEBOOTSTRAP="qemu-debootstrap"
fi

DEBOOTSTRAPOPTS=("${DEBOOTSTRAPOPTS[@]}" "--arch=$ARCH")
BASETGZ="/var/cache/pbuilder/$NAME-base.tgz"
DISTRIBUTION="$DIST"
BUILDRESULT="$HOME/pbuild-results/"
APTCACHE="/var/cache/pbuilder/$NAME/aptcache/"
BUILDPLACE="/var/cache/pbuilder/build"
HOOKDIR="/var/cache/pbuilder/hook.d/"
```

Make the directory where pbuilder will place the packages:

`mkdir -p $HOME/pbuild-results`

### Bootstrap the chroots

Raspbian:

> sudo OS=raspbian DIST=stretch ARCH=armhf pbuilder --create

Debian stable:

> sudo OS=debian DIST=stretch ARCH=amd64 pbuilder --create

## Preparing for build

(compiling for Raspbian stretch in this example)

Download the latest .tar.gz from github.com/peercoin.

> wget https://github.com/peercoin/peercoin/archive/v0.6.3ppc.rc1.tar.gz

Debian build system is very strict about names, so we need to rename this to:

`peercoin_0.6.3.orig.tar.gz`

Extract the contests of the file using `tar xf` and `cd` to it.

Copy the debian directory from the contrib to this directory:

`cp -r contrib/debian .`

### Some modifications

(this is just an extra step required for the Raspbian, to fix problem with autotools)

`sed '/./configure --with-gui=qt5 --with-incompatible-bdb/s/$/ --with-boost-libdir=/usr/lib/arm-linux-gnueabihf/' debian/rules`

## Building the package

`OS=raspbian DIST=stretch ARCH=armhf pdebuild`

And wait, it will take a while so go get a coffee or something. It's compiling by emulating ARM cpu in QEMU.

The concept of pbuild and cross-platform compilations is that you pass it this environment variables like "OS" and "DIST".

For example OS=debian and DIST=wheezy will use Debian Wheezy chroot, you can also pick architecture by using ARCH= environment variable.

## Footnotes

<a id="footnote-3.1">3.1</a>: https://jodal.no/2015/03/08/building-arm-debs-with-pbuilder/

# JSON-RPC API reference

Peercoin daemon offers JSON-RPC interface which can be used to control the daemon or integrate it with software stack.
You can send commands to the daemon by using `peercoin-cli` tool.

There are two official wrappers for this interface, a PHP one and a Python2.7+ one.

> Peercoin_rpc is a simple and minimal library made for communication with peercoind via JSON-RPC protocol. It has a single dependency - a Python requests library and it supports both mainnet and testnet peercoin network with authentication or SSL encryption. There is a single class to be imported from the library - Client.

https://github.com/peercoin/peercoin_rpc

> peercoin-php-rpc is a simple and minimal library made for communication with peercoind via JSON-RPC protocol for PHP 7.1+. Easiest way to use is to use composer. Otherwise include RpcClient class in your project an you are good to go.

https://github.com/peercoin/peercoin-php-rpc

## List of JSON-RPC calls

| Command            | Parameters  | Description    | Requires unlocked wallet? (yes/no)  |
|--------------------|-------------|---------------------------------|--------------------|
| `getinfo`          |             |Returns an object containing various state info.|no|
| `getblock`         |  `hash`     |Returns information about the block with the given hash.|no|
| `getblockcount`    |             |Returns the number of blocks in the longest block chain.|no|
| `getblockhash`     |`block_num`  |Returns hash of block in best-block-chain at `block_num`; 0 is the genesis block|no|
| `gettransaction`   | `txid`        |Returns an object about the given transaction containing:<br>  "amount" : total amount of the transaction<br>"confirmations" : number of confirmations of the transaction<br>"txid" : the transaction ID<br>"time" : time associated with the transaction|no|
| `walletpassphrase` | `passphrase`   `timeout` |Stores the wallet decryption key in memory for `timeout` seconds.|no|
| `getbalance`       |[account] [minconf=1]|If [account] is not specified, returns the server's total available balance.<br>If [account] is specified, returns the balance in the account.|no|
| `getreceivedbyaddress`| `address` [minconf=1] |Returns the amount received by `address` in transactions with at least [minconf] confirmations. It correctly handles the case where someone has sent to the address in multiple transactions. Keep in mind that addresses are only ever used for receiving transactions.<br>Works only for addresses in the local wallet, external addresses will always show 0.|no|
| `getdifficulty`    |  |Returns proof-of-stake and proof-of-work difficulty|no|
| `getpeerinfo`      |  |Returns data about each connected node.|no|
| `getaddressesbyaccount`| `account` |Returns the list of addresses for the given account.|no|
| `getnewaddress`    | [account] |Returns a new address for receiving payments.<br>If [account] is specified payments received with the address will be credited to [account].|no|
| `getaccount`       | `address` |Returns the account associated with the given `address`.|no|
| `getaccountaddress`| `account` |Returns the current address for receiving payments to this account.<br>If `account` does not exist, it will be created along with an associated new address that will be returned.|no|
| `sendtoaddress`    | `address` `amount` [comment] [comment-to] |  `amount` is a real and is rounded to 6 decimal places. Returns the transaction ID `txid` if successful.|yes|
| `sendfrom`         | `fromaccount` `topeercoinaddress` `amount` [minconf=1] [comment] [comment-to] |`amount` is a real and is rounded to 6 decimal places. Will send the given amount to the given address, ensuring the account has a valid balance using [minconf] confirmations. Returns the transaction ID if successful (not in JSON object).|yes|
| `sendmany`         | `fromaccount` {address:amount,...} [minconf=1] [comment] |  amounts are double-precision floating point numbers |yes|
| `getconnectioncount`|    |Returns the number of connections to other nodes.|no|
| `getrawtransaction`|  `txid` [verbose=0] |Returns raw transaction representation for given transaction id.|no|
| `getrawmempool`    |  |Returns all transaction ids in memory pool.|no|
| `listtransactions` | [account] [count=10] [from=0] | Returns up to [count] most recent transactions skipping the first [from] transactions for account [account]. If [account] not provided it'll return recent transactions from all accounts.|no|
| `listreceivedbyaddress`| [minconf=1] [includeempty=false] |Returns an array of objects containing:<br>"address" : receiving address<br>"account" : the account of the receiving address<br>"amount" : total amount received by the address<br>"confirmations" : number of confirmations of the most recent transaction included<br>To get a list of accounts on the system, execute `peercoin-cli listreceivedbyaddress 0 true`|no|
| `listreceivedbyaccount`| [minconf=1] [includeempty=false] |Returns an array of objects containing:<br>"account" : the account of the receiving addresses<br>"amount" : total amount received by addresses with this account<br>"confirmations" : number of confirmations of the most recent transaction included|no|
| `listaccounts` | [minconf=1] |Returns Object that has account names as keys, account balances as values.|no|
| `listunspent`  | [minconf=1] [maxconf=999999] |Returns array of unspent transaction inputs in the wallet.|no|
| `dumpprivkey`  | `address`   |Reveals the private key corresponding to `address`.|yes|
| `importprivkey`|  `privkey` [label] [rescan=true]|Adds a private key (as returned by dumpprivkey) to your wallet. This may take a while, as a rescan is done, looking for existing transactions.|yes|
| `createrawtransaction`| [{"txid":txid,"vout":n},...] {address:amount,...} |Creates a raw transaction spending given inputs.|no|
| `decoderawtransaction`| `hex_string` |Produces a human-readable JSON object for a raw transaction.|no|
| `signrawtransaction`  | `hex_string` [{"txid":txid,"vout":n,"scriptPubKey":hex},...] [`privatekey1`,...]|Adds signatures to a raw transaction and returns the resulting raw transaction.|yes|
| `signmessage`         | `address` `message` |Sign a message with the private key of an address.|yes|
| `verifymessage`       | `address` `signature` `message` |Verify a signed message.|no|
| `sendrawtransaction`  | `hex_string` |Submits raw transaction (serialized, hex-encoded) to local node and network.|no|
| `validateaddress`     | `address` |Return information about `address`.|no|
| `encryptwallet`       | `passphrase` |Encrypts the wallet with `passphrase`|no|
| `enforcecheckpoint`   | `bool` |`enforce` is true or false to enable or disable enforcement of broadcasted checkpoints by developer.|no|
| `keypoolrefill`       | `size` |Fills the key pool with new keys [default 100 new keys]|yes|
| `listlockunspent`     |        |Returns list of temporarily unspendable outputs.|no|
| `createmultisig`      | `nrequired` `["key,"key"]`|Creates a multi-signature address and returns a json object.|yes|

# Peercoin Developer Notes

Constants that may be useful when looking to integrate / develop with Peercoin.

Peercoin source code repository: github.com/peercoin/peercoin

## Mainnet

| Attribute | Value |
|-----------|-------|
| p2pkh Base58 prefix | P |
| p2sh Base58 prefix | p |
| p2pkh Base58 prefix (hex) | 0x37 |
| p2sh Base58 prefix (hex) | 0x75 |
| Magic bytes |  \xe6\xe8\xe9\xe5 |
| WIF prefix | 0xb7 |
| Genesis hash hex (big-endian) |  0000000032fe677166d54963b62a4677d8957e87c508eaa4fd7eb1c880cd27e3 |
| Genesis hash bytes (little-endian) |  \xe3\x27\xcd\x80\xc8\xb1\x7e\xfd\xa4\xea\x08\xc5\x87\x7e\x95\xd8\x77\x46\x2a\xb6\x63\x49\xd5\x66\x71\x67\xfe\x32\x00\x00\x00\x00 |
| Genesis tx hash hex | 3c2d8f85fab4d17aac558cc648a1a58acff0de6deb890c29985690052c5993c2 |
| Genesis tx hash bytes |  \xc2\x93\x59\x2c\x05\x90\x56\x98\x29\x0c\x89\xeb\x6d\xde\xf0\xcf\x8a\xa5\xa1\x48\xc6\x8c\x55\xac\x7a\xd1\xb4\xfa\x85\x8f\x2d\x3c |
| Default port | 9901 |

## Testnet

| Attribute | Value |
|-----------|-------|
| p2pkh Base58 prefix | m or n |
| p2sh Base58 prefix | n |
| p2pkh Base58 prefix (hex) | 0x6f |
| p2sh Base58 prefix (hex) | 0xc4 |
| Magic bytes | \xcb\xf2\xc0\xef |
| WIF prefix | 0xef |
| Genesis hash hex (big-endian) | 00000001f757bb737f6596503e17cd17b0658ce630cc727c0cca81aec47c9f06 |
| Genesis hash bytes (little-endian) |  \x06\x9f\x7c\xc4\xae\x81\xca\x0c\x7c\x72\xcc\x30\xe6\x8c\x65\xb0\x17\xcd\x17\x3e\x50\x96\x65\x7f\x73\xbb\x57\xf7\x01\x00\x00\x00  |
| Genesis tx hash hex | 3c2d8f85fab4d17aac558cc648a1a58acff0de6deb890c29985690052c5993c2 |
| Genesis tx hash bytes |  \xc2\x93\x59\x2c\x05\x90\x56\x98\x29\x0c\x89\xeb\x6d\xde\xf0\xcf\x8a\xa5\xa1\x48\xc6\x8c\x55\xac\x7a\xd1\xb4\xfa\x85\x8f\x2d\x3c |
| Default port | 9903 |

# Bootstrapping

## What is it?

> In computer technology the term (usually shortened to booting) usually
> refers to the process of loading the basic software into the memory of
> a computer after power-on or general reset, especially the operating
> system which will then take care of loading other software as needed.<sup>[9.1](#footnote-9.1)</sup>

For Peercoin it means loading all of the block chain history from a special
file containing a snapshot of block data.

This special file, named `bootstrap.dat`, allows the Peercoin client to
sync from your hard drive instead of the internet. Using a
`bootstrap.dat` file is faster and reduces stress on the Peercoin network to sync new nodes.

## How do I make a `bootstrap.dat`?

Any synced client has the ability to make a `bootstrap.dat` file. Assuming
you're running linux you can do the following to manufacture your own.
First, shutdown your client. Allow it to cleanly exit so we know the block
data is settled.

Now, navigate to the directory `~/.peercoin/blocks` in your terminal and
notice the files named `blk00000.dat`, `blk00001.dat`, `blk00002.dat`, etc.
These are the raw block data files that can be combined to form the
`bootstrap.dat`!

The command:
> cat blk*.dat > bootstrap.dat

will produce the `bootstrap.dat`.
The file is often then compressed (zip'ed, tar/gzip'ed) and shared.

The same process can be executed on Microsoft Windows (7+):

> CD C:\Users\<my_user>\AppData\Roaming\Peercoin

> COPY /b blk0001.dat+blk0002.dat bootstrap.dat

Or on OS X:

> cd "~/Library/Application Support/Peercoin/"

> cat blk*.dat > bootstrap.dat


On linux and OS X you can create hash of the bootstrap:

> sha256 bootstrap.dat

## How do I use a `bootstrap.dat`?

Assuming you're on linux and you haven't started the Peercoin client before.

Make the directory `~/.peercoin` if it doesn't exist and then move the
`bootstrap.dat` into the `~/.peercoin` directory.

Start the Peercoin client. You should see the status `Importing blocks from disk...` if the client has found the `bootstrap.dat` and is using it to
sync the block chain.

## Where can I download a `bootstrap.dat`?

We've put some recent copies on our [file server](https://files.peercoin.net) :)

* [Mainnet bootstrap.dat.zip](https://files.peercoin.net/download/peercoin_mainnet_2018_08_06_bootstrap.dat.zip) SHA256 `66c494e0c2a4c78ba19f14a3781ca77f1b8b16f3833fb85c10959ee991764a4c` | [torrent](https://files.peercoin.net/download/peercoin_mainnet_2018_08_06_bootstrap.dat.zip.torrent) | [magnet](magnet:?xt=urn:btih:9fc1f0d09a6598ae96ba5d8b9ac5caca0ae92402&dn=peercoin%5Fmainnet%5F2018%5F08%5F06%5Fbootstrap.dat.zip&tr=udp%3A%2F%2Fpublic.popcorn-tracker.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.ilibr.org%3A80%2Fannounce&tr=http%3A%2F%2Fatrack.pow7.com%2Fannounce&tr=http%3A%2F%2Fbt.henbt.com%3A2710%2Fannounce&tr=http%3A%2F%2Fmgtracker.org%3A2710%2Fannounce&tr=http%3A%2F%2Fmgtracker.org%3A6969%2Fannounce&tr=http%3A%2F%2Fopen.touki.ru%2Fannounce.php&tr=http%3A%2F%2Fp4p.arenabg.ch%3A1337%2Fannounce&tr=http%3A%2F%2Fpow7.com%3A80%2Fannounce&tr=http%3A%2F%2Fretracker.krs-ix.ru%3A80%2Fannounce)
* [Mainnet bootstrap.dat.tar.gz](https://files.peercoin.net/download/peercoin_mainnet_2018_08_06_bootstrap.dat.tar.gz) SHA256 `bac807186735347e2c7ccbfecb3d91045de32246258a7ba3e3d0a9c2a10b8ff0` | [torrent](https://files.peercoin.net/download/peercoin_mainnet_2018_08_06_bootstrap.dat.tar.gz.torrent) | [magnet](magnet:?xt=urn:btih:77f1c5352e9eca71e9f4f1e31487e7d13900a335&dn=peercoin%5Fmainnet%5F2018%5F08%5F06%5Fbootstrap.dat.tar.gz&tr=udp%3A%2F%2Fpublic.popcorn-tracker.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.ilibr.org%3A80%2Fannounce&tr=http%3A%2F%2Fatrack.pow7.com%2Fannounce&tr=http%3A%2F%2Fbt.henbt.com%3A2710%2Fannounce&tr=http%3A%2F%2Fmgtracker.org%3A2710%2Fannounce&tr=http%3A%2F%2Fmgtracker.org%3A6969%2Fannounce&tr=http%3A%2F%2Fopen.touki.ru%2Fannounce.php&tr=http%3A%2F%2Fp4p.arenabg.ch%3A1337%2Fannounce&tr=http%3A%2F%2Fpow7.com%3A80%2Fannounce&tr=http%3A%2F%2Fretracker.krs-ix.ru%3A80%2Fannounce)
* [Testnet bootstrap.dat.zip](https://files.peercoin.net/download/peercoin_testnet_2018_08_06_bootstrap.dat.zip) SHA256 `1312aaaf0d8466b6f7006bac60a5cad4daf36e1241f791924e45bc5959ff2452` | [torrent](https://files.peercoin.net/download/peercoin_testnet_2018_08_06_bootstrap.dat.zip.torrent) | [magnet](magnet:?xt=urn:btih:c70afb5100953362b45df75133e01bf1f9466e04&dn=peercoin%5Ftestnet%5F2018%5F08%5F06%5Fbootstrap.dat.zip&tr=udp%3A%2F%2Fpublic.popcorn-tracker.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.ilibr.org%3A80%2Fannounce&tr=http%3A%2F%2Fatrack.pow7.com%2Fannounce&tr=http%3A%2F%2Fbt.henbt.com%3A2710%2Fannounce&tr=http%3A%2F%2Fmgtracker.org%3A2710%2Fannounce&tr=http%3A%2F%2Fmgtracker.org%3A6969%2Fannounce&tr=http%3A%2F%2Fopen.touki.ru%2Fannounce.php&tr=http%3A%2F%2Fp4p.arenabg.ch%3A1337%2Fannounce&tr=http%3A%2F%2Fpow7.com%3A80%2Fannounce&tr=http%3A%2F%2Fretracker.krs-ix.ru%3A80%2Fannounce)
* [Testnet bootstrap.dat.tar.gz](https://files.peercoin.net/download/peercoin_testnet_2018_08_06_bootstrap.dat.tar.gz) SHA256 `15f0e40a7e99083b2ed27c78d37d0f201fd6c744537cf643925d0aae84395896` | [torrent](https://files.peercoin.net/download/peercoin_testnet_2018_08_06_bootstrap.dat.tar.gz.torrent) | [magnet](magnet:?xt=urn:btih:eb2a70e90285ca847be47b2f96e36e5cdec4580e&dn=peercoin%5Ftestnet%5F2018%5F08%5F06%5Fbootstrap.dat.tar.gz&tr=udp%3A%2F%2Fpublic.popcorn-tracker.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.ilibr.org%3A80%2Fannounce&tr=http%3A%2F%2Fatrack.pow7.com%2Fannounce&tr=http%3A%2F%2Fbt.henbt.com%3A2710%2Fannounce&tr=http%3A%2F%2Fmgtracker.org%3A2710%2Fannounce&tr=http%3A%2F%2Fmgtracker.org%3A6969%2Fannounce&tr=http%3A%2F%2Fopen.touki.ru%2Fannounce.php&tr=http%3A%2F%2Fp4p.arenabg.ch%3A1337%2Fannounce&tr=http%3A%2F%2Fpow7.com%3A80%2Fannounce&tr=http%3A%2F%2Fretracker.krs-ix.ru%3A80%2Fannounce)

## Footnotes

<a id="footnote-9.1">9.1</a>: https://en.wikipedia.org/wiki/Bootstrapping


---


# Graphics

A variety of Peercoin graphics are available here: https://github.com/peercoin/media/tree/master/Peercoin%202018%20Logo%20Files

# Brand Identity

Please use these color codes on your Peercoin related websites whenever possible. This will help us keep the Peercoin ecosystem and its branding and visuals consistent.

Green:
#3cb054
RBG: 24, 69, 33
CMYK: 66, 0, 52, 31

White: #ffffff

The Peercoin text logo uses the following font:
Font: FF Mark
Type: Mark-Medium
Website: http://www.ffmark.com/

The Peercoin website and wallets use the Roboto font for its content.

---


# Frequently Asked Questions

## How old is the Peercoin project?

Peercoin's chain started on August 19th, 2012 at 18:00:00 UTC. There was no premine and the launch of the project was announced nine days before it went live.  You can read the original announcement thread here: https://bitcointalk.org/index.php?topic=101820.0

## How can I mine Peercoin?

Peercoin uses the SHA256 cryptographic hash function. Any hardware that can effectively mine Bitcoin can be used to mine Peercoin.

## Why a 1% minting return on staking?  Why isn't there a hard limit on the total number of Peercoin's? Doesn't this disqualify Peercoin as a deflationary currency?

Peercoin has a 1% inflation rate to allow for participant determined growth over time. Fully deflationary currencies cannot be used as mediums of exchange, but rather solely stores of value. By allowing for a manageable inflation rate, Peercoin remains scares while allowing for growth determined by participation. This also helps offset coins that are removed through circulation through lost wallets or malevolent destruction.

## Why a fixed transaction fee?

Peercoin has a fixed transaction fee filters out spam transactions which have damaged chains like Bitcoin. It also allows for predictable sending fees, which may become rapidly unpredictable on chains where fees can rapidly change leaving transactions in limbo for several days. This allows for first come, first serve transactions as well. Peercoin is able to scale without worrying about valuation effecting the usability.  In version 0.7, the transaction fee is being lowered from 0.01 Peercoin to 0.001 Peercoin.

## How can the Peercoin network survive without miners providing PoW security, especially during times of low interest?

Proof of work serves to distribute coins through as an inflationary mechanism. The Peercoin network is secured by coin age and proof of stake.  With pure proof of work chains, holders have little ability to secure the chain with the high cost of mining equipment being a barrier to entry. Any Peercoin holder can protect their investment by allowing a transaction to mature and leaving the wallet open for minting keeps the network secure and has done so since Peercoin's inception.

## I just moved Peercoins to my wallet and it says I have a zero percent chance of minting in the next 30 days.  Why is that?

Peercoin transactions must mature 30 days or roughly 4320 blocks before they can become eligible for minting. This number is updated roughly every six hours. Once the 30 day period passes, your coins will become eligible and the minting probability should adjust accordingly.

## How many confirmations are required on the Peercoin network for a transaction?

Six confirmations for a transaction to be verified. Each block takes about 10 minutes.

## I just minted some coins but it says they are unavailable at the moment.  Why is that?

Once a transaction mints, it takes 520 confirmations before these become unlocked. This is done to prevent spoofed minting. Each block on the Peercoin network takes about 10 minutes and so it takes 5,200 minutes or around 3.6 days for the minted coins to become available.

____________
