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
