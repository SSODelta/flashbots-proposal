---
id: 
title: Stackelberg Attacks and Miner-Extractable Value (MEV)
team: Daji Landis and Nikolaj I. Schwartzbach
created: 2023-10-01
---

# Stackelberg Attacks and Miner-Extractable Value (MEV)
## Background and Problem Statement

It is a well-researched fact that smart contracts have the potential to alter the expected outcomes of known games. There are two defining properties that precipitate these new equilibrium. First, smart contracts allow players to commit to strategies irrevocably; contracts can self-execute the players’ strategies and, once set in motion, the players cannot meddle in their own strategy.  Second, smart contracts can condition on the content of other contracts.  This means that a player can not only condition on the actions another player executes, but on the content of their strategy, which is visible in those players’ smart contracts.  These two nuances taken together have the potential to change the equilibrium of a game.  In particular, the commitment to contracts induces a meta-game before the actual execution of the game actions in question, making for a more complicated and sometimes decidedly different game.  We note that the advantage always lies with the player with the first contract.

In our papers [2-3], we show that the transaction fee mechanism of most major blockchains (including EIP-1559) are amenable to these attacks. In [2], we considered a model where the users of the blockchain are given the capacity to deploy smart contracts, and showed that this enables the users to spontaneously collude against the miner, who loses most of their revenue as a result. However, this model neglects the fact that the miner essentially has full control over the transactions put on the block. This implies that the miner *de facto* has the first contract move, and the first mover advantage will be enjoyed by the miner and not some user.  In particular, the contracts that constitute the attack must themselves be deployed on a blockchain and a savvy miner would block their deployment. The miner’s first mover advantage on one chain could be undermined by relocating the contracts that constitute the attack to a different blockchain  Thus, we want to introduce two blockchains in order to model both the need for a second blockchain for the commitments as well as a second token for MEV arbitrage. 

We believe this would not be enough to counter the miner’s power and would in fact allow the miner to extract all the value of the users.  This would constitute an inversion of the model we propose in [2], and add to the complexity of designing good transaction fee mechanisms. Beyond countering the attack in [2], we suspect  our model will show that, under these model conditions, miners will so completely extract the users’ utility that the blockchain will become effectively useless.

## Plan and Deliverables
* Give a simple formal model of MEV (potentially expanding on [4] to account for arbitrage / multiple chains).
* Set up that model to include the details of attack contract deployment.
* Formalize the relation of commitment devices as a [lattice](https://en.wikipedia.org/wiki/Lattice_(order)).
* Propose Stackelberg attack by the miner.
* Solve with different utility distributions.
* Write a research paper on results and pursue publications, as well as community facing blog posts and/or presentations. 

## References
* [1] Model for Games with Smart Contracts: https://arxiv.org/pdf/2107.04393.pdf
* [2] Stackelberg Attacks on Auctions: https://arxiv.org/pdf/2305.02178.pdf
* [3] Stackelberg Attacks in General:  https://arxiv.org/pdf/2305.04373.pdf
* [4] Related Model of MEV: https://arxiv.org/pdf/2208.13464.pdf
