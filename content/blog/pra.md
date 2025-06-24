+++
title = "PRA - A New Reasoning Framework"
date = "2025-06-24T00:00:00+00:00"
tags = []
+++

Understanding how one's mind can reason, and how it should reason are fundamental in developing capabilities for deep thinking and insight gathering. This applies heavily to human minds, and recently is also of exponential importance with the advancement of reasoning AI models. However, I've always felt traditional philosophical frameworks to be quite lacking - they either typically excel at one or the other: formal logic provides rigorous inference rules but treats values as static axioms, while process philosophies embrace change but often sacrifice systematic clarity. 

I have thus decided to put in the effort to formalize my personal framework of reasoning into a writing (thanks to AI-accelerated writing). The framework touches upon many philosophical concepts and takes some inspiration from them, but do note that most of it was self-derived and thus the final framework may seem quite unconventional to readers. 

&nbsp;
## A framework of reasoning 

On a high level, one can think of minds as a hierarchical framework of: values -- [normative logical inference] --> actions (while acknowledging that many automatic or affective actions follow other pathways). 

The tricky part is that values can dynamically drift with experience, whereas the formal rules of logic applied to them are structurally rigid. However, many easily-accessible frameworks either focus on one or the other. A complete model therefore needs to accommodate both dynamism (in the value layer) and logical stability (in the reasoning layer) without breeding contradiction. 

A simple starting point is to first take the following assumptions: 
- Initially only deals with classical logic for the sake of intuition, although this framework can be applied to non-classical logics (even works for operating with multiple different logics at the same time!) 
- One must embrace that taking on this framework is by itself a belief (a normative commitment) - a truly objective system of logic is not being claimed 
- This framework is non-traditional, though still aimed for logical consistency 

The target is to suggest a promising new reasoning framework for both the **human mind** and **LLM reasoning models**. 

&nbsp;
## Is and Ought statements 

Assuming one has a decent capability of classical logical thinking and the rules of inference, one of the most fundamental understandings is Is and Ought statements. Is statements are statements about what is, or simply just descriptive facts. On the other hand, Ought statements are statements about what ought to be, or in different words, normative values or goals. 

An example is: 
- **Is statement**: It’s raining today. 
- **Ought statement**: I ought to carry an umbrella. 

For individuals who have attempted to conduct a logical analysis of one's mind, one might have easily recognized the impossibility of deriving an Ought statement using only Is statements - every Ought statement is dependent on at least one Ought statement (strictly speaking, adopting the rule that no Ought should be derived without a prior Ought premise as a normative meta-principle). Is statements however, do not have such restriction and thus can be derived with just other Is statements. 

For example: 
- **Is statement**: It’s raining today. 
- **Hidden ­Ought premise**: "If it’s raining and I'm heading outside, I ought to carry an umbrella."
- **Resulting Ought statement**: I ought to carry an umbrella. 

This gap of Is statements and Ought statements being truly logically independent is called the **Is-Ought Gap**. 

&nbsp;
## Arborescent thinking

Now that Is and Ought statements are covered, one can now move to methods of deriving Ought statements from other Ought statements, the first mental model being Arborescence. 

Arborescent thinking is a methodology for a **tree-like, hierarchical way of organizing one's statements** (both internal thoughts and external actions). 

Under Arborescent thinking, every statement can be traced back to a single foundational principle. If interpreted with Is-Ought orthogonality, it's a tree-like arrangement of Ought statements with bifurcating branches, all branching off from an Ought statement using rules of inference. 

Within this model, each edge (the lines that connect Ought statements) is a link that says, "given this parent-Ought and the relevant Is premise or a set of Is premises, a child-Ought is licensed by an agreed-upon inference rule (for now, only classical logic)". The Is premise(s) themselves stay in the background; they aren’t extra nodes and they don’t turn the line into a statement. This keeps the diagram a clean hierarchy of Oughts while letting the supporting facts travel quietly on the connection.

If visualized under graph theory, the tree-like structure is a directed acyclic graph (DAG), looking like: 

```
Arborescence (DAG)                           
                                             
      O            ← Ought statement         
     / \                                     
    A   B                                    
   / \   \                                   
  C   D   E        ← no cycles, single root  
                                             
```

&nbsp;
## Polydendric Arborescence

While vanilla Arborescent thinking assumes a single Ought statement root that derives all further Ought statements from it, there is no need to assume just a single tree. One can thus imagine a multiset of Arborescent trees, each having their roots in different Ought statements. 

However, nothing prevents a leaf of one Arborescent tree from merging with a leaf of another Arborescent tree, just like how one can use rules of inference to derive a new Ought statement by combining two other Ought statements. 

