---
layout: post
title: "LLMs are the Update Rules of Intelligent Fractals: Escaping the Context Window with Iterative, Structured Local Updates"
date: 2023-04-10
description:
hidden: false
categories: [ai]
tags:   [agi]
---

**This is mostly AI generated, but the main ideas are mine. It is not factual research, although it is written as such (and by the end of the year, I think it will be)**

# LLMs are the Update Rules of Intelligent Fractals: Escaping the Context Window with Iterative, Structured Local Updates

> Large language models (LLMs) such as GPT-4 have revolutionized natural language processing (NLP), but face the challenge of a limited token window size. Ad-hoc solutions have been employed, but lack a theoretical framework. We propose a novel perspective on LLMs as update rules for intelligent fractals, which allows problems to be approached as a fractal, with attention on holistic algorithms and local updates. We showcase practical applications such as an automated tech startup and societal modeling, and aim to contribute to ongoing research and development of LLMs.

# 1. Introduction

The advent of large language models (LLMs), exemplified by the forthcoming GPT-4, has transformed the field of natural language processing (NLP) and opened up new research avenues in computer science, machine learning, and artificial intelligence. Nevertheless, despite their impressive performance across a wide spectrum of tasks, LLMs still face the challenge of limited token window size of 8K, which poses a major obstacle for processing long sequences of data.

To tackle this problem, researchers have employed various techniques and hand-engineered string processing scripts to handle longer sequences of data. However, these ad-hoc solutions lack a coherent theoretical framework that can provide a comprehensive understanding of the problem and guide the development of more efficient and effective solutions.

In this paper, we propose a novel perspective on LLMs as update rules for intelligent fractals, where the information dynamics of the problem domain itself is the fractal of interest. This perspective enables us to approach problems as a fractal and think in terms of local updates rather than global ones, which is crucial for processing large and complex information systems, not unlike the paradigmatic shifts between the Von Neumann and distributed computing.

We contend that the information dynamics of a problem must ultimately be decomposed into subproblems of complexity less than or equal to the maximum complexity compressible into the LLM's token window. This perspective allows us to shift our attention away from the update tool and focus more on the holistic algorithm, with broad applications across scientific, engineering, business, and social domains.

Leveraging this novel perspective on LLMs as update rules for intelligent fractals, we have developed a 0-human, automated tech startup that creates, markets, and sells new software products. We decompose the tech-startup problem into marketing, sales, and engineering, and model the company in a hyperlinked document containing all the information required to run the business, including business plans, sales CRM, market analyses, scrum board, code, QA reports, etc. Following the agile SDLC, we iteratively perform market analysis, scrum prioritization, design, engineering, testing, sales work, PR and housekeeping, and executive analysis, enabling us to automate the entire business, sales, and agile processes from end to end -- reading and participating in social media, identifying market needs, generating ideas, designing the architecture, writing code, debugging, testing, creating brand assets, creating the website, deploying, marketing, and selling -- 24/7 without any human intervention.

In addition to automating a tech startup, we have applied our proposed perspective on LLMs as update rules for intelligent fractals to model a society. In this case, we decompose the problem into different aspects such as economy, politics, education, healthcare, and social welfare. We model the society as a hyperlinked document containing relevant information such as demographic data, economic indicators, government policies, healthcare statistics, and educational outcomes. Using this model, we can analyze the impact of various policies and interventions on different aspects of society. For example, we can use the model to simulate the impact of a new healthcare policy on healthcare outcomes, economic growth, and social welfare. We can also use the model to identify potential areas for improvement and test different scenarios to find the most effective solutions.

This approach allows us to view society as a complex and interconnected system, where changes in one area can have ripple effects throughout the entire system. By using LLMs as update rules for intelligent fractals, we can better understand the dynamics of these systems and develop more effective solutions to complex problems.

Our paper is organized as follows: we propose a novel perspective on LLMs as update rules for intelligent fractals, which allows us to approach complex problems as fractals and think in terms of local updates rather than global ones. In Section 2, we discuss the challenges posed by the limited token window size of LLMs and review current advancements, while identifying present shortcomings. In Section 3, we formalize our methodology and present several theoretical statements about it. In Section 4, we demonstrate the practical applications of our approach by showcasing the automated tech startup and societal modeling. Finally, in section 5, we provide an analysis and discussion of our findings, including broader scope and future directions. With this paper, we aim to contribute to the ongoing research and development of LLMs and their potential to transform natural language processing and other fields.

# Section 2: Challenges and Limitations of the Limited Token Window in LLMs

## 2.1 Background

### 2.1.1 LLMs

