<img src="https://farm5.staticflickr.com/4503/37148677233_71edc5a37b_o.png" width="1041" height="53" alt="blueband">

# [https://ibm.biz/startinghyperledger](https://ibm.biz/startinghyperledger)

# The Promise of Blockchain Is a World Without Middlemen
Vinay Gupta in Harvard Business Review: https://hbr.org/2017/03/the-promise-of-blockchain-is-a-world-without-middlemen

# How it all started
<p>
October 2008 It all started with Satoshi Nakamoto and his paper [Bitcoin: A Peer-to-Peer Electronic Cash System](https://bitcoin.org/bitcoin.pdf) 
which addressed a key problem in electronic commerce:
<h3>
<b> 
 
~~~
A purely peer-to-peer version of electronic cash would allow online payments
to be sent directly from one party to another without going through a financial 
institution. 

Digital signatures provide part of the solution, but the main benefits are lost 
if a trusted third party is still required to prevent double-spending.

We propose a solution to the double-spending problem using a peer-to-peer network.
~~~

</b>
</h3>

# Bitcoin versus Blockchain
<table>
 <tr><th> Bitcoin <th> Blockchain </tr> 
 <tr><td>Cryptocurrency <td>Assets</tr>
<tr><td>Anonymity <td> Identity</tr>
 <tr><td>Proof of work (mining) <td>Selective endorsement (consensus)</tr>
 </table>

## [The similarities of public and private blockchain](https://www.ibm.com/blogs/blockchain/2017/05/the-difference-between-public-and-private-blockchain/)

1. Both are decentralized peer-to-peer networks, where each participant maintains a replica of a shared append-only ledger of digitally signed transactions.
1. Both maintain the replicas in sync through a protocol referred to as consensus.
1. Both provide certain guarantees on the immutability of the ledger, even when some participants are faulty or malicious.

## [Public blockchain and known participants](https://www.ibm.com/blogs/blockchain/2017/05/the-difference-between-public-and-private-blockchain/)

1. The sole distinction between public and private blockchain is related to who is allowed to participate in the network, execute the consensus protocol and maintain the shared ledger. 
1. A public blockchain network is completely open and anyone can join and participate in the network. The network typically has an incentivizing mechanism to encourage more participants to join the network. Bitcoin is one of the largest public blockchain networks in production today.

1. One of the drawbacks of a public blockchain is the substantial amount of computational power that is necessary to maintain a distributed ledger at a large scale. More specifically, to achieve consensus, each node in a network must solve a complex, resource-intensive cryptographic problem called a proof of work to ensure all are in sync.

1. Another disadvantage is the openness of public blockchain, which implies little to no privacy for transactions and only supports a weak notion of security. Both of these are important considerations for enterprise use cases of blockchain.




[Bitcoin: Proof of Work vs Proof of Stake](https://www.ccn.com/bitcoins-future-proof-of-stake-vs-proof-of-work/)
 
 
## Background to Blockchain, Connected Markets. <p>
Networks connect participants: customers, suppliers, banks, consumers
 * <b>Markets </b> organize trades: Public and private markets
 * Value comes from <b>assets</b>: Physical assets (house, car ...), Virtual assets (bond, patent ...), Services are also assets
 * <b>Transactions </b> exchange assets 

An asset can be tangible — a house, a car, cash,  land  —  or  intangible  like  intellectual  property,  such  as 
patents, copyrights, or branding. Virtually anything of value can be tracked and traded on a blockchain network, reducing risk and 
cutting costs for all involved.
<p>
 <p>
 https://www.itu.int/en/ITU-T/Workshops-and-Seminars/201703/Documents/Christian%20Cachin%20blockchain-itu.pdf
<p>
A blockchain is a <b>decentralized virtual ledger</b> for recording <b>transactions about assets </b> without <b>central authority</b> through a <b>distributed cryptographic protocol</b>. 
<p>
 The blockchain ledger is permissioned, it supports consensus, it has provenance, immutability and finality.

## The Blockchain Distributed Ledger

<img src="https://www.ibm.com/blogs/internet-of-things/wp-content/uploads/2017/05/2-1.jpg">
<p>
 
<b>Anything that you can make a list of, you can manage with blockchains</b> 

## Four elements characterize Blockchain

### Replicated ledger
* History of all transactions
* Append-only with immutable past
* Distributed and replicated
 
### Cryptography
* Integrity of ledger
* Authenticity of Transactions
* Privacy of Transactions
* Identity of Participants

### Consensus
* Decentralized Protocol
* Shared conrol tolerating disruption
* Transactions validated

### Business Logic
* Logic embedded in the ledger
* Executed together with transactions
* From simple "coins" to self-enforcing "smart contracts" 
                       
<p>
which combined provide a trustworthy service to a group of nodes that do not fully trust each other. 
<p>
With blockchain, several users can write entries into a block or a record of information, and a community can control how the record of information is modified and updated.

[E-book Blockchain for Dummies](https://www-01.ibm.com/common/ssi/cgi-bin/ssialias?htmlfid=XIM12354USEN)
<p>

# Bockchain concepts

## The Ledger and the State Database

There are two place which "store" data in Hyperledger Fabric:
### The ledger is the actual "blockchain". 
It is a file-based ledger which stores serialized blocks. Each block has one or more transactions. <br>
Each transaction contains a read-write set which modifies one or more key/value pairs. <br>
The ledger is the definitive source of data and is immutable.

### The state database holds the last known committed value for any given key. 
It is populated when each peer validates and commits a transaction. <br>
The state database can always be rebuilt from re-processing the ledger. <br>
There are currently two options for the state database: an embedded LevelDB or an external CouchDB.
<p>
As an aside, if you are familiar with Hyperledger Fabric channels, there is a separate ledger for each channel as well.
<p>
When we query from where do we retrieve data?  1) from the blockchain chain or 2) from state db? <p>.
If it is from state db how can it retrieve a specific key because you mentioned "state database holds the last known committed value for any given key" <p> 
Queries or GetState in chaincode return data from the state db. They will only return the last value for a key. <p>
If you want to get the entire history for a key, you need to enable the historical database in the configuration of your peer 

### Chaincode.
Like <b>Stored Procedures</b> in a traditional database, handles business logic. http://hyperledger-fabric.readthedocs.io/en/release/chaincode4ade.htm

<img src="https://farm5.staticflickr.com/4503/37148677233_71edc5a37b_o.png" width="1041" height="53" alt="blueband">

<img src="https://www.hyperledger.org/wp-content/uploads/2016/09/logo_hl_new.png"><p>
<p>

[Hyperledger](https://www.hyperledger.org/) is an umbrella project of <a href="https://github.com/hyperledger">open source blockchains and related tools</a>, started in December 2015 by the Linux Foundation, to support the collaborative development of blockchain-based distributed ledgers.
<p>

[Hyperledger Fabric](github.com/hyperledger/fabric) is an implementation of a distributed ledger platform for running smart contracts, leveraging familiar and proven technologies,  with  a  modular  architecture  allowing  pluggable  implementations  of  various  functions. [It is excellently documented here](https://hyperledger-fabric.readthedocs.io/en/release/)
<p>
<img src="https://farm5.staticflickr.com/4630/27933522299_0f031eb17b_o.jpg" width="638" height="359" alt="Hyperledger">
<p>

<img src="https://farm5.staticflickr.com/4458/37771305586_6bf75bc2af_o.png" width="853" height="482" alt="hyperledger architecture">  
<p>

[Hyperledger Composer](https://www.hyperledger.org/projects/composer) Hyperledger Composer is a set of collaboration tools for building blockchain business networks that make it simple and fast for business owners and developers to create smart contracts and blockchain applications to solve business problems.

[Hyperledger Composer Tutorial](https://hyperledger.github.io/composer/tutorials/tutorials.html)
<p>
<img src="https://farm5.staticflickr.com/4503/37148677233_71edc5a37b_o.png" width="1041" height="53" alt="blueband">

# Designing and creating Blockchain applications with Hyperledger

## Step 1: Learn Design Thinking

[IBM Design Thinking Field Guide](https://www.ibm.com/blogs/bluemix/2016/12/ibm-design-thinking-field-guide/)

## Step 2: Go through IBM Blockchain Use Cases

[IBM Blockchain Use Cases](https://www.ibm.com/blockchain/use-cases/)

## Step 3a: Take the IBM Blockchain on-line course

[Zero to Blockchain An IBM Redbooks course](https://www.redbooks.ibm.com/Redbooks.nsf/RedbookAbstracts/crse0401.html)

## Step 3b: Go through selected Blockchain Developer Patterns
[Blockchain Developer Patterns](https://developer.ibm.com/code/technologies/blockchain/)

## Step 4: Create your own Hyperledger Data Model
[Hyperledger Composer Tutorial](https://hyperledger.github.io/composer/tutorials/tutorials.html)

In Hyperledger Composer: save data model as a .bna file.

## Step 5: Deploy the business network to Hyperledger Fabric. 
* This requires the Hyperledger Composer chaincode to be installed on the peer,
* then the business network archive (.bna) must be sent to the peer, 
* and a new participant, identity, and associated card must be created to be the network administrator. 
* Finally, the network administrator business network card must be imported for use, 
* and the network can then be pinged to check it is responding.

[Step by step description](https://developer.ibm.com/code/patterns/decentralized-energy-hyperledger-composer/)

## Steo 6: [Deploy on the IBM Blockchain Platform](https://www.ibm.com/blockchain/platform/)

<img src="http://34b70.http.dal05.cdn.softlayer.net/broker-static/v1-ga1/img1.png"><br>
<img src="http://34b70.http.dal05.cdn.softlayer.net/broker-static/v1-ga1/img2.png"><br>
<img src="http://34b70.http.dal05.cdn.softlayer.net/broker-static/v1-ga1/img3.png"><br>
<img src="http://34b70.http.dal05.cdn.softlayer.net/broker-static/v1-ga1/img4.png"><br>

[Deploy a sample application to the IBM Blockchain Platform Get up and running with the Enterprise Membership fast](https://www.ibm.com/developerworks/cloud/library/cl-deploy-sample-application-ibm-blockchain-platform/index.html)

<img src="https://farm5.staticflickr.com/4503/37148677233_71edc5a37b_o.png" width="1041" height="53" alt="blueband">

# Appendix
