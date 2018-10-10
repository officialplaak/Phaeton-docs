##Technical Paper##
#PLAAK Phaeton Chain##
##www.plaak.com##


Index


Abstract
	1	Introduction
Basic Terminology
	2	Cryptocurrencies: Overview
	3	Mining
	4	Consensus Mechanisms
	5	Peer-to-Peer Networks
	6	Data compression
	7	Cryptography
8	Digital Signatures
	9	Hashing 
	10	Algorithms

#Performance
Improvements
•	Nodes
	•	Consensus protocol (DPoS)
	•	Side chains & DAPPS
How it works
Sidechain benefits 
Use cases
	•	Sidechain validation network (SVN)
•	Economics & Fees
	•	Business info & applications





Table of Contents

Table of Contents	2
1. Abstract	4
1.1 Introduction	4
2. Basic Terminology	7
3. Cryptocurrencies: Overview	8
3.1 Bitcoin & Ethereum: Basics	8
3.2 Bitcoin & Ethereum: Differences	11
3.2.1 Use Case: Ethereum	11
3.2.3 Use Case: Bitcoin	12
4. Consensus Mechanisms:	13
4.1 Mining	13
4.2. Consensus layer support	15
4.2.1 The linked list data pointer structure	15
4.2.2 Traversing the blockchain	16
4.2.3 Non-interactive blockchain suffix proofs	16
4.2.4 Example	17
4.2.5 Exact probabilities of covert forkability for explicit values of n	17
5. P2P Network	19
5.1 Architecture	20
5.1.1 System Headers	20
5.1.2 Block Propagation	21
5.1.3 Transaction Propagation	21
5.1.4 Transaction Pool	22
5.1.5 Key Pair	22
5.1.6 Second passphrase	22
5.1.7 Multisignature	22
5.1.8 Address	23
6. Data Compression	24
7. Cryptography	25
7.1 What is Cryptography?	25
7.2 What is Public-Key Cryptography?	26
7.2.1 Elliptic Curve Cryptography	26
8. Digital Signatures	26
8.1 What is a Digital Signature?	27
8.1.1 Multisignature	28
8.1.2 Can one person use a multisig?	28
9. Hashing	28
9.1 Hashing as a security layer	29
9.1.1 Hashing as an essential part of the Blockchain	29
9.2 Hashing and the Blockchain structure	30
10. Algorithms	31
10.1 BLAKE2b Specifications	31
10.1.1 Blake2 Hashing Algorithm History	32
10.2 BLAKE2b Improvements	33
10.2.1 Fewer rounds	33
10.2.2 Rotations optimized for speed	33
10.2.3 Minimal padding and finalization flags	33
10.2.5 Fewer constants	34
11. Nodes	35
11.1 Nodes in the Blockchain	35
11.1.2 Roles of nodes in Proof of Work protocol	35
11.2 Roles of nodes in Delegated Proof of Stake protocol	36
11.2.1 Running a Blockchain Node	36
12. Consensus Delegated Proof of Stake:	37
12.1 The Delegated Proof-of-Stake Method	37
12.1.1 Advantages of Delegated Proof-of-Stake:	38
13. Side Chains, Smart Contracts and DApps	39
13.1 Side chains explained	39
13.1.2 Phaeton’ side chains solution	39
13.2 Side chain use cases	40
13.2 Smart Contracts	41
13.2.1 Smart contract use cases:	41
13.3 Decentralized Applications (DApps)	41
14. Sidechain Validation Network (SVN)	43
14. Economics & Fees	44
15. Business info and applications	46
15.1 The team behind Phaeton	46
15.2 Business Objectives	46
Citations:	48



1. Abstract
					
It’s increasingly difficult to create constructive solutions and find real-world outlets for the novel business abstraction layer that stems from blockchain technology. Decentralization, as a key feature of a blockchain, can be transposed to a self-governed societal or organizational group. There is a discrepancy between the degrees of authentic autonomy compatible with technology development in general. The measurement of success among emerging blockchain companies is the value they provide to investors and the community. Two innovations based on the underlying technology recently arose as a prominent factor in the form of Smart Contracts and distributed applications (DApps). To maximize the potential for prosperity in the current market-specific environment, we resort to utilizing the technology to the furthest extent. This implies providing an all-encompassing blockchain product and a blockchain network as a service. We developed a proprietary, custom virtual currency called Phaeton to minimize operational costs, maximize efficiency and mitigate risks. In our view, a virtual currency is a means and not a goal. While developing applications based on blockchain technology, the company engages with the underlying technology and as multifaceted solutions are scarce, offering it as a service is conducive as long as it doesn’t jeopardize the primary applicative use. For expanding the use cases of the network without compromising the security of assets of investors and users, Phaeton uses side chains. The original term of side chains is pegged chains as an attribute of Bitcoin. Additionally, they contribute to maintaining performance for both the main and the side chains. Based on the detrimental effect on the efficiency of the Ethereum network, we isolate the distributed applications in side chains.To protect the application ecosystem from the volatility of the cryptocurrency market, side chain validation and maintenance of consensus over the entire network, we apply the Delegated Proof of Stake(DPoS) consensus protocol. All of the aspects of Phaeton are intertwined and segregated at the same time, adhering to best practices which are described in this paper to their full extent.
					
Keywords: Cryptocurrency, Blockchain, Side Chains, Smart Contracts, DPoS
				
1.1 Introduction

Currency transactions between persons or companies are often centralized and controlled by a third party organization. Making a digital payment or currency transfer requires a bank or a credit card provider as a middleman to complete the transaction. In addition, a transaction incurs a fee from a bank or a credit card company. The same process applies to several other domains, such as games, music, software, etc. The transaction system is typically centralized. All data and information are controlled and managed by a third party organization, rather than the two principal entities involved in the transaction. Blockchain technology has been developed to solve this issue. The goal of Blockchain technology is to create a decentralized environment where no third party is in control of the transactions and data.
		
The blockchain is a distributed database solution that maintains a continuously growing list of data records that are confirmed by the nodes participating in it. The data is recorded in a public ledger, including information about every transaction ever completed. The blockchain is a decentralized solution which does not require any third party organization in the middle. The information about every transaction ever completed is shared and available to all nodes in the blockchain.

This attribute makes the system more transparent than centralized transactions involving a third party. In addition, nodes in the blockchain are all anonymous, which makes it more secure for each node to verify the transactions. Bitcoin was the first application that introduced blockchain technology. Bitcoin created a decentralized environment for its cryptocurrency, where the participants can buy and exchange goods and assets with digital money. However, even though blockchain technology seems to be a suitable solution for conducting transactions by using cryptocurrencies, it still has some technical challenges and limitations that need to be studied and addressed.[1] High integrity of transactions and security, as well as the privacy of nodes, are needed to prevent attacks and attempts to disturb transactions in the blockchain. In addition, confirming transactions in the blockchain requires computational power. It is important to identify which topics have already been studied and addressed in blockchain technology and what are currently the biggest challenges and limitations that require further study.[2]

What is needed is an electronic payment system based on cryptographic proof instead of trust, allowing any two willing parties to transact directly with each other without the need for a trusted third party. Transactions that are computationally impractical to reverse would protect sellers from fraud, and routine escrow mechanisms could easily be implemented to protect buyers. In this paper, we propose a solution to the double-spending problem using a peer-to-peer distributed timestamp server to generate computational proof of the chronological order of transactions. The system is secure as long as honest nodes collectively control more CPU power than any cooperating group of attacker nodes.[3]

While policymakers are concerned about the opportunities and challenges brought about by these technological advances, there is very little guidance provided by economic theory regarding the appropriate usage of these technologies and the optimal design of these systems. This paper attempts to provide an economic theory to help us understand the fundamental economic trade-offs and address relevant policy issues. Most existing models of cryptocurrencies are built by computer scientists who focus mainly on the feasibility and security of these systems. This line of research often ignores the incentives of participants (e.g., the incentives of malicious attackers) and the endogenous nature of key variables (e.g., the real value of cryptocurrencies). More importantly, to study the optimal design of a cryptocurrency system, we need to model from first principles the behaviours of different participants, to derive the equilibrium interactions among these agents and to study the optimal usage of different policy instruments. To this end, this paper develops a general equilibrium monetary model of a cryptocurrency system to study its optimal design. This approach is desirable because the model endogenizes the value of cryptocurrency, and endogenizes the underlying trading activities and mining activities. It also provides a welfare notion for assessing alternative system designs. We will use this model to evaluate the performance of a cryptocurrency system calibrated to Bitcoin transaction statistics. We will study the optimal design of the cryptocurrency system in different settings. Furthermore, we compare the usage of different consensus protocols.
	
Since the creation of Bitcoin in 2009, an introduction of numerous private cryptocurrencies followed. Bitcoin is by far the most successful one. It has been getting a lot of media attention, and its total market value has reached 20 billion USD in March 2017. More importantly, a number of central banks started recently to explore the adoption of cryptocurrency and blockchain technologies for retail and large-value payments. For example, the People’s Bank of China aims to develop a nationwide digital currency based on blockchain technology; the Bank of Canada and Monetary Authority of Singapore are studying its usage for interbank payment systems; the Deutsche Bundesbank has developed a preliminary prototype for blockchain-based settlement of financial assets. Many proponents believe that cryptocurrency and blockchain technology will have a significant influence on the future development of payment and financial systems.

The economic literature on cryptocurrencies is very thin. So far, there are only a few economic models developed to study this new payment technology. These models use different frameworks to address different research questions and often focus on different aspects of cryptocurrencies.
		
Chiu and Wong (2015) apply the mechanism design approach to review several e-money technologies including Bitcoin, PayPal and M-Pesa and identify some essential features of e-money that can help implement constrained efficient allocations. Gans and Halaburda (2013) develop a model of platform management to study platform-specific digital currencies such as Facebook Credits.

Fernảndez-Villaverde and Sanches (2016) model cryptocurrencies as privately issued fiat currencies and analyze whether competition leads to efficiency. Agarwal and Kimball (2015) advocate that the adoption of digital currencies can facilitate the implementation of a negative interest rate policy. Rogoff (2016) suggests subsidizing the provision of digital money to the unbanked in order to phase out paper currency which facilitates undesirable tax evasion and criminal activities. To the best of our knowledge, our work is the first paper that explicitly models the distinctive technological features of a cryptocurrency system (e.g. blockchain, mining, double-spending problems) in an equilibrium monetary model and investigates its optimal design both qualitatively and quantitatively[4].





2. Basic Terminology

Blockchain - A decentralized, public Ledger of Information
Consensus protocol - An irrefutable system of agreement between various devices
dPOS - Delegated Proof Of Stake consensus protocol
Nodehash - Versioning scheme and update mechanism 
SHA256 - Cryptographic Encryption Algorithm
Hashing - Takes an input and convert into a cryptographic fixed output.
Seed - it kicks off a random number 
Digest - Ensures the security and integrity of the data
Master node - Genesis Block of a blockchain.
Delegate - Collecting transactions across the network into blocks
P2P – Peer-to-Peer protocol
SVN - Side chain validation network