Large Language Models (LLMs) refer to neural networks that are trained to process large amounts of text data, allowing them to learn the underlying patterns and structure in the data. These models often use techniques such as the Transformer architecture, which employs self-attention mechanisms to process sequences of tokens. While there exist many variants, a 'vanilla' self-attention mechanism can be represented as:

y = Attention(Q, K, V) = softmax(QK^T / sqrt(d_k))V

where Q, K, and V are the query, key, and value matrices respectively, typically produced via linearly projecting the inputs, and d_k is the dimensionality of the key vectors. The softmax function ensures that the attention scores sum to 1, effectively creating a weighted average of the values based on the compatibility of the query and key vectors. This mechanism allows input tokens to dynamically alter the routing of information, but it also introduces computational constraints, as the memory and time complexity of the self-attention mechanism scale quadratically with sequence length, thus limiting effective token window size, and hence the amount of total information that can be considered at any given pass.

### 2.1.2 Von Neumann and Distributed Computing

Von Neumann and distributed computing are two paradigms for designing and implementing computer systems. The Von Neumann architecture, named after the prominent mathematician John von Neumann, is a centralized architecture in which a single processing unit, the central processing unit (CPU), performs all computations while accessing a common memory. Mathematically, the Von Neumann architecture can be described using the stored-program model:

M[PC] -> IR; PC += 1

where M is the memory, PC is the program counter, and IR is the instruction register. The architecture is based on the fetch-decode-execute cycle, which involves fetching instructions from memory, decoding them, and executing the corresponding operations.

On the other hand, distributed computing refers to a decentralized architecture in which multiple processing units work together to perform computations. Distributed computing can be modeled using graph theory, with nodes representing processing units and edges representing communication links between them. One common algorithm for distributed computing is the message-passing model, which involves exchanging messages between nodes to coordinate computation and share information.

Distributed computing is often used in large-scale computing systems, such as cloud computing, that require high levels of scalability and fault tolerance. It can also be applied to model complex systems, such as fractals and cellular automata, that exhibit emergent behavior and self-organization.

### 2.1.3 Fractals

Fractals refer to self-similar patterns that repeat at different scales, exemplified by phenomena such as snowflakes, coastlines, and fractal geometry. Fractals can be described mathematically using recursion, iterative functions, or cellular automata. 

Fractals are often used to model complex systems, such as natural landscapes, social networks, and economic markets, that display intricate patterns and behaviors. These systems can be challenging to understand and manipulate, as they involve numerous interrelated components and often exhibit nonlinear dynamics. However, humans possess a limited context window, which constrains their ability to process and update their environment, especially when faced with intricate fractal-like systems. Thus, it is natural to ask whether it is possible to perform intelligent operations such as pseudocode-to-code translation or debugging via local intelligent updates, rather than attempting to process the entire system at once.

### 2.1.4 Self-organization

Self-organization is a process by which the components of a system spontaneously arrange themselves into an ordered structure or pattern without the need for external guidance or control. This phenomenon arises from the local interactions between the components and the underlying rules governing their behavior. Self-organization is a key concept in the study of complex systems, as it can lead to the emergence of global order and functionality from simple, local rules.

Mathematically, self-organization can be described using concepts from dynamical systems theory, such as attractors, basins of attraction, and bifurcations. A system exhibits self-organization if it possesses an attractor, which is a stable state or set of states towards which the system evolves over time. The basin of attraction is the set of initial conditions that lead to the attractor, while bifurcations represent critical points where the system's behavior changes qualitatively.

Examples of self-organization can be found in various domains, such as physics (e.g., pattern formation in reaction-diffusion systems), biology (e.g., flocking behavior in birds), and computer science (e.g., swarm intelligence algorithms). In the context of LLMs and intelligent fractals, self-organization can play a crucial role in the development of efficient algorithms and update rules that enable the system to adapt and respond to its environment, while overcoming the limitations imposed by the token window.

## 2.2 Current Approaches and Shortcomings

Despite the success of LLMs, such as GPT-4, in addressing a broad range of natural language processing tasks, these models still suffer from a fundamental limitation: their restricted token window size, usually capped at 8,000 tokens. This limitation significantly hampers their ability to process and understand long sequences of data, which are prevalent in real-world scenarios, such as processing lengthy scientific documents, understanding legal contracts, and simulating intricate sociopolitical systems.

To cope with the limited token window size, several techniques have been proposed in the literature. Some common approaches include:

A. Document segmentation: Dividing longer documents into smaller, manageable chunks before processing with LLMs. However, this approach may lead to loss of context, especially when dealing with highly interconnected topics or concepts. For example, in the case of a legal document, segmenting it into smaller portions may result in overlooking important clauses that relate to different sections of the document.

