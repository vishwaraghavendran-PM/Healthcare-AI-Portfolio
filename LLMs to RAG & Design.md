## Agenda

- Introduction  
- Understanding LLMs and Their Role  
- Exploring Retrieval Augmented Generation (RAG)  
- Model Context Protocol (MCP)  
- Prompt Engineering  
- Agents  
- Conclusion and Future Outlook  

---

## Introduction

AI is rapidly evolving. Technologies such as Large Language Models (LLMs), Retrieval Augmented Generation (RAG), Model Context Protocol (MCP), and Agents are transforming how businesses and developers approach technical challenges.

---

## What Are LLMs?

An LLM (Large Language Model) is a sequence‑based model trained on massive amounts of text data to predict and generate human‑like language.  
LLMs learn statistical patterns in language to process sequences of tokens, understand context, and generate coherent text.

### Key Features

- Transformer‑based architecture (Attention mechanism).  
- Token‑based representation of text.  
- Pre‑training on large, diverse datasets.  
- Fine‑tuned for specific tasks such as chat, summarization, coding.  
- Context‑window constrained; uses embeddings and attention layers.  

---

## Core Components

1. **Input Layer**  
   - Converts text into tokens and embeddings.  

2. **Encoder‑Decoder or Decoder‑only Transformer**  
   - Attention mechanism: Focuses on relevant words in context.  
   - Feed‑forward layers: Process embeddings.  

3. **Output Layer**  
   - Predicts next word or generates text.  

---

## Diagram of LLM Architecture & How LLM Works – Step by Step

1. User inputs a question or prompt.  
2. Text is tokenized and embedded.  
3. Transformer layers process the sequence.  
4. Output tokens are decoded to text.

---

## Popular LLMs and Cutoff Dates

- GPT‑3: Trained on data up to 2019.  
- GPT‑3.5: Cutoff September 2021.  
- GPT‑4: Cutoff 2023.  
- Claude‑2: Cutoff early 2023.  
- LLaMA‑2 (Meta): Cutoff 2023.  

---

## Exploring Retrieval Augmented Generation (RAG)

Retrieval Augmented Generation (RAG) grounds answers in exact, current, domain‑specific data.  
RAG combines pre‑trained LLMs with a retrieval system that pulls in relevant external knowledge.  
Instead of relying only on model parameters, RAG augments the response with retrieved documents so answers are more accurate, explainable, and up‑to‑date.

### Why Use RAG?

- LLMs have limited context windows.  
- They cannot access live, external information.  
- RAG allows models to access external knowledge dynamically.

---

## What Is RAG Architecture?

RAG stands for Retrieval Augmented Generation. It is an architecture that combines:

1. **Retrieval** – Fetching relevant information from a large knowledge base.  
2. **Generation** – Using a language model to produce a response based on retrieved data.  

This improves response accuracy and reduces hallucinations because the model uses real, factual data during generation.

---

## Core Components of RAG

1. **User Query**  
   - The input question or prompt from the user.  

2. **Retrieval**  
   - Searches vector databases or document stores for relevant chunks.  
   - Uses embedding similarity so the closest matches to the query are selected.  

3. **Knowledge Base / Document Store**  
   - Stores documents in vector format for fast similarity search.  

4. **Generator (LLM)**  
   - Takes the retrieved context + user query.  
   - Generates a detailed answer.  

5. **Pipeline**  
   - Orchestrates retrieval and generation steps into one workflow.  

## How RAG Works – Step by Step

1. User submits a question.
2. Question is sent to a retrieval system that searches a knowledge base.
3. Relevant documents or passages are retrieved.
4. The query and retrieved context are sent to an LLM.
5. Final response is returned to user.

## LLMs vs RAG

| Feature      | LLMs                              | RAGs                                         |
|-------------|------------------------------------|----------------------------------------------|
| Data Source | Internal (trained on data only)    | External (retrieves real‑time info)          |
| Accuracy    | May hallucinate                    | More accurate; grounded in documents         |
| Context     | Limited by window size             | Extended via retrieved context               |
| Examples    | GPT‑4, Claude, LLaMA               | ChatGPT + Bing, Enterprise Copilots          |

### Advantages of RAGs