3. Cryptocurrencies: Overview

3.1 Bitcoin & Ethereum: Basics				
			
Bitcoin’s three main technical components: transactions (including scripts), the consensus protocol, and the communication network. Bitcoin is exceedingly complex. Our goal is to present a system with sufficient technical depth which the literature on Bitcoin lacks. The evaluation and systematized proposal of changes are made insightful by “decoupling” concepts that may be changed independently benefits from of our three-component breakdown. The idea of utilizing its enablement of technology to develop applications beyond currency has been receiving increasing attention. In particular, the public and append-only ledger of transactions (the blockchain) and the decentralized consensus protocol that Bitcoin nodes use to extend it. The archetypal implementation of smart contracts is Ethereum, a platform rendering them in a Turing-complete language. The consensus protocol of Ethereum ensures that all and only the valid updates to the contract states are recorded on the blockchain, thus ensuring their correct execution. [5]
	
Besides Bitcoin and Ethereum, a remarkable number of alternative platforms have flourished over the last few years, either implementing cryptocurrencies or Smart Contracts in some form. For instance, the number of crypto-currencies hosted on coinmarketcap.com has increased from 0 to more than 600 since 2012; the number of Github projects related to blockchains and smart contracts has reached, respectively, 2,715 and 445 units. In the meanwhile, ICT companies and some national governments have also started dealing with these topics with significant investments. [6]

Also, there are some identified technical challenges and limitations of blockchain technology. Seven technical challenges and limitations for the adoption of blockchain technology in the future:

• Throughput: The potential throughput of transactions in the Bitcoin network is currently at a maximum of 7tps (transactions per second). For comparison, other transaction processing networks have the following throughput: VISA (2,000tps), Twitter (5,000tps). When the frequency of transactions in the blockchain increases to a similar level, the throughput of the blockchain network needs to be improved.
	
• Latency: To achieve sufficient security for a Bitcoin transaction block, it currently takes roughly 10 minutes to complete one transaction. To achieve efficiency in security, more time has to be spent on a block, because it has to outweigh the cost of double-spending attacks. Double-spending is successful spending of money more than once. In Bitcoin, each transaction is verified before appendment to the blockchain for protection from double-spending, acting as insurance from the previous spending of inputs for a transaction. Currently, this makes latency a big issue in blockchain technology. Making a block and confirming the transaction should happen in seconds while maintaining security. Completing a transaction in VISA, for example, takes only a few seconds which is a huge advantage compared to the blockchain.

• Size and bandwidth: At the moment, the size of the blockchain in the Bitcoin network is over 50,000MB (February 2016). The Bitcoin community assumes the size of one block is 1MB and the creation of a new block happens every ten minutes. Therefore, there is a limitation in the number of transactions that can be handled (on average 500 transactions in one block). If the Blockchain needs to control more transactions, the size and bandwidth issues have to be solved.

• Security: The possibility of a 51% attack persists in current blockchain technology. In a 51% attack, a single entity would have full control of the majority of the network’s mining hash-rate and would be able to manipulate the blockchain. To overcome this issue, more research on security is necessary.
• Wasted resources: Mining Bitcoin wastes huge amounts of energy ($15million/day). The Proof-of-Work effort causes the waste of resources. There are some alternatives in industry fields, such as proof-of-stake, DPOS (Delegate Proof of Stake). With Proof-of-Work, the probability of mining a block depends on the work done by the miner. However, in Proof-of-Stake, the resource that matters is the amount of stake a miner holds. For example, someone holding 1% of the Bitcoin blockchain could mine 1% of the “Proof-of-Stake blocks”. The issue with wasted resources needs to be solved to have more efficient mining in the blockchain.

• Usability: The Bitcoin API for developing services is difficult to use. There is a need to develop a more developer-friendly API for the blockchain. This is comparable to REST APIs.

• Versioning, hard forks, multiple chains: A small chain that consists of a small number of nodes has a higher possibility of a 51% attack. Another issue emerges when chains are being split for administrative or for versioning purposes.[7]

Ethereum, taken as a whole, can be viewed as a transaction-based state machine: It begins with a genesis state and incrementally executes transactions to morph it into some final state. It is this final state which we accept as the canonical “version” of the world of Ethereum. The state can include information such as account balances, reputations, trust arrangements, and data pertaining to information of the physical world; in short, anything that can currently be represented by a computer is admissible. Transactions thus represent a valid arc between two states; the ‘valid’ part is important—there are far more invalid state changes than valid state changes. Invalid state changes might e.g. be things such as reducing an account balance without an equal and opposite increase elsewhere. 
	
A valid state transition is one which comes about following a transaction. Formally:
	
σt+1 ≡ Υ(σt, T)
Where Υ is the Ethereum state transition function


In Ethereum, Υ, together with σ are considerably more powerful than any existing comparable system; Υ allows components to carry out arbitrary computation, while σ allows components to store arbitrary states between transactions.

Blocks are the result of collating transactions; blocks are chained together using a cryptographic hash. Blocks function as a journal, recording a series of transactions together with the previous block and an identifier for the final state (though do not store the final state itself—that would be far too large). They also punctuate the transaction series with incentives for nodes to mine. This incentivisation takes places as a state transition function, adding value to a nominated account.

Mining is the process of dedicating effort (working) to bolster one series of transactions (a block) over any other potential competitor block. The achievement depends on cryptographically secure proof. [8]
	
3.2 Bitcoin & Ethereum: Differences	
3.2.1 Use Case: Ethereum

Transaction format: A transaction contains an array of inputs and an array of outputs. The entire transaction is hashed using SHA-2564 and this hash eventually serves as its globally unique transaction ID. Transactions are represented using an ad hoc binary format; each output contains an integer value representing a quantity of the Bitcoin currency. The precision of this value limits the extent to which units of the currency can be subdivided; the smallest unit is called a satoshi. By convention, 108 satoshis are considered the primary unit of currency, called one “bitcoin” and denoted B, BTC or XBT. Each output also has a short code snippet (in a special scripting language) called the scriptPubKey which represents conditions under which that transaction output is redeemable, that is, included as an input in a later transaction.

Transaction scripts: Typically, the scriptPubKey specifies the hash of an ECDSA public key and a signature validation routine. This is called a “pay-to-pub-key-hash” transaction and the entire redeeming transaction must be signed using a key with the specified hash. The vast majority of Bitcoin transactions are pay-to-pub-key-hash while the system is often described as this being the only possibility, although other transaction types are possible. The scripting language is an ad hoc, non-Turing-complete stack language with fewer than 200 commands called opcodes. They include support for cryptographic operations—e.g., hashing data and verifying signatures. Like the transaction format, the scripting language is only specified by how the Bitcoin blockchain implements it. Transaction inputs refer to previous transactions by their transaction hash and the index of the output within that transaction’s output array. They must also contain a code snippet which “redeems” that transaction output called the scriptSig. To successfully redeem a previous transaction, the scriptSig and scriptPubKey, both must execute successfully, one after the other, using the same stack. For pay-to-pubkey-hash transactions, the scriptSig is simply a complete public key (with the correct hash) and a signature.
	
Conservation of value: In addition to the requirements that each transaction input should match a previous transaction output and that the two scripts execute successfully, transactions are only valid if they satisfy the fundamental constraint that the sum of values of all transaction outputs is less than or equal to the sum of the values of all inputs.[9]
	

3.2.3 Use Case: Bitcoin
	
The account state comprises the following four fields:

Nonce: A scalar value equal to the number of transactions sent from this address or, in the case of accounts with associated code, the number of contract-creations made by this account. For an account with an address [a] in state σ, this would be formally denoted σ[a]n.

Balance: A scalar value equal to the number of Wei* owned by this address. Formally denoted σ[a]b.

StorageRoot: A 256-bit hash of the root node of a Merkle Patricia tree(trie) that encodes the storage contents of the account (a mapping between 256-bit integer values), encoded into the trie as a mapping from the 256-bit integer keys to the RLP-encoded 256-bit integer values. The hash is formally denoted σ[a]s.

CodeHash: The hash of the EVM code of this account—this being the code that gets executed should this address receive a message call; it is immutable and thus, unlike all other fields, cannot be changed after construction. All of such code fragments are contained in the state database under their corresponding hashes for later retrieval. The formal denotation of this hash is σ[a]c thus the code may be denoted b, given that KEC (b) = σ[a]c.[10]

4. Consensus Mechanisms:    

4.1 Mining 

To understand the consensus mechanism of the Bitcoin system, we first have to discuss the role of a miner. A miner collects pending Bitcoin transactions, verifies their legitimacy, and assembles them into what is known as a “block candidate.” The goal is to earn newly created Bitcoin units through this activity. The miner can succeed in doing this if he or she can convince all other network participants to add his or her block candidate to their copies of the Bitcoin blockchain.

Bitcoin mining is a permissionless process. Anyone can become a miner by downloading the respective software and the most recent copy of the Bitcoin blockchain. In practice, however, there are a few miners who produce most of the new generally accepted blocks. The reason is that competition has become fierce and only large mining farms with highly specialized hardware and access to cheap electricity can still make a profit from mining.
    			
For a block candidate to be generally accepted, it must fulfill a specific set of predefined criteria. For instance, all included transactions must be legitimate. Another important criterion is the so-called “fingerprint” of the block candidate. A miner obtains this fingerprint by computing the block candidate’s hash value using the hash function SHA256.
	
For example, we will take a look at the hash value for the text, “Federal Reserve Bank of Saint Louis.” The fingerprint of this text, which was calculated using the hash function SHA256, is

72641707ba7c9be334f111ef5238f4a0b355481796fdddfdaac4c5f2320eea68.

Now notice the small change in the original text to “Federal Reserve Bank of Saint Louis.” It causes an unpredictable change of the fingerprint, which is noticeable in the corresponding new hash value:
            
423f5dd7246de6faf8b839c41bf46d303014cffa65724ab008431514e36c4dba.

This characteristic is employed in the mining process as follows: For a block candidate to become accepted by all miners, its fingerprint must possess an extremely rare feature; the hash value must be below a certain threshold value—that is, it must display several zeros at the beginning of the fingerprint. An example of a fingerprint of a block added to the Bitcoin Blockchain in 2010 is given in the following example:
Block #69785 (July 23rd, 2010, 12:09:36 CET)
0000000000	14243
293b78a2833b45d78e97625f6484ddd1accbe0067c2b8f98b57995

There are M miners performing mining activities to update the public ledger in the night trading sessions n = 0,..., N¯. In each session, miners perform a costly computational task with a random success rate by investing computing power with a qn value. This task is called the proof of work (PoW). As specified by the Bitcoin protocol, if the computational power of miner i in session n is qn(i), then the probability that a particular miner j will be the first one to solve the proof-of-work problem is given by:


In other words, the probability of winning the mining game is proportional to the fraction of computational power owned.
    
Miners are continuously trying to find block candidates that have a hash value satisfying the above-mentioned criterion. For this purpose, a block includes a data field (called the nonce) that contains arbitrary data. Miners modify this arbitrary data in order to gain a new fingerprint.
    	
