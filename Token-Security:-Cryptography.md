> _Cryptography is an important tool for the secure management of tokens in a network of anonymous and untrusted actors. It allows for transparency of interactions while maintaining the privacy of all network actors. Cryptography is used to trustfully identify all network actors and is also an integral part of the consensus protocol in a blockchain network._

Cryptography is the practice and study of secure communication in the presence of third parties. The aim is to create information systems that are resilient against eavesdropping, manipulation, and other forms of attack. While the history of cryptology dates back to the advent of handwritten texts, it has evolved significantly in the computer age. Cryptography represents a subfield of cryptology and mainly refers to the process of encryption, where a piece of information (plaintext) is converted into unintelligible text (ciphertext). A ciphertext is unreadable without the corresponding cipher to decrypt it. 

Ciphers were one of the first encryption techniques developed to encrypt plain text with either substitution ciphers (where units of plaintext are replaced with single letters, pairs of letters, or triplets of letters) or transposition ciphers (where units of the plaintext are rearranged in a different and usually quite complex order). Decryption is the process of converting the unreadable ciphertext back to the original plaintext. A cipher is, therefore, a pair of algorithms that creates the encryption as well as the reversing decryption: It is designed in a way that makes it easy to encrypt a message, but very hard to reverse it if you don’t know the code. 

Historically, cryptography has been used in various forms, such as a carved ciphertext on a stone in Egypt. Other forms of ciphers date back to Sassanid Persia, Ancient Greece, The Roman Empire, India, etc. Since the development of the enigma machine (a rotor cipher machine) in World War I, and the emergence of computers in World War II, cryptographic applications and methods have radically evolved. Classical ciphers became redundant because they were very easy to guess with simple “brute-force attacks,” where a computer algorithm runs all possible combinations until it guesses the right code. Computers not only enhanced the possibilities of cryptanalysis, which refers to the process of breaking encryption, they also made more complex ciphers possible. Modern cryptographic algorithms are designed to be infeasible to break them in terms of time and money applying brute-force. However, such “computational hardness assumptions” have to consider the continuous increase in processing power of computers. 

Computers, furthermore, introduced new forms of encryption of any kind of digital information, not only pieces of text. With the advent of quantum computers, many researchers are studying the relationship between cryptographic problems and quantum physics. Post-quantum cryptography is being developed by some researchers and engineers who have already started factoring in potential effects of quantum computing when designing new algorithms. In the information age, the use of cryptography also raises many legal questions. Some governments limit or prohibit the use of cryptography, and in some cases, even classify it as a weapon.  Certain jurisdictions might permit government authorities to mandate the disclosure of encryption keys for documents that could be relevant to an investigation. Additionally, cryptography can be an interesting factor when discussing human rights in a digital era. The question of how to guarantee privacy in the machine age is slowly becoming a discussion led by a wider general public, and will probably become more dominant in the years to come. The crucial question, in this context, is whether and how the constitutional right to privacy of communication, or the sanctity of one’s home, could correspond to the right to encrypted communication or encrypted data trails (read more: Part 3 - Privacy Tokens).

While early attempts to encrypt electronic communication focused on providing secrecy and preserving technologies for the communications of government institutions, the field has expanded. Over the past decades, encryption technologies have been applied in various other domains, such as electronic commerce, digital payments, digital rights management, password management, message integrity checking, authentication of identity, digital signatures, interactive proofs, and secure computation. In the context of blockchain networks and other distributed ledgers, cryptography is used for identification, verification, and security purposes on the core protocol level. Three relevant cryptographic building blocks are used in the context of public blockchain networks and other Web3 technologies: (i) hash functions, (ii) symmetric cryptography, and (iii) asymmetric cryptography (public-key cryptography).

**<span style="text-decoration:underline;">Hash Functions</span>** are mathematical algorithms that convert any type of data of an arbitrary size (message) into data of a fixed size (hash value or hash). The only way to recreate the original data (message) from the hash is to attempt to try all possible variations to see if they produce a match. While this is possible, it is time consuming and therefore expensive, which is why it is referred to as a one-way function. Hash functions can be used for assuring the integrity of transmitted data and privacy. Selected applications are digital signatures, authentication services, fingerprinting, detection of duplicates, unique identification of files, or the creation of checksums to detect data corruption. In order to be considered resilient, cryptographic hash functions need to fulfill certain properties: They need to be designed in a way that they are (i) easy to compute; (ii) deterministic, meaning that the same message always results in the same hash; (iii) time consuming and expensive to generate a message from its hash value with sheer brute force; (iv) small changes to the original input value should change the hash value. It should furthermore be (v) infeasible to find two different messages (input) with the same hash value (output).

