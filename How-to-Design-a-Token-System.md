> _If you would like to tokenize your business or community and make it Web3 ready, how do you need to approach your token design? Which questions do you have to ask yourself? What know-how do you need in your team to be able to properly “design” or “engineer” these tokens? The aim of this chapter is to understand what questions are relevant in the design and engineering process of a new token system, depending on what type of token you want to create._

Design thinking approaches found widespread adoption in the product design practices of startups and scaleups of the Web2, with a particular focus on user-centered design or human-centered design. The term “design thinking” dates back to the 1950s and found widespread adoption in the business community over the 1990s.  The aim was to apply creativity techniques for novel problem-solving techniques that were solution oriented, yet holistic in their approach. Design thinking approaches help to strategically plan concepts for any new technology, product, or service. The process ranges from problem definition, ideation, solution-focused strategies, modeling, prototyping, testing, and evaluating, including iterative feedback loops thereof. 

With the emerging Web3, the term “engineering” is being used in the context of designing token systems by a growing “token engineering” community. [^1](http://tokenengineering.wikidot.com/) The motivation behind using the word engineering (instead of design) is to do justice to the infrastructural and mission-critical nature of Web3 networks and many of their potential applications. Trent McConaghy states that, “Engineering is about rigorous analysis, design, and verification of systems; all assisted by tools that reconcile theory with practice. Engineering is also a discipline of responsibility: being ethically and professionally accountable to the machines that you build, as illustrated by the Tacoma Narrows Bridge viewings and iron rings.” He was probably the first person to coin the term “token engineering,” hoping that “token ecosystem design would also become a field of rigorous analysis, design, and verification. It would have tools that reconcile theory with practice. It would be guided by a sense of responsibility.”

The terms “design” and “engineering” are closely related but not the same. Rather, they complement each other. While the term “Design" [^2](https://en.wikipedia.org/wiki/Design) might be a more known and intuitive term, carrying a more subjective, creative, and even artistic meaning, the term “engineering” tends to bring to the forefront the technical aspects, the composition of inert parts to create a predictable and robust whole. “Engineering refers to the use of scientific principles to design and build machines, structures, and other items, including bridges, tunnels, roads, vehicles, and buildings.” [^3] (https://en.wikipedia.org/w/index.php?title=Engineering&oldid=943637749). Design is, therefore, a part of an engineering process. The term “engineering design” is used to describe the part of the engineering process which is open ended and ultimately more subjective. 

Similar to electrical engineering and public policy design, token engineering is about rigorous analysis, design, and verification of systems and their assumptions. Their assumptions need to be assisted by tools that reconcile theory with practice. However, as opposed to electrical engineering, designing human behavior is much more similar to steering national economies, and public policy design, as it requires much more “fuzzy” modeling techniques. With the emergence of AI and better simulation tools, we might be able to design and deploy more effective purpose-driven tokens that also factor in unknown probability distributions, unknown or adversarial behaviors of agents, potential network externalities, and “tragedy of the commons” incurred to other parts of society.

While the “token engineering” community points out the necessity for rigorous software engineering practices, it often seems to me that in the theories outlined and practices lived, it mostly focuses on what I would call the “technical engineering” aspects of a token system. A look at the composition of team members of most blockchain/web3/token startups reflects this techno-centricity quite well. Engineering, however, is the practice of creating a technology that ultimately always has a social goal. Looking at engineering through a purely technological lens perpetuates a reductionist mindset on why and how we build technology. 

There seems to be a growing understanding for the need of using the term “engineering” in the broader sense when designing a token system. The Web3 with its distributed ledgers and smart contracts provides a governance layer and an economic layer for the Internet. If something goes wrong, the collateral damage is high, as we have seen with “TheDAO” exploits of 2016 or the “Parity” multisignature contract exploit of 2017 that resulted in millions of Euros drained from one or more smart contracts, or the more recent DeFi Hacks of 2020. I therefore suggest that we explicitly distinguish between the “technical engineering,” “legal engineering,” “economic engineering,” and “ethical engineering” aspects of a token. 


***
![Token Engineering](https://github.com/sherminvo/TokenEconomyBook/blob/main/imgs/28_TokenEngineering.png)
***


## Technical Engineering

When creating a token system, one needs to decide whether to create an infrastructure token or an application token, and how to technically implement the token system. **“Infrastructure tokens” **are tokens that either steer public blockchain networks (1st layer) or second-layer protocols such as state channels, or other Web3 protocols such as distributed file storage networks (more: Part 1 - Web3, the Stateful Web). These infrastructure tokens are purpose driven, incentivizing collective maintenance of said networks. The most important design questions in the engineering process are related to questions of security, scalability, and privacy. 

* <span style="text-decoration:underline;">Security aspects</span> address the design of the cryptoeconomic mechanisms to provide the level of security needed (more: Part 1 - Token Security & Blockchain and other Distributed Ledgers). 

* <span style="text-decoration:underline;">Scalability aspects</span> address the trade off between security, decentralization, and scalability. Maintaining security and a high level of decentralization while enabling scalability is an engineering question with a variety of trade-offs. Different scalability techniques, such as sharding, interoperability, state channels, and alternative cryptographic tools that reduce bloating of transactions, are currently being tested to address these issues (more: Annex - Scalability). 

* <span style="text-decoration:underline;">Privacy aspects</span> address the questions of what type of cryptography should be used to allow for the right “privacy by design.” In early blockchain networks, the data that is included in a token and its exchanges is public to anyone. Via additional cryptographic mechanisms, access grants can be managed in a more privacy-preserving manner (more: Part 3 - Privacy Tokens). However, that does not come for free, as every additional encryption is a cost to add up on the contract invocation.

**“Application tokens”** are managed by an underlying distributed ledger and other Web3 networks. The technical engineering process will need to consider which infrastructure and token standards to use. It furthermore needs to consider potential interoperability needs of the token system.

* <span style="text-decoration:underline;">Infrastructure used</span>: Since application tokens are managed by a distributed ledger, all privacy, scalability, decentralization, and security needs of the token will have to be met by the underlying infrastructure. Infrastructural constraints, therefore, need to be considered when choosing between the trade-offs of one solution and another.

* <span style="text-decoration:underline;">Interoperability</span>: In spite of the fact that distributed ledgers currently have limited interoperability, there are solutions on the horizon that might favor one system over the other.  Depending on how much interoperability your token system requires in the long run, infrastructure questions need to be considered.

* <span style="text-decoration:underline;">Standards</span>: The technical engineering process can choose from a growing list of standardized token contracts. The token standards used depend on the properties a token should have (privacy, fungibility, transferability, expiry date), and the properties depend on the purpose of the token, taking into account all economic, legal, or ethical constraints.

***
![Token Engineering Aspects](https://github.com/sherminvo/TokenEconomyBook/blob/main/imgs/27_TokenEngineeringAspects.png)
***


## Legal Engineering

Legal Engineering of tokens is the predominant task when we deal with “simple token systems.” The term “simple” is commonly used in the complex systems[^4] domain. In the context of token engineering, the term “simple” refers to the fact that the dynamics of the business or governance models of a potential token are well known, as in the case of (i) central bank money, (ii) securities and other assets, (iii) identification and certification processes, (iv) voting rights, (v) vouchers and coupons, or (vi) entry tickets and other access rights. The respective business or governance processes of these use cases have been stress tested over decades, sometimes centuries. Potential loopholes have been closed over the years in a process of trial and error, and there is regulation in place. Tokenization of such business/governance processes requires predominantly legal engineering, which refers to making the tokenization of existing assets, access rights, and voting rights legally compliant with local legislation. Legal engineering, therefore, refers to the tokenization of traditional governance models where smart contracts replace many of the existing human/paper/client-server–based operations. Relevant questions in the legal engineering process of identity tokens, currency tokens, asset tokens, or voting-rights tokens are:

* Which transnational/national/local jurisdiction(s) need to be considered?

* Which regulatory bodies might be concerned?

* How do we design smart contracts so that they are legally compliant?

* Does the jurisdiction need to be changed to cater to the new possibilities/dynamics of tokenization and the Web3?


## Economic Engineering

Economic engineering is predominantly required when designing “complex token systems.” The incentives and governance rules of the community are tied to “purpose-driven tokens”[ ](https://medium.com/crypto3conomics/purpose-driven-tokens-51334d278c32)that steer collective action of the community through automated mechanisms (more: Part 4 - Purpose-Driven Tokens). The governance models are mostly unknown and a result of the myriad of new possibilities to regulate collective action over the Web3 in the absence of intermediaries by using smart contracts and distributed ledgers. Many refer to these tokens as “utility tokens,” “work tokens,” or “consensus tokens.” What all these tokens have in common is that they steer collective action toward a common purpose. Such common purposes could be consensus, resource sharing, reputation and curation, reduction of CO2 emissions, etc. The tools that are necessary to design such systems can be found in economics, network science, cyber-physical systems, and sociotechnical systems. 

* <span style="text-decoration:underline;">Economics</span> deals with the studies of economic institutions, policies, and ethics, including questions of resource allocation, wealth disparities, and market dynamics in the context of the production, distribution, and consumption of goods and services. 

* <span style="text-decoration:underline;">Network science</span> studies complex networks, from biological networks to classic telecommunication networks, computer networks to social networks. Methods used include mathematics, physics, computer science, and sociology. 

* <span style="text-decoration:underline;">Cyber-physical systems</span> are mechanisms that are controlled or monitored by computer-based algorithms, tightly integrated with the Internet and its users. Examples include power grids and large-scale transportation systems, which both share the property that behavior of uncontrolled human actors can create undesirable or even unsafe conditions in entirely counter-intuitive ways.

* <span style="text-decoration:underline;">Sociotechnical systems</span> was first coined in the 1940s and refers to the interaction of social and technical aspects of private and public organizations and communities, online and in the real world. It refers to the studies of the complex infrastructures a society uses, such as the Internet and other communication networks, supply chains, and legal systems, and human behavior. The relation can be either simple (linear cause-and-effect relationships) or complex (non-linear and hard to steer and predict).

The main questions that need to be answered in such design processes are

* <span style="text-decoration:underline;">Goal of your token system</span>: What kind of system do you want to create? 

* <span style="text-decoration:underline;">How many different token types do you need</span>? Some token systems have multiple token types to steer collective action within the network. Examples that were explained in previous chapters of this book are the decentralized social media network Steemit (STEEM, SP, SBD) or the stable token MakerDAO (DAI, WETH, PETH, SIN, MKR). Other token systems only have one token, like the Bitcoin network. It can be generally assumed that the more token types, the more complex the network dynamics of steering that network.

* <span style="text-decoration:underline;">Purpose</span>: The definition of a clear purpose of the token is necessary for the further design process. Having analyzed over 100 token systems, it seems that clearer the purpose, the more resilient the network. My personal opinion is that a token should only have one purpose. If you have multiple purposes, you probably need more token types. Otherwise, the mechanism design of your token system can become too complex.

* <span style="text-decoration:underline;">Properties</span>: Once the purpose is defined, one can derive the properties of the token, taking into account all economic, legal, or ethical constraints that could influence the dynamics of a token system. Examples for property choice and potential dynamics are: (i) Transferability: Are the tokens tied to a unique identity (person or institution) or do they have limited transferability? Depending on the use case, the answer would be different. Limited transferability automatically reduces the liquidity of a token, making it infeasible as a medium of exchange. Reputation tokens, for example, need to be tied to the identity of a person or organization in the network and should have no transferability at all. Transferable reputation tokens could be traded on the free market, making them non-indicative for personal behavior in the network, as in the case of “Steem Power” tokens in the Steemit ecosystem.  (ii) Fungibility: If tokens are identical and not tied to an identity, the monetary policy of a token system, including the inflation rate, needs to be determined because the tokens can act as a medium of exchange (payment token). (iii) Expiry Date: If a token has an expiry date, this will reduce inflation of the token. An expiry date might also be desirable in the case of coupons or entry tickets and other access rights.

* <span style="text-decoration:underline;">Proof-of…</span>: The properties of a token are the basis for modeling a fault-tolerant mechanism to steer the network toward a collective goal. The aim of such a fault-tolerant mechanism is to define upon which behavior the tokens are minted, so it is resilient against corruption, attacks, or mistakes. Proof-of-Work has proven to be resilient to achieve the purpose (P2P transactions). The reputation token of the Steemit network (Steem Power), on the other hand, doesn’t have a resilient token design to fit its purpose (to serve as a fault-tolerant reputation token that is indicative of quality content).


## Ethical Engineering

The design of token systems also requires ethical and political thinking. What type of system we want to create is not a technological question but a socio-economic and political question. Questions of politics, morals, and ethics will need to be answered, ideally before the design of such systems. If we fail to incorporate ethical questions in the design thinking process of such systems, we will create “protocol bias.” History has shown that, eventually, all these questions will need to be resolved. However, if that is done after the fact, after a system has been created, these biases are hard to reverse due to system inertia (see Cambridge Analytica scandal and the discussions on privacy, control, and social media governance that followed in the wake of the scandal, and the challenges the Facebook network is facing right now). However, we do not have to reinvent the wheel. We can apply engineering ethics[^5] to the creation of Internet-based systems, something that the Silicon Valley and other big players of the Internet era have failed to do. In terms of token design, two of the most important ethical and political questions are:

* <span style="text-decoration:underline;">Transparency vs. Privacy</span>: The trade-off between public and private interests is an age-old political discussion that has been studied by political science and sociology. While the privacy of the individual is important, it might undermine the public interest. Let’s take the case of supply chain transparency: while most consumers probably agree that more information about what happens along the supply chain of goods and services is what they would wish for, the act of providing such a level of transparency could infringe individual rights (i.e. a camera in a factory to monitor workers’ rights also violates the privacy of the workers, depending on how that data is revealed). It is therefore crucial that we hire social scientists with the right know-how when answering such questions.

* <span style="text-decoration:underline;">Power Structures</span>: Trade-off between decentralization, security, and scalability is a much discussed topic in blockchain networks. The trilemma of decentralization raises the political question of how much decentralization is needed/wanted depending on the use case and the values of a community. The more decentralized, the slower the network is, and vice versa. Otherwise, one has to sacrifice security of the network. Power structures are also important when designing reputation tokens on a social media network like Steemit.com. In its current design, most reputation tokens (Steem Power) are owned by a handful of big players in the network, and only those decide on which story is relevant or not. 

To cover all aspects mentioned above, one needs an interdisciplinary team with the necessary expertise in all four fields of the engineering process who work hand in hand. Having lawyers, economists, and social scientists as part of the team in addition to the technical engineers, on executive level and below, will be paramount to developing resilient token systems. However, interdisciplinary work takes time and effort, as all four categories overlap and communication between the disciplines requires some ramp-up efforts. The quick and dirty approach of the Web1 and Web2, where the development process was rather “hack now and pivot later” oriented, does not play out well in the Web3. Once the bias is in the protocol, it is hard to revert the changes without consensus of all network actors. We, therefore, need to move away from Silicon Valley “meme-based development” to an “engineering-based development” that includes all aspects of the engineering process. “Simple token systems” will probably require predominantly legal and technological engineering, while “complex token systems” will need a good balance of all four areas. 


### Chapter Summary

> The terms “design” and “engineering” are closely related but not the same. Rather, they complement each other. While the term “design” might be a more known and intuitive term, carrying a more subjective, creative, and even artistic meaning, the term “engineering” tends to bring to the forefront the technical aspects, the composition of inert parts to create a predictable and robust whole.

> Design is a part of an engineering process. The term “engineering design” is used to describe the part of the engineering process which is open ended and ultimately more subjective. Similar to electrical engineering and public policy design, token engineering is about rigorous analysis, design, and verification of systems and their assumptions. Their assumptions need to be assisted by tools that reconcile theory with practice. As opposed to electrical engineering, designing human behavior is much more similar to steering national economies, and public policy design, as it requires much more “fuzzy” modeling techniques.

> With the emergence of AI and better simulation tools, we might be able to design and deploy more effective purpose-driven tokens that also factor in unknown probability distributions, unknown or adversarial behaviors of agents, potential network externalities, and “tragedy of the commons” incurred to other parts of society. 

> Engineering is the practice of creating a technology that ultimately always has a social goal. Looking at engineering through a purely technological lens perpetuates a reductionist mindset on why and how we build technology. There seems to be a growing understanding for the need of using the term “engineering” in the broader sense when designing a token system. 

> The Web3 with its distributed ledgers and smart contracts provides a governance layer and an economic layer for the Internet. If something goes wrong, the collateral damage is high. 

> Technical engineering relates to the technical questions of creating an infrastructure token or an application token, and how to technically implement the token system: Infrastructure tokens or application tokens? Security aspects address the design of the cryptoeconomic mechanisms to provide the level of security needed. Scalability aspects address the trade off between security, decentralization, and scalability. Privacy aspects address the questions of what type of cryptography should be used to allow for the right “privacy by design.”

> Legal Engineering of tokens is the predominant task when we deal with “simple token systems.” The term “simple” is commonly used in the complex systems domain. In the context of token engineering, the term “simple” refers to the fact that the dynamics of the business or governance models of a potential token are well known, as in the case of (i) central bank money, (ii) securities and other assets, (iii) identification and certification processes, (iv) voting rights, (v) vouchers and coupons, or (vi) entry tickets and other access rights. Tokenizing known business/governance processes requires making the tokenization of existing assets, access rights, and voting rights legally compliant with local legislation.
> ~
> Economic engineering is predominantly required when designing “complex token systems.” The incentives and governance rules of the community are tied to “purpose-driven tokens” that steer collective action of the community through automated mechanisms. The tools that are necessary to design such systems can be found in economics, network science, cyber-physical systems, and sociotechnical systems. The main questions that need to be answered in such design processes deal with the following questions: What kind of system do you want to create? How many different token types do you need? Purpose? Properties: Transferability, fungibility, expiry date?

> The design of token systems also requires ethical and political thinking. What type of system we want to create is not a technological question but a socio-economic and political question. Questions of politics, morals, and ethics will need to be answered, ideally before the design of such systems, the most important of which revolve around the questions of “transparency vs. privacy” and “power structures.” If we fail to incorporate ethical questions in the design thinking process of such systems, we will create “protocol bias.”

> Having lawyers, economists, and social scientists as part of the team in addition to the technical engineers, on executive level and below, will be paramount to developing resilient token systems. However, interdisciplinary work takes time and effort, as all four categories overlap and communication between the disciplines requires some ramp-up efforts. 


***
### Chapter References & Further Reading

* Archer, L. Bruce: “Systematic Method for Designers. Council of Industrial Design,” H.M.S.O., 1965.
* Archer, L. Bruce. "Design Management," Management Decision 1.4, 47–51, 1967
* Arnold, J.E.: “Creative Engineering: Promoting Innovation by Thinking Differently, “ Edited With an Introduction and Biographical Essay by William J. Clancey. Stanford Digital Repository. Retrieved September 23, 2018. 
* Cooper, R.; Foster, M.:”Sociotechnical systems,” American Psychologist, 26, 467-474, 1971
* Cross, N., Dorst, K.;Roozenburg, N.: “ Research in Design Thinking,” Delft University Press, 1992
* Cross, N.: “A Brief History of the Design Thinking,” Research Symposium Series, Design Studies vol 57, 160–164, 2018
* Esener, Esen: “An Essay on Legal Engineering: From Confusion to Clarity,” Sep 11, 2019: https://medium.com/@esenesener/an-essay-on-legal-engineering-from-confusion-to-clarity-908c8e731df7
* Faste, Rolf, Roth, Bernard, Wilde, Douglass J.: "Integrating Creativity into the Mechanical Engineering Curriculum," Cary A. Fisher (Editor), ASME Resource Guide to Innovation in Engineering Design, American Society of Mechanical Engineers, New York, 1993
* Lawson, Bryan: “How Designers Think: The Design Process Demystified,” London, Architectural, 1980
* Long, Susan: “Socioanalytic Methods: Discovering the Hidden in Organisations and Social Systems,” 2018
* Merriam-Webster: https://www.merriam-webster.com/dictionary/design
* McConaghy, Trent: “Towards a Practice of Token Engineering Methodology, Patterns & Tools,” TE Series Part II, Mar 1, 2018: https://blog.oceanprotocol.com/towards-a-practice-of-token-engineering-b02feeeff7ca
* McKim, Robert: “Experiences in Visual Thinking,” Brooks/Cole Publishing Co, 1973
* Paruch, Krzysztof: “Token Engineering from an Economic Perspective,” Nov 6, 2018: https://medium.com/crypto3conomics/token-engineering-from-an-economic-perspective-b6c464f20241
* Rowe, G. Peter: “Design Thinking,” Cambridge, The MIT Press, 1987
* Simon, Herbert: ”The Sciences of the Artificial, “ Cambridge, MIT Press, 1969
* Wikipedia contributors, "Engineering," Wikipedia, The Free Encyclopedia, https://en.wikipedia.org/w/index.php?title=Engineering&oldid=943637749 (accessed March 16, 2020).
* Wikipedia contributors, "Design," Wikipedia, The Free Encyclopedia, https://en.wikipedia.org/w/index.php?title=Design&oldid=943088539 (accessed March 16, 2020).
* Voshmgir, Shermin: “Token Engineering Research,” Nov 6, 2018, https://medium.com/crypto3conomics/token-engineering-research-b6627add09ee
* Voshmgir, Shermin: “Purpose-Driven Tokens,” Apr 11, 2019: https://medium.com/crypto3conomics/purpose-driven-tokens-51334d278c32
* Zargham, Michael: “Token Engineering 101: Why Engineering is Necessary,” Jul 1, 2018: https://medium.com/@michaelzargham/token-engineering-101-why-engineering-is-necessary-3bac27ccb8b7
* Token Engineering Wiki: https://twitter.com/tokengineering
* Token Engineering Slides: https://www.slideshare.net/tokenengineering


***
### Footnotes

[^2]:https://en.wikipedia.org/w/index.php?title=Design&oldid=943088539](https://en.wikipedia.org/w/index.php?title=Design&oldid=943088539

[^3]:https://en.wikipedia.org/w/index.php?title=Engineering&oldid=943637749](https://en.wikipedia.org/w/index.php?title=Engineering&oldid=943637749

[^4]:
“Complex systems theory investigates the relationships between system parts with the system’s collective behaviors and the system’s environment. Complex systems differ from other systems, in that the system behavior cannot be easily inferred from the state changes induced by network actors. Properties such as emergence, nonlinearity, adaptation, spontaneous order, and feedback loops are typical to complex systems. Modeling approaches that ignore such difficulties will produce models that are not useful for modeling and steering those systems.” Voshmgir, S.; Zargham, M.: “Foundations of Cryptoeconomic Systems” (see references)

[^5]:
“engineering ethics identify a specific precedence with respect to the engineer's consideration for the public, clients, employers, and the profession. Many engineering professional societies have prepared codes of ethics. Some date to the early decades of the twentieth century (which) have been incorporated to a greater or lesser degree into the regulatory laws of several jurisdictions.” ([https://en.wikipedia.org/wiki/Engineering_ethics#General_principles](https://en.wikipedia.org/wiki/Engineering_ethics#General_principles)) Or, as the American Society of Civil Engineers states: “Engineers shall hold paramount the safety, health and welfare of the public and shall strive to comply with the principles of sustainable development in the performance of their professional duties.”  