These modifications do not affect the set of included transactions. Just as with our example, every modification results in a new hash value. Most of the time, the hash value lies above the threshold value, and the miner discards the block candidate. If, however, a miner succeeds in creating a block candidate with a hash value below the current threshold value, they broadcast the block candidate as quickly as possible to the network. All the other network participants can then easily verify that the fingerprint satisfies the threshold criteria by computing it themselves.[11]

The consensus among miners is that every miner who receives a block candidate with a valid fingerprint adds it to their own copy of the Bitcoin blockchain. From a game theory perspective, Nash equilibrium is a strategic economic model where all miners add valid blocks to their own copies of the Bitcoin blockchain. 
	
Mining is increasingly expensive, as the computations use large amounts of electricity and are dependent on highly specialized hardware. Moreover, valid block candidates can be found only through a trial-and-error procedure. The consensus mechanism is therefore called “Proof of Work.” If a miner finds a valid fingerprint for a block candidate, then this is proof that he or she has, on average, performed a large number of costly computations. Adding false information (e.g., illegitimate transactions) to a block candidate would render the block candidate invalid and essentially waste all the computations. Finding a valid fingerprint is, therefore, proof that the miner helped to maintain the Bitcoin system. [12]

With Phaeton, we use Delegated Proof of Stake (DPoS) as its consensus protocol. Delegates elected by the stakeholders generate all of the blocks within the system. The stakeholders, in this case, are all entities holding PLKX tokens. The total number of delegates is fixed at 101.  Each stakeholder can vote for up to 101 delegates, and the weight of the vote depends on the amount of PLKX that the stakeholder possesses. Any stakeholder can vote for a delegate using a vote transaction.

A consensus protocol is a key aspect of any blockchain system. It serves a vital purpose in a system comprised of countless nodes where all nodes need to agree on the integrity of the data appended to the blockchain. The term ‘consensus’, in this context, means that the nodes on the network agree on the same state of a blockchain, essentially making it a self-auditing ecosystem. This is an absolutely crucial aspect of the technology, carrying out two key functions. Firstly, consensus protocols allow a blockchain to be updated, while ensuring that every block in the chain is true as well as keeping participants incentivized. Secondly, it prevents any single entity from controlling or derailing the whole blockchain system. The aim of consensus rules is to guarantee a single chain is used and followed.[13]
	
4.2. Consensus layer support
                    
4.2.1 The linked list data pointer structure
                    
In order to construct our protocol, we rely on the same linked list data structure used by Proof-of-Proof-of-Work (PoPoW)[14]. This is an additional hash-based data structure that we propose to include in the header of each block. The linked list data structure is a skip-list that makes it efficient for a verifier to process a sparse subset of the blockchain, rather than only consecutive blocks. 
    	
Valid blocks satisfy the Proof-of-Work condition: id ≤ T, where T is the mining target. Throughout this work, we simplify by assuming that T is constant. Some blocks will achieve a lower id. If id ≤ T/2μ, we state that the block is of level μ. All blocks are level 0. Blocks with level μ are called μ-superblocks. The μ-superblocks for μ > 0 are also (μ − 1)-superblocks. The level of a block is given as μ = ⌊log(T ) − log(id(B))⌋ and denoted to level(B). By convention, for Gen we define the following values: id = 0 and μ = ∞.
                    	
Note that in a blockchain protocol execution it is expected that half of the blocks will be level 1, 1/4 of the blocks will be level 2, 1/8 will be level 3 and 1/2μ blocks will be level μ. In expectation, the number of superblock levels of a chain C will be Θ(log(C)). Figure 2 illustrates the blockchain superblocks starting from level 1 and progressing up to level 4 in case these blocks are distributed exactly according to expectation. Herein, each level contains half the blocks of the level below.
                    
In our protocol, the verifier must scan at roughly one level at a time. To enable this, instead of just the previous block, the linked list data vector also points to the most recent preceding block of every μ level. Genesis is an infinite set of values and hence a pointer to it is included in every block at the first available index within the linked list data structure. The number of pointers that need to be included per block is expected to hold the value of log (|C|).
                    
Figure 2 illustrates the blockchain superblocks starting from level 1 and going up to level 4 in case these blocks are distributed exactly according to expectation. Note that each level contains half the blocks of the level below.					
		 	 	 		
			
				
					
Fig. 2. The blockchain hierarchy. Higher levels have achieved a lower target (higher difficulty) during mining.
					
The algorithm for this construction is borrowed from and shown in Algorithm 1.
The interlink data structure turns the blockchain into a skip list-like data structure.
The updateInterlink algorithm accepts a block B′, which has a predefined linked list data structure. The function evaluates the linked list data structure which needs inclusion as part of the next block. It copies the existing interlink data structure and then modifies its entries from level 0 to level (B′) to point to the block B′.    
4.2.2 Traversing the blockchain

As we now have extended blocks containing multiple pointers to previous blocks, if we omit certain blocks from a chain we obtain a subchain, as long as the sequence maintains the blockchain property where each block includes a pointer to its previous block.

Blockchains are sequences, but it is more convenient to use set notations for some operations. Specifically, the meaning of B ∈ C; C1⊆ C2 and ∅ is obvious. C1 ∪ C2 is the chain obtained by sorting the blocks contained in both C1 and C2 into a sequence (this might not always be defined).  We will freely use the set builder notation { B ∈ C : p ( B ) } .C1 ∩ C2 is the chain { B : B ∈ C1 ∧ B ∈ C2 }. In all cases, we must maintain the blockchain properties. The lowest common ancestor is LCA (C1, C2) = (C1 ∩ C2)[−1]. If C1 [0] =C2 [0] and C1 [−1] = C2 [−1], we state that the chains C1, C2 span in the same block range. We will promptly clarify that it is useful to construct a chain containing only the superblocks of another chain. Given C and level μ, we define the upchain C↑μ as { B∈C : level ( B ) ≥ μ }. A chain containing only μ-superblocks is called a μ-superchain. It is also useful to go back to the regular C chain, given a μ-superchain C′. Given that chains C′ ⊆ C, we define the downchain C′↓C  as C [ C′ [0] : C′ [−1]]. C is the underlying chain of C′. The underlying chain is often contextually implied, so we will simply note C′↓.
By the above definition, the C↑ operator is absolute: (C↑μ)μ+i = C↑μ+i. Given a set of consecutive rounds S = {r,r+ 1,···,r+j} ⊆ N, we define CS = { B∈C:B was generated during S}.

4.2.3 Non-interactive blockchain suffix proofs
In this section, we modify the PoPoW scheme introduced in KLS to make it non-interactive. With foresight, we caution the reader that the non-interactive construction we present in this section is insecure because its base layer PoPoW scheme is also insecure. A very small patch will allow us to later modify our construction to achieve security.
    
Their scheme only allowed proving suffix predicates, predicates that pertain to the suffix of the blockchain. We continue along those lines to give our NIPoPoW construction which allows proving certain predicates Q of the chain C. Among the predicates which are stable, in this section, we limit ourselves to suffix sensitive predicates (similar to the previous work which did not make this distinction explicit). We extend the protocol to support more flexible predicates (such as transaction inclusion, as needed for our applications)

Definition 5 (Suffix sensitivity)
A chain predicate Q, called k-suffix sensitive if for all chains C, C′ with |C| ≥ k and |C′| ≥ k such that if C[−k :] = C′ [−k :] we derive that Q ( C ) = Q ( C′ ).
Notice that if a predicate Q is suffix-sensitive, then its value must be determined only by the k-suffix of the chain.
4.2.4 Example
In general, our applications will require predicates that are not suffix-sensitive. However, as an example, we take into consideration the predicate “an Ethereum contract at address C has been initialized with code h at least k blocks ago” where h does not invoke the self-destruct opcode. This can be implemented in a suffix-sensitive way because, in Ethereum, each block includes a Merkle Trie over all of the contract codes, unchangeable after initialization. This predicate is thus both monotonic and k-stable.[15]
		
4.2.5 Exact probabilities of covert forkability for explicit values of n
For comparison with the general use case, we computed the probability that a string drawn from the binomial distribution is covertly forkable. These results are presented in Figure 9. (Note that these probabilities are simply appropriate evaluations of the cumulative density function of the binomial distribution.) We present the analogous results for the general use case in Figure 3.
    
 

	


Figure 3: Graphs of the probability that a string drew from the binomial distribution is
covertly forkable. Graphs for string lengths n = 500, 1000, 1500, 2000 are shown with parameters. 40, 41,....,49, 50.(16)

5. P2P Network

The Peer to Peer(abbr. P2P) networking model is an essential component of blockchain technology, contributing to both stability and security. This segment of the technical paper gives a general overview of P2P and the advantages that its decentralized character offers over the standard networking schemes that prevalent at present. 
       
Peer to Peer infrastructure (P2P infrastructure) is subject to wide adoption as a network infrastructure where all users run computing instances referred to as nodes. In P2P, each node has the ability to provide and receive the same services. As opposed to standard network orchestration, where a single server provides services to multiple users called clients, a P2P network works in a divergent manner.

The quality of a peer to peer network which makes it suitable for blockchain technology is the equality of nodes, where the service providers and receivers are interchangeable. The prevalent networking model functions in a less interactive way. A central server or a server cluster provides services to a multitude of users, such as the Hypertext Transfer Protocol (HTTP) which is the basis of the world wide web. The participants in the centralized networking model have predefined roles: the servers deliver information upon a user's request.

Peer to Peer networking is an essential component of the Phaeton network. The P2P connection protocol provides the necessary architecture to reach a consensus on the network, validate transactions and propagate blocks.

Within a Peer to Peer network, nodes make use of and maintain the infrastructure of the network at the same time, albeit contributions are completely on a willing basis. The users of a P2P network, i.e. peers have equivalent permissions and responsibilities and are commonly called nodes. Peers distribute a part of their computational capability, storage or networking throughput to other users in accordance with the regulatory blockchain protocol, eliminating the requirement of a central coordinating point, such as a server.
    
Nodes in the P2P network are equal by definition but they differ in terms of the functions in the blockchain environment. For example, a node that contains the entire ledger is a full node, while one that adds blocks and validates transactions is a called a miner. The distribution of tasks contributes to dependable storage of information and their integrity. 

On a Peer to Peer network, as opposed to a classic networking model where the server provides the information to users, data is distributed across the nodes. There is a continuous process of appending and transmitting data among all constituents of a blockchain. Whereas in a centralized environment, the performance of data distribution slows down due to the overload of requests from adding clients, the blockchain network becomes more efficient with additional nodes entering the network.

The two major advancements that the development of a Peer to Peer networks have brought forth are security and dependability. As there is no central place of storage, the probability of compromising the integrity of data,  it's misuse or destruction is much lower.

The distributed nature of a P2P network implies that there is no need for a controlling party and no participant can abuse their authority can impose their interest. If all security standards are up to par, the information belongs solely to the user. Decentralization is an advancement in comparison with the schemes that are predominant today. Social networks usurp information of participants as their sole proprietor and financial scenarios, a bank has the final word on when they distribute assets and the authority to suspend the activity of an account if it's in their own interest. 

