+++
title = "[Mirror] San Francisco Blockchain Week: A Truly DeFi-ning Moment"
date = "2019-11-27T00:00:00+09:00"
tags = []
+++

> **NOTE: This is just a mirror of my old writing from 2019 for record-keeping purposes.**

### IMPORTANT: EVERETT IS NOT BEING WORKED ON SINCE 2020. THE CURRENT WHATEVER-THAT-IS YOU SEE ON https://everett.zone/ IS A SCAM AND NOT AFFILIATED WITH ANY OF THE PRIOR EVERETT PEOPLE - THEY ARE JUST COPYING THE EXACT SAME LOGO AND DOMAIN WE USED BACK IN 2019. 

Hi folks!

We are glad to be able to announce some of the progress we made during the last couple of weeks and to share some of the experience we had during the San Francisco Blockchain Week.

## SF DeFi Hackathon

One of the main highlights of SFBW was the DeFi hackathon. Teams gathered from all across the globe to participate and show how their ideas DeFi-es traditional thinking.

Our entry, Everett: Reloaded was fortunate enough to win a 1st prize for the Cosmos category. Explained below are the features we further developed during our 3 day sprint. This is a Demo video about what we’ve developed and further explanatory during our Hackatom.

https://www.youtube.com/watch?v=OfJrcIu9afo

### Implementation of IBC (the real thing)
Our previous entry for the 2019 HackAtom Seoul used a pseudo-version of IBC, as a workable version of IBC was not released at the time. However, as a working prototype of IBC was released, we decided to upgrade upon our last version.

However, as there are no operating relayers as of now, the relay of interchain packets had to be done manually.

### Cross-chain asset control with Interchain Accounts
One critical feature that is required in order for bATOMs to be fully backed is the ability to force liquidations of risky LSPs. A method to execute logic in blockchains is thus needed, usually in the form of smart contracts.

However, the Cosmos Hub lacks the necessary features that could easily enable this. Since smart contract-like abilities can only be implemented on top of a Cosmos Zone, a method for the Hub’s assets to indirectly access the decentralized logic execution of a Cosmos Zone.

Interchain Accounts allow this to be possible. With the use of interchain accounts, a special address on the Cosmos Hub can be controlled by a Cosmos Zone. In the case for Everett, this grants the Everett Zone to bond/unbond ATOMs held in the special address.

### Kepler, the wormhole to the interchain galaxy for non-aliens
One criticality that the entire blockchain ecosystem lacks is a smooth user experience. Everett is not an exception to this, so we came up with an idea to build our own point of interaction. Our aim was to make the creation/closure of LSPs simple enough for regular ATOM holders.

Since bATOMs are intended to be utilized in various applications (particularly DeFi), we decided to further expanded upon this idea to give users a way to easily interact with interchain dApps that reside on different Cosmos Zones.

### Liquid Staking Position (LSP) NFTs
We also experimented with the Cosmos NFT module, using it to tokenize LSPs (excluding the minted bATOMs). Before, LSPs could only be closed by the person who initially opened it. Packaging LSPs into a form of NFTs and enabling their transfers to allow them to be closed by someone else.

### Tokenized Leveraged LSPs
One feature of Everett is the ability to leverage on ATOM delegations. This process is enabled by selling minted bATOMs in exchange for more unbonded ATOMs and delegating them as well.

Combining the protocol with a bATOM/ATOM Uniswap pair can automate this process, which in turn can be further tokenized.

To sum up, we had a valuable experience in SF, being able to squeeze out great ideas and having the chance to network with like-minded individuals.

If you have further interests in our hackathon entry, please check out our Devpost for more details.

https://devpost.com/software/everett-reloaded#updates