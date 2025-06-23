+++
title = "Blockchains Are Inevitable"
date = "2025-06-23T00:00:00+00:00"
+++

For builders deep in blockchain work, it's a frequent occurrence - usually when deep in their career or in times of burnout - to question whether their work even has any meaning at all: something along the lines of "ok, blockchains / crypto / cryptography / new mechanisms / blockchain-native apps are cool and all and I find them very interesting, but what am I really doing here? Does trustlessness / open systems even matter at all? Do regular people even care? Am I even creating value to society?". 

{{< figure src="/images/blockchains/blockchains.png" width="300" >}}

This writing is to present a new mental model of understanding the value of blockchains. This is not about presenting vague values like "trustless, open systems with self-custody is good" - while they definitely do provide strong values to society, such reasoning lacks explicit, quantified value propositions. And thus they usually do not aid in rescuing an individual who's already in the state of questioning their own work. 

Instead, one of the most compelling arguments for blockchains is this: **Blockchains are a more cost-efficient system of handling data.** 


&nbsp;

## The intuition

Imagine a simple comparison of 2 data management systems, one being a simple centralized server and the other being a decentralized system of distributed computing nodes with added consensus (i.e. blockchains). 

We can now perform a cost analysis - but aside from obvious computing costs, we must also consider **1)** cost of human intervention in case of system failure, **2)** resulting value losses from system failures, and **3)** consensus costs. One must also note that this model of analysis is heavily oversimplified, but one must have comfort with the saying of: all models are wrong; some models are useful (and we strive to be useful). 

&nbsp;
### Option 1 - a centralized server

For a central-server system, the cost boils down to: 

```
compute_cost_per_node + probability_of_failure * ( human_labor_cost_for_system_recovery + cost_of_failure_itself )
```

**Note**: Multiregional SQL systems (e.g. Spanner, Aurora, Cockroach, etc.) also hit five-nines, but still fall inside their owner’s trust bubble. Once we include such owners in the failure model as well, such single-party dependencies now also fall under probability_of_failure. Obviously, there is no absolute need to always include them in failure probability - there are many, many cases where such trust dependencies are perfectly fine, but there are also many cases where it's not. 

&nbsp;
### Option 2 - a blockchain

And for a blockchain: 

```
number_of_nodes * compute_cost_per_node + consensus_cost
```

**Note**: `probability_of_failure` of blockchains never actually hits zero. Fat finger mistakes, protocol bugs, or world war 3... can still nuke all replicas at once. But the probability generally drops superlinearly with `number_of_nodes`, so in this simple model the expected hit falls off a cliff. In addition, L2s / rollups and shared sequencers are essentially attempts to further slash `consensus_cost`. 

&nbsp;

For PoS or PBFT chains, `consensus_cost` is a combination of: opportunity cost of locked capital (staked tokens) + networking overhead. For PoW chains, `consensus_cost` is the electricity costs of mining. This simplified mental model is more effective for PoS / PBFT, but that's where most infra developments are heading to anyways. 

Now on the individual values of the model: 

- `compute_cost_per_node` is exponentially **decreasing** every year with technological advancements (e.g. Moore's Law)
- `human_labor_cost_for_system_recovery` is linearly **increasing** every year since **1)** as systems get more complex, top percentile talent with such knowledge gets scarcer and thus more expensive, and **2)** human-driven politics in general pushes for raw human labor to be more valued (e.g. minimum wage increases)
- `cost_of_failure_itself` is also **increasing** with time as regulatory penalties for system failure and reputational burn is getting costlier over time
- `probability_of_failure` and `consensus_cost` have system-specific dependencies and thus are not targets of generalized analysis

Societies in the past operated with high computing costs but cheap human labor costs. During those times, it made sense to operate everything centrally - it was just cheaper to do so. 

&nbsp;
## Blockchains are an inflection point of society

However, we no longer live with the same cost assumptions. Our modern societies - with drastically cheaper computing and more expensive humans - have reached an inflection point where for specific systems and data types it now makes sense to switch to a newer model of operation. Blockchain cost savings have now just begun to make sense starting with high-value data, but with the computing / human cost trends further progressing with time, an increasing number of systems would receive cost-efficiency gains by switching. 

Some specific examples of today are: 
- **Financial data.** Failures on centralized management have extremely high recovery costs, both for system restoration and the cost of failure itself (lawsuits, fines, etc.)
- **Bitcoin's ledger** data and its immense value of enabling a highly neutral asset without a central authority is worth it even with extremely high consensus costs of PoW

Diving a bit more deeply into the financial data example, think of it as **bureaucracy vs. silicon**. Banks stay honest by piling on intentional bureaucratic complexity. When you have ten humans eyeballing and signing / stamping every big transaction, fraud needs ten insiders. Blockchains recreate that same bureaucratic firewall but with code - thousands of nodes gossip the state, crosscheck each other, and only then seal into a block.

The difference is price and speed. Humans validate in days and bill by the hour; computers validate in seconds and bill in fractions of a cent. Same effect of deterrence, but now orders of magnitude cheaper.

&nbsp;
## The acceleration

And with the continuation of mentioned cost trends (and with further advancements of practical cryptography), the data types can drastically expand to practically everything - app data, identity information, supply chain provenance, etc. There will however always be some data types that never fit for blockchains, no matter what the cost benefits are. 

In a world where compute is cheap and human time is the Louis Vuitton, it’s just simpler and cheaper to let machines shoulder the trust. Blockchains just represent an inflection point in society - being the logical endpoint of cost curves we’ve been trending on for decades. 

So when the burnout hits and you're wondering what the point of your work is: you're not evangelizing some vague speculative ideology. **You're literally coding the replacement for expensive human bureaucracy at the exact historical moment when the cost curves finally make it inevitable - the only logical response to computing getting cheaper and humans getting more expensive.** Even if the market doesn't care about manifestos - it cares about costs. It's just math - the same unstoppable math that killed film cameras and landlines.

&nbsp;