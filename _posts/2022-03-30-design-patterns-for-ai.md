---
layout: post
title: Design Patterns for AI
date: 2022-03-30
description: We need to transfer existing design patterns as far down the stack as possible.
categories: [ai, reflection, ideas]
tags:   [agi]
---

Here's how I'm approaching the problem of building artificial general intelligence:

Engineering generally starts off with a few high-level abstract ambitions that are refined and translated with increasing clarity into physical realizations. In software engineering, the outputs of this process are rendered into unambiguously crisp executable statements. In an agile environment, the entire software engineering process is iterative with loops of increasing frequency over the project lifespan and tools automating this optimization (compiler chains, code optimization, high-level languages) operating at progressively higher-levels further reducing the idea to implementation transit time. Now, when neural networks are the focus of software engineering, translation from informal to unambiguous specification is almost immediate (given sufficient understanding of programming, math, deep learning, and thermodynamics) and then the brunt of effort shifts (as it rightly should) to actually testing deep learning hypotheses. Finally, restricting the problem space to 'human-level' or 'general' artificial intelligence, this demands attempting to consolidate as many ideas in neuroscience, cognitive psychology, and artificial intelligence as possible into a working system implementation. While this consolidation appears deceptively simple in literature, the constituent ideas are easily lost in implementation[^1]. Still, the diverse array of tools and techniques which ML has developed represent orders-of-magnitude learning efficiency gains over independent effort. Ever striving to maximize the efficiency with which meaningful information can be infused into a system recommends riding on the energy-momentum of hundreds of thousands of researchers (and zillions of FLOPs), that is, incorporating permutations of as many ML research outcomes as possible: codebases, pretrained models, individual weights, architectures, training paradigms, existing datasets, and environments all guided by machine and human intuition. Following therefore, I explicitly list several observations and ideas below to help remind myself of the cognitive dynamics I desire to instill in increasingly general AI:

- Definite (e.g.: boolean) logic is inconsistent. Thermodynamics -- rather than logic -- governs the mind. Logical thought only emerges as a dissipating low-entropy trajectory.[^2] It seems reasonable then to devote more compute to System I-type components than System II-type components

- Differentiation evolves representations from vague to crisp culminating in perceptions and actions. Actions (thought words, decisions, motor activity) may modify the world state and destroy their causal crisp representation thus restarting the process.[^2]

- Synthesis integrates bottom up signals into composite models. Layer units activate if both a top-down model predicts their activation and a bottom-up signal initiates it. Top-down models compete to 'explain' a signal and sharpen their precision (cognitive niche) when correctly explained. They gradually loosen their precision if they cannot explain a bottom up signal field. If no sharp models explain a bottom up signal, then imprecise general models become competitive. I think model-signal similarity should be measured by $$KL[p_{bu} \vert \tau_{td}]$$ which heavily taxes precise models that get selected when they predict low probabilities but true signals have high probabilities. $$\tau_{td}$$ might be learned by a slower optimizer in resemblence of TRPO or SimClr. Only the winning model gets optimized by the signal. Loosing models increase their variances.[^2]

- Heterachical competition requires computing 'explanatum' (the model's predictive accuracy for an input signal normalized over all higher nodes offering predictions) for each unit-model connection. Since explanatum is softmaxed, it may be rolling-averaged as a nice coefficient $$a \in [0, 1)$$ to inform model optimization and growth.

- Real neurons don't reproduce (they're simply in abundance and specialize), but the architecture I am describing should only be as complex as necessary. Therefore, models (units with efferent td connections) should binary fizz when their explanatum score $$a$$ is high. Children can share identical parameters and connectivity since random noise should quickly break their symmetry.

- The Gaussian may only represent a small amount of data distributions, but deviations from an estimated and actual distribution are always Gaussian. Also variances. I'm not sure about higher-order moments.

- Dynamic precision training: start training at 32bit, shrink to 1bit for most pre-training, fine-tune back at 32bit. With 1bit networks at criticality, the network gets the maximum computational power out of its physical substrate, and critical dynamics should translate these gains into learnable logical flexibility. Maybe just stay at 1bit.

