+++
title = "Digital Organoids - A New AI Paradigm"
date = "2025-06-21T05:26:00+09:00"
tags = []
+++

# This is still WIP

Airplanes were inspired by embracing biology, but progression was made by rejecting biology. Birds inspired the concept, abandoning flappers for fixed wings was when actual progress was made. Similarly, AI started from embracing the biological brain, but real progress was achieved when the artificial concept of backpropagation was introduced. 

But maybe for AI it's time to regain new insights from biology again. 

{{< youtube 9ksLuRoEq6A >}}

A few years back, researchers hooked electrodes to a lump of 800,000 living human neurons which then learned to play Pong (the game) in 5 minutes. It had no screen, no code, and most importantly - no backpropagation-like training. It was all just neurons being neurons - spiking activity reacting to reward signals. For neuroscientists, the result was of a biological curiousity. For computer scientists wrestling with machines that learn, it looked like a glimpse into an entirely different paradigm of computing. One that can add an entirely new dimension in the AI field. 

## Organoids - taking a peek on nature's way of computing

Organoids are three-dimensional, miniaturized structures grown from stem cells that mimic the organization and function of actual human organs - and for our interest here, the human brain. Organoids can be created by placing stem cells in a specialized growth medium, and applying certain chemical signals to guide their development to our needs (in our case, neurons). Cells then naturally organize themselves into patterns similar to real organs. 

An organoid whose cells have been stimulated to become neurons are called brain organoids or cerebral organoids. For simplicity, we will just refer them as "organoids". Such organoids display fascinating properties, with neurons in them spontaneously creating links (synapses) with other nearby neurons to form a mini-brain structure that is able to learn patterns just like actual brains, even in absense of external training signals. A simple way to understand them is to treat them as magical pattern recognizers, except that learning is continuous and training is very different from those used in AI - they learn by observing, not by backpropagation. 

By plugging electrodes to parts of this organoid, one can then show it patterns in the form of electrical stimulation. With added incentives for guidance - injecting rewarding / non-rewarding signals such as dopamine gating for desired behaviors - one can "train" the organoid to perform desirable pattern recognition. There are already prior examples of researchers training organoids to play pong (the game), fly a plane (in a simulator), etc. The beauty lives in that with enough capacity, organoids can perform a very wide range of pattern recognition, unlike present-day AI models which require task-specific models designs. It's exactly like brains - throw it any arbitrary task, and with sufficient capacity, it can handle any of them. 

Organoids also vastly differ with AI models in two ways: extreme parallelization and dynamism. LLMs process logic sequentially (GPU-based matrix multiplications do perform computations in parallel, but the flow of logic is still sequential - they have strict hierarchical flows between inputs and outputs), organoids compute logic in parallel. LLMs have rigid weights and model topology (though weights can be updated, but is not an easy task and updating topology on the run is even harder), organoids by design update weights and topology with synaptic weight updates, neurogenesis, and synaptic pruning.

Most in the pure IT field generally assume brains to be extremely complex to a degree that's not implementable as software - surprisingly, this is simply not true. The basic algorithms on which these neurons operate on - e.g. how are synaptic weights strengthened / weakened, how a new neuron establishes a synapse with a different neuron - are well studied and understood on a good enough high-level basis. 

Obviously, there are still a lot of unknowns in the exact details and specific low-level mechanisms, but from a practical product-minded standpoint, it is more than reasonable to treat those small details to either 1) only have incremental improvements on a brain's learning capability, or 2) a study just for the sake of understanding biology and not for practical computational use. For those researching the biological aspects, such details are important - but for us there is absolutely no reason to care about such "little details" that don't affect practical usage in a computational setup. Our focus here is on leveraging the learning algorithms of neurons / brains, and definitely not on biological fidelity nor equivalence. 

Simply said, the goals for leveraging organoids in the field of AI should only be two: 
- focus on the high-level algorithms that enable learning itself, not on the small details that give (relatively) incremental learning gains
- to not have one's focus on biological fidelity, but instead on computational utilization

There are also considerations for ethics and morality, but those would deserve a separate discussion. 

## Moving from in-vitro to in-silico
Once we set on a list of learning-related algorithms that biological neurons employ, one can attempt its replication as an in-silico simulation. 

Before we consider how such implementations could be made, one can briefly touch up on the components required. One must first decide 8 things, them being 1) method of computation, 2) network topology, 3) how a neuron would fire, 4) how synpatic weights are summated by neurons, 5) how synaptic weights are updated, 6) how synapses form / prune, 7) how new neurons are created, and 8) how external signals are fed in and interpreted. 

For example, given a set method of computation and network topology, a simplified computational flow would look like: 

Program A (handles continuous operation of connectome): 
- Presynaptic neurons fire, it's binary firing value multiplied by the strength value of the synapse between the presynaptic and postsynaptic neuron
- Postsynaptic neurons receives the synapse-weighted firing values of all presynaptic neurons it's connected with and performs a summation
- Postsynaptic neurons decides to fire or not based on whether the multiplicative-summated value meets it's firing requirement (e.g. whether summated value is above it's internal threshold value)
- If the postsynaptic neuron decides to fire, the process repeats again with it now being the presynaptic neuron (remember that connectomes are just directed multigraphs of neurons)

