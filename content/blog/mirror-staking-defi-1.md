+++
title = "[Mirror] Staking and DeFi: Can They Coexist? Part 1"
date = "2019-08-29T00:00:00+09:00"
tags = []
+++

> **NOTE: This is just a mirror of my old writing from 2019 for record-keeping purposes.**

### IMPORTANT: EVERETT IS NOT BEING WORKED ON SINCE 2020. THE CURRENT WHATEVER-THAT-IS YOU SEE ON https://everett.zone/ IS A SCAM AND NOT AFFILIATED WITH ANY OF THE PRIOR EVERETT PEOPLE - THEY ARE JUST COPYING THE EXACT SAME LOGO AND DOMAIN WE USED BACK IN 2019. 

## Staking Rewards in Proof of Stake are Economically Flawed

![staking-defi-1](/writings/images/mirror-staking-defi-1/staking-defi-1-1.png)

## Economic analysis of Proof of Stake
Proof of Stake (PoS) is increasingly becoming popular as the core consensus layer for blockchains. Multiple blockchain platforms like Ethereum, EOS, Cosmos, and Tezos has already adopted PoS or has plans to do so in the near future. For a long time, a lot of consideration has been done on the security aspects of PoS. However, not much thought has gone into considering the potential economic effects on the ecosystem and the possible negative outcomes of them. In this article, we line up three potential problems that could arise from a PoS based economic system.

> ### To Stake or to Not Stake: 
> 
> ### The Introduction of a Central Interest Rate

![staking-defi-2](/writings/images/mirror-staking-defi-1/staking-defi-1-2.png)

Staking and DeFi products compete with each other

### 1. Disincentivizes Ecosystem Development
The first problem that could arise is that the existence of a staking rewards stake in PoS can badly influence the development of the dApp ecosystem. Currently by staking ATOMs in the Cosmos hub, one can receive a yearly return of around 11.5%. Since just by the simple act of staking ATOMs 11.5% yearly, investing (e.g. providing liquidity) into dApps (especially DeFi) that offer a return of less than 11.5% won’t be favored by holders of ATOM. It effectively creates an inefficient ecosystems where applications have to compete with the base protocol for users. This is a problem not just for Cosmos, but this also applies to other PoS based platforms, one example being post-Casper Ethereum.

Some might argue that this is natural and the ecosystem will reach an efficient equilibrium due to market effects. However, though it is likely that an equilibrium will be reached, it is highly doubtful that it’ll be efficient (in a way that it maximizes user utility). Two examples (Compound and Uniswap) are used to give a more in-depth explanation.

#### Compound on Post-Casper Ethereum
If you take a look at the current state of Ethereum, it does not have any kind of staking rewards so ETH has no barrier to be used to provide liquidity. In fact, holders are actually incentivized to, in order to counteract the devaluation of one’s assets via inflation. This is the reason why there exists an extremely high amount of more than $60M worth of ETH pooled up in Compound, even though the interest rate lenders receive are extremely low, current at around 0.1% APR (Annualized Percentage Rate). Because of the high supply of ETH lenders provide, user benefit from being able to borrow ETH from Compound at an low rate of around 2% (Compound takes 2% as a commission).

In contrast, in post-Casper Ethereum, a blockchain which we assume will have an staking reward rate of 2% APR from now on, ETH holders are incentivized to stake instead of pooling ETH to Compound. The supply of loanable ETH in Compound will decrease until the APR of lending goes above 2%. This will cause a rise in the borrow interest rate to 4% and above, forcing loaners to take higher interest rates, thus causing a decrease of social utility.

#### Uniswap on Cosmos

A liquidity provider based decentralized exchange like Uniswap could also suffer inefficiencies in PoS platforms. Using the example of Cosmos, an ATOM trade pair that fails to deliver more than 5.75% APR might end up in a virtuous cycle of endless decreases in liquidity and reduced trade volume.