B. Sliding window techniques: Using overlapping windows to extract local contexts and features within a longer document. This approach, while helpful, can still struggle to capture and maintain long-range dependencies and complex relationships within the data. A practical example would be processing a lengthy scientific article where the conclusion section may refer back to concepts and theories discussed in the introduction or other earlier sections.

C. Memory-augmented models: Expanding LLMs with external memory components to store and access information beyond the token window. Although promising, memory-augmented models can be computationally expensive and require substantial architectural changes. Moreover, incorporating external memory adds another layer of complexity in training the models, as it may require learning optimal memory storage and retrieval strategies.

These techniques, while offering some improvements, often involve hand-engineered solutions or modifications to the model architecture, which may lead to suboptimal performance and fail to provide a coherent theoretical framework to address the core issue.

## 2.3 The Need for a Novel Perspective

Given the limitations and shortcomings of current approaches, there is a pressing need to develop a more general and theoretically grounded framework for tackling the limited token window challenge in LLMs. By proposing LLMs as update rules for intelligent fractals, we offer a new perspective that emphasizes local updates within a broader, interconnected system. This approach enables us to manage the complexity of large-scale problems while staying within the boundaries imposed by the token window.

In the following sections, we will elaborate on our proposed methodology and present theoretical statements that support our perspective. We will then demonstrate the practical applications of this approach by showcasing our automated tech startup and societal modeling, highlighting the potential of LLMs as update rules for intelligent fractals to overcome the limitations posed by the limited token window.

# Section 3: Formalizing the Methodology of LLMs as Update Rules for Intelligent Fractals

## 3.1 Intelligent Fractals and Local Updates

We define an intelligent fractal as a complex, self-organizing, and interconnected system that can be modeled as a hierarchical or recursive structure. Examples of intelligent fractals include natural language texts, computer programs, and social systems. The key idea is that intelligent fractals can be understood and manipulated using local updates rather than attempting to process the entire system at once.

Mathematically, we represent an intelligent fractal as a graph G = (V, E), where V is the set of vertices or nodes, and E is the set of edges or connections between the nodes. Each node v_i ∈ V represents a subproblem or context within the intelligent fractal, and each edge e_ij ∈ E represents a relationship or dependency between subproblems v_i and v_j.

We define a local update as a transformation or operation applied to a node or a set of nodes within the intelligent fractal. Formally, a local update can be represented as a function f: V → V, where f(v_i) = v'_i, transforming node v_i into node v'_i.

## 3.2 LLMs as Update Rules

To formalize the idea of LLMs as update rules for intelligent fractals, we represent an LLM as a parametric function L: V → V, with L(v_i) = v'_i, transforming node v_i into node v'_i. The inputs V are composed of the context windows within the intelligent fractal, and the outputs V' represent the updated contexts after applying the LLM transformation. In this framework, LLMs learn to generate local updates by processing and understanding the relationships and dependencies between nodes within the context window.

Let C(v_i) be the context window of node v_i, consisting of a set of nodes within a certain distance from v_i in the graph G. The LLM function L operates on this context window, taking into account the local structure and dependencies of the intelligent fractal to generate an appropriate update. Formally, we can represent the LLM function as:

L(C(v_i); θ_pretrained) = v'_i

Here, θ_pretrained represents the fixed, pre-trained parameters of the LLM. The LLM generates local updates by processing the context windows C(v_i) within the intelligent fractal, leveraging its pre-trained knowledge to understand the relationships and dependencies between nodes and produce updated contexts v'_i.

## 3.3 Iterative Local Updates

Given the constraint of a limited token window, we propose an iterative approach to update the intelligent fractal by applying the LLM function L to subsets of nodes within the graph G. In each iteration, we select a subset of nodes S ⊆ V and perform local updates on their corresponding context windows C(v_i) using the LLM function L:

v'_i = L(C(v_i); θ_pretrained), ∀ v_i ∈ S

After each iteration, the updated nodes v'_i replace their corresponding original nodes v_i in the graph G, and the context windows for the next iteration are adjusted accordingly. This iterative process continues until a stopping criterion is met, which could be based on a predefined number of iterations, a convergence threshold, or an external evaluation metric.

## Section 3.4: Theoretical Statements

### 3.4.1 Statement 1: Dependence of Local Updates on Pre-trained Knowledge and Intelligent Fractal Complexity

Statement 1: The LLM's ability to generate meaningful local updates is contingent upon the quality of its pre-trained knowledge (θ_pretrained) and the complexity of the intelligent fractal.