With the development of Peer to Peer networks and their implementation in the blockchain technology novel scheme of exchanging information is brought forth. The blockchain eliminates the necessity of an authoritative mediator, enabling people to transmit any type of data solely between the parties involved in a protected, distributed environment without a central authority.

Despite monitoring of communication between peers on the network, the information is encrypted with algorithms used by organizations dealing with data of the highest degree of sensitivity. The purpose of viewable information is for dispute resolution or detection of illegal activities. 
 
5.1 Architecture

The nodes in the Phaeton network utilize JSON objects. The transaction data and the blocks are compressed. The Phaeton code operating in all peers in the Phaeton network utilizes remote procedure calls (RPCs) and events to broadcast the JSON objects, namely transactions and blocks, to the rest of the nodes. The RPCs and events are also communicated as JSON objects with additional fields and relayed to the Phaeton application to provide it with information used to choose the method for processing the transmitted object. In order to effectively transmit these JSON objects to the other peers, Phaeton uses WebSockets via the SocketCluster Framework.

5.1.1 System Headers

Every time a Phaeton node communicates with a peer on the Phaeton network, it adds a system header to the message. The system headers are used to identify full nodes and provide basic information about the software running on the system.

For this purpose, system data is used to generate the following JSON object:


    {
      "os":"darwin16.3.0",
      "version":"0.6.0a",
      "port":7000,
      "height":1574654,
      "nethash":"da3ed6a45429278bac2666961289ca17ad86595d33b31037615d4b8e8f158bba",
      "broadhash":"c7e0902a7016205d456a427edda2b09f4b875f98ef40a224018a0274347146ac",
      "minVersion":">=0.5.0"
    }

5.1.2 Block Propagation

Block propagation plays an integral part in the Phaeton network. As it is an essential structural component, if it wasn't for block propagation, the blockchain as a whole becomes inoperable. A single node creates a block and in a decentralized network, the data transmission to all nodes for the establishment of consensus is a must. Upon the creation of a new block, the node broadcasts a message to 25 blocks randomly chosen peers. The blockchain replicates the process by forwarding the message to the next batch of 25 random peers, and so forth. To avoid saturating the network with data broadcasts, we cap the turn over at 3 and blocks acquired by a satisfactory total of hosts are exempt from broadcasting.


5.1.3 Transaction Propagation

Transferring a transaction from a single node to all nodes on the network is a prerequisite for including them in blocks. Up to 25  transactions are sequentially pulled from the transactions pool, followed by subjecting them to the validation method. The rest of the nodes accept the transaction broadcast in a JSON bulk object. In accordance with the characteristics of the transaction,  it's explainable as a collection of objects. All nodes on the blockchain accept the broadcasted bulk object consistently, presently defined as every 5 seconds. During the interval, the bulk object amasses added transactions from the blockchain (25 at most). Additionally, the bulk object has a broadcast limit to avoid network congestion. At present, the broadcast limit is exercised as 3, implying the peers on the network relay every bulk object at a maximum of 3 hops. 
	

5.1.4 Transaction Pool

The transaction pool provides the Phaeton network with a robust solution for preserving unconfirmed transactions that have overflown into the next block. As described in blocks, each block can only include 25 transactions, the transaction pool allows up to 1.000 multi-signature transactions and another 1.000 for the other transaction types to remain queued for the next block(s). The transaction pool can be thought of as a memory pool, keeping transactions until they are ready to be signed into a block. The second usage of the transaction pool is to provide a mechanism for propagating transactions. When a node prepares a transaction bundle, it draws up to 25 transactions from the pool and broadcast them to the network. In order to keep the transaction pool tidy, all transactions have a time to live assigned to them. We defined the time to live as 10800 seconds or 1080 blocks. The final use for the transaction pool is to house transactions with pending signatures. Like unconfirmed transactions, these transactions will expire and dissipate from the pool as a container based on the lifetime specified when the transaction is first received.(17)
5.1.5 Key Pair

A key pair comprises of a private key and a public key. A private key string is a combination of numbers and letters that only the holder of the key is familiar with. The public key, obtained from the private key has a purpose of validating the private key belonging to the holder while withholding entry to their private key. Elliptic curve cryptography is a method of creating cryptographically secure key pairs.

The process used to generate the key pair operates in the following manner:

When a user creates an account, it entails generating BIP39 mnemonics (the passphrase). This passphrase is hashed using The BLAKE2B hash function into a 256-bit string. This hash is subsequently used as a seed in Ed25519 to generate the private key string and derive its public key. The public key serves as part of the transaction and enables the nodes that receive the transaction to verify the validity of the signature using a key pair. This provides effective security for both the user and the network since the key string is known only to the user and the key pair validates the signature.
5.1.6 Second passphrase
    
Phaeton also offers the option of an additional layer of security. For using these specific transactions, the user can register a second passphrase. The second passphrase is associated with the account.(18) This process requires all subsequent transactions to be additionally signed using the second passphrase for the transaction to be considered valid. The process of generating the second key pair is the same as the one for the initial key pair.
5.1.7 Multisignature
Phaeton supports multi-signature accounts as another security system for users requiring a higher degree of security. A multi-signature account is an account that requires multiple keys to authorize a transaction. Any user can enable multi-signature on their account by issuing a special transaction specifying a group of n keys and the minimum number of m signatures required to authorize a transaction.(19) Upon enabling this feature, it is mandatory that for processing any transaction originating from that account it must be signed by at least m out of the n keys for.
5.1.8 Address

An address or the wallet ID is derived from the public key. The public key is hashed using BLAKE2B, at which point the first 8 bytes of the hash are reversed. The account ID is the numerical representation of those 8 bytes, with the ’L’ character appended at the end. The following figure is the representation of an address and its associated account details.

	 {
	    "address": "16009998050678037905L",
	    "unconfirmedBalance": "0",
	    "balance": "0",
"publicKey":"73ec4adbd8f99f0d46794aeda3c3d86b245bd9d27be2b282cdd38ad21988556b,
	    "unconfirmedSignature": 0,
	    "secondSignature": 0,
	    "secondPublicKey": null,
	    "multisignatures": [],
	    "u_multisignatures": []
	  }


6. Data Compression

One of the underdeveloped aspects of Blockchain technology is data storage. As a blockchain grows by adding transaction and blocks, nodes need to store more information and new nodes on the network require a large chunk of information. That issue is addressed by data compression, reducing the size of the message through a compression algorithm. The original data is transformed through the compression method's codeword. 

Additionally, the encryption algorithms that secure the content of transmitted information reduce the performance of blockchain networks.   They permute the plaintext data to ciphertext which are encoded using an encryption key. Both of these operations are resource-demanding. By combining compression and encryption into one process, the Phaeton network gains efficiency and operates at a high level.

Phaeton utilizes the latest cryptography technology to enable fast transaction rates. Elliptic curve cryptography is the method of choice, as it provides the highest degree of security across the scheme of operations in the network. Edwards-curve Digital Signature Algorithm (EdDSA) used in Phaeton is the fastest scalable hashing scheme that complies with our strict security standards. 


7. Cryptography
7.1 What is Cryptography?
A lot of people use cryptography on a daily basis without realizing it. Many popular messaging apps use encryption. It is also one of the core features of blockchain technology. In this segment, we will provide a simple yet detailed explanation of cryptography, both symmetric and asymmetric key cryptography.[20] 

Cryptography is the method of disguising and revealing, otherwise known as encrypting and decrypting information through complex mathematical calculation. Nobody but the intended recipients can view the encrypted information. The method involves taking unencrypted data, such as a piece of text, and encrypting it using a mathematical algorithm, commonly known as a cipher. This produces a ciphertext, a piece of information that is completely useless and nonsensical until decrypted. This method of encryption is known as symmetric-key cryptography.

An early example of cryptography was the Caesar cipher, used by Julius Caesar to protect Roman military secrets. By substituting each letter in messages with the letter 3 spaces to the left in the alphabet, this method was essentially the key that encrypted the message. Caesar’s generals knew that to decode the letters they only had to shift each one to the right by three, while the information remained safe if intercepted by Caesar’s enemies. Modern cryptography works on the same level, albeit with far greater levels of complexity.
    	
The code base for most ciphers is an open source project, meaning their code is available to anyone to examine. The most widely used cipher in the world is called AES, it's free for anyone to use and its code is available to the public eye. As such, after conducting an extensive study, to date, no vulnerabilities have been discovered. This cipher is also used by the NSA and the United States Intelligence Agency, as the tool of choice for encrypting information. Therefore, the security of information recorded on a blockchain is as secure as some of the most sensitive secrets in the world.
	
Blockchain technology utilizes cryptography as a means of protecting the identities of users, ensuring transactions are done safely and securing all information and data of value. It provides complete confidence for anyone using blockchain technology that by recording something on a blockchain, it is done legitimately and in a manner that preserves security.
Despite being founded upon a similar framework, the type of cryptography used in blockchain technology, namely public-key cryptography, it is far more suitable to the functions associated with the technology than symmetric-key cryptography.

7.2 What is Public-Key Cryptography?

Public-key cryptography, i.e. asymmetric cryptography, is an advancement from symmetric-key cryptography. It permits data transmission with the help of a public key, for safe distribution to anybody where the predetermined receivers can decipher the data.
            
Instead of utilizing a single key for enciphering and deciphering, the way that symmetric key cryptography functions, individual keys are applied (a combination of a public key and a private key). 

The mixture of a user's public key and private encipher the data, while the receiver's private key and issuers' public key decipher it. Finding out the way a private key and the public key relate is beyond the realms of possibility. This enables a participant to issue the public key to anybody with the assurance that his or her private key is inadmissible. The issuer enciphers the data, with the guarantee that the only the recipient can decipher them.

Public-key cryptography generates a digital signature, protecting the soundness of information displayed to the receiver. This procedure mixes a participant private key with the information they want to put a stamp with an encryption method. 
    
Because the information comprises the digital signature in part, the network identifies it as false if any portion of it was subject third-party interference. Altering the smallest chunk of the information transmutes the signature as a whole, rendering it incorrect and unusable. The process enables blockchain technology to warrant the integrity, validity and correctness of any information stored on it. It is digital signatures that secure the data recorded on a blockchain from interference.

7.2.1 Elliptic Curve Cryptography

Phaeton uses ECC (Elliptic Curve Cryptography) to sign digital assets and to ensure the security of every transaction. It is possible to calculate the public key from a known private key. The Bitcoin network fully exercises ECC, widely regarded as the most powerful asymmetric algorithm given the key length.
    	
Elliptic curve cryptography (ECC) is an approach to public key cryptography based on the algebraic structure of elliptic curves over finite fields.[21]  ECC requires smaller keys compared to non-ECC cryptography (based on plain Galois fields) to provide equivalent security. Elliptic curves are applicable for key agreements, digital signatures, pseudorandom generators and other tasks. Indirectly, their purpose is encryption by combining the key agreement with a symmetric encryption scheme.
		
