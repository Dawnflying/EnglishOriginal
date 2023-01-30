> _Blockchain networks and similar distributed ledgers use public-key cryptography for the identification of all network actors. These identity-systems, however, are insufficient for the array of possible Web3-applications. Decentralized Identifiers (DIDs) in combination with distributed ledgers can provide “user-centric” identity solutions that are suitable for the Web3, allowing for more privacy and control over one's digital assets and digital footprint than “server-centric” solutions used in the Web2._

_Disclaimer: The intention of this chapter is to give a general overview, and shed a light on the urgency and importance of adequate digital identity solutions as a pivotal building block for the Web3. However, the topic of digital identities is much more complex than outlined in this chapter and cannot be discussed in detail, as that would be beyond the scope of this book._

Identity management refers to the process by which organizations, individuals, and objects can be trustfully  identified, authenticated, and certified. Trusted identity services are the basis for access rights management over the Internet and a necessary prerequisite for many socio-economic activities in general - offline or online. Identity-related use cases can be found in government (birth certificates, national ID cards, passports, or driver’s licenses), education (certifications and licenses), healthcare (personal health–related data records), e-commerce, banking or finance (client, B2B and employees’ data). In the Internet-of-Things, an  increasing number of objects that are connected to the Internet also need proper identification systems (such as serial numbers). From a computer science perspective, the term “identity” can be reduced to the data elements related to the identity management process: “identifier,” “authentication,” and “credentials.” 

* **Identifiers** are needed to uniquely identify a person, institution, or object. A phone number or an email address is unique in nature and would qualify as an identifier. The name of a person is not necessarily unique, and does not always qualify as an identifier. On the other hand, while the residential address and phone number of a person are unique in nature, they can change over time. Ideally, an identifier needs to be unique and persistent over time. A social security number, passport number, or driver's license number could be a unique identifier for a person, if it does not change over time. Whether or not such identifiers persist over time depends on the country in question and whether document numbers expire or not. Unique identifiers also exist for objects and companies: A serial number is a unique identifier for an object. A company registration number is a unique identifier for a for profit organization, so public authorities know how to identify companies for collecting taxes or granting subsidies.

* **<span style="text-decoration:underline;">Authentication</span>** is the process with which a person, institution, or object can prove that they are who they claim they are. A person can authenticate themselves by proving ownership of an object (ID card, hardware wallet, software wallet), knowledge (password or PIN), or by a personal property (biometric data, signature). Often, a combination of these systems is used. At least one strong and reliable method must exist to authenticate a person, institution, or object. Biometrics are the strongest forms for proving authentication for people. An ID card is an analogue form of authentication, as the picture and handwritten signature on the ID card are authentication methods. Passwords are the digital equivalent to a handwritten signature in the current Internet. However, usernames and passwords and all other personal data are controlled by mostly private institutions such as your bank, your university, or Facebook, Twitter, and Google. Blockchain networks and other distributed ledgers have popularized more user-centric identity-systems, applying public-key cryptography as a method of authentication.

* **<span style="text-decoration:underline;">Claims & Credentials</span>**: An identity is useless without linking relevant information to a person (personal data), institution (institutional data), or object (object-related data) to the identifier. Personal data, for example, involves claims made by the person themselves (claim) or by other people or institutions (credential). Such claims can include information about who I am, where I live, where I was born, or which degrees I have successfully completed and need to be attested by trusted authorities. Personal data can also include additional data, such as personal browsing histories, social media activities, or geo-locations, which are automatically authenticated by machines and also tied to the personal identifier. 

Historically, identity processes, such as passports, driver’s licenses, social security cards, or serial numbers for goods, have been issued by centralized institutions such as local and national governments and other trusted institutions. The emergence of the Internet created the need for digital identification systems. However, the current Internet does not provide a native identity layer for people, institutions, or objects other than the operating nodes in a network of computers. Problems such as “Can I trust my customer to pay their bills?” or “Can I trust the service provider to deliver my goods?” could not be resolved by the Internet Protocol. Companies and public institutions started to implement workaround solutions on the application layer of the Internet - often using internal databases and username-password combinations - the type of identification systems that had been in use since the time of mainframe computers and before the emergence of the Internet. 


## Server-Centric Identities

The Internet Protocol has no native format for managing the identities of people, organizations, and objects. Workaround solutions have been built on the application layer using internal databases (private infrastructure) to manage all the data involved with digital identity management processes. Due to the client-server structure of the Internet, any Web-based service - from university websites to online banking, social media, and e-commerce sites- provide their own identity-management-service, which means that all user-related data is managed by the service provider, on their private computer infrastructure. All elements related to the identity management process—such as issuing an identifier, providing an authentication method, providing the credentials, and managing user-related data—are centralized. The result is a series of incompatible data silos with proprietary - and often incompatible -  identity-management-service which have created considerable costs and trade-offs, both for companies and users alike such as:

* **<span style="text-decoration:underline;">Password chaos</span>**: Over the decades, as the number of Internet services grew, password management became a chaotic task. Users have to manage hundreds of usernames and passwords for each application or new online service they register for. Fragments of their personal data are scattered all over the Web. In the early days of the Internet, every online service required users to register with a username and password with their services, including more data if needed. Today, users can use “single sign-on solutions” provided by companies such as Google, Facebook, or Twitter, with the downside that these identities can be observed and revoked unilaterally by that service provider at any time, which can have cascading lockout effects from all other services one uses with this login. 

