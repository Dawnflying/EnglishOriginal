> _Decentralized lending services use smart contracts to create two-sided markets for  a P2P credit and lending system. Any non-bankable asset such as commodities, securities, real estate, artworks, or SME shares could, in the future, be tokenized and collateralized, which could lead to a convergence of financial markets and the real economy._

Smart contract–based execution of credit and lending services have lower operational costs than legacy financial services, as compliance verification could be executed on the fly. In a fully decentralized setup, P2P financial services only require a crypto-wallet, without complex identification systems. They allow for more control, security, and inclusion. Security and control refers to the fact that you can choose non-custodial services where you are in control of your private keys.[^1] Inclusion refers to the fact that these services, which are currently complementary to our current financial systems, could grant access to individuals who have been excluded from financial services before. 

Fully decentralized lending services enable a two-sided market, using smart contracts for P2P credit and P2P lending of tokens. Any non-bankable asset such as commodities, securities, real estate, art, SME shares, etc. could, in the future, be represented by a token. Commodities, national currencies, and securities are already being tokenized and can be traded on markets today, while tokenized real estate, art, and SME shares are still in their early stages of conceptualization. Any transferable tokens representing an asset could be used as collateral for open decentralized lending solutions, which could change the dynamics of our global economic system. The integrations of such tokenized non-bankable assets with lending and borrowing schemes would allow for instant transactions, which surpasses the possibilities of the legacy systems we have today.


## P2P Lending

Most investors today buy tokens for long-term investment only. The tokens usually stay dormant, in a hardware wallet, software wallet, or paper wallet, as token holders expect their value to grow over time and don’t use them for daily payments. P2P lending protocols allow token holders to convert their “dormant capital” into “working capital” by using smart contracts that earn periodic interest rates. P2P lending could easily be brokered by a smart contract. Dormant and previously non-bankable assets from around the world can now be tokenized to create a liquid P2P lending market. Anyone can earn passive income relatively risk free on their token holdings through interest paid by the borrowers. On the other hand, lower operational costs could also make loans more affordable for a wider array of people and institutions.


## P2P Borrowing

P2P borrowing allows for the borrowing of funds against a collateral of tokens you own, potentially paying lower interest rates than in the current financial system. Previously non-bankable assets, such as commodities, securities, art, or real estate, can be tokenized and leveraged against (i) fiat money or other (ii) transferable crypto-tokens. Borrowers can lock up tokens they own as collateral in a smart contract. This collateral serves as a guarantee that the lenders will be repaid. Since most tokens have volatile prices, decentralized lending applications only let you borrow a certain percentage of the value of your collateral. If the market price of the collateral begins to drop, the smart contract is programmed to sell collateral tokens at a pre-defined spot price or a market auction to mitigate counterparty risk of the lender. Collateralized borrowing is currently the only option, as decentralized systems have no KYC process to secure funds based on identification and reputation. That, however, might change as more sophisticated identification and reputation solutions evolve. At the time of writing this book, the main use case for P2P borrowing is for the sake of margin trading (the practice of borrowing funds to make an investment where one anticipates to make a higher profit off the investment than the interest one has to pay. Borrowed funds are used for leverage, which means that both profits and losses will be big).


## Flash Loans

Flash loans are a specific type of P2P loan that is valid within one network transaction and must be repaid by the end of that transaction. The lender can offer loans at zero-risk and the borrower can get any amount of tokens, without a collateral, provided the borrower can return all tokens borrowed within the same transaction. The default and illiquidity risk that a lender usually bears is reduced to zero due to the fact that the borrower has to repay the borrowed tokens within the same transaction, otherwise the smart contract won’t execute the deal. A series of smart contract operations can be programmed in a way that either all occur, or nothing occurs. Due to the atomic nature[^2] of blockchain networks, smart contract–based transactions can be reverted during execution, if the condition of a repayment is not satisfied. The concept was first introduced in 2018 by the “Marble Protocol.” Flash loan transactions will fail in the case of (i) insufficient transaction fees, (ii) conflicting transactions, or (iii) if another condition within the transaction cannot be met. The loans are taken from a public smart contract–governed liquidity pool, which means that anyone could borrow the entire amount of tokens available in the pool at any point in time. DeFi services relevant in the context of a flash loan are decentralized exchanges, decentralized margin trading, or credit/lending services. 