Proof:

Let X be an intelligent fractal, and let L be an LLM with pre-trained knowledge θ_pretrained. We model X as a graph G = (V, E), and Ω(X) be a function measuring the complexity of the underlying fractal structure within X. Let Y = L(X; θ_pretrained) be the output fractal generated by applying local updates using L.

First, we aim to analyze the relationship between the quality of pre-trained knowledge θ_pretrained and the resulting output fractal Y. Intuitively, the better the pre-trained knowledge, the more effectively the LLM can understand the dependencies and structure within X, resulting in more accurate local updates. We define the quality of θ_pretrained as a metric Γ(θ_pretrained) that measures how well the LLM's understanding correlates with the true structure of X. Clearly, the higher Γ(θ_pretrained), the more accurate and coherent the output fractal Y.

Second, we analyze the relationship between the complexity of the intelligent fractal structure Ω(X) and the effectiveness of LLM-generated local updates. As Ω(X) increases, the task of generating meaningful updates becomes more challenging due to the intricate dependencies and relationships within the fractal. The LLM may struggle to capture the complex structure within X, resulting in output fractal Y that deviates from the true structure.

From both analyses, the LLM's ability to generate meaningful local updates is contingent upon the quality of its pre-trained knowledge (θ_pretrained) and the complexity of the intelligent fractal. In summary,

Y = f(Γ(θ_pretrained), Ω(X))

### 3.4.2 Statement 2: Overcoming Token Window Limitations Through Iterative Local Updates

Statement 2: The iterative local update approach enables the LLM to process and update large-scale intelligent fractals by breaking down the problem into smaller, manageable subproblems that fit within the limited token window.

Proof (Logical Argument):

Let X be a large-scale intelligent fractal with a complexity greater than the token window limitations of the LLM L with pre-trained knowledge θ_pretrained. By utilizing iterative local updates, we perform the following steps:

1. Divide X into subproblems or contexts: Partition X into a set of smaller subproblems {X_1, X_2, ..., X_n} that fit within the LLM's token window. These subproblems should capture essential dependencies and relationships within the intelligent fractal.

2. Apply local updates iteratively: For each subproblem X_i, apply the LLM transformation L(X_i; θ_pretrained) to generate an updated context Y_i. Replace the original subproblem X_i with the updated context Y_i in X.

3. Repeat steps 1 and 2 until a stopping criterion is met: Continue updating subproblems iteratively until convergence, a predetermined number of iterations, or an external evaluation metric is satisfied.

By iteratively updating smaller subproblems that fit within the LLM's token window, the intelligent fractal X can be progressively refined, capturing the complexity of the overall system without violating the token window limitations.

### 3.4.3 Statement 3: Effect of Increasing Iterations on LLM's Understanding of Intelligent Fractals

Statement 3: As the number of iterations increases, the LLM progressively refines its understanding of the intelligent fractal and generates increasingly accurate and coherent updates, provided that the pre-trained knowledge (θ_pretrained) captures relevant information about the problem domain.

Proof (Logical Argument):

Suppose we update a large-scale intelligent fractal X using the LLM L with pre-trained knowledge θ_pretrained. As we apply iterative local updates, the LLM continues to refine its understanding of the relationships and dependencies within X. During each iteration, the LLM operates on context windows C(v_i) that capture local structure and dependencies within the intelligent fractal.

Given that the pre-trained knowledge θ_pretrained captures relevant information about the problem domain, it is likely that the LLM will generate progressively more accurate and coherent updates in each iteration. As the number of iterations increases, the LLM's understanding of the intelligent fractal X converges, resulting in a more accurate representation of the overall structure and dependencies within the system.

This statement implies that, with sufficient iterations and adequate pre-trained knowledge, the LLM can generate increasingly precise and coherent updates that capture the intricate dependencies and relationships within the intelligent fractal X.

In the following sections, we will demonstrate the practical applications of our proposed perspective on LLMs as update rules for intelligent fractals by showcasing the automated tech startup and societal modeling. These examples will highlight the potential of our approach to overcome the limitations posed by the limited token window and contribute to ongoing research and development of LLMs.

# Section 4: Practical Applications of LLMs as Update Rules for Intelligent Fractals

## 4.1 Automated Tech Startup

To demonstrate the potential of LLMs as update rules for intelligent fractals in real-world scenarios, we have implemented an automated tech startup that operates entirely without human intervention. By applying our proposed methodology, we have automated key aspects of business operations, such as market analysis, product development, and sales. This section discusses the implementation details and unique features of our automated tech startup.