* **<span style="text-decoration:underline;">Protection against bad actors</span>**: In an e-commerce setup, companies need to identify bad actors that might order goods they never pay for in order to prevent potential business losses. Due to the fragmented nature of current digital identity systems, the process of identifying bad actors for fraud protection is a cost-intensive business overhead. “82% of businesses struggle with fake users and on average 10% of a web-facing organisation’s user base will be fake. The average retailer cost for each stolen record containing sensitive and confidential information is 65. 5 billion in losses from 13.1 million consumers in 2015 is the US alone.”[^1]

* **<span style="text-decoration:underline;">Data protection & custodial costs</span>**: Users have to trust the service providers to maintain the integrity and privacy of their data. A growing number of personal data is in the custody of often private institutions who manage a growing amount of customer data on their private servers, which results in what many privacy activists have been referring to as “Surveillance Capitalism.”[^2] Username-password combinations are often compromised by internal or external data breaches. Workarounds such as multi-factor authentication methods have been introduced to mitigate this problem. But security management of identity-related data against theft or loss still remains an expensive and patchy task. With the emergence of a growing body of data protection laws, and in light of potential lawsuits and government fines, collecting sensitive information about their users and storing that data on their servers has become an increasing business risk for companies.

* **<span style="text-decoration:underline;">Data portability</span>**: In Business-to-Business applications, portability is especially relevant along the supply chain of goods and services to process the provenance of goods and services and reduce document-handling costs. In Business-to-Consumer applications, new legislation such as Article 20 of the European Union General Data Protection Regulation grants users the right to have their personal data ported from one company to another, and mandates companies to provide for such data portability. In a client-server setup, however, such data portability with other institutions comes at high operational costs.

* **<span style="text-decoration:underline;">Lack of Control & Sovereignty</span>**: Users have no direct control over what happens with their data, and don’t know whether and to whom it has been passed on. Depending on the regulation of a country, users of Internet-based services can be locked out from using the services (and their data) at any time. Data protection depends on the applied business ethics of the company providing the identity services, and is also subject to the jurisdiction of the country under which the company falls. 

* **<span style="text-decoration:underline;">Re-centralization of the Internet</span>**: Network effects have the tendency to lock in customers and business partners to use one service provider only. Take the example of Amazon or eBay. Once users have undergone an authentication process with Amazon or eBay, they tend to stay on Amazon or Ebay, rather than buying products with others online. Buying a product on the website of a neighborhood store would require a separate authentication process on the website of that store and create a new identity (username and password) including payment information, which many people tend to avoid due to the time-consuming nature of this process. On the other hand, the more users Amazon and eBay have, the more these services become attractive to sellers, and vice versa. As a result of such network effects, power started to accumulate around these networks. This led to a re-centralization of the Internet around Internet platform providers, who not only manage the identities of their users, but also control all other user-related data. The “digital footprint” of all users is often stored in plain text (not encrypted) on the servers of the companies and used for data mining that creates recommendation algorithms, advertising algorithms, and other forms of user profiling that generate more income for these Internet platforms.


## History of Digital Identity Management

Over the decades, several initiatives tried to find alternative solutions to centralized identity management. In 1999, “Microsoft Passport” launched an initiative to provide a “federated identity solution”  that people could use across various Internet services. The main idea was to provide an online identity service that mitigated the password chaos for the users. However, this solution put Microsoft at the center of the federation. Sun Microsoft initiated the “Liberty Alliance” in 2001 as a more distributed solution, where control over digital identities was now divided among several institutions, but personal data still remained under the authority of each individual site. In 2001, the “Identity Commons” began to consolidate all works on digital identity with a focus on decentralization, which ultimately led to the creation of the “Internet Identity Workshop” in 2005. The open-source developer community started to work on alternative concepts, such as  “OpenID,” that countered the “server-centric model” with a “user-centric model” where individuals could control their identity using their own personal domain name, and fill their own data store with personal data that could be provided to other organizations with the permission of the individual. However, these solutions were not very user friendly and required some technical know-how. 

In the meantime, companies such as Facebook adopted the idea of “OpenID” but provided better usability, which was one of the reasons why, “Facebook Connect” became more successful than “OpenID” around 2008. Anyone could use their Facebook identity to sign up for other  Internet services, which could now use a Facebook API instead of managing their own identities. This was very useful to smaller Internet startups that could save costs on identity management, and to users who could save time and headaches on password management. Soon Google, Amazon, Apple, and Twitter followed in providing similar “server-centric” identity solutions - all of which control the majority of the online identity market today. This also includes the personal browsing history, social media behavior, and geo-locations of their users. 

Meanwhile, a growing set of initiatives continued to work on the idea of more “user-centric” identity solutions, such as the Web-of-Trust initiative, which had its roots in the Pretty Good Privacy (PGP) movement. They proposed the use of asymmetric cryptography where anyone could be a validator of identities. Unfortunately, both initiatives focused on email addresses as identifiers, which meant that they still depended on institutions such as ICANN[^3] to issue the domain names on which these email addresses are based. For a variety of reasons, PGP never became broadly adopted. 

