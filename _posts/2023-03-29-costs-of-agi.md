---
layout: post
title: The Cost of Large Scale Training
date: 2023-03-29
description: Speculative analysis on the cost of training large scale machine learning architectures
hidden: false
categories: [ai]
tags:   [agi]
---

### Statements

1. 
> I find it hard to imagine OpenAI could finance a training run much over $50m. There’s probably a good reason they recently raised more capital. \[...\] we are looking at a model with 600B-1T parameters trained on 1.5T to 4T tokens. (r/Singularity/Realistic size of GPT-4)[https://www.reddit.com/r/singularity/comments/106sd1z/realistic_size_of_gpt4/]

2. 
> GPT\[3\] has a vocabulary of 50257 words (The GPT-3 Architecture, on a Napkin)[https://dugas.ch/artificial_curiosity/GPT_architecture.html#:~:text=(GPT%20has%20a%20vocabulary%20of%2050257%20words).]

3. 
> | Cloud TPU type | v4 cores | Chips | VMs | Total memory | Evaluation price (USD) | 1-year commitment price (USD) | 3-year commitment price (USD) |
> | --- | --- | --- | --- | --- | --- | --- | --- |
> | ... | ... | ... | ... | ... | ... | ... | ... |
> | v4-64 | 64 | 32 | 8 | 1024 GiB | $103.04 / hour | $47,388 / month	| $33,849 / month |
> | ... | ... | ... | ... | ... | ... | ... | ... |
> (Cloud TPU pricing
 \#TPU Pod type pricing
)[https://cloud.google.com/tpu/pricing]

4. 
> Peak compute per chip 275 teraflops (bf16 or int8) (System Architecture \# TPU v4)[https://cloud.google.com/tpu/docs/system-architecture-tpu-vm#tpu_v4]

5. 
>  they claim that the forward pass of decoder-only Transformers involves $\approx 2N$ add-multiply operations, where $N$ is the number of non-embedding parameters in the model. (Understanding FLOPs-per-token estimates from OpenAI’s scaling laws)[https://discuss.huggingface.co/t/understanding-flops-per-token-estimates-from-openais-scaling-laws/23133]

### Assumptions

6. GPT4 cost $100m *(1)*

7. GPT4 trained on 4T tokens *(1)*

8. GPT4 uses 50k vocab size *(2)*

9. 64 TPUv4 cores cost $33,849 / month at best *(3)*

10. The TPUv4 provides 275 teraflops *(4)*

11. GPT4 has N parameters *(5)*

12. GPT4 uses 2N flops per token *(5)*

### Implications

13. 4T tokens *(7)* &times; 50k vocab size *(8)* = 2e17 bits of training data compressed into GPT4 (though many are reduntant)

14. 2e17 bits *(13)* &div; $100m *(6)* = 2Gb/$ training cost

15. 4T tokens *(7)* &div; $100m *(6)* = 40k tokens/$ training cost

16. A TPUv4 offers 275 \[teraflops / sec\] *(10)* &times; 1 month &div; $33,849 *(9)* = 2.12e16 flops/$

17. 40k tokens/$ *(15)* &div; (2.12e16 flops/$) *(16)* = 1.89e-12 training tokens / flop

18. 1 / (1.89e-12 training tokens / flop) *(17)* = 5.31e13 flops / training token

19. GPT4 uses 5.31e13 operations per training token *(18)*

20. GPT4 has 5.31e13 operations / 2 \[operations per parameter\] = 2.65e13 parameters = 26T parameters

21. GPT cost $100m / 26T parameters = 3.85e-6 $/param or cost 260k params/$

### Comments

I am only willing to spend 4k on a NN. Based on these assumptions and implications, I could only expect to train a 1B parameter model. However, that's assuming the same data efficiency and architecture as the decoder only transformer. I can utilize sparsity, like tok k layers, hyper recurrent architectures, and smart sampling to improve performance at smaller scales.

**Update (6/29/23): [George Hotz](https://youtu.be/dNrTrx42DGQ?t=5538): “Sam Altman won't tell you that GPT-4 has 220B parameters and is a 16-way mixture model with 8 sets of weights?”**