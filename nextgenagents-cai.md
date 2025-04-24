# From Code to Intelligence – Building NextGen AI Agents

As a hands-on enterprise developer, I’ll take you on a fast, code-first tour of what separates real agents from garden-variety functions. We’ll crack open the architecture that lets them reason, measure that intelligence with hard metrics, then wire up semantic-aware functions that pick the right tools and recover gracefully when things get weird. We’ll bolt on true memory—short-term context for snappy conversations and long-term state for constant self-improvement—and inject Microsoft’s latest research, from AutoGen’s swarming agents to Magnetic-One’s rock-solid enterprise patterns. By the end, you’ll have a blueprint you can push straight into Azure and the confidence to future-proof whatever you build next.

## Session Details
**Event Tickets:** [AI Community Conference – Boston](https://allevents.in/cambridge/ai-community-conference-boston/100001274004524829)

**Format:** In-person technical half-day workshop

**Focus:** Developer-oriented, hands-on approaches to building enterprise-grade AI agents

**Prerequisites:** Basic understanding of AI concepts and programming fundamentals

**Speaker:** [Paul Swider](https://sessionize.com/pswider/), Chief AI Officer, RealActivity

**Location:** Boston, Massachusetts, United States

***[5/1/2025 AI Agent workshop setup instructions](repo-rundown.md )*** 

**Pro Tip:** *Aim your favorite LLM at this repo—let it ingest the patterns, then come to the workshop ready to debate architecture choices with data in hand.*

## About the Presenter

A technology leader with 29 years of proven mission-critical solutions experience, specializing in healthcare technology innovation and AI applications. My journey began in 1996 with critical healthcare projects, including pioneering one of the earliest mission-critical AI applications for same-day surgery triage in 2001.

As founder of the Boston Healthcare Cloud and AI Community (2020), I've dedicated my career to advancing AI and cloud solutions for healthcare. My work has been recognized with Microsoft's Azure MVP (2019) and Azure Most Influential (2020) awards.

### Connect

[Technical Accomplishments (Summary)](bio.md)

[LinkedIn](https://www.linkedin.com/in/pswider)

[Speaking Profile and Events](https://sessionize.com/pswider/)

[My Substack](https://substack.com/@pauljswider) (great enterprise AI agent content)



## What You'll Learn

### Workshop Agenda

#####  From Code to Intelligence – Building Next-Gen AI Agents

######  Main Room (Abigail Adams / Horace Mann), Thursday • May 1 2025 • 1:00 – 4:00 PM ET

| Time (ET)          | Segment                                         | Format             | Key Take-Aways & Repo Mapping                                |
| ------------------ | ----------------------------------------------- | ------------------ | ------------------------------------------------------------ |
| **1:00 – 1:10 PM** | **Welcome & Goals**                             | Slides             | Why agentic AI matters for the enterprise; room logistics; pointer to setup guide in Bootcamp repo [GitHub](https://github.com/realactivity/copilot-dev-bootcamp/blob/main/nextgenagents-cai.md) |
| **1:10 – 1:35 PM** | Demystifying AI Agents                          | Talk + demo        | Agent lifecycle, patterns (tool use, planning, metacognition) using *AI Agents for Beginners* Lessons 1-3 |
| **1:35 – 1:55 PM** | Architecture Deep-Dive                          | Live coding        | How Semantic Kernel, Azure AI Agent Service, and AutoGen mesh; quick tool-calling demo |
| **1:55 – 2:25 PM** | **Lab 1 – Build Your First Agent**              | Hands-on           | Fork *ai-agents-for-beginners*; complete Lesson 1 and add a custom tool (Python) |
| **2:25 – 2:35 PM** | Break / Open Q&A                                | —                  | Stretch, troubleshoot, share wins                            |
| **2:35 – 2:50 PM** | Semantic-Aware Functions in C#                  | Talk + live coding | Walk through *ai-developer* Challenge 02; intro to auto-planner basics |
| **2:50 – 3:15 PM** | **Lab 2 – Plugins & Planning**                  | Hands-on           | Complete Challenge 03; wire an OpenAPI plugin, then test auto-calling (C#) |
| **3:15 – 3:25 PM** | Memory & RAG for Agents                         | Talk + demo        | Short- vs. long-term state, embeddings, grounding; preview *Azure AI Agents Labs* RAG notebook |
| **3:25 – 3:45 PM** | **Lab 3 – Agentic RAG \*or\* Multi-Agent Chat** | Hands-on           | Choose: Lesson 5 (RAG) *or* Lesson 8 (Multi-Agent) from *ai-agents-for-beginners*; optional Alt-path with *Agent Innovator Lab* notebooks |
| **3:45 – 3:55 PM** | Production & Responsible AI                     | Slides             | Content filters, eval harnesses, observability; patterns from Magnetic-One & Bootcamp notes [GitHub](https://github.com/realactivity/copilot-dev-bootcamp/blob/main/nextgenagents-cai.md) |
| **3:55 – 4:00 PM** | Wrap-Up & Next Steps                            | Discussion         | Share GitHub starter branch, slides, Discord link, feedback QR |

## Resources

### Presentation Materials

- [Session Slides]() *(Will be updated after the presentation)*
- ***[5/1/2025 AI Agent workshop setup instructions](repo-rundown.md )*** 

### Workshop Research and Preparation - New for 2025

- [Semantic Kernel Documentation](https://learn.microsoft.com/en-us/semantic-kernel/overview/)
- [Microsoft AutoGen Project](https://microsoft.github.io/autogen/)
- [Boston Healthcare Cloud and AI Community Resources]()
- **AI Agents for Beginners** – https://github.com/microsoft/ai-agents-for-beginners offers a 10-lesson, clone-and-run curriculum that walks you from first prompt to multi-agent RAG patterns, making it the fastest on-ramp to Microsoft-flavoured enterprise agents. [GitHub](https://github.com/microsoft/ai-agents-for-beginners/blob/main/README.md)
- **Generative AI for Beginners (.NET)** – https://github.com/microsoft/Generative-AI-for-beginners-dotnet distills hands-on C# examples and MCP/Semantic-Kernel integrations into bite-sized lessons so .NET developers can embed LLM power without leaving their comfort zone. [GitHub](https://github.com/microsoft/Generative-AI-for-beginners-dotnet/blob/main/README.md)

  **AI Agents Hackathon** – https://github.com/microsoft/AI_Agents_Hackathon bundles slides, code starters, and session replays from Microsoft’s three-week virtual hack, giving you community-tested blueprints (and prize-winning ideas) for building production-ready agents. [GitHub](https://github.com/microsoft/AI_Agents_Hackathon/blob/main/README.md)

  **Magma** – https://github.com/microsoft/Magma open-sources Microsoft Research’s multimodal foundation model that lets agents see, plan, and act across images, video, and text—crucial for the next wave of perceptive enterprise agents. [GitHub](https://github.com/microsoft/Magma)

  **AI Developer (Semantic Kernel Fundamentals)** – https://github.com/microsoft/ai-developer presents eight progressive challenges (C# & Python) that teach Azure AI Foundry, plugin auto-calling, RAG, and multi-agent workflows, serving as a deeper-dive companion to the beginner course. [GitHub](https://github.com/microsoft/ai-developer)

  **Agent Innovator Lab** – https://github.com/Azure/agent-innovator-lab provides modular Azure-centric labs on agentic RAG, evaluation, and optimization design patterns, making it ideal for teams refining real-world agent architectures. [GitHub](https://github.com/Azure/agent-innovator-lab)

  **Azure AI Agents Labs** – https://github.com/Azure/azure-ai-agents-labs contains notebook-style labs that showcase the brand-new Azure AI Agent Service SDK + Semantic Kernel working together, guiding you from a single tool-calling agent to a full multi-agent system. [GitHub](https://github.com/Azure/azure-ai-agents-labs)

### Questions & Feedback

Have questions before or after the session? Want to discuss implementation details for your specific scenarios? Feel free to reach out via LinkedIn or bring your questions to the session!

- **Say Hi:**

  - [X](https://www.twitter.com/pswider)
  - [Bluesky](https://bsky.app/profile/paulswider.bsky.social))
  - [LinkedIn](https://www.linkedin.com/in/pswider)
  - [Blog](https://www.paulswider.com)
  - [About RealActivity](https://www.realactivity.ai)