8. Digital Signatures				
8.1 What is a Digital Signature?

In a way, digital signatures do what their names suggest: they provide validation and authentication in the same way signatures do, in digital form. In this segment, we will discuss how they work as well as how multi signatures (multisigs) can be used to add an extra layer of security.[22]
	
Digital signatures are one of the main aspects of ensuring the security and integrity of the data that recorded onto a blockchain. They are a standard part of most blockchain protocols, mainly used for securing transactions and blocks of transactions, transfers of sensitive information, software distribution, contract management and any other cases where detecting and preventing any external tampering is important. Digital signatures utilize asymmetric cryptography, meaning that information is safely shareable with anyone, through the use of a public key.

Digital signatures provide three key advantages of storing and transferring information on a blockchain. First of all, they guarantee integrity. Theoretically, encrypted data are subject to altering upon sending without being seen by a hacker. However, if this happens, the signature would also change, thus becoming invalid. Therefore, digitally signed data is not only safe from the eyes of onlookers but in the case of tampering, reveal if it has been tampered with, cementing its incorruptibility.
	
Digital signatures not only secure data but also the identity of the individual sending it. Ownership of a digital signature is always bound to a certain user and as such, one can be sure that they are communicating with whom they intend to.

For example, even the most proficient hacker could not fake anyone's digital signature as a means of convincing someone else to send money; it is simply mathematically not within the realms of possibility. Therefore digital signatures not only guarantee the integrity of communicated data but also the identity of the individual communicating it.

Finally, the fact that private keys link to individual users gives digital signatures a quality of non-repudiation. This means that if a user signs something digitally, it can be legally binding and in entirety associated with that individual. As previously explained, this is heavily dependent on there being no doubt that the private key that signed the data was not compromised, used or seen by anyone other than its owner.

Digital signatures are unique to the signer and created by utilizing three algorithms:
A key generation algorithm, providing a private and public key
A signing algorithm that combines data and private key to create a signature
An algorithm that verifies signatures and determines whether the message is authentic or not based on the message, the public key and signature
    	
The key features of these algorithms are:
Making it absolutely impossible to work out the private key based on the public key or data that it has encrypted
Ensuring the authenticity of a signature based on the message and the private key, verified through the public key
8.1.1 Multisignature

Multisignature, abbr. multisig is a digital signature method addressing the need of multiple signees for authorization of transactions. A shared signature is more effective at all times than a group of singular digital signatures.
        
Multiple cryptocurrencies utilize multisigs for enhancing security and as a means for distributed decision making. This feature of sending PLKX transactions contributes to system safety, both from cyber-attacks or anyone who might have exploited a Phaeton user’s account and obtained their passphrase.
The total of possible cosigners and the necessary number of signatures is agreed upon at the start during the creation of the address. This is not the case with Phaeton, where you can convert your account into a multisig account at any time.  
8.1.2 Can one person use a multisig?

The feature of a multisig enables a user to keep two distinct keys kept at two segregated points. The two keys are needed to complete any transfer which supplies an additional security level. For someone to get an entry to your assets, they will need to acquire the two keys together, increasing the level of difficulty to near zero point chance of success as long as both keys adequately protected.

For instance, a multi-signature makes it possible to conduct a 2-of-3 collateral transaction which implies that to conduct a transfer two out of three participants have to hold the same notion. An exemplary event is an interest-bearing account of a minor where a met condition of a settlement between the guardians gives permission to receive a payout. Alternatively, the guardians are able to make an important choice if they both settle on the matter at hand. 

Multisignatures can be developed in countless combos (4-of-4, 3-of-5 collateral transaction accounts, etc), making them equally suitable for both tinier transfers, and transfers conducted by big business. For instance,  shareholder electees can build 7-of-11 collateral system built.

Digital signatures constitute an essential component as a warranty for information on a blockchain, while nodes comprise the bedrock, performing the role of an underlying layer in the network.  
9. Hashing

Hashing is one of the fundamental processes in Blockchain technology. It warrants that all input data being processed by the cryptographic algorithm are unique providing a trustworthy environment in a trustless system. It eliminates the potential of the same transaction being validated and recorded in the Blockchain ledger.
The algorithm that is used to transfer data utilizes its cryptographic capacity to create an encrypted output out of any information derived by a client on the network. In case when the transaction is deemed legitimate, the output is recorded in the Blockchain and is also used to constitute the link between blocks which is essentially a hash output.
As the Blockchain grows in size, the computation can require random data to be combined with the input for the hash to be unique while keeping in mind future transactions will follow.
9.1 Hashing as a security layer
Taking into account the value of the data in the ledger, the hashing process has to secure the information itself to the degree that neither parameter of the input can be reverse engineered. This means the extent of the objects in the Blockchain can’t be derived from the hash value itself.

The cryptographic algorithm has to ensure a number of qualities in the Blockchain:
-        A different hash value for any distinct data
This is crucial for both the security and the cohesive nature of the Blockchain.
-        The digest hash value needs to be equivalent for the same input
The purpose is quality assurance of the algorithm itself as well as for identifying double-spending.
-        The faster a secure hash is produced, the better
As the purpose of the hashing process is transactions, the speed of the Blockchain algorithm adds to its value
-        Hash values need to relate but can’t be traced back to input data itself

Hashing speed and security are the breakthrough aspects of Blockchain technology. A similar input can’t produce hashes where the initial information can be compared for the purpose of decrypting it.

The integrity that hashing provides is essential to Blockchain security. Another purpose of the hashing algorithm, which is open source is the fact that the message which is received can be validated by running the algorithm by the recipient which should produce the same hash value.
                                            	
9.1.1 Hashing as an essential part of the Blockchain
The hashes as a whole comprise the eco-system and the current state of the Blockchain. Any new data is combined with the history of the Blockchain itself and the hashing algorithm automatically updates its status. What the algorithm digest produces is based on previous transactions and connected to the previous state.

Data processed by the hashing algorithm upon the slightest change would produce an incomparable value; the security of the Blockchain can’t be questioned. If a perpetrator would manage to replace even a bit in the values contained in the ledger, all of the hashes would lose the correlation and as such they would all be incorrect.

One of the basic features of the Blockchain is that data that don’t store personal information of a user but contributed to the transparency and functionality is available to the general public. Any tampering with a record that would alert the network would be easy to detect for the purpose of damage control and restoring the correct state.
9.2 Hashing and the Blockchain structure
For every program to run, a file structure needs to be defined. As the Blockchain is an advanced decentralized system, it depends on what we could call structure as code codependent. The algorithm makes use of public addresses when creating a new hash and stores them in the system. In favor, they serve as a pointer to the origin and destination of the previous and following transaction or block hash.

The blocks are a sort of linear file structure where the pointers are connecting them in the Blockchain file system, the term being used for only for referential purposes.

Initial transactions in the Blockchain are subject to processing by the cryptographic algorithm. The values that comprise a valid transaction along with the algorithmic encryption generate the hash of the first block which is called the Genesis block. The process of generating the next blocks is similar but contains the hash value of the original block as well. As all the blocks are connected by their distinctive hash, the security of the Blockchain is maintained.

The progressive nature of Blockchain technology stems from how all of the components come together. Aside from the functions of hashing that were elaborated on previously, hashing is implemented in the structure of the Blockchain itself. This data structure is where the coding components come into play within Blockchain technology. The pointers are hashing endpoints 

The hashing tree is a concept developed by Ralph Merkle, thus the term Merkle tree.
The initial concept is a pioneering technology that can be compared to AI in finance. Hashes were attributed to group of transactions, or a block upon analyzing the authenticity of the data based on previous transactions. This is adopted in Blockchain technology with a point of notice that every transaction is being hashed one at a time and all of the transactions have a certain structure that connects them through hashing. The result of the transactions coupled together is run through the same algorithm, producing the hash of a Block.

The tree structure in the Blockchain is a common concept in IT for representing hierarchical data. In the Blockchain, a better term would be relational data structures, as the blocks are organized in what could be compared to a relational database with the algorithm being the trustless silent mediator producing the hashes which connect the data.



10. Algorithms 

BLAKE2 is a cryptographic hash function faster than MD5, SHA-1, SHA-2, and SHA-3, yet is at least as secure as the latest standard SHA-3. It’s predecessor, BLAKE made the final round in the NIST hash function competition. The winner of the competition was chosen as the SHA-3 standard algorithm. As the argument for BLAKE being omitted from the SHA-3 process was a subjective opinion of the judges, without any factual basis, we have many reasons to believe that it’s second version is the right choice for Phaeton. 

Many projects adopted BLAKE2 used in Phaton due to its high speed, security, and simplicity.[23] The BLAKE2b Coding used for the PLAAK Phaeton Core is the most advanced Military Grade system, increasing speed, efficiency and security. The ability to function at up to 1GB Tx Hash Rate per second implies security and performance. 

The throughput isn't conducive just for transaction speed. As vulnerabilities lie in the potential of a transaction subject to a silent listener in the middle, the faster it's transmitted stands as opposed to the chance of a breach. Most blockchains use SHA-256. Phaeton Core is faster and more secure, literally impenetrable.

Another key factor for making BLAKE2b our go-to hashing algorithm is the ability to produce a block in an estimated period of 1 second. Considering all the use cases for Phaeton, this is vital to the user experience and extending the possible scenarios for our blockchain. This is a major improvement over Bitcoin, which takes around 10 minutes to produce a block and even the Ethereum network, where a block production takes from 10 to 19 seconds.
10.1 BLAKE2b Specifications 
	
RFC 7693 contains the specifications on BLAKE2b, and the code and test vectors are available on GitHub, licensed under CC0 (public domain-like). The book "The Hash Function BLAKE (2015)" describes BLAKE2 to the fullest extent. 

BLAKE2 comes in two flavours:
BLAKE2b (or just BLAKE2) is optimized for 64-bit platforms—including NEON-enabled ARMs—and produces digests of any size between 1 and 64 bytes
BLAKE2s is optimized for 8- to 32-bit platforms and produces digests of any size between 1 and 32 bytes

BLAKE2 includes the 4-way parallel BLAKE2bp and 8-way parallel BLAKE2sp protocols designed for increased performance on multicore or SIMD CPUs. BLAKE2 offers fine-tuning these algorithms to specific requirements, such as keyed hashing (that is, MAC or PRF), hashing with a salt, updatable or incremental tree-hashing, or any combination thereof. The BLAKE2 document contains these specifications. 

BLAKE2 also includes the BLAKE2x variants, which can produce digests of arbitrary length. A separate document contains BLAKE2x specifications. 

BLAKE2 shines on 64-bit CPUs: on an Intel Core i5-6600 (Skylake microarchitecture, 3310MHz), BLAKE2b can process 1 gibibyte per second or a speed rate of 3.08 cycles per byte. 

The plot below shows how BLAKE2 outperforms MD5, SHA-1, SHA-2, and SHA-3 on a Skylake Intel CPU (speeds are for hashing using a single core; using multiple cores, BLAKE2 can be even faster):


  


10.1.1 Blake2 Hashing Algorithm History