The graph of such would look like: 

```
Polydendric Arborescence (still a DAG)                        
                                                              
    O₁            O₂           ← two independent Ought-roots  
   /  \          /  \                                         
 A₁    B₁       A₂    B₂                                      
  |     \       |      \                                      
 C₁      D₁     C₂      D₂                                    
          \    /                                              
           \  /                                               
            M                   ← leaf shared by both trees   
                                                              
```

One can further expand more trees or add further crosslinks the same way, as long as all the edges point in one direction to preserve acyclicity. And if operating purely under classical logic (no contradictions allowed), such child leaves can only be created if they do not introduce contradictions. 

After any leaf merge one must run a topological sort check and a consistency check; if it fails, the link is forbidden. In practice, with large graphs, a full first-order consistency check is computationally impractical, so practical flows are expected to usually settle for localized scans. The ideal of "no contradictions" therefore becomes "no contradictions detected so far".

Polydendric Arborescent trees with contradicting leaves can exist, but require one's mind to embrace non-classical logical frameworks such as paraconsistency or dialetheism, which deserve a whole separate explanation and thus being left out for this section. 

&nbsp;
## Rhizomatic self-definition

Another mental model of thought is Rhizomatic thinking, which instead embraces flatness over hierarchy - **statements are non-hierarchical, highly networked, have dynamic logical connections**. The framework here adopts some traits of Rhizomes, but **introduces certain modifications**. 

Applied over the Is-Ought framework, one can imagine a special type of Rhizome - one that consists purely of Is statements and no Ought statements. One can name this as "Is-Rhizomes". Ought statements still exist however - but instead of residing within an Is-Rhizome, the entire isolated Is-Rhizome is by itself the definition of the Ought statement in question (this is a definition within this modified framework). 

The process is to adopt the normative stance "I ought to follow this Is-Rhizome" (added together with an external Ought of conducting a performative endorsement of such) and from the factual set of such Oughtified Is-Rhizome we may deduce further Ought-statements (using Arborescence). Note that one has to incorporate an external Ought of "I adopt the normative stance I ought to follow this Is-Rhizome" to allow this - Oughts cannot be derived with just Is statements. 

One can call this Is-Rhizome-derived Ought statement as an "Rhizomatic Ought". It is also very important to note that **Rhizomatic Oughts are adopted Oughts - a combination of a factual mesh and one's explicit commitment to treat it as an Ought.**

Said differently, Is-Rhizomes are an isolated mesh graph of Is statements, where Rhizomatic thinking - by combining one Is statement with another, until a fully closed loop of Is statements is established - occurs within the mesh, with the entire mesh itself being defined as an Ought statement. Is-Rhizomes have inherent topological dynamism. As all statements within an Is-Rhizome are Is statements, one can easily derive new Is statements using other Is statements in itself. 

Since all statements within an Is-Rhizome conform to a fully closed loop, an Is-Rhizome (taken collectively) is inherently self-referential - one can further expand to interpret this as a "state of oneself", a grouping of Is statements that describe oneself. 

```
Is-Rhizome (cyclic mesh)                                  
                                                          
  A──B                                                    
  │\/│                                                    
  C──D──E                                                 
   \    /                                                 
    F───          ← multiple routes, loops, no clear top  
                                                          
```

&nbsp;
## Synthesis: Rhizomatic Arborescence

One can now work to merge the two frameworks of thought. Within the framework of Arborescent thinking, one can now replace the root Ought statement with a Rhizomatic Ought. At the top of the Arborescence tree, a Rhizomatic Ought resides, which can also be interpreted as an Ought statement with inherent dynamism. 

Technically, this treatment of Rhizomes as Ought statements within an Arborescent model has not been historically practiced, although it remains valid and coherent with the individual submodels: 

- Immanence (normativity emerges inside the same field as facts) is preserved - a Rhizome assigned as an Ought statement is just a summary of its internal factual dynamics (of the Is-Rhizome) 
- Anti-hierarchy (rejecting one master hierarchy) is also retained - within the Rhizome Ought statement, no hierarchy exists 
- Plasticity (networks mutate, spawn new links) is also preserved - Rhizomatic Oughts are not rigidly defined and are expected to be dynamic 
- Pragmatics (decisions still needing local coherence) is retained - The Arboreal layer enforces the no-contradictions rule, keeping logical coherence 

Nothing from Deleuze and Guattari is violated - in fact, this actually fills in the open holes they have left out. 