### 4.1.1 Decomposing the Tech Startup Problem

We begin by decomposing the tech startup problem into critical components, including marketing, sales, and engineering. Our goal is to automate each of these components using LLMs as update rules for intelligent fractals. We model the company as a hyperlinked document containing all crucial information needed to run the business, such as business plans, sales CRM, market analyses, scrum boards, code repositories, QA reports, and more.

By iterating through the different components of our tech startup model, we can automate processes, including market analysis, scrum prioritization, design, engineering, testing, sales work, public relations, and executive analysis.

### 4.1.2 Automating Market Analysis and Idea Generation

The first step in establishing an automated tech startup is to derive insights about market needs and generate ideas for potential products or services. Using LLMs, we analyze textual data gathered from social media, news articles, blog posts, and other sources relevant to our domain. We then generate insights regarding customer needs, trends, and market gaps. Next, the LLM processes these insights and produces ideas for potential software products or services that address identified opportunities.

### 4.1.3 Automating Design and Engineering

Once potential ideas emerge, the LLM proceeds to design and implement the software. This process starts with the creation of a high-level architecture, followed by decomposing the architecture into smaller, manageable tasks that fit within the LLM's context window.

The LLM then generates source code for each task iteratively, leveraging its extensive pre-trained knowledge in software engineering techniques, languages, and libraries. The generated code is automatically integrated and compiled, followed by a testing and debugging phase to ensure the final product meets quality standards.

### 4.1.4 Automating Branding, Marketing, and Sales

When the software product is ready, the LLM creates a brand identity, including logos, color schemes, and taglines, followed by the development and deployment of a responsive website tailored to showcase the product features and benefits.

The LLM then formulates marketing strategies and campaigns, targeting relevant markets and potential customers, using both organic and paid advertising channels. Simultaneously, the LLM manages the sales CRM, identifying leads and conducting sales conversations via email or messaging platforms to convert leads into customers.

### 4.1.5 Results and Discussion

Through our automated tech startup, we demonstrated the efficacy of using LLMs as update rules for intelligent fractals. By decomposing the problem into smaller, manageable subproblems and leveraging the LLM's context window, we achieved end-to-end automation of various business processes without human intervention.

This approach exemplifies how LLM-based intelligent fractal updates can streamline workflows, automate decision-making, and ultimately drive innovation in various domains, including scientific, engineering, business, and social settings.

## 4.2 Societal Modeling

Applying our proposed perspective on LLMs as update rules for intelligent fractals, we have further developed a societal model that enables us to investigate the effects of different policies and interventions on a range of societal aspects, such as economy, politics, education, healthcare, and social welfare.

### 4.2.1 Decomposing the Problem of Societal Modeling

We start by decomposing the societal modeling problem into its critical aspects, such as demographics, resources, institutions, governance, and individual behaviors. We model the society as a hyperlinked document containing relevant information, such as demographic data, economic indicators, government policies, healthcare statistics, and educational outcomes.

### 4.2.2 Analyzing the Impact of Policies and Interventions

Using the societal model, we can assess the effects of various policies and interventions on different aspects of the society. For instance, we can use the model to examine the impact of a new healthcare policy on healthcare outcomes, economic growth, and social welfare. The LLM processes the hyperlinked document to understand the complex relationships and dependencies within the society and generates predictions for the impacts of specific policies on the system as a whole. This analysis helps identify areas for improvement and offers insights to find effective solutions.

### 4.2.3 Results and Discussion

Our societal modeling application demonstrates the potential of using LLMs as update rules for intelligent fractals in modeling complex systems. By decomposing the societal problem into smaller subproblems fitting within the LLM's context window, we have successfully captured intricate relationships and dependencies within the society.

The ability to analyze the impacts of various policies and interventions on societal aspects through LLM-based intelligent fractal updates offers a powerful tool for decision-makers, researchers, and stakeholders across fields such as economics, politics, and public health.

# Section 5: Conclusion and Future Directions

LLMs are the update rules of intelligent fractals, providing a theoretically grounded perspective to tackle the challenge of limited token window size. By decomposing complex problems into manageable subproblems and applying local updates iteratively, we can leverage the power of LLMs to model and manipulate large-scale, intricate systems such as tech startups and societies.

We demonstrated the practical utility of our approach in automating a tech startup and modeling a society, showcasing the potential of LLMs to transform NLP and contribute to ongoing research and development across multiple domains.

Moving forward, we plan to expand our research and applications of LLMs as update rules for intelligent fractals to address other complex problems in fields such as climate modeling, molecular biology, and finance, enhancing our understanding of these interconnected systems and their hidden intricacies.