- Enhanced factual accuracy by grounding answers in real data.
- Access to up‑to‑date information without retraining.
- Domain adaptability by indexing domain‑specific knowledge bases.
- Cost efficiency since models need less retraining.
- Personalization from user‑specific or enterprise‑specific data.

### Disadvantages of RAGs

- System complexity due to separate retrieval and integration.

---

## RAG Limitations

- Retrieval quality dependency: Output quality depends on relevance and organization of the knowledge base.
- Latency: Additional retrieval steps may increase response time.
- Maintenance: Knowledge bases must be regularly updated and curated.
- Potential retrieval errors: Poorly formatted queries or unstructured data can lead to irrelevant or incomplete answers.

---

## Model Context Protocol (MCP)

MCP helps tools “talk” to each other. When you compose queries across several tools, MCP manages the details without rebuilding entire architectures.

### What is MCP?

Model Context Protocol (MCP) is an open standard for connecting AI models to external tools and data sources.  
Its purpose is to provide safe, controlled, and real‑time, cross‑tool access to information and actions.

### MCP Architecture

- MCP Servers: Expose data, tools, or actions.
- MCP Clients: Integrate LLMs and agents.
- MCP Hosts: Manage where clients and agents operate.

### Applications, Benefits, and Timing of MCP Usage

- Where: Enterprises, AI‑first companies, software development, education, DevOps.
- Benefits: Standardization, interoperability, real‑time access, security, and scalability.
- When: Dynamic workflows, cross‑platform integration, compliance needs, multi‑tool orchestration.

### MCP Advantages

- Unified integration: Standardizes AI connections to tools and data.
- Real‑time access: Enables live data and actions.
- Interoperability: Works across different vendors and systems.
- Security and governance: Centralized policies and access controls.
- Scalability: Easily extends integrations.
- Developer productivity: Reduces custom coding.

### MCP Disadvantages

- Evolving standard: Documentation and best practices still maturing.
- Implementation overhead: Requires setup and governance.
- Performance overhead: Extra abstraction layer.
- Complexity: Steeper learning curve versus direct APIs.
- Community support: Still growing compared with older standards.
- Data governance: Requires strong policies over cross‑system data.

### Common Examples of MCP

- GitHub MCP Server: Manages repositories and issues.
- Microsoft Copilot Studio: Connects Copilot to applications and data.
- DevOps Agents: Manage pipelines and deployments.
- HR/Finance Agents: Integrate with enterprise systems.
- Data Platforms: Route AI to structured and unstructured data sources.

---

## Prompt Engineering Overview

Prompt engineering is the practice of designing and optimizing input prompts so that AI models generate accurate, reliable, and useful outputs.

### Why is it Important?

- Improves accuracy and relevance of AI outputs.
- Reduces hallucinations.
- Enables specific tasks like summarization, coding, or reasoning.

### Core Principles

1. Clarity: Be explicit and unambiguous.
2. Context: Provide background or constraints.
3. Role assignment: Tell the model what role to assume.
4. Examples: Use a few‑shot pattern by giving samples.
5. Constraints: Define format, tone, or length.

### Prompt Engineering Workflow

1. Define goal.
2. Draft prompt.
3. Test with examples.
4. Refine and iterate.

### Examples

- Basic prompt: “Explain quantum computing.”
- Better prompt: “Explain quantum computing in simple terms for college students; keep it under 200 words.”

### Engineered Prompt Example

- “Act as a physics professor. Explain quantum computing in simple terms for college students using bullet points and an introduction.”

### Few‑Shot Example

- “Translate English to French. Example: ‘Hello’ → ‘Bonjour’. Now translate: ‘Good morning’.”

---

## Agents
Observe → Reason → Plan → Act

Agents are systems that perceive, reason, and act autonomously.  
An AI agent is an autonomous software system that perceives its environment, makes decisions, and performs actions with minimal human intervention.

### Utilization of Agents

- Customer service: Chatbots and virtual assistants.
- Healthcare: Triage, remote monitoring, decision support.
- Finance: Fraud detection, trading bots, risk analysis.
- Operations: Supply‑chain optimization, robotics, autonomous vehicles, drones.

### Reasons for Using AI Agents