Since BLAKE2 is very similar to BLAKE, we first describe the changes introduced with BLAKE2. We refer to https://131002.net/blake for a complete specification of BLAKE.[24]
10.2 BLAKE2b Improvements
10.2.1 Fewer rounds
	
BLAKE2b does 12 rounds, and BLAKE2s does 10 rounds, compared to 16 and 14 respectively for BLAKE. Based on the security analysis performed so far, and with reasonable assumptions on future progress, it is unlikely that 16 and 14 rounds are meaningfully more secure than 12 and 10 rounds. Considering that the initial BLAKE submission had 14 and 10 rounds, respectively, and that the later increase was due to the high speed of BLAKE.
This change gives a direct speed-up of about 25% and 29%, respectively, on long data. Speed on short data also improves significantly.

10.2.2 Rotations optimized for speed 

The G function of BLAKE-512 performs four 64-bit word rotations of respectively 32, 25, 16, and 11 bits. BLAKE2b replaces 25 with 24, and 11 with 63:
    • Using a 24-bit rotation allows SSSE3-capable CPUs to perform two simultaneous rotations with a single SIMD instruction (namely, pshufb), whereas a rotation of 25 bits requires two shifts plus a logical OR. This reduces the arithmetic cost of the G function in recent Intel CPUs, from 18 single cycle instructions to 16 instructions, resulting in a 12% decrease of resource consumption.
	
    • A 63-bit rotation implementation is optional as an addition (doubling) and a shift followed by a logical OR. This provides a slight performance improvement on platforms where simultaneous addition and shift are possible but two shifts aren't (i.e., some recent Intel CPUs). Additionally, since a rotation right by 63 is equal to a rotation by 1 to the left, this may be slightly faster in architectures that treat 1 as a special case. No platform experiences a downgrade in performance from these changes. For an in-depth analysis of optimized implementations of rotations, we refer to a previous work by two co-designers of BLAKE2. Past experiments by the BLAKE designers as well as third parties suggest that known differential attacks are unlikely to improve significantly, nor get worse.

10.2.3 Minimal padding and finalization flags

BLAKE2 pads the last data block if and only if necessary, with null bytes. If the data length is a multiple of the block length, no addition of a padding byte occurs.

BLAKE2 introduces finalization flags f0 and f1, as auxiliary inputs to the compression function:
    • The security functionality of the padding is subject to transfer to a finalization flag f0, a word set to ff...ff if the block processed is the last, and to 00...00 otherwise. The flag f0 is 64-bit for BLAKE2b and 32-bit for BLAKE2s.

    • A second finalization flag f1 is used to signal the last node of a layer in tree-hashing modes. When processing the last block—that is, when f0 is ff...ff—the flag f1 issues also set to ff...ff if the node considered is the last, and to 00...00 otherwise. The finalization flags are processed by the compression function as described in §2.4. BLAKE2s thus supports hashing of data of at most 64 − 1 bytes, that is, almost 16 exbibytes (the amount of memory addressable by 64-bit processors). The upper bound for BLAKE2b are even more ridiculous, with up to 128 − 1 bytes supported.

10.2.5 Fewer constants

Whereas BLAKE used 8 word constants as IV plus 16 word constants for use in the compression function, BLAKE2 uses a total of 8 word constants, instead of 24. This saves 128 ROM bytes and 128 RAM bytes in BLAKE2b implementations, and 64 ROM bytes and 64 RAM bytes in BLAKE2s implementations. 

11. Nodes					
Nodes in the Blockchain are essential to one of the most valuable features in the decentralized network. One of the functions of a node is maintaining the history of the Blockchain ledger and the more active nodes a certain Blockchain has add up to its stability and potential endurance.
In broader terms, a node is every device that is connected to a network through a certain protocol. In the world of IT, they can be central devices that host information and distribute it to computers, smart phones or tablets.
11.1 Nodes in the Blockchain
Respectively, in Blockchain technology a node is a device that uses the proprietary protocol of a specific Blockchain. All of the nodes are connected through the peer to peer protocol and don’t require a central authority to connect to the protocol. Similar to the organization of blocks in the chain, the architecture of the network is based on the structured tree concept.
There are two main types of nodes:
-        A full node
-        A lightweight node
The full node contains all of the history of the Blockchain ledger and as such can confirm and act as a backbone to the protocol. The lightweight nodes are primarily used for sending and receiving funds as progress in Blockchain technology has allowed for three reference points to be used in order to complete transfer.
In some Blockchains, a node can act as an issuer of a Smart Contract. A node can be used by the Blockchain protocol as one connected to the network or a point of connection for other nodes.
The development of different approaches and usability of Blockchain technology has created a new distinction of nodes according to the consensus protocol used to confirm transactions.
11.1.2 Roles of nodes in Proof of Work protocol
In this protocol, the main purpose is processing money transfers. Thus, nodes can act as a means to transfer funds and it’s up to the user if he wants to run a full or a lightweight node. When the Proof of Work protocol is used, one can run a wallet that can process transactions and receive fuel money, or the cost of the amount of computing power, electricity and being connected to the internet.
As this became a lucrative endeavor in certain Blockchains where many transactions took place, a new type of node became the popular choice called a miner. Depending on the algorithm of the Blockchain, the hardware being used depended either on CPU and GPU power. It even resulted in the development of proprietary hardware for the Bitcoin network known as Asic miners.

11.2 Roles of nodes in Delegated Proof of Stake protocol
The types of nodes in the PoS protocol Blockchains are the same as in the Proof of Work usage case, in the sense that they can be lightweight or full nodes. The difference is that there is a hierarchy introduced when it comes to benefitting from processing transactions.
Namely, there is a selective process when it comes to profiting from processing transactions. A consensus protocol is introduced which utilizes delegation where only a predefined number of nodes can profit from their computing power. You can either cash in by buying tokens or contribute to the community and the combination of both can define your rank.
While at first this may seem as a multilevel scheme, there are benefits to in regards to the benefits received in the Proof of Work system. The competition for profit from mining has become so competitive that the equipment and the power needed is nearly impossible to achieve. There are ethical concerns as well, with claims that extra coal has been used in China in mining farms. This isn’t good P.R. for Blockchain technologies nor is it good for the environment.
Environmental and ethical issues aside, the process of forging in Proof of Stake as opposed to mining guarantees that the equipment being used will bring the top nodes profit and they won’t be stuck in the continuous loop of a level of difficulty and spending money on hardware as in PoW.
11.2.1 Running a Blockchain Node
The requirements to own a node vary between cryptocurrencies and their consensus protocols. For example, we use a Delegated Proof of Stake consensus protocol which requires stakeholder approval. Therefore, in order to become an owner of a node that is forging, a user must first become a delegate which requires a certain number of PLKX tokens supporting them. In our ecosystem this is done by gaining votes, each PLKX token is worth a vote. 
    
In practice, this means either buying tokens or receiving votes from other users of the network who are holding tokens. Regardless, the delegate must have enough PLKX supporting them to break into the top 101 and become a node that can validate transactions and earning token as a reward.

At this point, nodes can only be run on the AWS infrastructure. In order to save our users from a complicated installation process and costs of running a node, we will update this document with detailed instructions when the next phase of development is finished. 
12. Consensus Delegated Proof of Stake:

Delegated Proof of Stake (abbr. DPoS) is a consensus protocol keeping undeniable concurrence on the authenticity across the network, validating transactions and resolving disputes in a civil manner. We chose it as the consensus mechanism for Phaeton due to its undeniable qualities. 
   
The DPoS protocol diverges into two components: voting for a collective of block generators and planning block production. The voting mechanism ensures stakeholders have absolute control because stakeholders risk the most when the network does not function at an optimal level. The voting method has a low level of influence on continuous consensus attainment. Hence, this section will focus on the delegated proof of stake in general.
12.1 The Delegated Proof-of-Stake Method 

The Delegated Proof-of-Stake method differs from the common consensus protocols. Participants in a blockchain regulated by DPoS constitute of stakeholders and delegates. Delegates are casually called witnesses and these terms are interchangeable. 

Stakeholders vote for witnesses and can cast only one vote for an individual witness. However, their voting capacity depends on the percentage of tokens they possess, in correlation to the total amount. In DPoS, we call this voting weight. Whoever gets the most votes is promoted into a witness.

Witnesses are in charge of generating new blocks and appending them to the blockchain, for which they receive compensation. The goal of the voting process is for 50% of the stakeholders to come to the conclusion of accomplishing adequate decentralization through the totality of witnesses. Because voting for delegates is an ongoing mechanism, delegates are motivated to complete their duties to the furthest extent of their ability. If they don't perform their responsibilities, they jeopardize their position and can be voted out in the next round. Additionally, a record is kept through a credibility ranking system to help stakeholders in an improved evaluation of the performance of witnesses. 

In accordance with the adoption of a DPoS consensus protocol in the specific cryptocurrency, the body of delegates is usually subject to supersession at a predefined period of time. This is usually done on a daily or weekly basis. Every delegate has a chance to generate a block and if they fail to do so on a timely basis will usually ensue with them being passed on.  In turn, this will affect their credibility rank.    

DPoS applies real-time voting along with a public scheme of credibility as a consensus protocol. It can be viewed upon as the most decentralized consensus mechanism alternative because it's very well-rounded. Any token owner is empowered to have an impact on the entire network. 

It is paramount that witnesses are elected having the prosperity of the network in mind because they maintain the secure and stable operation of the network. In a few DPoS variants, a witness must prove dedication by allocating his assets in a time-triggered account (where assets are subject to seizure due to malicious conduct). These DPoS variants are called deposit-based proof of stake. 

The main responsibilities of witnesses are to:
    
Provide a node that is operational at all times
Assembling transactions on the network into blocks
Sign and broadcast blocks and validate transactions
Addressing consensus issues, as DPoS relies on honest and democratic settlement

Witnesses are unable to alter any transaction elements. Nevertheless, due to the fact they validate blocks, in theory, they could prevent appending particular transactions to a block. However, can't have a drastic negative impact as the following block generated will incorporate these transactions, providing the next witness with compensation for validating them. Therefore, postponement of transactions is trivial. Moreover, an untrustworthy witness would unavoidably lose his position in the consequential voting round by the rest of the network. Essentially, a DPoS network is sovereign and guarded by all of its users, to make sure the prosperity of the network remains the prime concern.
12.1.1 Advantages of Delegated Proof-of-Stake:

The most significant improvements that Delegated Proof of Stake offers, compared to the standard Proof of Work(PoW) consensus protocol are:

Saving on energy consumption and maintenance costs
Increased decentralization

Saving on energy consumption: The Proof of Work protocol demands a considerable amount of electric energy to derive the hash of the next block and validate transaction among a vast, competitive network. In Delegated Proof of Stake, that is the responsibility of a chosen group of delegates, who are provided with a precise time schedule to complete their task. Hence, the excessive rivalry for appending the next block is eliminated, which reduces the energy and maintenance costs for validating transactions and adding them into blocks.