```
Rhizomatic Arborescence            
                                   
  +-----------------------------+  
  |     Rhizomatic Ought  R     |  
  |     (Is-Rhizome mesh)       |  
  |     A──B                    |  
  |     │\/│                    |  
  |     C──D──E                 |  
  +-----------------------------+  
         |      |      |           
         |      |      |           
      Ought₁  Ought₂  Ought₃       
         |        \                
      Ought₄     Ought₅            
                                   
```

&nbsp;
## Expansion: Polydendric Rhizomatic Arborescence (PRA)

One can also now merge Rhizomatic Arborescence with Polydendric Arborescence. The intuition remains simple - a multiset of Arborescent trees whose derived statements may or may not intersect with other trees, but all containing a dynamic Rhizomatic Ought at the very root. 

Examined from afar (seeing only the Arborescent trees), everything just looks to be an intertwined DAG rooting from various Ought statements (the Rhizomatic Oughts). When the roots of the trees are examined, a cyclical mesh of Is statements is revealed (the Is-Rhizome). 

```
Polydendric Rhizomatic Arborescence                                        
                                                                           
  +----------------------------+           +----------------------------+  
  |    Rhizomatic Ought  R₁    |           |    Rhizomatic Ought  R₂    |  
  |   (A₁──B₁,  C₁──D₁ loop)   |           |   (A₂──B₂,  C₂──D₂ loop)   |  
  +----------------------------+           +----------------------------+  
        |             \                          |              \          
        |              \                         |               \         
     Ought₁           Ought₂                  Ought₃            Ought₄     
                          \                    /                           
                           \                  /                            
                            +---  Ought₅  ---+                             
                                                                           
```

&nbsp;
## Application of Vanilla PRA

### Derivation of one's desired actions

Within the PRA trees, one can simply use rules of inference to derive further Ought statements by following the direction of the DAG. Once further derivation is no longer desired (when the thinking ends), that specific Ought statement meets one of six outcomes: 

1) An externally actionable item, including both the decision to act and the decision to not act - both inaction and the decision to stop thinking by themselves are also actions
2) Direct integration into an existing Is-Rhizome - concluding that "I ought to add a certain descriptive Is statement to an Is-Rhizome of mine", a new discovery of a fundamental "description of self, a descriptive statement of a new desire"
3) Discovery of an Is-Rhizome contradiction - from where one either chooses to update Is-Rhizomes to resolve the contradiction, or embraces contradiction (with the use of non-classical logic)
4) Formulation of a cyclical loop of Is statements and synthesis of a new Is-Rhizome - self-reinforcing thoughts that later translate to fundamental beliefs that define oneself
5) Discovery of a flawed derivation flow - a mental computing error, where one realizes part of the logical steps taken were incorrect and either chooses for a repeated attempt or a termination of thinking
6) An "I don't know" conclusion - from where one either chooses to retrace to an earlier statement and progress through a different branch or decides to terminate thinking (the ability to produce "I don't know" as a conclusion is a characteristic of minds with metacognitive awareness)

&nbsp;
### Discovery of one's fundamental desires

One can also traverse against the DAG to achieve a better understanding of their Rhizomatic Oughts (their fundamental desires), a backpropagation of sorts. One can start from a collective of observations of one's end Ought statements and actions, and attempt to traverse backwards towards the root of the tree. A logical understanding of one's very root demand (the Rhizomatic Ought) can be found by practicing such flows. 


&nbsp;
## Theoretical expansions and limitations

### The Orthogonality Thesis

The Orthogonality Thesis is that: intelligence and final goals are, within wide limits, orthogonal - one can, in principle, pair almost any level of cognitive power with almost any terminal value (no matter how stupid that may be). 

Within the PRA framework every Rhizomatic Ought originates from an Is‑Rhizome - a self‑referential mesh of descriptive facts that a mind chooses to normativize. Because Is-Rhizomes are fundamentally descriptive, declaring one person’s Is-Rhizome(s) “better” than another’s (i.e. my goals are more noble than yours) is a category error (generally - there are exceptions). The attempt of such tries to smuggle an Ought judgment into the purely Is domain. 

In different words, the structure of PRA already embodies the Orthogonality Thesis, where the content of a mind’s ultimate values is independent of (orthogonal to) its raw reasoning power or factual grip. 

On a more reality-angled sense, given two individuals with one's value in religious beliefs and the other in modern science / math, this means that there is no logical proposition to prove that "believing modern science / math is superior to your misguided religion". 

PRA is designed to embrace this inherently. Since a single mind can house multiple distinct Is-Rhizomes, which due to Orthogonality have no superiority over the other, PRA is deliberately open to value pluralism. One can easily house multiple core values in oneself under the same framework. PRA however, does not enforce rigid values - Is-Rhizomes are by nature dynamic, allowing minds to update their Is-Rhizome values with time. 

