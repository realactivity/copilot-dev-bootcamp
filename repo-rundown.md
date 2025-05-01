## Repo Rundown

During the labs we’ll be coding against two freshly minted Microsoft repos that showcase the same agentic patterns from two angles:

- **[AI Agents for Beginners](https://github.com/microsoft/ai-agents-for-beginners)** – a Python-first tour of tool-calling, planning, and RAG that lets us peek under the hood with minimal boilerplate. 
- **[AI Developer (Semantic Kernel)](https://github.com/microsoft/ai-developer)** – a C# re-take that layers the same concepts onto .NET and enterprise-ready SK primitives. 

By running the labs in **both** repos you’ll see identical agent workflows expressed in two stacks—cementing the core ideas while sharpening your language of choice. Clone, configure, and come ready to dive straight into the code.

## Quick Start — Environment Setup (10 min)

> *Pre-event - Follow these two links first, then breeze through the bullets below.*

1. **Python Labs (AI Agents for Beginners)** – Full setup guide
    https://github.com/microsoft/ai-agents-for-beginners/blob/main/00-course-setup/README.md 

   [GitHub](https://github.com/microsoft/ai-agents-for-beginners/blob/main/00-course-setup/README.md)

   

2. **C# / Semantic Kernel Labs (AI Developer, Challenge 00)** – Prerequisites
    https://github.com/microsoft/ai-developer/blob/main/Dotnet/challenges/Challenge-00.md 

   [GitHub](https://github.com/microsoft/ai-developer/blob/main/Dotnet/challenges/Challenge-00.md)

   

------

### One-Page Checklist

| Step                | Python Track ✔️                                               | C# Track ✔️                                                   |
| ------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| **1. Fork & Clone** | `git clone https://github.com/microsoft/ai-agents-for-beginners.git` | `git clone https://github.com/microsoft/ai-developer.git`    |
| **2. Install SDKs** | Python 3.12+                                                 | .NET 8 SDK + VS Code/VS 2022                                 |
| **3. Create .env**  | Copy `.env.example` → `.env`; add your **GitHub PAT** and Azure keys | Use `appsettings.json` or environment vars for Azure keys    |
| **4. Dependencies** | `pip install -r requirements.txt`                            | From repo root: `dotnet restore`                             |
| **5. Azure Login**  | `az login --use-device-code` (keyless auth)                  | Same `az login` (needed for Foundry)                         |
| **6. Verify**       | `python 01_intro_agent.py` (prints a greeting)               | `dotnet run --project Dotnet/Quickstart` (gets a chat response) |

> **Gotchas:**
>  • No Azure yet? Grab a free subscription or workshop pass.
>  • Corporate proxy? Use VS Code Dev Containers or GitHub Codespaces.
>  • Problems? Ping the **#agents-workshop** channel in Azure AI Community Discord.

That’s it—you’re ready to code when the workshop clock starts!

### Workshop Research and Advanced Reading- New for 2025

- [Semantic Kernel Documentation](https://learn.microsoft.com/en-us/semantic-kernel/overview/)

- [Microsoft AutoGen Project](https://microsoft.github.io/autogen/)

- [Cursor IDE](https://learn-cursor.com/en/wiki/user-guide/install)

- [GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/introduction-to-github-copilot-enterprise/3-how-to-get-started)

- ([Boston Healthcare Cloud & AI Community | Linktree](https://linktr.ee/BOSHUG))

- **AI Agents for Beginners** – https://github.com/microsoft/ai-agents-for-beginners offers a 10-lesson, clone-and-run curriculum that walks you from first prompt to multi-agent RAG patterns, making it the fastest on-ramp to Microsoft-flavoured enterprise agents. [GitHub](https://github.com/microsoft/ai-agents-for-beginners/blob/main/README.md)

- **Generative AI for Beginners (.NET)** – https://github.com/microsoft/Generative-AI-for-beginners-dotnet distills hands-on C# examples and MCP/Semantic-Kernel integrations into bite-sized lessons so .NET developers can embed LLM power without leaving their comfort zone. [GitHub](https://github.com/microsoft/Generative-AI-for-beginners-dotnet/blob/main/README.md)

  **AI Agents Hackathon** – https://github.com/microsoft/AI_Agents_Hackathon bundles slides, code starters, and session replays from Microsoft’s three-week virtual hack, giving you community-tested blueprints (and prize-winning ideas) for building production-ready agents. [GitHub](https://github.com/microsoft/AI_Agents_Hackathon/blob/main/README.md)

  **Magma** – https://github.com/microsoft/Magma open-sources Microsoft Research’s multimodal foundation model that lets agents see, plan, and act across images, video, and text—crucial for the next wave of perceptive enterprise agents. [GitHub](https://github.com/microsoft/Magma)

  **AI Developer (Semantic Kernel Fundamentals)** – https://github.com/microsoft/ai-developer presents eight progressive challenges (C# & Python) that teach Azure AI Foundry, plugin auto-calling, RAG, and multi-agent workflows, serving as a deeper-dive companion to the beginner course. [GitHub](https://github.com/microsoft/ai-developer)

  **Agent Innovator Lab** – https://github.com/Azure/agent-innovator-lab provides modular Azure-centric labs on agentic RAG, evaluation, and optimization design patterns, making it ideal for teams refining real-world agent architectures. [GitHub](https://github.com/Azure/agent-innovator-lab)

  **Azure AI Agents Labs** – https://github.com/Azure/azure-ai-agents-labs contains notebook-style labs that showcase the brand-new Azure AI Agent Service SDK + Semantic Kernel working together, guiding you from a single tool-calling agent to a full multi-agent system. [GitHub](https://github.com/Azure/azure-ai-agents-labs)
  
  **Azure Health Bot** – https://learn.microsoft.com/en-us/azure/health-bot/ is Microsoft’s low-code, compliance-ready platform for building AI-driven virtual health assistants that can triage, educate, and escalate across healthcare workflows. [Docs](https://learn.microsoft.com/en-us/azure/health-bot/)
  
  **SK Agents Framework RC1** – https://devblogs.microsoft.com/semantic-kernel/release-the-agents-sk-agents-framework-rc1/ introduces the first release candidate of the Semantic Kernel Agents Framework, enabling advanced agent orchestration, memory, and planning via Microsoft’s official SDK. [Blog](https://devblogs.microsoft.com/semantic-kernel/release-the-agents-sk-agents-framework-rc1/)
  
  **AutoAuth Solution Accelerator** – https://github.com/Azure-Samples/autoauth-solution-accelerator offers a turnkey sample for integrating secure, automated authentication in Azure-hosted apps, ideal for regulated or enterprise scenarios. [GitHub](https://github.com/Azure-Samples/autoauth-solution-accelerator)
  
  **Cursor Install Guide** – https://learn-cursor.com/en/wiki/user-guide/install walks developers through installing Cursor, a next-gen AI coding assistant IDE designed to optimize productivity across multi-agent workflows. [Guide](https://learn-cursor.com/en/wiki/user-guide/install)
  
  **Getting Started with GitHub Copilot for Enterprise** – https://learn.microsoft.com/en-us/training/modules/introduction-to-github-copilot-enterprise/3-how-to-get-started is an official Microsoft Learn module to onboard teams to GitHub Copilot Enterprise, covering policy setup, integration, and initial usage. [Module](https://learn.microsoft.com/en-us/training/modules/introduction-to-github-copilot-enterprise/3-how-to-get-started)
  
  **MCP-Go Example (Everything)** – https://github.com/mark3labs/mcp-go/blob/main/examples/everything/main.go showcases a full-featured Go-based implementation of the Model Context Protocol (MCP), useful for understanding message orchestration in AI agents. [GitHub](https://github.com/mark3labs/mcp-go/blob/main/examples/everything/main.go)
  
  **Build a Model Context Protocol (MCP) Server in C#** – https://devblogs.microsoft.com/dotnet/build-a-model-context-protocol-mcp-server-in-csharp/ is a detailed walkthrough from the .NET team on building an MCP-compliant server in C#, illustrating key concepts of stateful AI orchestration. [Blog](https://devblogs.microsoft.com/dotnet/build-a-model-context-protocol-mcp-server-in-csharp/)
  
  **AzureChat** – https://github.com/microsoft/azurechat is a Microsoft-built reference app that demonstrates real-time chat using Azure OpenAI, SignalR, and Cognitive Search, designed as a production-grade Copilot pattern. [GitHub](https://github.com/microsoft/azurechat)

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

#### Extra Credit Bonus:

**Additional Labs**

[Expert Level Lab - Running LLM Locally](expertlab-phi-3.md)

[Expert Level Lab - Azure AI Agent Service](https://github.com/microsoft/build-your-first-agent-with-azure-ai-agent-service-workshop)