Increased decentralization: To profit from a cryptocurrency using the Proof of Work consensus protocol, one needs massive computational power. This isn't conducive to decentralization as only those that can afford the specialized equipment will have a shot at deriving the hash value of a valid block, and consequently, receive a substantial portion of the block reward. A DPoS consensus protocol, in contrast, allows stakeholders to vote for transaction validators in accordance to their reputation, consequently advancing decentralization even further. It's plausible for stakeholders to pick an unlimited total of individual delegates, as long as they believe it is conducive to achieving a satisfactory level of decentralization.	

13. Side Chains, Smart Contracts and DApps
13.1 Side chains explained
Albeit a concept in circulation in blockchain technology for a while, functional side chains are a relatively new development. A side chain is a blockchain linked to its parent blockchain network, operating on a compatible layer, keeping it’s data private.

They stem from an initial proposal to the Bitcoin network for leveraging the network. In the blockchain gold rush, the Ethereum blockchain network issued ERC-20 tokens as a means for startups to launch their ICOs’ and save costs on proprietary blockchain developments. The advantage Ethereum had over Bitcoin was the capability to issue Smart Contracts and create distributed applications based on their platform.

Smart Contracts were a means to create an ICO token sale. However, one DApp running on the Ethereum platform comprised a total of 15% of the entire transactions on the network, creating a pyrrhic victory. While the platform gained media attention, the performance of other serious projects that ran on the network suffered.

This resulted in a paradygm shift in blockchain technology and prompted many blockchain companies to create side chains as a service and generate profit for their main chain. With the development of Phaeton, we offer a side chain using a different approach. The Phaeton main chain is reserved for the PLAAK distributed apps ecosystem, but our blockchains qualities along with the concept for adding value to side chains is the first of a kind.
13.1.2 Phaeton’ side chains solution
Phaeton side chains are an enterprise grade, fully decentralized blockchains. The information transferred on them is available only to the users of a specific side chain. They use the same infrastructure, have Phaeton’s technological specifications and interacts with other side chains for added value.
Unlike two-pegged side chains, where the value of a token is a fixed ratio between the main network and the side chain, Phaeton offers creating a completely separate system of values(tokenomics). While side chains in general are two-way pegs where the underlying chain has a fixed ratio of it’s token value to the main chain, the financial principles are entirely up to the stakeholders of the side chains.

With the emergence of Smart Contracts and DApps, fast and secure blockchains are in high demand but running one with enterprise grade performance and security in a fully decentralized manner is both costly and conceptually difficult. Phaeton solves this by generating revenue from its proprietary DApps and creating a network where independent side chains are used for transaction validation.

We tackle the main issue of decentralization when it comes to validating transactions. As our solution suits organizations, companies or communities, confirming transactions on a side chain by the nodes running on it compromise its integrity, all of our side chains comprise an isolated, purposefully connected environment. This leaves no room for manipulating a side chain where users might be acquainted on a personal basis, share a similar agenda or could manipulate the side chain for financial benefits. Transactions are validated by third-party participants and the side chain subject to validation gets added value to its economy by validating transactions on a separate side chain.

We present the core features of Phaeton’ side chains:
- Secure, lightning-fast transactions
- Creation of an independent token
- Utilizing different side chain nodes for transaction verification
- Deploying Smart Contracts and DApps
- Data and application privacy   
	- Customized allocation of resources

There is a reason behind using the term Blockchain technology as opposed to a specific Blockchain where the only purpose would be currency transfers. Just as the peer-to-peer network is the network layer of the Blockchain, the technology itself is flexible enough for applications and especially databases to be distributed through it with an added level of safety.
13.2 Side chain use cases
The Phaeton side chains are aimed at developers or organizations involved in projects that require a dependable platform for their distributed application. The resource consumption and infrastructure make them suitable for every scenario where blockchain applications and Smart Contracts are in a production phase and need to be deployed on a grand scale. as well as internal use for for safe testing of upgrades.

There are numerous applicative uses through Smart Contracts and DApps based on the programming languages we support. Their compatibility with off-chain technology which can be used to scale resources and connect them through an API with existing applications or databases extends the usability of side chains to the furthest extent.

They encompass all of the industrial components where blockchain technology is an upgrade over existing infrastructure or it benefits future expansion and scalability. These include the supply and demand chain, research and development, secure distribution of personal information, any service that requires quick and secure transactions or transactions on a large scale. We don’t exclude the deployment of games, social networks or the entertainment industry.

Aside from the aforementioned, any of the use cases for Smart Contracts are suitable for Phaeton side chains. The original fully distributed manner of the network allows for blockchain applications with variable transaction demands, as applicative uses with a smaller transaction total would benefit from the other side chains which have more users, or nodes, through our proprietary SVN (Side Chain Validation Network) solution. SVN will be elaborated on in the next chapter.

The properties of our side chain technology is aimed at:

Deployment of large scale Smart Contracts
Tested novel DApps with a potential large user base
Enterprise DApps for organizations or companies
Testing future upgrades in a safe environment
13.2 Smart Contracts
Before we discuss how developers can use a plethora of opportunities on the Blockchain for applications we’ll take a quick overview of Smart Contracts, as they’re the gateway between a DApps developers and their users.

The workflow and coding should be concise and accurate, bearing in mind the fact that the execution of a Smart Contract is decentralized and deterministic in nature. That implies that it should be used in scenarios where it can be resolved by strictly defined contract conditions and a community that would like from the benefit of Smart Contracts should strive to create an environment where they could be applied.
13.2.1 Smart contract use cases:
-        Securities
-        Trade Finance
-        Derivatives
-        Land title recordings
-        Supply and demand chains
-        Clinical trials
-        Real estate lending

The benefits of Smart Contracts are eliminating lawyers and notaries and as more countries gravitate toward Blockchain they’re considered legal in nature. Other upsides are the fact no paperwork is needed nor any data can be lost as it’s kept by the Blockchain ledger which offers better security and confidentiality than standard contracts. From a financial standpoint, Smart Contracts offer intelligent money management where objectives have to be met for the funds to be released.

The coding is done in JavaScript and is pretty straightforward. An issuer uses a Smart Contract towards the other party involved and as long as conditions are met, the balance of the other party is required to have the funds defined to put the contract into action. If both of the factors are met, the buyer releases the funds and the contract is applied to the Blockchain Ledger. 
13.3 Decentralized Applications (DApps)                                         
Being a Blockchain developer can be interpreted in two ways – you’re ether working the protocol itself or solutions based on the functionality of the decentralized network. The main difference between a classic and a decentralized app is that the database and at least part of the code is distributed on Blockchain nodes, as opposed to a single server.

Many corporate entities and organizations as well as governments are starting to recognize the advantages of blockchain technology. Decentralized apps offer the same benefits, primarily in terms of security. This is why many coders are gravitating towards Blockchain projects while some are even working on their individual ideas.

Funding can be gained in the form of an initial token offering that is similar to crowd funding but more variables are thrown in the equation. Blockchain applications require substantial investment to be deployed so the code would need to be past a testing period. A token offering also requires legal compliance and a well-documented project which is more adequate for a team project which includes leeway for marketing.

There are a lot of tools available for working on a project in a test environment or a sandbox, as well as testing the code for bugs in a simulated real-time environment. It would be a good decision to factor in the time and marketing needed for it to see the light of day if you choose to embark on such a mission coupled with the fact you’d end up being a major stakeholder and responsible for your investors and clients. In any case, the best way to go about it would be starting small.

Things aren’t bland for blockchain developers as there are quite a few options to consider, such as:
-        Joining an organization working on a project matching your interest
-        Contributing to an incentivized Blockchain community

Another notable difference between programming for major platforms like Android or IOS is the fact of no central authority to approve your application. The Blockchain community is all about innovation and mostly comprised of people that are familiar with fintech at the least. In practical terms, working with Blockchain technology is more dynamic and the potential gains are higher.

The coding languages used in Phaeton DApps are Javascript, C++ and python, supporting some of the proprietary libraries. Backend development is the same as in classic programing – for the time being. There are some limitations but bear in mind that this is a developing technology and some of the downsides are in beta stages as we speak.

Most of the DApps developed are fully open source and blockchains are starting to be tailor made to developers. The general consensus is that the major issues are and the processing speed of transactions, or in this case computing. In our opinion, this is partially due to the infrastructure and influence of the major Blockchains, namely Bitcoin and Etherium.

In fact, there are a lot of contradicting statements about dApps as there are for Blockchain technology in general. For a developer, the best way to get their facts straight about their particular interests would be through online contact with other developers through Gitter or Telegram, where the community resides.


14. Sidechain Validation Network (SVN)
The fundamental problem with side chain networks is an added degree of centralization where validating transaction relies on a group of individuals who are users on a side chain aren’t incentivized for their contributions and the side chain itself is potentially unable to function as a trust-less system.

All of the side chain nodes in Phaeton benefit from blockchain technology by being a part of a financial neural network. Independent of their inner economics, the transactions are distributed among side chains unknown to each other and the nodes on all networks benefit from confirming transactions on each side chain.

It implicates that whatever constitutes the tokenomics on a specific side chain, they will gain value from other side chains, eliminating the chance of a zero-value on a side chain. This risk mitigation strategy contributes to the performance of a side chain, as all nodes on side chains connected to Phaeton’s main network append the blockchain ledger of the other network and in a disaster case scenario, the side chain that was compromised can be rebuilt and continue to function. 
	
This enables the development of genuinely trustless blockchain application.  If you have carefully read this technical paper to this point, you might have realised that you can build almost any kind of innovative blockchain applications. However, until this point blockchain application developers are still able to exercise a large amount of control over their side chains, possibly to the detriment of decentralization.
	
Startups who want to keep control of development and build a business model around their blockchain applications prefer this model, taking advantage of the other benefits of blockchain technology all the while. However, some the users would benefit from trust-less blockchain applications the most. Phaeton gives the option of building applications which can’t be shut down by any single entity, such as the developer, and are secured by anyone who wants to participate.
 

14. Economics & Fees
Blockchain applications require rapid transfers and in order to offer an improvement over centralized infrastructure, costs need to be kept at a minimum. The Phaeton blockchain is built with throughput and performance in mind, as the main chain is developed for application specific requirements.

We construct the economic model to offer value and promote blockchain technology as a solution for entities, companies and organizations that can benefit from it with fees lower than any competitive solution with the performance and security standards implemented.

The costs of a single transaction are at a fixed rate of 0.001$ to meet the needs of the most demanding micro-transaction applications. We provide a transparent micro-economy of all Phaeton components and applications aimed at offering value while promoting the autonomous virtual currency created by developing the Phaeton blockchain,

For the Phaeton side chains, incentives are provided to leverage the network. When new side chains are added, not only does the network improve in performance and dependability, it adds fiscal value to each side chain. Combining these elements of the Phaeton micro-economy offers scalability to a degree available only in speculative statements.

The PLKX coin, originating from Phaeton which is regulated by DPoS implies that it returns value on investments and the market cap increases according to market demand without compromising the assets of stakeholders. The profits are divided between the stakeholders, operational costs and marketing efforts.