- Increase efficiency by automating repetitive tasks.
- Orchestrate workflows across multiple tools and systems.
- Enable continuous interactions, complex multi‑step tasks, and real‑time decisions.

### When AI Agents Are Used

- In complex tasks requiring autonomy, dynamic or partially observable environments, long‑running decisions, and high‑stakes outcomes.

### Advantages of Agents

- Increased efficiency and productivity.
- Consistency and error‑free outputs.
- Scalability for handling many tasks or sessions.
- Personalization through context awareness.
- 24/7 availability.
- Data‑driven insights.

### Disadvantages of Agents

- Dependency and risk of errors or malfunction.
- Cost of development, deployment, and maintenance.
- Potential bias and fairness issues.
- Security and privacy concerns.
- Loss of human control in decisions.

### Common AI Agent Examples

Examples include virtual assistants, customer support bots, workflow automations, autonomous vehicles, recommendation systems, diagnostic copilots, and supply‑chain optimization agents.

---

## Generative AI vs Agentic AI

### High‑Level Comparison Table

| Aspect        | Generative AI                                                | Agentic AI                                                       |
|--------------|--------------------------------------------------------------|------------------------------------------------------------------|
| Definition   | Creates new content from patterns in data                    | Autonomous systems perceiving, deciding, and acting              |
| Core Tasks   | Generate text, images, audio, and code                       | Plan, sequence actions, call tools, and execute workflows        |
| Examples     | GPT, DALL·E, Stable Diffusion                                | Diagnostic copilots, robotic agents, autonomous vehicles, triage |

---

## Detailed Aspect Comparison

| Aspect      | Generative AI                           | Agentic AI                                    |
|------------|------------------------------------------|-----------------------------------------------|
| Autonomy   | Reactive; no persistent goals or memory | Proactive; sets goals, remembers context      |
| Learning   | Learns during training; limited online  | Can learn and adapt continuously              |
| Interaction| One‑shot or session‑based; limited memory | Ongoing, context‑aware, multi‑step           |
| Use Cases  | Content creation, summarization, code   | Workflow automation, decision support, robotics |
| Strengths  | Creativity, scalability, rapid generation | Autonomy, adaptability, multi‑step reasoning |
| Limitations| May hallucinate; lacks real‑world awareness | Complex design; needs safety and modeling  |

This comparison highlights generative AI’s strengths in content creation and fluency, while agentic AI excels at autonomy, adaptability, and real‑world task execution.

---

## Use‑Cases for Generative AI

- Content creation: text, images, audio, video, code.
- Text summarization and drafting.
- Data analysis: pattern finding and summarizing.
- Customer support chatbots.
- Healthcare: drug discovery and imaging.
- Design and prototyping.
- Research assistance.

## Use‑Cases for Agentic AI

- Autonomous workflow automation.
- Complex customer support with escalation.
- IT helpdesk and infrastructure monitoring.
- Finance and compliance automation.
- Sales and marketing campaign management.
- Healthcare workflow automation.
- Research and R&D automation.
- Supply‑chain and logistics optimization.
- Collaboration in multi‑agent systems and swarm robotics.

---

## Generative‑AI vs Agentic‑AI Use Cases

| Category         | Generative‑AI Use Cases                       | Agentic‑AI Use Cases                                 |
|-----------------|-----------------------------------------------|------------------------------------------------------|
| Content Creation| Text, images, audio, video, code generation   | Dynamic content creation within workflows           |
| Data Analysis   | Summarization, insights, extraction           | Automated decision‑making and real‑time analytics   |
| Customer Support| Chatbots, virtual assistants                  | Autonomous query handling, escalation               |
| Automation      | Report generation, document processing        | End‑to‑end workflow orchestration                   |
| Personalization | Product recommendations, tailored marketing   | Context‑aware task execution                        |
| Healthcare      | Drug discovery, medical imaging               | Patient triage, diagnostic support                  |
| IT & Operations | Code generation, documentation                | Helpdesk automation, infrastructure monitoring      |
| HR & Research   | Learning content, tutoring                    | Resume screening, research assistance               |
| Supply Chain    | Data‑driven optimization                      | Inventory management, logistics planning            |