Years later, individuals such as Christopher Allen and initiatives such as Rebooting-the-Web-of-Trust picked up on these efforts, especially as blockchain networks emerged and allowed the use of public-key cryptography for pseudo-anonymous identification without linking identities to an email address. The emergence of blockchain networks and other distributed ledgers provided a natural continuation of previous decentralization efforts. Christopher Allen and other individuals elevated the discussion of identity management to a political level and proposed the concept of “Self-Sovereign Identity,” a type of user-centric identity management system that needs to meet a series of guiding principles:

* **<span style="text-decoration:underline;">Access & Control</span>**: Direct control of one’s personal identity data, where users are the ultimate authority and have control over the level of anonymity of their data. 

* **<span style="text-decoration:underline;">Transparency & Interoperability</span>**: Algorithms governing identity-related data should be transparent, open source, and independent from any particular infrastructure. Identity-related data must be long-lived and should preferably last forever, or at least for as long as the user wishes. 

* **<span style="text-decoration:underline;">Portability</span>**: Identity-related data must be portable to other services, otherwise they are subject to censorship or control. Portable identities ensure that users remain in control of their identities independent of the services they use. 

* **<span style="text-decoration:underline;">Consent & Minimization</span>**: Users must, at all times, agree to the access of third parties to their personal data. Furthermore, when personal data is disclosed, that disclosure should involve only the minimum amount of data necessary.

In his manifesto Allen outlined the delicate balance between the right to privacy and the need to disclose certain information for the security of the whole network of people. He warned that these principles can be a double-edged sword, usable for both beneficial and malevolent purposes, and concluded that an identity system must balance transparency, fairness, and support of the common interests of a group while at the same time guaranteeing protection for the individual. However, such discussions are not new and have been subject to political science, as well as centuries of debates that have been resolved to varying degrees depending on the political regime and governing laws of the nation state in question. The balance between individual privacy versus public interest has been - and still is - a topic of constitutional law in many democratic countries,  subject to regulation around the “secrecy of correspondence” or “sanctity of the home” (read more: Part 3 - Privacy Tokens).

The above mentioned principles have been incorporated into a series of user-centric identity initiatives and working groups over the years, such as  “Social Linked Data,” “Rebooting the Web of Trust,” “WebIDs,” and most recently the “W3C Working Group on Decentralized Identifiers (DIDs).” The aim of all these initiatives has been to provide international open standards that decouples the process of issuing a credential and marking a claim from verifying those claims over a set of actors, which removes many of the issues that server-centric solution face. 