The marketing strategy includes promoting the coin by prioritizing the application development roadmap. The PLAAK exchange acts as a means of self-promotion without spending additional costs.Trading pairs of PLKX and every coin added to the Exchange are subject to a 0.05% to encourage PLKX transactions and contribute the participants in block production, or witnesses and delegates.

With the robust throughput volume of 1.000.000 transactions per second, PLKX transactions speed up the process of sending and receiving cryptocurrency. This competitive advantage along with the options that users have (such as a vast number of investment opportunities in the form of other coins and tokens) contributes to a variety of applicative uses. For example, traders that identify a token which can be exchanged through PLKX is subject to gaining in value, the transaction speed will give them a higher chance of taking advantage of the cryptocurrency market.

PLKX coins can be used for:
Payments within Smart Contracts
PLAAK ecosystem DApp transactions
Smart Contract applications
Cryptocurrency payments between individuals
Cryptocurrency exchanges
Purchasing of PLAAK hardware wallets & shop items
PLAAK payment gateway


As the participants in maintaining the Phaeton network dedicate time, resources and effort to maintain a stable economy, the incentives contribute to the quality and efficiency of completing their responsibilities, which are essential to the functioning of the Phaeton network.

Distribution of rewards is defined at 50% for voters, 20% for delegates and nodes and 10% for PLAAK, the organization behind Phaeton. The rewards are in accordance with the number that gets a specific portion and in the case of the organization itself act as a contribution to future developments.

The PLKX coin will benefit from the innovative side chain technology as it generates income for coin issuers. To be able to run Smart Contracts and DApps on Phaeton side chains, entities have to buy an amount of PLKX, according to the scale of operations on the side chain.

All participants in the upkeep of Phaeton will be rewarded, and as such joining the program will require a monthly fee. This is a mitigation strategy to avoid including users who would simply waste resources - either their own or of the whole Phaeton community.

15. Business info and applications
Our extensive analysis and research aimed at identifying the market needs. Along with understanding Blockchain technology and present solutions, we identified the deficiencies and came to the idea of creating a technological novelty.

Phaeton is an high-end blockchain, aimed at enterprise solutions. The unique proposal it offers is usually subject to an ICO (Initial Coin Offering). Our organization is past that stage, but the qualities of the blockchain itself hold value in itself. The fully decentralized side chains are an original development of the managerial staff and developed upholding the highest quality standards by the technical staff.
15.1 The team behind Phaeton

PLAAK is the organization behind Phaeton, which is working on multiple parallel projects. Tasks are distributed among experts in their fields which includes a savvy approach to micromanagement and acquiring quality professionals that provide a best return on investment.
PLAAK as a project is an entire ecosystem of distributed blockchain applications connected to a cloud infrastructure to cover the areas blockchain technology is yet to tackle. Our cryptocurrency platform is fully functional while the blockchain technology that is the subject of this paper is the next step of our development. The ecosystem is further comprised of a Freelance Application, a Business Suite, a Health Care solution, Investment and an E-Commerce platform. Phaeton is the core of the project but also a solution in itself. By applying cutting edge technology with innovative, applicable thinking we are able to offer blockchain solutions to companies across industries, various infrastructures and scale.
15.2 Business Objectives
The direction that PLAAK is heading for is acquiring clients from medium to corporate entities, and large organizations in industries that are matching our solutions. We resort to our experience and promote the use of blockchain technology on a global level in industries that we are knowledgeable in and use cases that it has already covered.

Fields that we are actively seeking customers are:

Financial Solutions
Cryptocurrency Exchanges
I.T. and I.o.T. related
Health and Medical Solutions
Logistics / Supply Chain
Freelance Work
Personal Data and Identity Management

As an organization, we have already implemented a biometric identification solution and an exchange platform. Simultaneously, several projects that were the objective of our ICO are in progress and the results motivated us to expand our operations along with upgrading our managerial staff and skill set.

We firmly believe that by working hard on our set goals, having the financial groundwork covered and our human resource network constantly expanding results are imminent. Our ambition drives us to implement every novelty we developed. Every technological project that alleviates issues, solves a problem for the general public and improves the overall functioning of organizations and the society gains wide adoption. 

The improvements that blockchain technology offers will bring clients at one point or another. However, the products we develop take time, effort and financial means and we are following best practices by informing the general public of how we can improve their livelihood. We are in the know we have to meet our clients half-way and are resorting to all means necessary to bring the benefit of technological advancements to communities.

Citations:

1. Yli-Huumo J., Ko D., Choi S, Park S., Smolander K. “Where Is Current Research on Blockchain Technology?—A Systematic Review.” PLoS ONE 11(10): e0163477. October 3, 2016 Available: https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0163477 [Accessed: Sep. 27, 2018]
2. Yli-Huumo J., Ko D., Choi S, Park S., Smolander K. “Where Is Current Research on Blockchain Technology?—A Systematic Review.” PLoS ONE 11(10): e0163477. October 3, 2016 Available: https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0163477  Accessed: Sep. 27, 2018] 
3. S. Nakamoto. “Bitcoin: A Peer-to-Peer Electronic Cash System” Internet: https://nakamotoinstitute.org/bitcoin/#selection-7.4-9.38 October 31, 2008 [Accessed: Sep. 27, 2018]
4. J. Chiu, T. Koeppl. “The Economics of Cryptocurrencies – Bitcoin and Beyond” Internet: https://www.chapman.edu/research/institutes-and-centers/economic-science-institute/_files/ifree-papers-and-photos/koeppel-april2017.pdf April, 2017 [Accessed: Sep. 27, 2018] 
5. Joseph B., Andrew M. , Jeremy C., Arvind N., Joshua A. K., Edward W. F. “SoK: Research Perspectives and Challenges for Bitcoin and Cryptocurrencies” 
Internet: https://wws.princeton.edu/system/files/research/documents/Felten_SoK.pdf May, 2015 [Accessed: Sep. 27, 2018]
6. Massimo B, Livio P. “An empirical analysis of smart contracts: platforms, applications, and design patterns” arXiv:1703.06322 [cs.CR], March, 2017 Available: https://arxiv.org/pdf/1703.06322.pdf  [Accessed: Sep. 27, 2018] 
7. Yli-Huumo J., Ko D., Choi S, Park S., Smolander K. “Where Is Current Research on Blockchain Technology?—A Systematic Review.” PLoS ONE 11(10): e0163477. October 3, 2016 Available: https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0163477  Accessed: Sep. 27, 2018] 
8. Dr. Gavin W. “ETHEREUM: A SECURE DECENTRALISED GENERALISED TRANSACTION LEDGER - BYZANTIUM VERSION e94ebda” Internet: https://ethereum.github.io/yellowpaper/paper.pdf June, 05, 2018 [Accessed: Sep. 27, 2018]
9. Joseph B., Andrew M. , Jeremy C., Arvind N., Joshua A. K., Edward W. F. “SoK: Research Perspectives and Challenges for Bitcoin and Cryptocurrencies” 
Internet: https://wws.princeton.edu/system/files/research/documents/Felten_SoK.pdf May, 2015 [Accessed: Sep. 27, 2018]
10. Dr. Gavin W. “ETHEREUM: A SECURE DECENTRALISED GENERALISED TRANSACTION LEDGER - BYZANTIUM VERSION e94ebda” Internet: https://ethereum.github.io/yellowpaper/paper.pdf June, 05, 2018 [Accessed: Sep. 27, 2018]
11. A. Berentsen, F. Schär (2018, Jan) “A Short Introduction to the World of Cryptocurrencies”, Federal Reserve Bank of St. Louis Review, [Online], 100(1), pp. 5-6, Available: https://files.stlouisfed.org/files/htdocs/publications/review/2018/01/10/a-short-introduction-to-the-world-of-cryptocurrencies.pdf [Accessed: Sep. 27, 2018]


12. A. Berentsen, F. Schär (2018, Jan) “A Short Introduction to the World of Cryptocurrencies”, Federal Reserve Bank of St. Louis Review, [Online], 100(1), p. 7, Available: https://files.stlouisfed.org/files/htdocs/publications/review/2018/01/10/a-short-introduction-to-the-world-of-cryptocurrencies.pdf [Accessed: Sep. 27, 2018]
13. Lisk, [2018], Lisk Consensus Protocols, Consensus protocols are one of the most important and revolutionary aspects of blockchain technology, URL: https://lisk.io/academy/blockchain-basics/how-does-blockchain-work/consensus-protocols 
14. Aggelos K., Nikolaos L., Aikaterini-Panagiota Stouka. “Proofs of proofs of work with sublinear complexity”in Proc. of the 2008 Twentieth International Conference, Financial Cryptography and Data Security 2016, February 22–26, 2016 Bridgetown, Barbados, [Online] Available: https://eprint.iacr.org/2017/963.pdf [Accessed: Sep. 28, 2018].
15. Aggelos K. Andrew M., Dionysis Z. “Non-Interactive Proofs of Proof-of-Work”, Cryptology ePrint Archive, Report 2017/963(edited), May 31, 2018 [Online] Available: https://eprint.iacr.org/2017/963.pdf [Accessed: Sep. 28, 2018].
16. Aggelos K., Alexander R., Bernardo D., Roman O. “Ouroboros: A Provably Secure Proof-of-Stake Blockchain Protocol”, Cryptology ePrint Archive, Report 2016/889(edited), August 21, 2017,  [Online] Available: https://eprint.iacr.org/2016/889.pdf [Accessed: Sep. 28, 2018]
17.  Lisk, [2018], Lisk Peer-to-Peer Communication, Transaction Pool, URL: https://lisk.io/documentation/lisk-protocol/peer-to-peer-communication [Accessed: Sep. 28, 2018]
18. Lisk, [2018], Lisk Security, Second Passphrase, URL: https://lisk.io/documentation/lisk-protocol/security [Accessed: Sep. 28, 2018]
19. Lisk, [2018], Lisk Security, Multisignature, URL: https://lisk.io/documentation/lisk-protocol/security [Accessed: Sep. 28, 2018]
20. Lisk, [2018], Cryptography, What is Cryptography?, URL: https://lisk.io/academy/blockchain-basics/how-does-blockchain-work/blockchain-cryptography-explained [Accessed: Sep. 28, 2018]
21. Standards for Efficient Cryptography Group, SEC 1: Elliptic Curve Cryptography, [Online] Available: http://www.secg.org/sec1-v2.pdf [Accessed: Oct. 3, 2018]
22. Lisk, [2018], Digital Signatures, What is a Digital signature, URL: https://lisk.io/academy/blockchain-basics/how-does-blockchain-work/digital-signatures [Aug, 
23. Jacobson, M., Locasto, M., Mohassel, P., Safavi-Naini, Eds., Applied Cryptography and Network Security, 11th International Conference, ACNS 2013, Banff, Canada, June 25-28, 2013. New York: Springer, 2013 [Accessed: Sep. 28, 2018]
24. BLAKE2 project, [Feb. 27, 2017], BLAKE2 — fast secure hashing, URL: https://blake2.net/ [Accessed: Sep. 28, 2018]