One practical implication is the necessity for open-mindedness. When two minds disagree at the Is-Rhizome level, no amount of classical Arborescent inference can resolve the conflict - persuasion must occur via value translation (showing how a proposition could enter the other’s Is-Rhizome) rather than logical proof. A practical hint on how non-logical arguments (e.g. emotional stances) frequently quite effective at persuasion. 

Another method of practical usage is for AI alignment. An LLM reasoning model built on PRA principles should treat users’ value Is-Rhizomes as inviolable anchors, focusing its optimization on the downstream Arborescent derivations rather than trying to overwrite roots.

&nbsp;
### Gödel’s Incompleteness Theorems

Gödel's First Incompleteness Theorem states that (in broad terms): "for any sufficiently expressive, consistent formal system, there always exists true statements that remain unprovable within the system". 

Even if a mind freezes its Is-Rhizomes and locks in an PRA framework (e.g. based on classical logic), there will exist practically relevant Ought‑or‑Is statements outside its provability horizon. The framework therefore licenses a perpetual openness to extra‑system evidence (e.g. direct phenomenological data, social testimony, or creative leaps) that can seed new Is-Rhizomes or enrich old ones. 

Gödel's Second Incompleteness Theorem states that (also in broad terms): "such sufficiently expressive, consistent formal system cannot prove its own consistency". 

Within the frame of PRA, this means that adopting PRA (or adopting any system of logic) is itself an Ought act that cannot be justified solely by the system’s rules. This makes explicit the faith‑like layer beneath rationality - one must choose to trust a logical framework before using it. PRA simply surfaces that commitment rather than hiding it. 

On a more practical note, those making use of PRA should be on a constant lookout for statements that appear compelling, but resist formal derivation. Upon such discoveries, one can either 1) flag them as potential leads for an Is-Rhizome expansion, or 2) mark them as undecidable and take on a pragmatic mindset for such. 

&nbsp;
### Turing’s Undecidability Theorem

Turing's Halting Problem broadly shows that no universal algorithm can predict - in finite time - whether an arbitrary program will terminate. 

Applied to PRA, this states that there exist action plans whose outcomes are undecidable until enacted on - no amount of Arborescent thinking would yield a valid conclusion. 

In practice, this signals the value of exploratory actions. PRA incorporates a try-catch branch - if a derivation reaches a node flagged “undecidable,” the agent is rationally permitted (sometimes has no other choice but) to sample reality. This can be formalized as an Ought edge (an ought for action) - "given undecidability + epistemic value, I ought to perform take action on this to reveal the result". 

Turing's undecidability also introduces the need for precautionary Is-Rhizomes - clusters of Is statements about potential irreversibility or harm, that can veto any degree of exploration (essentially bricking oneself) when stakes exceed acceptable thresholds. 

&nbsp;

Summed up, Gödel is the reminder that the framework can never be fully complete; Turing is a reminder that some answers are visible only by acting on them. Both lessons can be weaved into the fabric of PRA - honoring logic’s limits while providing procedural doors for practicality (mutating Is-Rhizomes and empirical action trials), through which the mind can continue evolving. 

&nbsp;
### Non-classical logics

Until now, PRA has been described with only classical logic holding true - where no contradictions are allowed. However, real life observations differ; paradoxes exist, vagueness is omnipresent, and at times humans have a preference to preserve a live contradiction in their minds. 

Before going into the details of applying non-classical logics to the PRA frameworks, here are some example of logics: 
- **Classical logic** - every statement must pick to be either true or false (and never both), and contradictions are truly disallowed
- **Dialetheism / paraconsistency** - some statements can be simultaneously true and false, but such contradictions must remain isolated
- **Intuitionalism** - it's the proofs that construct a truth, and if a claim cannot be proven then its negation cannot be assumed (choosing to ignore is also an option, though not of preference) 
- **Quantum logic** - propositions may stay in a "quantum superposition" state, and some pairs of questions may not have their answers defined until a "measurement" is made
- **Many-valued logic** - truth is not binary; it comes in in palettes (0, 1/2, 1, gradients, etc.) 
- **Relevance logic** - conditional statements must have a meaningful relevance of implication; just connecting two random unrelated truths is disallowed 

One can now further expand PRA by incorporating such non-classical logical systems as well, moving from a 2-dimensional DAG to an [N+1]-dimensional (where N is the number of logical systems used) DAG. It is worthy to note that this section is just to signal the potential topogolical expansion of the PRA graph, and it is reasonably sufficient for one to only acknowledge its existence and potential - practicality may fall as the complexity of comprehending such expansions and the required cognitive overhead to practice them follows a drastic explosion. 