**<span style="text-decoration:underline;">Symmetric Systems</span>**: Before the emergence of public-key cryptography, two parties relied on one encryption key that they exchanged over a non-cryptographic method, through secret meetings, sealed envelopes, or trusted couriers. If you wanted to communicate privately with somebody, you would need to physically meet and agree on a secret key. In the world of modern communications, where one needs to coordinate over a network of many untrusted actors (the Internet), such methods would not be feasible. This is why symmetric encryption is not used for communication in public networks. It is, however, faster and more efficient than asymmetric encryption, and therefore used for encrypting large amounts of data, certain payment applications, or random number generation.

**<span style="text-decoration:underline;">Asymmetric Systems</span>**, also referred to as public-key cryptography, resolved the coordination problem by introducing two keys, a public key and a private key. The private key is only known to the owner and needs to be kept private, while the public key may be given to anyone. The public key can be broadcasted to the network, which allows anyone in the network to use the public keys to send an encrypted message to the “owner” of the public-key. This encrypted message can only be decrypted with the receiver’s private key. Senders can combine a message with their private key to create a digital signature on the message. Now, anyone can verify with the corresponding public key whether the signature is valid. How the keys are generated depends on the cryptographic algorithms used. Examples of asymmetric systems include RSA (Rivest-Shamir-Adleman) and ECC (Elliptic-Curve Cryptography), which is also used in Bitcoin. Use of asymmetric cryptography enhanced the security of communication in untrusted networks, like the Internet, in a scalable way.[^1] The following chapters will focus on how cryptography is used in the Bitcoin network and similar blockchain networks. 