## P2P Lending Protocols

[MakerDAO](https://makerdao.com/ko/) is one of the more seasoned projects, that was launched in 2017 to create a stable token system. The stable token DAI comes with inbuilt decentralized lending aspects. DAI is issued against a collateral token (ETH). Borrowers receive newly created DAI tokens by locking up their ETH tokens as collateral, using a smart contract–based collateralized debt position (CDP). The current collateralization ratio is 150 percent. The interest rate is volatile and around 2.5 percent to 19.5 percent each month. A range of tokens are supported as collateral (read more: Part 3 - Stable Tokens).

[Uniswap:](https://uniswap.io/) Uniswap is a decentralized token exchange that runs without an order book. Instead of order books they use “liquidity pools” to facilitate the exchange of tokens.  Each token has a global borrow and lend pool that represents a market for that token’s borrow and lend positions. In such a setup, any token holder can contribute their tokens to the liquidity pool and earn interest on their token holdings. The 2020 upgrade of the Uniswap protocol allows direct token-to-token swaps, instead of relying on asset pairs with ETH as a fixed base token. The protocol upgrade also introduced “flash swaps,” a flash loan function that allows users to withdraw tokens for instant on-chain trades and return them by the end of the transaction. The upgrade was furthrmore designed to be more resistant against potential attacks and manipulation such as the “flash attacks” of February 2020 which will be described later in this chapter.

[Compound](https://compound.finance/) was launched in 2018 as a decentralized lending protocol with liquidity pools. Lenders can deposit their tokens into lending pools to earn interest. Loans are tokenized.  The interest rate of each token lent is algorithmically defined based on supply and demand of tokens in each pool and thus variable. One can receive one type of token in exchange for depositing another type of token (e.g. cDAI for DAI.) The loans have no fixed durations, which means that lenders can withdraw their funds at any time. Loans also have an unlimited duration. The current collateralization ratio is 150 percent. Tokens supported as collateral are currently: ETH, DAI, BAT, REP, USDC, WBTC, and ZRX. 

[Dharma](https://www.dharma.io/) was launched in 2019 and was initially not fully decentralized, offering lending and borrowing at fixed interest rates and fixed durations of up to 90 days. Borrowers collateralized their smart contract account with 150 percent of the value of the funds being borrowed, and the interest rate was determined by Dharma’s management, instead of a market algorithm. They later pivoted and are now using Compound’s liquidity pools, which determine the interest rates algorithmically based on supply and demand in these pools. Tokens supported as collateral are currently: DAI.

[dYdX](https://dydx.exchange/) is a decentralized lending platform and an exchange. Supporting trading in addition to borrowing and lending allows for more functionalities than other lending platforms, which is why many margin traders seem to prefer the service. Similar to “Compound,” it uses a pool-based approach with algorithmically determined variable interest rates. It has lower collateral requirements (125% initial,  115% minimum) and borrowing is limited to 28 days. Tokens supported as collateral are currently: DAI, ETH, and USDC.

[Nexo](https://nexo.io/) is a smart contract–based lending platform that offers instant loans in over 45 fiat currencies. Anyone can collatoralize their existing tokens (asset tokens, payment tokens) in a smart contract and immediately borrow. It comes with an off-ramping service that delivers the money to your bank account at a fixed interest rate. The loan can be paid back any time against release of the tokens.

Other examples for decentralized lending systems are “[Aave](https://aave.com/),” “[Bloqboard](https://github.com/bloqboard/bloqboard-lending-wallet),” “[BlockFi](https://blockfi.com/),” “[Cred](https://mycred.io/),” “[Colendi](https://www.colendi.com/),” “[Curve](https://www.curve.fi/),” “[ETHLend](https://ethlend.io/),” “[EOS REX](https://eosrex.io/), “[Lendoit](https://lendoit.com/),” “[NUO](https://www.nuo.network/),” “[SALT](https://saltlending.com/),” “[Iearn](https://iearn.finance/),” “[InstaDapp](https://instadapp.io/),” “[Uniswap](https://uniswap.io/),” “Crypto.com,” “Nexo,” “INLOCK,” “ICONOMI,” “CoinLoan,” “Nuo Network,” “LendaBit,” “Bitbond,” “BTCpop,” “Helio Lending,” “Lendingblock,” “xCoins,” and “Genesis Capital,” who all offer various degrees of decentralization and functionalities. 


## Flash Attacks

Flash attacks refer to capital-intensive attack vectors on decentralized financial services enabled by flash loans. The first flash attacks occurred in 2020 on “[bZx](https://bzx.network/),” a decentralized lending service. An anonymous person or group of people without any funds instantaneously borrowed hundreds of thousands of USD with ETH, exploiting a series of vulnerable on-chain protocols that had not been stress tested before within a single ethereum transaction. This happened in spite of prior warnings from different people within the crypto community. Months before, an anonymous hacker, SamCZSun,[^3] exposed the possibility that flash loans could be used to manipulate data feeds about asset prices (oracles). Taylor Monahan, the founder of Mycrypto.com, had also pointed out vulnerabilities in public tweets.[^4] Even though bZx claimed to have fixed the problem, flash loans were used to drain around 954,000 USD total in two attacks within four days: once on February 14, 2020 (350,000 USD), and the second time during a copycat attack with a few modifications on February 18, 2020 (600,000 USD). The attacker(s) took advantage of these oracle vulnerabilities and a bug within the bZx protocol’s code to secure the payout. 

In a DeFi setup, smart contracts must have information about the value of the collateral token at all times. This data is collected from the outside oracles provided by, for example, token exchanges. However, as opposed to traditional financial markets, where stock prices are traded on one particular stock exchange only, and a stock’s price has one reliable source, tokens can be traded on various exchanges, and very often have highly volatile price spreads across and within exchanges. This spread across different token exchanges creates arbitrage opportunities. One could, therefore, profit by borrowing tokens at a low price, then selling at a higher price before repaying the loan. This whole process can be performed within the same transaction, on-chain, since most DeFi services, including many decentralized exchanges, run on the Ethereum network. 

Flash loan borrowers can leverage almost unlimited amounts of funds to profit from arbitrage possibilities by coding all the steps into the same smart contract, which is how the flash attacks on “bZx” were conducted. The attacker(s) used the borrowed tokens of the flash loan to manipulate the market price of an ERC-20 token backed by BTC on a decentralized exchange with little market depth, pumping the price to 109.8 from the original 38, using a chain of transactions and also exploiting other loopholes in the code, and repaying the flash loan with a 350,000 USD and later 600,000 USD profit. In the current financial industry, such market manipulation can only be conducted by individuals or institutions with many assets. In a way, flash loans democratize market manipulation. However, while you don’t need any assets, you do need a market know-how. The recent exploits showed how markets with low liquidity and smart contracts are prone to attacks, and that flash loans in combination with smart contracts that have unintentional loopholes and/or unreliable data feeds can be exploited.

There is a discussion regarding whether to refer to these incidents as “attacks,” “hacks,” or “exploits” and is reminiscent of the discussions back in 2016 around TheDAO incident. The attacks demonstrate that the DeFi community has not yet developed attack-resistant mechanisms for a sustainable DeFi architecture. Smart contract code needs to be audited, including attack surfaces that can result from oracles. Reliable data feeds are well known architectural issues in smart contracts, so the bZx flash attack was evitable. Furthermore, liquidity of token markets is essential for efficient pricing mechanisms.

While P2P lending protocols create exciting new possibilities, the scene is still nascent. At the time of writing this book, decentralized lending services cannot compete with legacy financial systems: (i) many services are not fully decentralized yet, (ii) missing regulation, and (iii) not stress tested processes, which make smart contract exploits possible, and have (iv) limited usability and unintuitive user experience (control of their own private key), (v) low liquidity of decentralized exchanges, and (vi) many DeFi products are still over-collateralized as a result of missing credit scoring or shared collateral. These are just some of the many challenges ahead.

***
### Chapter Summary

> Smart contract–based execution of credit and lending services have lower operational costs than legacy financial services, as compliance verification could be executed on the fly. In a fully decentralized setup, P2P financial services only require a crypto-wallet, without complex identification systems. They allow for more control, security, and inclusion. 

> Decentralized lending services use smart contracts to create two-sided markets for  a P2P credit and lending system. Any non-bankable asset such as commodities, securities, real estate, artworks, or SME shares could, in theory, be tokenized and collateralized, which could lead to a convergence of financial markets and the real economy. Commodities, national currencies, and securities are already being tokenized and can be traded on markets today, while tokenized real estate, art, and SME shares are still in their early stages of conceptualization. 

> The integrations of such tokenized non-bankable assets with lending and borrowing schemes would allow for instant transactions, which surpasses the possibilities of the legacy systems we have today. Any transferable tokens representing an asset could be used as collateral for open decentralized lending solutions, which could change the dynamics of our global economic system.

> P2P lending could easily be brokered by a smart contract. Dormant and previously non-bankable assets from around the world can now be tokenized to create a liquid P2P lending market. Anyone can earn passive income relatively risk free on their token holdings through interest paid by the borrowers. On the other hand, lower operational costs could also make loans more affordable for a wider array of people and institutions. 

> P2P borrowing allows for the borrowing of funds against a collateral of tokens you own, potentially paying lower interest rates than in the current financial system. Previously non-bankable assets, such as commodities, securities, art, or real estate, can be tokenized and leveraged against (i) fiat money or other (ii) transferable crypto-tokens. Borrowers can lock up tokens they own as collateral in a smart contract. This collateral serves as a guarantee that the lenders will be repaid.

> Since most tokens have volatile prices, decentralized lending applications only let you borrow a certain percentage of the value of your collateral. If the market price of the collateral begins to drop, the smart contract is programmed to sell collateral tokens at a pre-defined spot price or a market auction to mitigate counterparty risk of the lender. 

> Flash Loans Flash loans are a specific type of P2P loan that is valid within one transaction and must be repaid by the end of that transaction. The lender can offer loans at zero-risk and the borrower can get any amount of tokens, without a collateral, provided the borrower can return all tokens borrowed within the same transaction. A series of smart contract operations can be programmed in a way that either all occur, or nothing occurs.

> Flash Attacks Flash attacks refer to capital-intensive attack vectors on decentralized financial services enabled by flash loans. Flash loan borrowers can leverage almost unlimited amounts of funds to profit from arbitrage possibilities by coding all the steps into the same smart contract, and profit by borrowing tokens at a low price, then selling at a higher price before repaying the loan. This whole process can be performed within the same transaction, on-chain.

> In the current financial industry, such market manipulation can only be conducted by individuals or institutions with many assets. In a way, flash loans democratize market manipulation.



### Chapter References & Further Reading

* Asolo, Bisade: "What is Uniswap? A Detailed Beginner’s Guide," MyCryptopedia, March 28 2019, https://www.mycryptopedia.com/what-is-uniswap-a-detailed-beginners-guide/
* Chandler, Simon: “DeFi and Credit on the Blockchain: Why Loans Are Better When They’re Decentralized,” May 25, 2019, retrieved from: https://cointelegraph.com/news/defi-and-credit-on-the-blockchain-why-loans-are-better-when-theyre-decentralized
* Curran, Brian: “What is DeFi? Understanding The Decentralized Finance Landscape,” Oct 24, 2019, retrieved from: https://blockonomi.com/what-is-decentralized-finance-defi
* Juliano, Antonio: “Decentralized Lending: An Overview,” May 21, 2019, retrieved from: https://medium.com/dydxderivatives/decentralized-lending-an-overview-1e00fdc2d3e
* Foxley, William: “Everything You Ever Wanted to Know About the DeFi ‘Flash Loan’ Attack,” Feb 19, 2020, https://www.coindesk.com/everything-you-ever-wanted-to-know-about-the-defi-flash-loan-attac
* Kistner, Kyle J.: “Post-Mortem,” Feb 17 2020, retrieved from: https://bzx.network/blog/postmortem-ethdenver
* Kohli, Kerman: “How Decentralised is bZx? Some alarming conclusions about a protocol that has over $15m USD locked up,”, Defi weekly, retrieved from: https://defiweekly.substack.com/p/how-decentralised-is-bzx
* Kohli, Kerman: “Announcing DeFi Audits & The Holistic bZx Post-Mortem),” Feb 20,  2020,  retrieved from: https://defiweekly.substack.com/p/announcing-defi-audits-and-the-holistic
* Koksal, Ilker: “The Shift Toward Decentralized Finance: Why Are Financial Firms Turning To Crypto?” Enterprise Tech, Sep 29, 2019, retrieved from: https://www.forbes.com/sites/ilkerkoksal/2019/09/29/the-shift-toward-decentralized-finance-why-are-financial-firms-turning-to-crypto/#56da02636392
* Lau, Darren; Lau, Daryl, Teh Sze Jin, Kho, Kristian; Azmi, Erina; Lee, TM; Ong, Bobby: “How to DeFi,” 1st Edition, March 2020, CoinGecko.
* Monahan, Taylor: Twitter feed, @tayvano, Feb 18. 2020, retrieved from:  https://twitter.com/tayvano_/status/1229708599867232256
* N.N.: "A Beginner’s Guide to Decentralized Finance (DeFi)," Coinbase Blog, Jan 6 2020, https://blog.coinbase.com/a-beginners-guide-to-decentralized-finance-defi-574c68ff43c4
* Qin, Kaihua; Zhou, Liyi;Livshits, Benjamin; Gervais, Arthur: “Attacking the DeFi Ecosystem with Flash Loans for Fun and Profit,” submitted on 8 Mar 2020 (v1), last revised 11 Mar 2020 (this version, v2), retrieved from:  https://arxiv.org/abs/2003.03810
* Qureshi, Haseeb: “The DeFi ‘Flash Loan’ Attack That Changed Everything,” Feb 27, 2020, retrieved from: https://www.coindesk.com/the-defi-flash-loan-attack-that-changed-everything
* Redman,Jamie:“Understanding Defi Flash Loans: Complex Attacks, Inflation and Composable Systems,”  Feb 22, 2020, https://news.bitcoin.com/defi-flash-loans/
* Sandner, Philipp  “Decentralized Finance (DeFi): What Do You Need To Know?”, Dec 9, 2019, retrieved from: https://medium.com/@philippsandner/decentralized-finance-defi-what-do-you-need-to-know-9cd5e8c2a48
* samczsun: " Taking undercollateralized loans for fun and for profit”, Sept 30 2019, retrieved from: https://samczsun.com/taking-undercollateralized-loans-for-fun-and-for-profit/
* Wolff, Max: “Introducing Marble, A Smart Contract Bank” Jul 16, 2018, retrieved from: https://medium.com/marbleorg/introducing-marble-a-smart-contract-bank-c9c438a12890
* Zafar, Taha: "Uniswap v2 Launch Targeted For Q2 2020, Team Announces"  On April 5 2020, https://cryptoticker.io/en/uniswap-v2-launch/
* Blockboard: https://github.com/bloqboard/bloqboard-lending-wallet
* BlockFi: https://blockfi.com/
* bZx:https://bzx.network/
* Cred: https://mycred.io/
* Colendi: https://www.colendi.com/
* Compound: https://compound.finance/
* Curve: https://www.curve.fi/
* Dharma: https://www.dharma.io/
* Dydx: https://dydx.exchange/
* ETHLend: https://ethlend.io/
* EOS REX: https://eosrex.io/
* Iearn: https://iearn.finance/
* InstaDapp: https://instadapp.io/
* Lendoit: https://lendoit.com/
* MakerDAO: https://makerdao.com/
* Nexo: https://nexo.io
* Nuo: https://www.nuo.network/
* Salt: https://saltlending.com/
* Uniswap: https://uniswap.io/



### Footnotes

[^1]:
The reality in the near future, however, could be more complex due to regulatory requirements, which will, very likely, oversee this still nascent scene.

[^2]:
“Atomicity of atomic transactions” is a computer science term that refers to database systems where a series of database operations can be programmed in a way that either all occur, or nothing occurs. Either all transactions (in this case, within the smart contract) execute or none of them execute. This prevents partial updates to the database system. 

[^3]:
[https://samczsun.com/taking-undercollateralized-loans-for-fun-and-for-profit/](https://samczsun.com/taking-undercollateralized-loans-for-fun-and-for-profit/)

[^4]:
[https://twitter.com/tayvano_/status/1229708599867232256](https://twitter.com/tayvano_/status/1229708599867232256)