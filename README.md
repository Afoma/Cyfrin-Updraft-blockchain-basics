# Cyfrin-Updraft-blockchain-basics
Summary of what I'm learning on Cyfrin Updraft's course on blockchain basics

EIP 1559 model

Changes proposed in the1559 model have a lot of implications which may be severe-
- Less profit for the miners: the miners in the current fee system receive both the block subsidy reward and the entire gas fee. With the recent high gas prices caused by defi, miners were able to collect more money from the fees than the actual block rewards even though historically block rewards were higher than the extra gas fees collected from transactions. After the changes from EIP 1559 are implemented, miners will only receive block rewards plus the miner tip. This is one of the reasons why miners are quite reluctant to implement the proposal and suggest that this change be pushed to ETH 2.0
- Change required by the wallet: With EIP 1559 in place, wallets don't have to estimate the gas fees anymore. They can just set the base fee automatically based on the information available in the previous block. This should simplify wallet user interfaces. Base fee burning also has major implications when it comes to the ETH supply. Burning the base fee creates an interesting feedback loop between the network usage and the ETH supply. More network activity equals more ETH burned and this equals less ETH available to be sold on the market by miners, making the already existing ETH more valuable. Burning the base fee rewards the users of the network by making their ETH more scarce instead of overpaying miners. This fee-burning mechanism sparked a lot of discussions about ETH being deflationary. This would be possible if the block reward and the miner tip were lower than the base fee burned. One potential drawback of burning the base fee is the fact of losing control over the long-term monetary policy of ETH. With this change, ETH would end up being sometimes inflationary and sometimes deflationary. This doesn't look like a major problem as the maximum inflation would be capped at 0.5% to 2% per year.

* Will EIP 1559 make gas fees much lower?
Not really. It will optimise the fee model by smoothing the spikes in gas fees and limiting the number of overpaid transactions but the main ways of lowering gas fees are still ETH 2.0 and Layer 2 scaling solutions.

There are still a few challenges to be overcome especially when it comes to making sure that miners can safely process bigger blocks without making the whole network more prone to denial-of-service attacks. EIP 1559 belongs to the core category of EIPs, implying that the change affects the Ethereum consensus and requires all the clients to upgrade at the same time.

The base fee gets programmatically and algorithmically adjusted to try to target all the blocks to be 50% full. If they're more than 50% full, the base fee automatically goes up, if they're less than 50% full, the base fee automatically goes down.

Traditional websites run on the same server, even if they use different servers, they are still controlled by the same group or entity. Blockchains, on the other hand, make use of different independent nodes.

A node is a single instance in a decentralised network- Peer A, Peer B, Peer C, and so on. Blockchain is so potent because anybody can join these networks. The only barrier to entry is hardware requirements. Anybody can run their node, you can go to GitHub and run your Ethereum node. 

In a blockchain, if a node acts maliciously other nodes ignore it, keep running, and might even punish it in some instances. Each blockchain keeps a full list of every transaction that happens on that blockchain.

### Proof of Work
This is when miners compete to find a nonce value that when it is combined with other block header data and hashed, produces a hash value that meets a certain criteria, typically a target difficulty level. It ensures that blocks are difficult to create but easy to verify.

### Consensus
Proof of Work and Proof of Stake fall under the umbrella of consensus. Consensus in blockchain is defined as the mechanism used to reach an agreement on the state or the single value on the blockchain. An example of the application of a consensus mechanism is other nodes kicking out a malicious node. 

A consensus protocol in a blockchain or decentralised system can be broken down into 2 pieces:

- Chain Selection algorithm
- Sybil Resistance mechanism

Proof of Work is known as a Sybil Resistance mechanism. This is what Ethereum and Bitcoin currently use. Proof of Work is defined as a Sybil Resistance mechanism because it defines a way to figure out who the block author is, and which node is going to be the node that finds that mine and becomes the block author so that all the other nodes can verify that it is accurate. 

According to Chat GPT, "Ethereum is gradually moving away from Proof of Work towards Proof of Stake to improve scalability, energy efficiency, and security, as Proof of Stake consensus mechanisms offer several advantages over Proof of Work, including reduced energy consumption and increased network participation incentives. 

### Sybil Resistance
Sybil resistance is a blockchain's ability to defend against users creating a large number of pseudo-anonymous identities to gain a disproportionately advantageous influence over a said system.