### 2. Disincentivizes dApp Usage
The second potential problem is that PoS could prevent people from using dApps (especially DeFi) more freely. Since by using a dApp that require locking up a PoS token forces users to miss out on staking rewards, users would be less willing to use those dApps there. MakerDAO on Ethereum after Casper is a great example of this.

#### MakerDAO on Post-Casper Ethereum
A staking reward rate without any further solutions also disincentivize opening MakerDAO CDPs. As ETH locked up in a CDP cannot be used to claim staking rewards, users effectively miss out on a relatively stable yearly profit of 2%. CDP holders now cost an extra opportunity cost, a potential staking reward rate of 2% per year. This opportunity cost could indeed reduce the number of people willing mint DAI.

#### Kava on Cosmos
This problem intensifies even more on DeFi dApps on Cosmos. Kava, being a great example. Users of Kava has to sacrifice a potential staking reward rate of 11.5% per year in order to mint stablecoins using their ATOMs as collateral. This will obviously also disincentivize users from actively using the product.

### 3. Opportunity Cost of Interchain Transfers
Lastly, this problem applies to interchain platforms, which aim to connect different blockchains to make asset transfers possible across blockchains. The problem arises with transfers of PoS based tokens, which the staking reward rate will disincentivize interchain transfers from happening.

#### Ethereum-Cosmos Peg
One example is Cosmos, where it is planned to be connected to Ethereum using peg zones. This might not be a problem now, but as Ethereum moves on to Ethereum 2.0 and Casper is implemented, only ETH being staked in the Ethereum blockchain receive staking rewards and ETH that has been moved to the Cosmos network cannot.

Therefore, since by moving one’s ETH to Cosmos holders basically miss out on potential staking rewards, the incentive to move ETH to Cosmos is reduced.
In order for the Ethereum-Cosmos ecosystem to grow, transfers to ETH to Cosmos should happen regularly, but the above problem adds hurdles to this from happening.

### The Inflation Rate Dilemma
Another interesting point here is the effects of the inflation rate on the network and a dilemma following it. For a PoS blockchain it can either choose to have a high inflation rate or a low inflation rate. In the status quo, both choices have a trade-off between security and usefulness. This trade-off prevents the network from being more Pareto efficient.

#### High Inflation Rate
Having a high inflation rate by increasing the staking reward rate incentivizes token holders to stake more and thus increases the total value of staked tokens. By this, attackers have to acquire more capital in order to perform an attack on the network. A high inflation rate also forces attackers to have a higher potential loss for byzantine/offline nodes and thus further re-enforces the security of the network.

However, since in current models tokens can only be either staked or invested/used, this reduces the total amount of assets that can be used to develop the ecosystem. This negative effect is further deepened since potentially useful applications that offer returns lower than the staking reward rate are neglected by those that can help improve them.

#### Low Inflation Rate
A low inflation rate on the other hand, can help catalyze the development of the ecosystem by incentivizing more investments in applications but reduces the network security by potentially preventing more tokens from being staked and by decreasing potential losses for attackers.

#### A Potential Solution
To solve this critical problem of PoS, here at Everett, we are developing a decentralized protocol named Everett Protocol that can be used to create a secondary shadow token backed by the staked base tokens. The shadow token is fungible and no matter who stakes, they will all receive the same tokens. It is also one-to-one price pegged to the base token by design so that price differences between the shadow token and the base token creates arbitrage opportunities in the protocol that maintains the peg.

Our proof of concept implementation on Cosmos, bATOMs (bonded ATOMs) was made during the 2019 Cosmos Seoul Hackatom (which we won the 1st prize). Our aim is that ATOM delegators could generate bATOMs from their delegation positions and use those bATOMs to invest/use in various Cosmos dApps (e.g. provide liquidity to a Cosmos version of Uniswap, Open a CDP on Kava etc.). We believe by doing this PoS blockchains can achieve a higher level of security without hurting developments in the ecosystem and also help achieve higher security with a lower inflation rate.
