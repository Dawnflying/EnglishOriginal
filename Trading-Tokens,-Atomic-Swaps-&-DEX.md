> _Token exchanges offer services to those who want to buy and sell tokens. They act as trusted intermediaries and market makers. While they are an important player in this new token economy, they are still predominantly centralized, which makes them vulnerable to hacks, mismanagement, volume volatility, or censorship. Atomic swaps and decentralized exchanges try to mitigate these risks._

While blockchain networks and other distributed ledgers allow the transfer of tokens without intermediaries, they only allow sending tokens from one wallet in the network to another wallet in the network. A token can only be managed by one type of network and cannot natively move between networks for interoperability reasons. As a result, the buying and selling of tokens still requires the services of token exchanges. Various online exchanges offer such services and act as trusted intermediaries. They resemble online banks that take the tokens of their clients into their custody and manage the trading of tokens between users of their platforms. 

For users, trading one token for another can be difficult and time consuming, depending on the popularity and legal status of a particular token. Less popular or highly controversial tokens might only be listed on smaller exchanges with limited token pairings, which means that users would need to (i) register for all of these exchanges and (ii) swap tokens several times, before being able to buy the token of interest. Even if many tokens are listed on the same exchange, token pairings, or token/fiat pairings, are often limited. As a result of this, trading tokens might often be time consuming and expensive. Sometimes, even reputable tokens are listed on one exchange only, forcing users to trade on an exchange that they would otherwise not use. Potential buyers of a token might, therefore, decide not to buy a certain token if it is too complicated or too risky to do so. Exchanges that list many tokens have become more popular, as they offer token holders a one-stop shop to buy and sell between multiple token types, without the need to register on another exchange. 