The Bitcoin network mainly uses hashes in combination with digital signatures to protect the integrity of the data flowing through the network using public-key cryptography. Hashes are furthermore used in the context of the consensus protocol “Proof-of-Work.” Bitcoin uses public-key cryptography, and more specifically, elliptic-curve cryptography. Please note that alternative blockchain networks and other distributed ledger systems might use alternative cryptographic tools to the ones described below. Some blockchain networks, for example, use more privacy-preserving cryptography, such as “[Zcash](https://z.cash/)” (zero-knowledge proofs)[^2] and “[Monero](https://getmonero.org/)” (ring signatures)[^3]. The Bitcoin community itself is currently looking into alternative cryptographic signature schemes that are more privacy preserving and more scalable, for example, with “Mimblewimble”  (read more: Part 3 - Privacy Tokens).


***
![Symmetric Cryptography vs. Assymmetric Cryptography](https://github.com/sherminvo/TokenEconomyBook/blob/main/imgs/06_Symmetric_Assymmetric_Cryptography.png)
***


## Public-Key Cryptography

The Bitcoin network uses public-key cryptography to create a secure digital reference about the identity of a user with a set of cryptographic keys: a private key and a public key. Secure digital references about who is who, and who owns what, are the basis for P2P transactions. In combination with a transaction, these keys can create a digital signature that proves ownership of one’s tokens and allows control of the tokens with a wallet software. Similar to how a check is signed by hand, and passwords are used to authenticate in Internet banking, public-key cryptography is used to authenticate and sign Bitcoin transactions. 

The public key is mathematically generated from the private key. While it is very easy to compute the public key from the private key, the reverse is only possible with sheer brute force; guessing the key is possible but prohibitively expensive. It would take the world’s most powerful supercomputer trillions of years to crack, making it practically impossible. This means that, even though one’s public key is known to everybody, nobody can derive one’s private key from it. A message that is encrypted with the public key can now travel securely to the owner of the private key, and only the owner of this private key is able to decrypt the message. This method also works the other way around. Any message with a private key can be verified with the corresponding public key. 

An analog example for a public key would be the example of a padlock. If Bob wants to send a message to Alice, but is scared that somebody might intercept and read it, he will ask Alice to send her padlock (unlocked) over to him, and to keep her key to that padlock. Bob can now put his letter in a small box and lock it with the padlock that Alice sent him, closing it with a simple push. The letter can now be sent around the world without being intercepted by an unauthorized person. Only Alice, who has the key to her padlock, can open the letter. Of course, someone could try and break the box with sheer brute force, instead of using the key. While it is possible, the difficulty would depend on the resilience of the box, and the strength of the lock. The same basic principles apply to modern cryptography.


## Secure Algorithms

The crucial question in public-key cryptography revolves around computational hardness assumptions: How one can widen the computational effort between deriving the private key from the public key, compared to deriving the public key from the private key? How hard is it to break the encryption by guessing the result, how long would it take to guess the private key, and how expensive would it be? The private key is represented by a number, which means that the larger the number, the harder it is to guess that (random) number by someone who does not know the number. If it takes a couple of decades to guess a random number, the number is considered secure. However, every cryptographic algorithm is vulnerable to brute-force attack, which refers to guessing one’s private key by trying all possible combinations until a solution fits. As computers are becoming faster and more efficient, one must come up with more sophisticated algorithms, either by using bigger numbers or by inventing more resilient algorithms.

To make sure that it is hard to guess the number, a resilient private key has minimum requirements: It needs to be a (i) randomly generated number. It needs to be a (ii) very large number. It has to use a (iii) secure algorithm for the generation of the keys. Randomness is important, as we don’t want any other person or machine to use the same key, and humans are bad at coming up with randomness. Large key sizes allow for further distribution of randomness, and are much harder to crack with brute force, but also slower to compute. Due to their complexity, secure algorithms need to be scientifically proven and stress tested against security breaches. One should avoid inventing one’s own algorithm. This issue became obvious when the team developing the IOTA network decided to implement their own hash function, called Curl. IOTA is an alternative distributed ledger solution to blockchain, which claims to resolve Bitcoin’s scalability problem with an alternative consensus mechanism and alternative cryptography. Their self-made Curl function, however, was later found to be “non-collision resistant.”[^4]<sup> </sup>Since the emergence of Bitcoin, cryptographic algorithms used in the Bitcoin network have withstood all attempts of data-tampering. 

Without cryptography, there could be no distributed consensus in a network of actors who do not know or trust each other. As computers get more powerful and can guess numbers faster, the algorithms used will need to withstand time and rapidly evolving technological standards to maintain the current level of security. Many researchers and developers argue that supercomputers, in particular quantum computers, will soon be able to crack most conventional encryption algorithms through brute force. This is not entirely true and depends on the cryptographic algorithm. While quantum computers are not significantly better at cracking hashes, they are much more powerful when it comes to elliptic curves and prime factorization. The answers are complex and not fully resolved yet. Quantum-computer-resistant cryptographic algorithms are, therefore, a mission-critical research area. For more details on this topic, see references at the end of this chapter.


## Hashing

Hashing is a method for transforming large amounts of data into short numbers that are difficult to guess. One can convert a text or a picture, which represents a variable-length bit sequence, to produce a fixed-length bit sequence in the form of a hash. These functions ensure data integrity. The Bitcoin network uses Secure Hash Algorithms (SHA), such as SHA-256. An important property of hashes is that if one single bit of input data is changed, the output changes significantly, which makes it easy to detect small changes in large text files, for example. As you can see from the example below,[^5] an entirely different hash gets generated when we change only one symbol. This is based on the “avalanche effect,” and it is useful for easily providing data integrity. An entirely different string results from hashing the hash.


* Hash of the sentence “How to buy Bitcoin?”: 156aedcfab1d49f73abddd89faf78d9930e4b523ab804026310c973bfa707d37

* Hash of the sentence “How to buy Bitcoin”: 4314d903f04e90e4a5057685243c903fbcfa4f8ec75ec797e1780ed5c891b1bf

* Hashing the hash produces: 4c9622e1148ff0b855de50e62999d194039eb2faa9e715cc9d9ef604015aa1fe

The avalanche effect describes the behavior of a mathematical function where even a slight change in an input string should cause the resulting hash value to change drastically. This means that if one adds only one word, or even a comma, to a document of several hundred pages, the hash of that document will change. A document’s hash value can, therefore, serve as a cryptographic twin of the document, which is why it is often referred to as a “digital fingerprint.” As a result of this, one does not need to encrypt the entire document with a sender’s private key, as this consumes time, bandwidth and money. Instead one can compute the document’s hash value. 

Hashing in the Bitcoin network is part of the following processes: (i) encoding wallet addresses; (ii) encoding transactions between wallets; (iii) verifying and validating the account balances of wallets; and for the consensus mechanism (iv) Proof-of-Work.


## Wallets & Digital Signatures

A blockchain wallet is a piece of software that stores your private key, public key, and blockchain address, and communicates with the blockchain network. This wallet software can run on a computer or a mobile phone (like[ “Bitcoin Core](https://bitcoin.org/de/download),”[ “Electrum](https://electrum.org/#home)”) or a dedicated hardware device (like[ “Trezor](https://trezor.io),”[ “Ledger](https://www.ledger.com)”). The wallet software allows for user-authentication and the management of tokens. With a wallet software one can send tokens and inspect the receipts of tokens that were sent to you. Every time you send Bitcoin tokens, you need to use a wallet to sign the transaction with your private key. Subsequently, your personal balance of tokens is adjusted on all copies of the ledger, which is distributed across the P2P network of computers. 

When launched for the first time, a Bitcoin wallet generates a key pair consisting of a private key and a public key. In a first step, the private key is a randomly generated 256-bit integer. The public key is then mathematically derived, using elliptic-key cryptography, from the private key. In a second step, the blockchain address is derived from the public key, using a different type of cryptographic function from the one that was used to derive the public key, adding metadata like checksums and prefixes. Using a different type of cryptographic function to derive the address adds an extra level of security: if the first layer of security, elliptic-key cryptography, is broken, then someone who has the public key would be able to crack the private key. This is important, as elliptic-key cryptography is especially vulnerable to being broken if quantum computers become a reality, while the hashing, which is used in a second layer to derive the address, is not as vulnerable to quantum computer brute-force attacks. This means that if someone has the blockchain address, and has cracked the elliptic-key cryptography, that person would still have to get through the second layer of security that was used to derive the address from the public key. This is similar to why locking your bicycle twice, with two different locks that have different security mechanisms (key or number lock), gives you an added layer of security when locking your bike on the street. As a result of this, the address acts as a digital fingerprint of the public key but does not give any information about the person’s public key (unless they send the first transaction). Blockchain addresses have a similar function to a bank account number in the context of traditional financial transactions, or an email address when people want to send you an electronic mail.

Digital signatures in the Bitcoin network and similar blockchain networks are performed using a wallet software. Similar to a handwritten signature, a digital signature is used to verify that you are who you say you are. Properly implemented, they are more difficult to forge than handwritten signatures. Digital signatures have been in use for decades, mostly in the context of financial transactions, software licenses, or contract management software. In blockchain networks, digital signatures are used for the authentication (proof that the sender of tokens is, in fact, the sender) and integrity of the transaction (i.e. the amount of tokens sent). The private key is used for signing token transactions. The public key is used by the validating nodes in the network to verify the signature. This way, a wallet cannot pretend to be another wallet. This is also referred to as “non-repudiation.” Practically speaking, this means that another person cannot pretend to control your wallet, unless they have your private key. 

***
![Generation of keys and adresses](https://github.com/sherminvo/TokenEconomyBook/blob/main/imgs/04_GenerationKeysAdresses_alt.png)
***

## Types of Wallets & Key Management

Your private key must always be kept secret and should not be shared with other people unless you want to give them deliberate access to your tokens. Because of the two-step process of deriving the public key from the private key and the address from the public key, one only needs to back up the private key; everything else can be derived from the private key with the cryptographic algorithm used in the network. If you lose access to your wallet, without having a backup of your seed phrase[^6] or your private key, you will lose access to your tokens.  While your tokens will still exist in the network you won’t be able to access them. 

Contrary to popular belief, a blockchain wallet does not store any tokens. It only stores the public-private key pair associated with your blockchain address. It also keeps a record of all transactions where the wallet’s public keys are involved, along with some other data. Therefore, the term “wallet” is misleading. The word “keychain” would be more appropriate, as it acts as a secure key storage, and as a communication tool with the blockchain network. A blockchain wallet has more similarities to a keychain containing your home keys. If you lose the keys to your apartment, the apartment is still yours, but you cannot access your apartment as long as you don’t recover the key; maybe you have a backup key that you left with a neighbor, friend, or family member, or find a locksmith to help you break into your own house. Breaking your lock would translate to a brute-force attack to guess your private key. There are two different types of wallets, custodial and non-custodial wallets: 

**<span style="text-decoration:underline;">User-controlled wallets</span>** offer personal control over one’s tokens. Private keys are in the sole custody and responsibility of the users and transactions are signed directly from the users’ devices. With user-controlled wallets, however, the user becomes a unique point of failure in the case of loss or theft of their keys.

**<span style="text-decoration:underline;">Hosted wallets</span>** are custodial services, offered by online exchange services, where the service provider manages one’s wallet on their servers. In most cases, the private keys related to one’s wallet are also managed by those intermediaries. The wallet software replicates the user’s private key in such a way that a third party can submit transactions on the user’s behalf. Many people, therefore, prefer to host their tokens on online exchanges and delegate key-management responsibilities to those trusted institutions. Similar to banks today, these token-exchange services act as custodians of one’s funds (read more: Part 3 - Token Exchanges). 

A more autonomous solution to the problem of losing your private keys could be so-called “social key recovery solutions,” where you can appoint a set of trusted friends, family members, or institutions to confirm your identity and allow key recovery in a multi-signature process. In such a setup, you could, for example, appoint five trusted people who could be contacted in case of loss of your private key. Three out of five could be defined to sign with their private keys to recover your private key. This way, you fine-tune who you trust, without making yourself a unique point of failure. However, if these people know each other, they could collude or be bribed to collude against you. In order to enable a true P2P token economy, where people can send and receive tokens wallet to wallet, without the need for trusted third parties, we will need better wallet management solutions, where the individual is the sovereign of their tokens, maintaining high levels of security and usability. A less sophisticated solution for key recovery would be to automatically create a backup on a cloud service such as Google Drive. While this is not at all advisable, for convenience reasons, it seems to have become a trend with some token exchanges, such as “[Coinbase](https://www.coinbase.com/).”

At the time of writing this book, most wallets only allow the management of one type of token, and in some cases, a limited number of tokens. This is due to the fact that different distributed ledger systems are, for the most part, not interoperable. Most token systems have different technical specifications, which depend on the type of distributed ledger they are issued on, and therefore require individualized wallet development. Wallets that are multi-ledger compatible are time consuming and expensive to develop. Multi-ledger compatibility also bloats the wallet software. Another aspect of wallet design is whether a wallet (in combination with the underlying distributed ledger) enables co-signing of transactions. Many blockchain networks, such as Ethereum, do not enable native multi-signature transactions. In the case of Ethereum, you need to resolve this via a smart contract, which has been subject to security issues. 

Ring signatures, collective signatures, and “Shamir’s Secret Sharing”[^7] are all examples of alternative cryptographic algorithms that need to be enabled by the blockchain networks and supported by the wallet software to allow for co-signing of transactions. Co-signatures are an important feature that allow transferring custodianship over your tokens to someone else (a bank or an exchange manages your tokens), collective management of assets (in cases of collective ownership of the same asset or collective management as in the case of a DAO, Decentralized Autonomous Organization), or social key recovery. Chapters 3 and 4 of this book will deep-dive into the aspects of token management and token use cases, where the role of wallets will become more tangible.


***
![DigitalSignatures BlockchainWallets](https://github.com/sherminvo/TokenEconomyBook/blob/main/imgs/03_DigitalSignatures_BlockchainWallets.png)
***



## Sending Tokens

If Alice wants to send Bitcoin tokens to Bob, she will use a wallet software to authenticate herself, specify the amount she wants to send, and indicate Bob’s address. Her wallet software broadcasts the transaction to all computers in the network. Every computer in the network can now check if the transaction is valid, according to the network rules. The steps are as follows:

* Alice uses a wallet software that manages her private key. By performing standard mathematical operations, the wallet software can always derive her public key and her address from the private key.

* If Alice wants to send tokens to Bob, she uses her wallet software to create a transaction that includes all the necessary details: her public key. Alice needs to specify Bob’s address, and the number of tokens she wants to send. Alice then creates a digital signature of this transaction, a hash (performed by her wallet software).

* In order to prove to the rest of the network that she is the owner of the address, and thus the tokens, Alice signs the hash with her private key (automatically performed by her wallet software).

* Alice now broadcasts this transaction to any computer in the network: she sends out both the plaintext transaction and the signed hash (automatically performed by her wallet software).

* Any computer in the network receiving the transaction can now verify the validity of the transaction. They can use Alice’s public key to mathematically verify whether the signed hash was really signed by her. They can use the hashing operations on her readable transaction and will receive the same hash value. They can also use Alice’s public key to verify whether the signed hash was really signed by her.

* After confirming all of these details, by consensus of all network actors, validated transactions are stored into a block and hashed. This block becomes part of the updated ledger if other computers in the network validate that the hash number on the block is valid. This process of creating new blocks of transactions is subject to the consensus mechanism Proof-of-Work (read more about Proof-of-Work in the next chapter). 

* All network nodes will amend their ledger accordingly upon creation of the next block, so that Bob now owns the funds that Alice sent him. This transaction becomes part of the universal state of the Bitcoin network and is tamper resistant. The information on the ledger can be altered, but at prohibitively high costs (read more about how much it costs in the next chapter).


#### 


### Chapter Summary

> Cryptography is the practice and study of secure communication in the presence of third parties. The aim is to create information systems that are resilient against eavesdropping, manipulation, and other forms of attack. 

> Cryptography in blockchain networks allows for transparency of interactions while maintaining the privacy of all network actors. 

> Public-key cryptography is used to prove one’s identity with a set of cryptographic keys: a private key and a public key, which in combination with a transaction creates our digital signature. This digital signature proves ownership of our tokens and allows us to control them through a piece of software called a “wallet.”

> Similar to a handwritten signature, a digital signature is used to verify that you are who you say you are. In Bitcoin and other blockchains, digital signatures are mathematical functions that reference a specific wallet address that manages your tokens on a blockchain. 

> A hash function is a mathematical algorithm that can take any type of input, such as a string, a text file, or a picture file, and digest it to a fixed-size output string called a hash. It is a one-way function, which means that the only way to recreate the original input data (message) from the hash is to attempt to try all possible variations to see if they produce a match. While this is possible, it is time consuming and therefore expensive.


### Chapter References & Further Reading

_* Alonso, Kurt M.: “Zero to Monero: First Edition a technical guide to a private digital currency; for beginners, amateurs, and experts”, June 26, 2018 (v1.0.0): [https://www.getmonero.org/library/Zero-to-Monero-1-0-0.pdf](https://www.getmonero.org/library/Zero-to-Monero-1-0-0.pdf)_

_* Antonopoulos, Andreas M.: “Mastering Bitcoin: Programming the Open Blockchain”, O’Reilly, 2017_

_* Becket, B.: “Introduction to Cryptology”, Blackwell Scientific Publications, 1988_

_* Ben-Sasson, Eli;Chiesa, Alessandro; Garman, Christina; Green, Matthew; Miers, Ian; Tromer, Eran; Virza, Madars: „Zerocash: Decentralized Anonymous Payments from Bitcoin“ May 18, 2014 (extended version): [http://zerocash-project.org/media/pdf/zerocash-extended-20140518.pdf](http://zerocash-project.org/media/pdf/zerocash-extended-20140518.pdf)_

_* Ben-Sasson, Eli; Chiesa, Alessandro; Tromer, Eran; Virza, Madars: “Succinct Non-Interactive Zero Knowledge for a von Neumann Architecture”, February 5, 2019 (updated version): [https://eprint.iacr.org/2013/879.pdf](https://eprint.iacr.org/2013/879.pdf)_

_* Boyle, David: “The Little Money Book”, Alastair Sawday Publishing, 2003_

_* Buterin, Vitalik: “Bitcoin Is Not Quantum-Safe, And How We Can Fix It When Needed”: [https://bitcoinmagazine.com/articles/bitcoin-is-not-quantum-safe-and-how-we-can-fix-1375242150/](https://bitcoinmagazine.com/articles/bitcoin-is-not-quantum-safe-and-how-we-can-fix-1375242150/)_

_* Buterin, Vitalik: “Privacy on the Blockchain”, January 2016: [https://blog.ethereum.org/2016/01/15/privacy-on-the-blockchain/](https://blog.ethereum.org/2016/01/15/privacy-on-the-blockchain/)_

_* Castryck, Wouter: “ELLIPTIC CURVES ARE QUANTUM DEAD, LONG LIVE ELLIPTIC CURVES”, n COSIC Cryptography Blog, 31/05/2017: [https://www.esat.kuleuven.be/cosic/elliptic-curves-are-quantum-dead-long-live-elliptic-curves/](https://www.esat.kuleuven.be/cosic/elliptic-curves-are-quantum-dead-long-live-elliptic-curves/)_

_* Esslinger, Bernhard: “The CrypTool Script: Cryptography, Mathematics, and More”, 10th edition, distributed with CrypTool version 1.4.30: [https://web.archive.org/web/20110722183013/http://www.cryptool.org/download/CrypToolScript-en.pdf](https://web.archive.org/web/20110722183013/http://www.cryptool.org/download/CrypToolScript-en.pdf)_

_* Flannery, Sarah; Flannery, David: “In Code: A Mathematical Journey”, Workman Publishing Company, 2001_

_* Goldreich, Oded: “Foundations of Cryptography” Cambridge University Press, 2001_

_* Ito, Joi: “Our response to „A Cryptocurrency Without a Blockchain Has Been Built to Outperform Bitcoin“, Dec. 20, 2017: [https://www.media.mit.edu/posts/iota-response/](https://www.media.mit.edu/posts/iota-response/)_

_* Katz, Jonathan; Lindell, Yehuda: “Introduction to Modern Cryptography”, Chapman & Hall/CRC, Cryptography and Network Security Series, 2nd Edition, 2014_

_* Nakamoto, Satoshi: “Bitcoin: A Peer-to-Peer Electronic Cash System”, 2008: [https://bitcoin.org/bitcoin.pdf](https://bitcoin.org/bitcoin.pdf)_

_* Narula, Neha: “Cryptographic vulnerabilities in IOTA”, September 7, 2017[ https://medium.com/@neha/cryptographic-vulnerabilities-in-iota-9a6a9ddc4367](https://medium.com/%2540neha/cryptographic-vulnerabilities-in-iota-9a6a9ddc4367)_

_* Narula, Neha:“IOTA Vulnerability Report: Cryptanalysis of the Curl Hash Function Enabling Practical Signature Forgery Attacks on the IOTA Cryptocurrency”, 7 September, 2017: [https://github.com/mit-dci/tangled-curl/blob/master/vuln-iota.md](https://github.com/mit-dci/tangled-curl/blob/master/vuln-iota.md)_

_* N.N.: “Bitcoin”, Github repository: [https://github.com/bitcoin](https://github.com/bitcoin)_

_* N.N.: “Bitcoin Core”, Github repository, [https://github.com/bitcoin/bitcoin](https://github.com/bitcoin/bitcoin)_

_* N.N.: “Bitcoin Core Integration”, Staging tree: [https://bitcoincore.org/en/download](https://bitcoincore.org/en/download)_

_* N.N.: “Mimblewimble Protocol”, Github Archives: [https://github.com/mimblewimble/grin/blob/master/doc/intro.md](https://github.com/mimblewimble/grin/blob/master/doc/intro.md)_

_* N.N.: Monero Research Lab, Technical Resources: [https://ww.getmonero.org/resources/research-lab/](https://ww.getmonero.org/resources/research-lab/)_

_* N.N.: “Post-Quantum Cryptography” Information Technology Laboratory, COMPUTER SECURITY RESOURCE CENTER: [https://csrc.nist.gov/projects/post-quantum-cryptography/round-1-submissions](https://csrc.nist.gov/projects/post-quantum-cryptography/round-1-submissions)_

_* Prasanna: “Litecoin To Implement Mimblewimble”, Altcoin News, February 8, 2019: [https://cryptoticker.io/en/litecoin-implement-mimblewimble/](https://cryptoticker.io/en/litecoin-implement-mimblewimble/)_

_* Rogaway, Phillip; Bellare, Mihir: “Introduction to Modern Cryptography”, May 11, 2005:[ http://web.cs.ucdavis.edu/~rogaway/classes/227/spring05/book/main.pdf](http://web.cs.ucdavis.edu/%257Erogaway/classes/227/spring05/book/main.pdf)_

_* Schär, Fabian; Berentsen, Aleksander: “Bitcoin, Blockchain und Kryptoassets: Eine umfassende Einführung”, Books on Demand, 2017_

_* Schor, Lukas: “On Zero-Knowledge Proofs in Blockchains”, Argon Group, March 2018:[ https://medium.com/@argongroup/on-zero-knowledge-proofs-in-blockchains-14c48cfd1dd1](https://medium.com/%2540argongroup/on-zero-knowledge-proofs-in-blockchains-14c48cfd1dd1)_

_* Stallings, William: “Cryptography and Network Security: Principles and Practice”, Prentice Hall, 6th ed., 2013_

_* Stolbikova, Veronika: „Can Elliptic Curve Cryptography be Trusted? A Brief Analysis of the Security of a Popular Cryptosystem“, ISACA Journal Volume 3, 2016 [https://www.isaca.org/Journal/archives/2016/volume-3/Pages/can-elliptic-curve-cryptoraphy-be-trusted.aspx](https://www.isaca.org/Journal/archives/2016/volume-3/Pages/can-elliptic-curve-cryptoraphy-be-trusted.aspx)_

_* Tibco, Nelson Petracek: “What zero-knowledge proofs will do for blockchain”, Venturebeat, Dec 16, 2017: [https://venturebeat.com/2017/12/16/what-zero-knowledge-proofs-will-do-for-blockchain/](https://venturebeat.com/2017/12/16/what-zero-knowledge-proofs-will-do-for-blockchain/)_

_* Wetzel, Tyler: “Understanding the Jargon of the Blockchain and Cryptocurrency World” Medium, Aug 23, 2018: [https://medium.com/@twwetzel76/understanding-the-jargon-of-the-blockchain-and-cryptocurrency-world-64b5f431bcd5](https://medium.com/@twwetzel76/understanding-the-jargon-of-the-blockchain-and-cryptocurrency-world-64b5f431bcd5)_

_* Wikipedia contributors, "Cryptography," Wikipedia, The Free Encyclopedia, [https://en.wikipedia.org/wiki/Cryptography](https://en.wikipedia.org/wiki/Cryptography) (accessed Jun 10, 2017)._

_* Wikipedia contributors, "Digital signature," Wikipedia, The Free Encyclopedia, [https://en.wikipedia.org/wiki/Digital_signature](https://en.wikipedia.org/wiki/Digital_signature) (accessed Jun 10, 2017)._

_* Wikipedia contributors, "Cryptographic hash function," Wikipedia, The Free Encyclopedia, [https://en.wikipedia.org/wiki/Cryptographic_hash_function](https://en.wikipedia.org/wiki/Cryptographic_hash_function) (accessed Jun 10, 2017)._

_* Young, Joseph: “Anonymous Cryptocurrencies: Why Edward Snowden Supports Zero-Knowledge Proofs”, January 2018: [https://journal.binarydistrict.com/anonymous-cryptocurrencies-why-edward-snowden-supports-zero-knowledge-proofs/](https://journal.binarydistrict.com/anonymous-cryptocurrencies-why-edward-snowden-supports-zero-knowledge-proofs/)_

_* Bitcoin Core: [https://bitcoin.org/de/download](https://bitcoin.org/de/download)_

_* Electrum: [https://electrum.org/](https://electrum.org/)_

_* Ledger: [https://www.ledger.com/](https://www.ledger.com/)_

_* Monero: [https://getmonero.org/](https://getmonero.org/)_

_* Mimblewimble: [https://github.com/mimblewimble/grin/blob/master/doc/intro.md](https://github.com/mimblewimble/grin/blob/master/doc/intro.md)_

_* Trezor: [https://trezor.io/](https://trezor.io/)_

_* Zcash: [https://z.cash/](https://z.cash/)_


### Footnotes

[^1]:
While elliptic-curve cryptography provides the same level of security as RSA, it needs less computation and smaller key size, thus reducing storage and transmission requirements. It therefore allows for reduced storage and transmission requirements.

[^2]:
Zero-knowledge proofs cryptography allows for the validation of information without revealing that information with the verifier of that information.

[^3]:
Ring signatures can be used to obfuscate the identity of token owners, combining a group of partial digital signatures from various transactions sent by different users, to form a unique signature that is used to sign a transaction.

[^4]:
Hashing functions take an arbitrary-length input and return a seemingly random but fixed-length output. When more than one input resolves to the same output, serious problems can result from such a collision. A team of MIT and Boston University researchers found exactly such flaws in the IOTA Curl function. While the IOTA team fixed said vulnerabilities, they claimed that these flaws were introduced on purpose, which was highly criticized by the open-source community.

[^5]:
Calculate hash values here: [https://www.browserling.com/tools/all-hashes](https://www.browserling.com/tools/all-hashes)

[^6]:
A seed phrase, also called a “mnemonic seed,” is a method to tie the private keys with an easy-to-remember combination of words, which can be provided and managed by your wallet software. “Mnemonics” is a mapping technique that helps to reproduce something that is hard to remember, with random words that are easy to remember. 

[^7]:
Shamir’s Secret Sharing is a cryptographic algorithm that divides a secret (key) into parts, distributing shards of the secret to different people. To reconstruct the secret, all shards need to be added. In the “threshold” setup, only a certain number of parts is required to reconstruct the secret.