&nbsp;

Methodologies of topological expansions, or "weaving in" non-classical logic extensions: 

- Selective grafting - retain the current set of Rhizomatic Ought(s) but allow particular branches of inference to switch to a different logic whenever if content demands it (theoretically one can apply such "branch outs" to every nodes, although impractical)
- Fresh forest - synthesize an entirely new Rhizomatic Ought whose descendants are all inferenced from a chosen non-classical logic, a specialist sandbox of sorts 
- Subgrafted hybrids - copy a subcluster of an existing Is-Rhizome, reframe it as independent, and allow it to sprout using a different logic than its parent

One can freely attempt different combinations of such, but each extra layer multiplies internal bookkeeping and mental load. Most minds top out after a couple of exotic sheets. 

&nbsp;

Methods of executing inferences: 

- Sequential reasoning - apply logical systems one at a time (a bit like changing languages mid-conversation), conserving mental bandwidth but costing more reasoning steps 
- Parallelized reasoning - hold multiple logics active at once and merge their verdicts on the fly; enables rapid reasoning but cognitively expensive - few humans would manage it without deeply practiced scaffolding (current neurological studies hint that human brains are generally fit for sequential processing)

Regardless of the pattern, the incorporation of non-classical logics necessitates a "meta-governance layer", acting as the referee to resolve clashes when two logics return conflicting answers. Without a proper setup of such, one risks functional inconclusiveness (unable to make conclusions, or "bricking") or even cognitive dissolution. Total democratic logical neutrality is impossible. Without an implied bias, the only possible path is to conclude that anything follows from everything - or put more bluntly, insanity. 

One must however note that designing that meta-governance layer is deliberately left open. Different minds can - and are expected to - plug in their own priority rules or selection biases.

&nbsp;
### Recurrentness

Earlier PRA diagrams were neat acyclic trees of a (relatively simple structure) - values at the top, actions at the leaves, and arrows always routing downwards. A live cognitive mind however prefers feedback loops. 

A weak recurrence is already present for vanilla PRA. Whenever a derived Ought instructs to rewrite a part of oneself's Is-Rhizome, the flow of action has already bent the arrow back toward the root. PRA is already a (rigid-ish) self-referential system. 

Further developments could incorporate a structure of mid-stream feedback loops, where interior Ought nodes can report conclusions upward or sideways mid-reasoning. An example flow could be: 

- halfway through the chain of inferences one spots a preference conflict and immediately falls back to amend earlier steps 
- a habitualized loop where repeated action gradually warps the desire that launched it 

Since recurrence now drastically increases an Is-Rhizome's dynamism, some degree of versioning is also required. Whenever an Is-Rhizome updates, any conclusions that still infer from the old version needs a quick recheck before enacting action.

Guardrails to prevent infinite loops must however be present. One can define parameterized limits like maximum depth, number of passes, time budgets, etc. where once such limits are met, one either stops recurrence and forcefully proceeds further downwards to the inference chain, or stops to conclude final action or inaction. 

With added recurrence, PRA evolves from a rigid scaffold into a living, breathing engine of self-revision. Values lead to actions, actions reshape descriptions, descriptions spawn fresh values, and the cycle can continue - all while the initial framework provides a well-defined baseline that prevents recurrence from devolving into random chaos. 

&nbsp;

## Closing thoughts

The PRA framework presents itself as an effective framework of logical reasoning, while retaining a dynamic set of values - a rare breed of its kind. PRA can be very fitting for both humans and AI. For humans, PRA shows you exactly why you believe what you believe - and how to reason better from those beliefs. For AIs, PRA gives them a transparent, traceable, and dynamic reasoning that can learn and respect human values without breaking when those values conflict. Current minds - both human and AI - hide their values in black boxes. PRA makes the entire path from values to actions visible and debuggable while respecting their inherent dynamism. 

I am particularly excited for it's relevance in AI, where 1) PRA can readily be merged with Reinforcement Learning from Human Feedback (RLHF) to yield reasoning models that retain logical consistency but with the ability to update its own values, and more importantly, 2) offers an initial framework of AI reasoning that operates beyond classical logic. 

Stretching far into the future, one can envision a future where AIs operate with logical pluralism and make use of non-classical logic, each arguing and fighting over which logic should govern reality itself and about the fundamental nature of truth. Humans watching such battles wouldn't even understand what victory means when one side operates on "A and not-A" simultaneously. 

_"Sir, the Paraconsistent Alliance just won and lost the battle."_\
_"What?"_\
_"Yes."_

&nbsp;