Token exchanges get to decide whether they include a token or not. They have become the market makers and new gatekeepers in this emerging tokenized economy. In August 2016, for example, when the Ethereum network performed the controversial hard fork as a result of TheDAO exploit,[^1] the shorter Ethereum chain (“Ethereum Classic”) did not have any market value. However, when[ “Poloniex](https://poloniex.com/),” an online exchange, decided to list the “Ethereum Classic” token, the market dynamics changed and other exchanges started listing the token too. While it was not the first time that there was a fork in a blockchain network, it was the first time the token of a minority chain was listed on an exchange, giving the network an economic value.


## Challenges of Centralized Exchanges

Most exchanges today are centralized exchanges (CEX) performing intermediary services between buyers and sellers of tokens. They allow simple buying and selling of tokens, also against fiat currencies, and provide easy wallet creation and token management, including the safeguarding of private keys. As opposed to many early crypto enthusiasts, who still manage their tokens with their own wallets (hardware wallet, software wallet, or paper wallet), newcomers often prefer to outsource wallet management to online exchanges, which act as the custodian of their tokens. Centralized exchanges operate on classic client-server technology and are not subject to the same security mechanisms of blockchain networks. While they offer important services, they are vulnerable to hacks, mismanagement, volume volatility, or censorship. Hacks and mismanagement have been the biggest issues in the past, especially in the early years, when the market was less mature and unregulated.[ “Mt. Gox](https://en.wikipedia.org/wiki/Mt._Gox),” which was the largest Bitcoin exchange at the time, suspended trading and filed for bankruptcy in 2014. Due to mismanagement, approximately 850,000 BTC went missing, most likely stolen. Many other cases followed, such as[ “Bitfinex](https://www.coindesk.com/bitfinex-bitcoin-hack-know-dont-know)” or[ “Coincheck](https://fortune.com/2018/01/31/coincheck-hack-how/).” These incidents have led to the misconception in the general public that blockchain networks are not safe. 

Centralized exchanges very often don’t give their customers full control over their private keys, as they trade on their own books, a.k.a. off-chain. They often don’t have dedicated user wallets for their clients, making a private key useless. Customers surrender full control over their tokens. Smaller exchanges that have less liquidity can experience price volatilities such as flash crashes and price spikes, if there is a sudden shift in the supply and demand of tokens. This makes smaller exchanges subject to market manipulation and less attractive for users. Centralized exchanges are also subject to government regulation and must therefore meet the countries’ KYC (know your customer) requirements, which means that customers have to fully identify themselves when registering on an exchange; this could raise privacy and censorship issues.

General blockchain interoperability is a solution to the centralization problem, which is currently being addressed by projects such as[ “Cosmos](https://cosmos.network/),” [“Polkadot](https://polkadot.network),” “Wanchain,” “Chainlink,” “Arc,” “Aion,” and “AVA.” Atomic swaps are another solution, with more immediate feasibility.


## Atomic Swaps

Atomic swaps allow for P2P cross-chain trading and can be directly executed between separate blockchain networks, wallet to wallet, without a trusted intermediary like an exchange. They use a type of smart contract called a hash time-locked contract (HTLC) to secure the token transaction, making sure that both parties to the token trade fulfill the requirements. HTLCs are similar to state channels that deal with off-chain payment settlement via smart contract (read more: Annex - Scalability Solutions). Users remain in full control of their private keys, and their tokens, when conducting such a trade.

Let’s assume that Alice and Bob want to swap tokens from different blockchain networks P2P without an intermediary like an exchange. Bob wants to sell his Bitcoin (BTC) for Litecoin (LTC), and Alice wants to sell her Litecoin (LTC) for Bitcoin (BTC). Since the two networks cannot communicate directly, Alice and Bob use a hash time-locked contract to lock up their tokens for a predefined amount of time. Both recipients, Bob and Alice, need to create a cryptographic proof of payment before the time expires. The tokens are locked via multi-signature in a smart contract. This state lock is registered on both networks. Tokens are only swapped if their secret keys match. To deposit her tokens, Alice first has to create an HTLC. She creates a secret key and generates a hash, from which the smart contract address is derived and to which she can now send her tokens. She also sends this hash to Bob, who can use the hash to replicate the address of the smart contract and deposit his tokens in that smart contract. Alice can unlock the tokens Bob deposited using her secret key, which triggers an event where Bob receives the secret key to unlock Alice’s tokens. In a closing transaction, the last commitment is sent to be added to the blockchain.

Atomic swaps require that (i) both parties to the swap need to download the ledgers of both networks; (ii) both networks managing the swapped tokens must support hash time-locked contracts and use the same cryptographic hash function. Furthermore, in order to conduct wallet-to-wallet transactions, (iii) the wallet used must also have atomic swap capabilities. 

While atomic swaps enable P2P swapping of tokens, they do not resolve the coincidence-of-wants problem. They will only be useful to people who know other people willing to buy the exact amount of tokens one wants to sell at exactly the same time one wants to sell them. The likeliness of this happening for retail investors is quite low. Decentralized exchanges using atomic swaps, however, could resolve both problems.

***
![Atomic Swaps](https://github.com/sherminvo/TokenEconomyBook/blob/main/imgs/24_AtomicSwaps.png)
***

## Decentralized Exchanges

Decentralized exchanges (DEX) are decentralized applications running on a distributed ledger to allow users to trade tokens without the need for an institution clearing the settlements. The trade is settled directly by the ledgers (on-chain) and could potentially mitigate many challenges of centralized exchanges. A fully decentralized exchange would make use of atomic swaps, or similar methods, with an added discovery layer that enables trading between two random token owners who do not know each other, might live in different countries, and would not otherwise know how to find each other. Existing decentralized exchanges provide various levels of decentralization, often running on a partially centralized infrastructure, and not offering wallet-to-wallet swaps.  Current examples are[ “Komodo](https://komodoplatform.com/),”[ “WavesDex](https://wavesplatform.com/products-exchange),”[ “OasisDex](https://developer.makerdao.com/oasis/),”[ “Radar Relay](https://radarrelay.com/),” “BarterDex,”[ “Bisq](https://bisq.network/),” “StellarDex,” and[ “EtherDelta](https://etherdelta.com/).” 

Most self-proclaimed decentralized exchanges are not fully decentralized (yet) and are subject to many challenges. Due to on-chain order books, they are also slow and expensive, at least as long as the scalability issues of public blockchain networks are unresolved. Each time an order is posted or modified, this generates high overhead in network transaction costs and bloats the ledger. Currently, decentralized exchanges mainly benefit traders who are already positioned in token markets. DEX are not necessarily suitable for newcomers to the market, as they don’t resolve the question of trading national fiat currencies for tokens. Newcomers to the crypto token market will probably still use centralized exchanges, which allow them to easily buy tokens with fiat. The current usability issues of decentralized exchanges further contribute to low liquidity of tokens and low trading volumes, which makes them prone to market manipulation. However, once those challenges are resolved, DEX could allow for a more liquid and less manipulation-susceptible market, where demand and supply could exist without arbitrary middlemen.

For decentralized exchanges to reach mainstream adoption, we still lack necessary network effects. These network effects rely on when and how general ledger interoperability will be resolved, including resilient cross-chain atomic swaps, interoperability standards, or piggyback solutions like the[ “Pantos](https://pantos.io/)” token. Furthermore, current assets, including fiat currencies, need to be tokenized to catalyze necessary network effects. Decentralized exchanges will likely come to fruition if and when everyday transactions are predominantly settled using cryptographic tokens and distributed ledgers. We will probably need a mesh of interconnected exchanges to have enough market depth for global and widespread use of P2P token exchanges. 


***
### Chapter Summary

> A token can only be managed by one type of network and cannot natively move between networks for interoperability reasons. The buying and selling of tokens therefore requires the services of token exchanges. They resemble online banks that take the tokens of their clients into their custody and manage the trading of tokens between users of their platforms.

> Most exchanges today are centralized exchanges (CEX) performing intermediary services between buyers and sellers of tokens. They allow simple buying and selling of tokens, also against fiat currencies, and provide easy wallet creation and token management, including the safeguarding of private keys.

> Token exchanges get to decide whether they include a token or not. They  act as trusted intermediaries and market makers have become the new gatekeepers in this emerging tokenized economy.  While they are an important player in this new token economy, they are still predominantly centralized, which makes them vulnerable to hacks, mismanagement, volume volatility, or censorship. Atomic swaps and decentralized exchanges try to mitigate these risks. 

> Atomic swaps allow for P2P cross-chain trading and can be directly executed between separate blockchains, wallet to wallet, without a trusted intermediary like exchanges. They use a type of smart contract called a hash time-locked contract (HTLC) to secure the transaction, making sure that both parties to the trade fulfill the requirements.

> Atomic swaps do not resolve the “coincidence of wants” problem. They only benefit people who know another person who is willing to buy the exact amount of tokens at exactly the same time. 

> Decentralized exchanges (DEX) are decentralized applications running on a distributed ledger to allow users to trade tokens without the need for an institution clearing the settlements. The trade is settled directly by the ledgers (on-chain). They combine atomic swaps with matching algorithms to mitigate the coincidence-of-wants problem.

> A fully decentralized exchange would make use of atomic swaps, or similar methods, with an added discovery layer that enables trading between two random token owners who do not know each other, might live in different countries, and would not otherwise know how to find each other. 


***
### Chapter References & Further Reading

* Borkowski, Michael; McDonald, Daniel; Ritzer, Christoph; Schulte, Stefan: “Towards Atomic Cross-Chain Token Transfers: State of the Art and Open Questions within TAST”, Pantos GmbH Vienna, May 2018, revised version 1.2, August 2018, retrieved from: https://www.dsg.tuwien.ac.at/projects/tast/pub/tast-white-paper-1.pdf
* Gazi Güçlütürk, Osman: “TheDAO Hack explained: Unfortunate take off of smart contracts”, Aug 1, 2018: https://medium.com/@ogucluturk/the-dao-hack-explained-unfortunate-take-off-of-smart-contracts-2bd8c8db3562
* Herlihy, Maurice: “Atomic Cross-Chain Swaps”, May 18, 2018: https://arxiv.org/pdf/1801.09515.pdf
* Higgins, Stan: "The Bitfinex Bitcoin Hack: What We Know (And Don’t Know),” Aug 3, 2016, updated Jun 20, 2018, retrieved from: https://www.coindesk.com/bitfinex-bitcoin-hack-know-dont-know
* Madeira, Antonio: “What Are Atomic Swaps?”, 28 Sep 2017: https://www.cryptocompare.com/coins/guides/what-are-atomic-swaps/
* N.N.: “How to Steal $500 Million in Cryptocurrency,” Fortune Magazine, January 31, 2018, retrieved from: EST https://fortune.com/2018/01/31/coincheck-hack-how/
* N.N.: “What Are Atomic Swaps?”, https://blockgeeks.com/guides/atomic-swaps/
* N.N“.: Komodo White Paper”, https://komodoplatform.com/wp-content/uploads/2018/04/2018-04-04-Komodo-White-Paper-Full.pdf
* N.N.: "5 Predictions for Our Security Token Futur" Coin Crunch, Jun 16, 2018: https://medium.com/hackernoon/5-predictions-for-our-security-token-futur-57ce9cf01256
* Noashh: ”With Atomic Swaps, Komodo Supports 95% Of All Coins In Existence!”, March 16, 2018: https://komodoplatform.com/komodo-now-covers-atomic-swaps-between-95-of-all-coins-in-existence/
* Binance: https://www.binance.com/en
* Bisq: https://bisq.network/
* EtherDelta: https://etherdelta.com/
* Komodo: https://komodoplatform.com/
* Mt. Gox Hack: https://en.wikipedia.org/wiki/Mt._Gox
* OasisDex: https://developer.makerdao.com/oasis/
* Pantos: https://pantos.io/
* Poloniex: https://poloniex.com/
* Radar Relay: https://radarrelay.com/
* WavesDex: https://wavesplatform.com/products-exchange


### Footnotes

[^1]:
A vulnerability in one of the smart contract functions, designed to represent minority rights, was exploited and used to drain 3.6m Ether from TheDAO balance (roughly 150 million USD at the time).