***
![History of Identities](https://github.com/sherminvo/TokenEconomyBook/blob/main/imgs/30_HistoryOfIdentities.png) 
***


## User-Centric Identities using DIDs

Blockchain networks currently only offer a minimum set of identity attributes that are not sufficient for many socio-economic interactions over the Web. However, if set up correctly, the ledger can offer critical components for a user-centric and privacy-preserving identity management system, providing less friction and lower costs for everyone involved. Decentralized Identifiers (DIDs) in combination with distributed ledgers allow for a more sophisticated identity-management-systems. 

A Decentralized Identifier (DID) is a public and pseudo-anonymous unique digital identifier for a person, company, or object that grants personal control over one’s digital identity without the need for centralized institutions managing those identifiers. To guarantee independence of centralized registries, DIDs need to have certain properties. They need to be permanent so they cannot be reassigned to other entities by whomever is in control. They need to be resolvable so everyone understands how to interact with the subject identified by the DID, and they need to be cryptographically verifiable.

Public-key infrastructure, inherent to distributed ledgers, allows for the registration of DIDs of all actors involved in a publicly verifiable way. Any user can create and register a DID when activating a new blockchain wallet, which creates a pair of private and public keys. Any DID can be linked to credentials that are issued by other people and institutions attesting specific characteristics for an identity owner (claims they make about themselves), such as name, address, email, age, existing diplomas, or other certifications such as a driver’s license. 

The wallet is the digital equivalent to a physical wallet, which - in addition to storing one’s cash - also acts as a container for ID cards, such as driver’s license, bank card, gym membership, national ID card, social security card, or loyalty cards. A Web3 wallet can be used to manage all your cryptographically secured digital credentials that others have issued about you, tokenized credentials that represent the digital version of your driver's license, bank card, gym membership, national ID card, social security card, loyalty cards, etc. Just as you open your wallet to reveal your ID card, you need to activate your Web3 wallet to reveal your digital credentials to third parties (using a password). No one can see the contents of your Web3 wallet without your consent. The content of the wallet remains concealed until you choose to reveal something. The players in such a setup are:

* **<span style="text-decoration:underline;">Identity issuers:</span>** trusted institutions such as local governments, universities, and other public and private institutions, and in some cases, even private individuals. These identity issuers can provide credentials for an identity owner (such as name, age, and date of birth) and attest to the validity of the personal data.

* **<span style="text-decoration:underline;">Identity owners:</span>** manage the credentials that have been issued by third parties mentioned above, in their Web3-wallet, and can use them at any point in time to prove statements about their identity to another third party.

* **<span style="text-decoration:underline;">Identity verifiers</span>** are third parties that provide services upon verification of certain identity-related  attributes. For example, if there is an age limit on buying alcohol, or watching a movie, the identity verifier (the shop or movie theater) can validate the signature of the government  that issued and attested to this credential. 

***
![User-Centric Identities](https://github.com/sherminvo/TokenEconomyBook/blob/main/imgs/29_UserCentricIdentities.png) 
***


The credentials are signed by their issuers using public-key cryptography. Once signed by an issuer, credentials can be managed by the identity owner to make claims, simply by using their wallet. Identity owners use their wallet to disclose which data they want to share with the outside world. They get to decide and control not only with whom they want to share their data, but also when to share that data. To do that, they need to attest to the network their consent to share selected data with authorized institutions. 

Both identity issuers and identity owners need to be registered on a public ledger with their DIDs. In such a setup, distributed ledgers can be used to attest the authenticity of the data and attestations, only registering indirect “pointers” for the purpose of verification. Distributed ledgers can be used as a public infrastructure to facilitate the verification of identity-related data. Anyone in a blockchain network can now verify whether a claim made by an identity owner is valid and which institutions attested to the validity of the claim, without having to reveal the data itself.

Pairing the private key with a DID allows the identity owner to create a QR code, for example, that represents that verified identifier. Scanning the QR code, a service provider can now run the data through a blockchain network or similar distributed ledger and verify if an attestation is associated with that person’s DID. The public key is used to attest to the authenticity of the issuing authority’s signature associated with a credential. If attestation and DID match, access is granted, and a person can qualify to buy alcohol, rent a car, etc. In addition to such attestations, any other data can also be associated to a DID and directly controlled by the identity owner through the wallet software. Examples of such “non-attested” data are personal browsing histories or social media posts. In such a setup, one would not rely on third-party digital identity providers such as Google or Facebook anymore. The “Brave browser” is a practical example for how a Web3 wallet allows direct control of your digital footprint (read more: Part 4 - Basic Attention Token). 

Revocation registries give identity issuers the possibility to revoke a claim since certain identity-related data can change over time. Personal data such as address, marital status, and number of children can change over time and therefore need to be updated. 

Separating the process of (i) issuing a credential, (ii) making a claim, and (iii) validating those claims against credentials is crucial to a user-centric setup. It can be seen as a system of checks and balances in a data-driven economy that guarantees the level of autonomy and privacy over one’s digital footprint, and is very contrary to how the Internet is set up today.

KERI (Key Event Receipt Infrastructure) is a novel technology  - a type of consensus network - that allows to move certain functions of decentralized identity-management systems off-chain to a different layer, and minimize the role of the distributed ledger. The aim is to provide a simple, scalable, more modular, identity-management system that is more interoperable across different blockchain networks and other distributed ledgers. It is currently being adopted by many players in the user-centric identity space and shows a lot of potential to act as a catalyst for user-centric identities.

## Outlook

User-centric identity solutions based on distributed ledgers and DIDs can disintermediate the identity industry. They can increase operational efficiency with on-the-fly auditing and real-time direct data access, while reducing costs. If set up correctly, they provide higher data security and protection from identity imposters, and provide more efficient regulatory compliance, granting more control to the data owners. User-centric identity solutions can provide for data portability, where individuals and institutions can easily reuse credentials to re-verify themselves for new services. For companies, this can reduce the costs and time involved with customer-onboarding and drop-out rates, as well as overall opportunity costs related to a full Know-Your-Customer identification process.

For the storage of personal data, user-centric identity solutions can use either personal data stores or distributed file storage networks. Credentials can be stored directly on the user’s device or securely in a private identity store, or identity hub, such as “TrustGraph” or “3Box.” Less privacy-sensitive data can be collectively managed by distributed file storage networks such as the “InterPlanetary File System” (IPFS) or “OrbitDB” to reduce data redundancies and disintermediate the identity management process. In both setups, data is designed around the user, and thus more interoperable across multiple service providers that can use the same set of information for different purposes. User data is not locked into one platform.

While some forms of zero-knowledge proof cryptography are already in use in user-centric identity solutions, there is more room to improve even stronger privacy-preserving cryptographic tools. A set of Web3 networks is already working to incorporate more privacy-preserving cryptographic mechanisms into distributed ledgers, such as “Zero-Knowledge Proofs” as implemented by “Zcash,” or “Ring Signatures” as implemented by “Monero,” or to perform computation on encrypted information using “Secure-Multi-Party-Computation” (read more: Part 3 - Privacy Tokens). KERI might also be a game changer in that aspect.

One of the most interesting future use cases will be the digital identification of objects. Currently, most Internet-of-Things (IoT) devices have no secure digital identity and access management capabilities. A DID-powered serial number can make any object in the Web3 addressable. Once we start tagging objects with mini computers (crypto accelerators) that come with a DID-powered serial number and communicate with a distributed ledger network, any object along the supply chain can prove ownership and credentials to others in the network using cryptographic proofs. Objects that have their own unique Web3 identity and Web3 wallet can become autonomous and trustable economic entities. Such a “cyber-physical link” between objects and DID allows for effective product tracking and data sharing on the provenance of goods and services between producers and consumers. 

Selected Web3-based identity solutions are:  “3Box,”“[Ageify](https://age-ify.com/),” “[Civic](https://www.civic.com/),” “[Edge](https://edge.app/),” “[Hu-manity.co](http://hu-manity.co/),”  “[Jolocom](https://jolocom.io/),”  “[Keyp](https://keyp.io/),” “[Madana](https://www.madana.io/),” “[Metadium](https://www.metadium.com/),” “[NewBanking Identity](https://newbanking.com/),”“[ObjectTech](https://www.objecttechgroup.com/),” “[THEKEY](https://www.thekey.vip/#/homePage),” “[Trusti,”](https://trusti.com/) “[PeerMountain](https://www.peermountain.com/),” “[REMME](https://remme.io/),” “[Riddle & Code](https://www.riddleandcode.com/ ),” “[Spherity](https://spherity.com/),” “[uPort](https://www.uport.me/),”“[UniquID](https://uniquid.com/),” “[ValidatedID](https://www.validatedid.com/),” and “[WoTT](https://www.wott.io/).” 


### Chapter Summary

> Historically, identity processes, such as passports, driver’s licenses, social security cards, or serial numbers for goods, have been issued by centralized institutions such as local and national governments and other trusted institutions. The emergence of the Internet created the need for digital identification systems.

> From a computer science perspective, the term “identity” can be reduced to the data elements related to the identity management process: “identifier,” “authentication,” and “credentials."

> Identifiers are needed to uniquely identify a person, institution, or object. An identifier needs to be unique and persistent over time. 

> Authentication is the process with which a person, institution, or object can prove that they are who they claim they are. A person can authenticate themselves by proving ownership of an object (ID card, hardware wallet, software wallet), knowledge (password or PIN), or by a personal property (biometric data, signature). Often, a combination of these systems is used. \

> An identity is useless without linking data related to a person (personal data), institution (institutional data), or object (object-related data) to the identifier.

> The current Internet was built around connecting machines, not people. The Internet does not provide a native identity layer for people, institutions, or objects other than the operating nodes in a network of computers. Workaround solutions have been built on the application layer using internal databases (private infrastructure) to manage all the data involved with digital identity management processes. All user-related data is managed by the service provider, on their private server infrastructure, and that all elements related to the identity management process are centralized.

>  These data silos and proprietary identity solutions have created considerable costs and trade-offs, both for companies and users alike such as (i) password chaos, (ii) protection against bad actors, (iii) data protection & custodial costs, (iv) data portability, (v) lack of control & sovereignty over data, and the (vi) re-centralization of the Internet.

> Blockchain networks and similar distributed ledgers use public-key cryptography for the identification of all network actors, but they are insufficient for a thriving tokenized economy. However, combined with DIDs, they can offer critical components for more “user-centric” identity solutions that are suitable for the Web3, and provide more privacy and control than “server-centric” solutions used in the Web2.  \

> The user-centric identity process requires three actors: (i) identity issuers, (ii) identity owners, and (iii) identity verifiers. If set up correctly, anyone in a blockchain network can verify whether a piece of data (credential) is valid and which institutions attested to the validity of the data without revealing the data itself.  

> While plain text data should never be stored on a public ledger, a privacy-preserving identity management system can use distributed ledgers to allow a person to prove that their personal identity-related data fulfills certain requirements without revealing the actual data. In such a setup, distributed ledgers can be used to attest the authenticity of the data and attestations, only registering indirect “pointers” for the purpose of verification.

> A user can create and register a DID when activating a blockchain wallet, which creates a pair of private and public keys. Public-key cryptography is used for authentication and encryption. Only the private key can prove one’s identity. The private key acts as your personal lock on the wallet.

> Any DID can be linked to attestations (verifiable credentials) that are issued by other people and institutions attesting specific characteristics for an identity owner, such as name, address, email, age, existing diplomas, or other certifications such as a driver’s license. The credentials are signed by their issuers using public-key cryptography. Once signed by an issuer, credentials can be managed using the wallet of the identity owner directly.

> The separation of the “identifier,” “authentication,” and “data” is crucial to a user-centric setup. It can be seen as a system of checks and balances in a data-driven economy that guarantees the level of autonomy and privacy over one’s digital footprint, and is very contrary to how the Internet is set up today. Using a public infrastructure such as a collectively maintained ledger as a unique source of truth, while splitting the roles in the identification management process, makes user-centric identity management systems “decentralized."

> The wallet acts as a personal container that allows you to control your digital identities. The wallet is the digital equivalent to a physical wallet, which usually acts as a container for all your ID cards, such as driver’s license, bank card, gym membership, national ID card, social security card, or loyalty cards, in addition to your money. While it is initially empty, over time, one can fill it with credentials that represent the digital version of your driver's license, bank card, gym membership, national ID card, social security card, loyalty cards, etc.

> Just as you open your wallet to reveal your ID card, you need to activate your Web3 wallet to reveal your digital credentials to third parties (using a password). No one can see the contents of your Web3 wallet without your consent. You choose who to share these credentials with. The content of the wallet remains concealed until you choose to reveal something. The digital wallet is portable, as a dedicated hardware device, or an app in your mobile phone or your notebook. 



### Chapter References & Further Reading
_* Allan, Christoper: “The Path to Self-Sovereign Identity,” March 1 2017, [https://github.com/ChristopherA/self-sovereign-identity/blob/master/ThePathToSelf-SovereignIdentity.md](https://github.com/ChristopherA/self-sovereign-identity/blob/master/ThePathToSelf-SovereignIdentity.md)_

_* Ellison,[ ](http://irl.cs.ucla.edu/index.html)Carl: “Establishing Identity without Certification Authority,” 1996, [https://irl.cs.ucla.edu/index.html](https://irl.cs.ucla.edu/index.html) _

_* Feisthammel, Patrick: “[Pretty good Privacy, PGP](https://www.rubin.ch/pgp/weboftrust.en.html), Web of Trust,” Oct 7 2004, [https://www.rubin.ch/pgp/weboftrust.en.html](https://www.rubin.ch/pgp/weboftrust.en.html)_

_* Jordan, Ken; Hauser, Jan; Foster, Steven: “The Augmented Social Network,” White paper, 2000, [https://firstmonday.org/ojs/index.php/fm/article/view/1068/988](https://firstmonday.org/ojs/index.php/fm/article/view/1068/988) _

_* Kameron, Kim: “The Laws of Identity,” March 2007, [https://docs.microsoft.com/en-us/previous-versions/dotnet/articles/ms996456(v=msdn.10)?redirectedfrom=MSDN](https://docs.microsoft.com/en-us/previous-versions/dotnet/articles/ms996456(v=msdn.10)?redirectedfrom=MSDN)_


_* Kütt, Andres: "MyData Webinar #5: Identity in the Digital Era," Mydata Global, Youtube Video, retrieved from: [https://www.youtube.com/watch?v=XjzJeys7PvM&fbclid=IwAR0qMDGYuZVk0c6aDHOX46AdFQMGdsI24SSZ6-lMfj7XZY-TrbkbT5LFlqk](https://www.youtube.com/watch?v=XjzJeys7PvM&fbclid=IwAR0qMDGYuZVk0c6aDHOX46AdFQMGdsI24SSZ6-lMfj7XZY-TrbkbT5LFlqk)_

_* Many authors: “[Rebooting the Web of Trust](http://www.weboftrust.info/papers.html),” Papers and Specs, [http://www.weboftrust.info/papers.html](http://www.weboftrust.info/papers.html)_

_* Many authors: “Charta for Digital Human Rights,” Version: 01.12.2016 Unofficial English translation of the German original text, published by ZEIT-Stiftung Ebelin und Gerd Bucerius [https://digitalcharta.eu/wp-content/uploads/2016/12/Digital-Charta-EN.pdf](https://digitalcharta.eu/wp-content/uploads/2016/12/Digital-Charta-EN.pdf)_

_* Many authors: “Self-sovereign Identity A position paper on blockchain enabled identity and the road ahead,”  October 23 2018, Identity Working Group of the German Blockchain Association, [https://www.bundesblock.de/wp-content/uploads/2019/01/ssi-paper.pdf](https://www.bundesblock.de/wp-content/uploads/2019/01/ssi-paper.pdf)_

_* Many authors: “The Respect Trust Framework, “ Version 2.1,  Feb 2016,  [https://oixnet.org/wp-content/uploads/2016/02/respect-trust-framework-v2-1.pdf](https://oixnet.org/wp-content/uploads/2016/02/respect-trust-framework-v2-1.pdf)_

_* Marlinspike, Moxie: “Sovereign Source Authority,” Moxytongue, Feb 2012, [https://www.moxytongue.com/2012/02/what-is-sovereign-source-authority.html](https://www.moxytongue.com/2012/02/what-is-sovereign-source-authority.html)_

_* Miller, Ron: "[The Promise of managing identities on the blockchain](https://techcrunch.com/2017/09/10/the-promise-of-managing-identity-on-the-blockchain/?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base_recent_activity_details_all%3BknkLT7NkR5Cex9bx3zogKg%3D%3D),” Sep 10, 2017, [https://techcrunch.com/2017/09/10/the-promise-of-managing-identity-on-the-blockchain/?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base_recent_activity_details_all%3BknkLT7NkR5Cex9bx3zogKg%3D%3D&guccounter=1](https://techcrunch.com/2017/09/10/the-promise-of-managing-identity-on-the-blockchain/?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base_recent_activity_details_all%3BknkLT7NkR5Cex9bx3zogKg%3D%3D&guccounter=1)_

_* Mire, Sam: “Blockchain Research Technologies Blockchain For Identity Management: 7 Possible Use Cases” Dec 5 2018, [https://www.disruptordaily.com/blockchain-use-cases-identity-management/](https://www.disruptordaily.com/blockchain-use-cases-identity-management/)_

_* N.N.: “Enterprise Ethereum Blockchain in Digital Identity,” Consensys website, [https://consensys.net/blockchain-use-cases/digital-identity/#usecases](https://consensys.net/blockchain-use-cases/digital-identity/#usecases)_

_* N.N.: “Identity Management with Blockchain: The Definitive Guide (2020 Update),”  TYKN website: [https://tykn.tech/identity-management-blockchain/](https://tykn.tech/identity-management-blockchain/)_

_* Preukschat, Alex; Reed , Drummond: "Self-Sovereign Identity Decentralized Digital Identity and Verifiable Credentials" MEAP began December 2019  Publication in January 2021 (estimated) ISBN 9781617296598  300 pages (estimated), electronically retrieved from:[https://www.manning.com/books/self-sovereign-identity](https://www.manning.com/books/self-sovereign-identity)_

_* Reed, Drummond; Tobin, Andrew: “[Sovereign White Paper](https://sovrin.org/wp-content/uploads/2017/07/The-Inevitable-Rise-of-Self-Sovereign-Identity.pdf),” Sept 29 2016, [https://sovrin.org/wp-content/uploads/2017/07/The-Inevitable-Rise-of-Self-Sovereign-Identity.pdf](https://sovrin.org/wp-content/uploads/2017/07/The-Inevitable-Rise-of-Self-Sovereign-Identity.pdf)_

_* Reed, Drummond; Sabadello, Markus: "Chapter 8 Decentralized identifiers" in Self Sovereign Identity, retrieved from on October 27, 2020: in [https://livebook.manning.com/book/self-sovereign-identity/chapter-8](https://livebook.manning.com/book/self-sovereign-identity/chapter-8)_
_* Ruff, Timothy: "When Explaining SSI, Start with the Wallet," Apr 21 2020, [https://medium.com/@rufftimo/when-explaining-ssi-start-with-the-wallet-bee5d2af6696](https://medium.com/@rufftimo/when-explaining-ssi-start-with-the-wallet-bee5d2af6696)_

_* Sabadello, Markus: “Human Rights in the Information Society,” 2011, [https://danubetech.com/download/Human-Rights-in-the-Information-Society.pdf](https://danubetech.com/download/Human-Rights-in-the-Information-Society.pdf)_

_* Shea, Michael;Smith, Samuel M.; Stöcker,Carsten, Caballero, Juan; Condon, Matt G.: “Decentralized Identity as a Meta-platform: How Cooperation Beats Aggregation a white paper from Rebooting the Web of Trust IX, [https://nbviewer.jupyter.org/github/WebOfTrustInfo/rwot9-prague/blob/master/final-documents/CooperationBeatsAggregation.pdf](https://github.com/SmithSamuelM/rwot9-prague.githttps://nbviewer.jupyter.org/github/WebOfTrustInfo/rwot9-prague/blob/master/final-documents/CooperationBeatsAggregation.pdf)_

_* Spike, Marlin: “Self Sovereign Identity, how the term has evolved,” Feb 2016, [https://www.moxytongue.com/2016/02/self-sovereign-identity.html](https://www.moxytongue.com/2016/02/self-sovereign-identity.html)_

_* Smith, Samuel M.: "Key Event Receipt Infrastructure (KERI)", Cornell University, retrieved from: [https://arxiv.org/abs/1907.02143](https://arxiv.org/abs/1907.02143)_

_* Smolenski, Natalie: ”The EU General Data Protection Regulation and the Blockchain,” Aug 2 2017, [https://medium.com/learning-machine-blog/the-eu-general-data-protection-regulation-and-the-blockchain-1f1d20d24951](https://medium.com/learning-machine-blog/the-eu-general-data-protection-regulation-and-the-blockchain-1f1d20d24951)_

_* Stöcker, Carsten: “The Economic Value of Decentralized Identity — Part 2 Reimagining the economics of trust and reputation,” Mar 11 2020, [https://medium.com/spherity/the-economic-value-of-decentralized-identity-part-2-733aa977eaf8](https://medium.com/spherity/the-economic-value-of-decentralized-identity-part-2-733aa977eaf8)_

_* Stöcker, Carsten: “Spherity’s Identity Tech Predictions for the decade of the 2020’s — Part 1,” Jan 16 2020 [https://medium.com/spherity/spheritys-identity-tech-predictions-for-the-decade-of-the-2020-s-part-1-410bc9b48be4](https://medium.com/spherity/spheritys-identity-tech-predictions-for-the-decade-of-the-2020-s-part-1-410bc9b48be4)_

_* Stöcker, Carsten: “Spherity’s Identity Tech Predictions for the decade of the 2020’s — Part 2,” Feb 13 2020 [https://medium.com/spherity/spheritys-identity-tech-predictions-for-the-decade-of-the-2020-s-part-2-6e480d2a57ea](https://medium.com/spherity/spheritys-identity-tech-predictions-for-the-decade-of-the-2020-s-part-2-6e480d2a57ea)_

_* Stöcker, Carsten: “SSI201: Upgrading products with intelligent serial numbers and DIDs How smart can an object’s identifier be? How can it enable cradle-to-grave traceability and other innovative capabilities?” Nov 26, 2019 ·, [https://medium.com/spherity/ssi201-upgrading-products-with-intelligent-serial-numbers-and-dids-78da623b91dd](https://medium.com/spherity/ssi201-upgrading-products-with-intelligent-serial-numbers-and-dids-78da623b91dd)_

_* Stöcker, Karsten: "KERI: A more Performant Ledger for Trusted Identities Securing the control of decentralized identifiers at the root with ambient verifiability", Medium, Sperity Blog, July 2 2020, [https://medium.com/@cstoecker](https://medium.com/@cstoecker)_

_* Voshmgir, Shermin: “Identity as a Bottleneck for Blockchain,” Oct 17, 2017, [https://stories.jolocom.com/identity-blockchain-the-road-to-self-sovereign-identity-f9f4439c52cb](https://stories.jolocom.com/identity-blockchain-the-road-to-self-sovereign-identity-f9f4439c52cb)_

_* Voshmgir, Shermin: “Self Sovereign — Identity vs Data?” Feb 27 2018, [https://stories.jolocom.com/self-sovereign-identity-vs-data-5abe5947a62](https://stories.jolocom.com/self-sovereign-identity-vs-data-5abe5947a62)_

_* Wikipedia contributors: "Pretty Good Privacy," Wikipedia, The Free Encyclopedia, https://en.wikipedia.org/w/index.php?title=Pretty_Good_Privacy&oldid=959437666 (accessed May 31, 2020)._

_* Zuboff, Shoshana: “ The Age of Surveillance Capitalism: The Fight for a Human Future at the New Frontier of Power.” New York: PublicAffairs, 2019._

_* Ageif: [https://age-ify.com/](https://age-ify.com/)_

_* Civic: [https://www.civic.com/wallet/](https://www.civic.com/wallet/)_

_* Edge: https://edge.app/_

_* General Data Protection Regulation (GDPR): [https://gdpr-info.eu/](https://gdpr-info.eu/)_

_* Hu-manity.co: [https://hu-manity.co/](https://hu-manity.co/)_

_* Jolocom: [https://jolocom.io/](https://jolocom.io/)_

_* Keyp: [https://keyp.io/](https://keyp.io/)_

_* List of Blockchain & Identity Solutions: [https://github.com/peacekeeper/blockchain-identity](https://github.com/peacekeeper/blockchain-identity)_

_* Madana: [https://www.madana.io/](https://www.madana.io/)_

_* Metadium: [https://www.metadium.com/](https://www.metadium.com/)_

_* NewBanking Identity: [https://newbanking.com/#/](https://newbanking.com/#/)_

_* ObjectTech: [https://www.objectivetgg.com/](https://www.objectivetgg.com/)_

_* THEKEY: [https://www.thekey.vip/#/homePage](https://www.thekey.vip/#/homePage)_

_* Trusti: [https://trusti.com/](https://trusti.com/)_

_* PeerMountain: [https://www.peermountain.com/](https://www.peermountain.com/)_

_* PGP WOT: [https://www.linux.com/training-tutorials/pgp-web-trust-core-concepts-behind-trusted-communication/](https://www.linux.com/training-tutorials/pgp-web-trust-core-concepts-behind-trusted-communication/)_

_* Rebooting the Web of Trust:[http://www.weboftrust.info/papers.html](http://www.weboftrust.info/papers.html)_

_* REMME: [https://remme.io/](https://remme.io/)_

_* Riddle & Code: [https://www.riddleandcode.com/](https://www.riddleandcode.com/)_

_* Spherity: [https://spherity.com/](https://spherity.com/)_

_* SPKI/SDSI project: [http://world.std.com/~cme/html/spki.html](http://world.std.com/~cme/html/spki.html)_

_* SoLid (Social Linked Data: [https://github.com/solid/solid-spec](https://github.com/solid/solid-spec)_

_* uPort: [https://www.uport.me/](https://www.uport.me/)_

_* UniquID: [https://uniquid.com/](https://uniquid.com/)_

_* ValidatedID: [https://www.validatedid.com](https://www.validatedid.com/)_

_* WebIDs: [https://www.w3.org/2005/Incubator/webid/spec/tls/](https://www.w3.org/2005/Incubator/webid/spec/tls/)_

_* WoTT: [https://wott.io/](https://wott.io/)_

_* W3C working group on verifiable claims: [https://www.w3.org/2017/vc/WG/](https://www.w3.org/2017/vc/WG/)_

_* W3C Verifiable Claims Task Force FAQ: [https://w3c.github.io/webpayments-ig/VCTF/charter/faq.html](https://w3c.github.io/webpayments-ig/VCTF/charter/faq.html)_

_* W3C initiative of Decentralized Identifiers (DIDs): [https://w3c.github.io/did-core](https://w3c.github.io/did-core/)_


### Footnotes

[^1]:
[https://sovrin.org/wp-content/uploads/2017/07/The-Inevitable-Rise-of-Self-Sovereign-Identity.pdf](https://sovrin.org/wp-content/uploads/2017/07/The-Inevitable-Rise-of-Self-Sovereign-Identity.pdf)

[^2]:
Such as Zuboff, Shoshana in “ The Age of Surveillance Capitalism: The Fight for a Human Future at the New Frontier of Power.” New York: PublicAffairs, 2019. Zuboff describes the commodification of personal information. She describes the tendency of accumulation of data, criticizing that many companies and institutions harvest and capitalize personal data without mechanisms of consent. She compares “industrial capitalism” and “surveillance capitalism,” explaining “industrial capitalism” as exploitation of  nature, and “surveillance capitalism” as  exploitation of human nature.

[^3]:
ICANN (Internet Corporation for Assigned Names and Numbers) is a nonprofit organization that coordinates the maintenance and procedures of several databases related to the namespaces and numerical spaces of the Internet, ensuring the network's stable and secure operation. It is a multi-stakeholder group based in the United States.