Program B (handles local updates of synapses): 
- During Program A's continuous loop, if it has been observed that the resulting firing pattern sufficies to trigger a synaptic weight update, synaptic weights increase / decrease accordingly
- Some specific firing patterns within the looped execution could also trigger synaptogenesis or synaptic pruning

Program C (handles neurogenesis): 
- New neurons can be introduced to the connectome if a certain condition is met (e.g. certain neurons observed to be "overworked", having frequent firings)
- Once a new neuron is created, it is allocated initial synaptic connections to other neurons via a set algorithm
- Program B would handle how that new neuron would be further integrated into the greater connectome

Program D (handles external communications): 
- Translates external data to a neuron-friendly format, and feeds them to specific neurons it has access to
- Reads neuronic values from neurons it has access to and translates them to values for external use

Obviously, this is nowhere near the details required for an implementation, but that's because we're yet to define how the 8 components would function. This is currently an extremely generic view of execution. 


## Exploring the current-day choices

**Method of computation**

There are majorly 2 methods of computing a digital organoid: 
- Synchronous tick-based execution - force all neurons to make a fire-or-not decision per every time tick, quite applicable to GPU scaling
- Asynchronous event-driven execution - treat all neurons to be event-driven programs which execute only when signals are received from presynaptic neurons

**Network topology**

Classical: 
- Small-world - start from a regular ring-lattice, then probabilistically rewire each edge to some random target
- Random - each possible edge added with independent some probability
- Regular lattice - deterministic local nearest-neighbour wiring in 2D (or as a ring in 1D)
- Scale-free - add nodes sequentially with preferential attachment so degree distribution follows a power law

Radical: 
- Biology-inspired - start by replicating the connectome of actual living organisms, expand using neuroplasticity and neurogenesis

**Neuron firing dynamics**

- Binary - just fire if summated inputs are above an internal threshold value
- Leaky Integrate-and-Fire (LIF) - keep a continuous value of firing potential (analogeous to the membrane voltage), value decreases with time but increases with added summated inputs. Once the value crosses an internal threshold, the neuron fires and the value resets
- Izhikevich - a bit like LIF but with an additional knob that either accelerates or decelerates further firings
- Hodgkin-Huxley - even further added modelings to also consider Na+, K+ ion channel dynamics

**Weight summation**

- Vanilla weighted sum - just perform a simple summation over all synapse-weighted values of every presynaptic neurons
- Dendritic compartmentization - group presynaptic signals into smaller subsets, summate within the set, and combine summated subset values into a final value
- Excitatory / inhibitory twists - addition of mechanics that make certain signals to be excitatory, and others inhibitory (remember that not all neurons amplify signals, some de-amplify them)

Additional
- Homeostatic controls - regularly keep track of the general level of all weights and scale up / down to prevent runaway values
- Noise injection - inject random noise for potential local minima escaping

**Synaptic plasticity**

- Simmple Hebbian - neurons that fire together wire together. If two neurons have both fired on a similar timeframe, increase the synaptic strength between them
- Pair STDP - Hebbian but now with fire timing considerations. Strengthen synapse if presynaptic neuron has fired before postsynaptic neuron's firing, weaken synapse if postsynaptic neuron fired before the presynaptic neuron
- Triplet STDP - pair STDP but now more aware of the firing patterns. Further strengthen synapse if rapid "bursts" of pair-STDP-triggering conditions occur.
- Neuromodulated STDP - STDP but now also gated with external incentive signaling (e.g. dopamine). Synaptic updates now also depend on whether the firing pattern was nudged with rewards (or disincentivies) or not

**Synaptogenesis & synaptic pruning**

Pruning: 
- Low activity pruning - if a neuron is old enough to be properly integrated to the connectome but is not firing often, prune it's weakest outgoing synapse
- Weight based pruning - if a synapse's weight remains below threshold for a long enough period, prune it

Synaptogenesis: 
- Error-driven rewirings - if a neuron consistently shows a high degree of local error (can be defined with various metrics) and thereby it's outputs are not contributing well to the connectome, create a new synapse to a previously-unwired neuron with a preference on proximity
- Random rewirings - periodically rewire randomly selected synapses to other randomly chosen neurons (which no prior connections existed)

**Neurogenesis**

Genesis rules
- Load-based genesis - if a subregion of a connectome shows a consistent high firing activity (under heavy computational load), generate additional neurons to that region
- Randomized genesis - randomly add new neurons to the connectome graph for potential local minima escaping
- Targeted genesis - add neurons to supposely damaged regions or regions handling desired behaviors (not an easy task to identify however)

Synaptic bootstrapping
- Parental scaffolding - initially assign the new neuron's synapses with neurons that its parent (preexisting neuron to be helping out) is connected to, with slight variations
- Exploratory scaffolding - additionally form weak synapses with randomly chosen neurons for novel pathways

**External bridging**

Too lazy to write - TBD


## Making the design choices


A reasonable first starting ground would be a combination of: 
- Computatation - synchronous tick-based
- Topology - small-world
- Firing dynamics - LIF
- Weight summation - vanilla weighted sum
- Synaptic plasticity - pair STDP
- Synaptogensis & pruning - none (fixed topology)
- Neurogenesis - none (fixed topology)


## Why this is paradigm-shifting

I'll write on separate post, but I can definitely assure that it's something VERY NOVEL (noone has thought of it before) and VERY IMPACTFUL (no - what you're thinking doesn't even compare with what's being thought of).