- If using 1bit representations, maybe have each unit transmit a vector at a time.

- Biological synaptic distribution is exponentially bimodal. I should recognize this by federating the weights into a few large neurons and many small connectivity neurons. This may reduce to sparse scattered (global connectivity) and fixed conv (local connectivity) layers.

- Sparse connectivity is essential, but some local dense connectivity may complement it.

- Maybe initialize the network with subgraphs taken from liquid state machines or from connectome research.

- Look beyond the computational realization of memory-compute. Maybe neurons exist in a geometric-structured field instead of being entries in an euclidean structured tensor? This allows for dynamically moving neurons, adding neurons, and deleting neurons.

- Look beyond statics to focus on system dynamics. Forget feedforward solutions.

- Integration -- which is not directly solvable like differentiation -- represents tremendous complexity reduction. Try to integrate this behavior into the system dynamics perhaps with a differentiable form of Risch's algorithm or taking advantage of Fourier or Laplace transforms (with inverses)

- Use the log-form of geometric mean to allow networks to selectively multiply or add incoming weights.

- Regularize synchronization and low entropy into the dynamics to favor system-II-type distributed trajectory emergence. Is their a way to estimate entropy empirically? For known distributions, yes (eg.: assume signals represent actual-expected input. THen they are normal with known confidence intervals.)

- Design the system to generate minimal activity at each realization level: minimal distributed trajectories, minimal activations, minimal structural connections.

- Prediction and reward maximization may supply the bulk of training information. However include maybe 10% data from more structured forms like task-specific probes and decoders as well as intrinsic behavioral objective satisfaction.

- To take advantage of existing pretrained models, other architectures, and for research and development convenience, make the above SOMPNet layer able to interface with other SOMPNet layers, DL layers in general, and python functions in a pythonic interface as if they were directly expressed in math.

- [Memorizing transformers](https://arxiv.org/pdf/2203.08913v1.pdf) perform nondifferentiable knn search over long trajectories. This allows agents to have very short soft attention sequences. A developing agent should  progressively utilize longer and longer hard attention.

- Agent Organization
  - botttom up observation and independant abstraction
  - top down action, forcing the world to be the way the agent thinks it should be
  - side communication. When agents have a strong idea of what's going on, they should broadcast it to their peers.

- Maybe represent everything by SDR of binary probits. This allows concretely defining entropy, KLD, and other metrics, it has low overlap and all the other benefits of SDR's, and it's easy to implement and might even scale to lower and lower precisions until it can work at single bit-level representations (classical SDR's). Maybe there's a way to make the precision dynamically determined (like entropy). Train a neural-CPU on the floating point data, and then whenever the precision reaches one bit, run the neural CPU instructions directly as machine code.

- Model capacity should grow linearly with experience. Ideally, this would take place continually and online. However there it seems more efficient to parallelize data collection (policy usage) and then make training and architectural changes offline. 

- While philosophy gets us nowhere, it is good to keep in mind relevant analogies to the AI system to guide creative design. For example, pain might be construed as a negative reward, and unselfish love, the objective of optimizing the loved object's objectives. Epistemic entropy minimization is to curiosity as high entropy combined with mutual information between internal states over time is to consciousness. Art is about engineering aesthetic qualities into observers' perceptions, and science is the perception of humanity as a whole.

- The AI should interact with the world in a way that is intuitive and natural for its own cognitive architecture just as we humans do with our bodies. Alternatively, for any given world interface (environment-body combination), the AI should be able to evolve its brain to conform to that interface.

[^1]: I know all the cuts to make before I enter the shop, but sawing for 2 hours leaves me exhausted and I end up incorrectly measuring or cutting material unless things are marked correctly.
[^2]: ["Neurodynamics of Cognition and Consciousness"](https://link.springer.com/book/10.1007/978-3-540-73267-9) ch.1, 5

**More notes [here](https://jacobvaldez.notion.site/AI-Musing-657e00cab4754dcd8f0c06088f374474)**