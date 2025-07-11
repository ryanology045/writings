+++
title = "[Mirror] Staking and DeFi: Can They Coexist? Part 2"
date = "2019-09-28T00:00:00+00:00"
tags = []
+++

> **NOTE: This is just a mirror of my old writing from 2019 for record-keeping purposes.**

### IMPORTANT: EVERETT IS NOT BEING WORKED ON SINCE 2020. THE CURRENT WHATEVER-THAT-IS YOU SEE ON https://everett.zone/ IS A SCAM AND NOT AFFILIATED WITH ANY OF THE PRIOR EVERETT PEOPLE - THEY ARE JUST COPYING THE EXACT SAME LOGO AND DOMAIN WE USED BACK IN 2019. 

## On Network Security

![staking-defi-2](/images/mirror-staking-defi-2/staking-defi-2-1.png)

## The Economics of Proof of Stake Security
In the previous article, we explained how proof-of-stake can negatively affect a blockchain ecosystem with its economic incentives.

However, as proof-of-stake fundamentally relies on its tokens for security, economics and market pricing fundamentally affect the security layer of a protocol.

## 1. Staking Rate Dependent on Price Movements
In the current scheme of proof-of-stake, ‘staking’ is the action of locking up tokens into the protocol. A large amount of locked tokens grant the staker a large amount of staking rewards as well as a bigger say in protocol governance.

However, this comes at a cost.

Bigger stake means bigger risk. The potential value lost for staked tokens in a volatile market is greater than the liquid tokens, as it is difficult to hedge illiquid assets. While this may not be an issue to those who hold small staking positions, it is a serious issue for those who hold large staking positions.

In the current design, the only way to hedge one’s staked assets is to either unstake and sell, or to enter a short position (and pay fees to platforms such as exchanges). For most proof-of-stake blockchains, the process of unstaking requires a ‘thawing period’ for the unstaked tokens to become liquid in order to prevent long-range attacks.

In the event that the price of the base token massively increases, some of those who staked may decide to cash out. This, in turn, causes an increase in the amount of unstakings that could happen. Although tokens that are sold are may change hands to those who purchase the tokens to stake, there exists an inbetween period where tokens are not securing the protocol.

The same problem arises when the market enters a prolonged bear market. In order for networks to remain stable, it is ideal that network security remain distanced from market conditions. However, this is currently not the case, as extended periods of bear markets lure people to sell now and buy again at a later date, causing them to unstake & sell tokens.

As security of a proof-of-stake network relies on ‘price of the token’ x ‘amount of tokens staked’, this badly affects the network security in two ways:

1. Decrease in value of the staking tokens makes for a cheaper attack
2. Lower staking rate (as people sell their tokens) leave bigger room for a potential attack on the network.
We propose that if there is a way of converting one’s staking position into a liquid asset without the need to unstake, the vulnerability of network security due to a prolonged bear market can be reduced.

If stakers use Everett Protocol to convert their staking position into liquid shadow tokens, then stakers can effectively hedge their locked tokens just by selling the shadow tokens. Preventing the need to reduce network security by unstaking.

## 2. Token Usage Decreases Security
Conservatively, many have argued that the only use-case for the base token of a proof-of-stake blockchain is to provide security via staking. While this is true, there tends to be an increased desire for individuals to reinvest their assets as value accrues to the protocol (and by extension, the token).

Therefore, the base token of a proof-of-stake blockchain will likely be used not only for staking but also act as a store of value in the network. One that is utilized as a form of currency in the network.

This already can be observed in networks like Ethereum (despite Ethereum not being a proof-of-stake blockchain) where its native token ETH, albeit being considered as a fee token in the protocol, is actively being used as a store of value & unit of account in DeFi dApps like MakerDAO and Uniswap.

However, in the current proof-of-stake design, tokens can be only staked or only used/invested in other products.

As more stakers choose to invest their tokens rather than stake, network security decreases. This creates a paradoxical situation where the usage of the token comes at the cost of network security. Ideally, token usage should not negatively affect network security, and economic limitations on token usability competing with security should not exist at all.

We propose an alternative where a shadow token created through the Everett Protocol can retain the value characteristics of the base layer token without the responsibility of a ‘staking token’.

Since the shadow tokens are price pegged to the base tokens, it is relatively easy to implement to dApps and easy for users to comprehend just like many users consider DAI and USD, WETH (wrapped ether) and ETH as the same thing.

## 3. High Issuance Rate becomes a Necessity
Proof-of-stake blockchains incentivize staking by adjusting the token issuance rate relative to the amount staked. When the staking rate is low, issuance increases. This has the effect of increasing staking incentives for higher network security.

However, the problem here is that if there is no way of utilizing the value locked up in staking positions, the network has to suffer from a higher rate of issuance in order to attract token holders to lock their tokens, rather than using them to invest/use in other applications.

An efficient validator market should contain many validators that are wishing to secure the network. A fierce price competition between validators should drive the validation cost to a minimum value.

Although most PoS networks do not rely on the free market to set the issuance rate, since it follows a function set by the protocol and thus is more similar to a planned economy. However this is still somewhat similar to the price mechanics of a free market, since the issuance rate function behaves similarly to its free-market based counterpart.

Thus to some degree, it is logical enough to apply the mechanics of a free market to the network of validators. (Validators also differ in that they do not compete to provide better services like in a free market, but their services cooperate with each other to maintain the network.)

If the usage of the base token in the ecosystem has to compete with staking, it is obvious that there will be fewer base tokens being staked. From a free-market perspective, this effectively means that: 1. There are fewer validators in the network providing security and 2. There is less competition for a lower validation cost. So in total, the illiquidity of staking positions should cause the network to have fewer validators and thus a lower security level, while costing the network a higher price by having a higher issuance rate.

Inflationary rewards can be considered as necessary expenses for maintaining the network. A high issuance rate basically means that more expenses are required for network maintenance, and as stated above, illiquid staking positions causes higher expenses for the network.

On the other hand, Everett allows for the creation of liquid staking positions which incentivizes more tokens to be staked while reducing the need to unstake for the purpose of using the utilizing the base token in a dApp or DeFi usage or investments. This should aid the network positively in this case by allowing for a lower issuance rate in total.

## In Summary
Current designs of PoS networks suffer from multiple economic-security problems. these include the network security being highly dependent on token price movements, and the usage of base tokens negatively affecting the network security by lowering the staking rate. Also, the network is forced to have a higher issuance rate, costing network participants more to be a part of the network.

We at Everett hope to solve these economic-security problems by allowing the creation of liquid staking positions as explained in this article.