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

- [Boston Healthcare Cloud and AI Community Resources]()

- **AI Agents for Beginners** – https://github.com/microsoft/ai-agents-for-beginners offers a 10-lesson, clone-and-run curriculum that walks you from first prompt to multi-agent RAG patterns, making it the fastest on-ramp to Microsoft-flavoured enterprise agents. [GitHub](https://github.com/microsoft/ai-agents-for-beginners/blob/main/README.md)

- **Generative AI for Beginners (.NET)** – https://github.com/microsoft/Generative-AI-for-beginners-dotnet distills hands-on C# examples and MCP/Semantic-Kernel integrations into bite-sized lessons so .NET developers can embed LLM power without leaving their comfort zone. [GitHub](https://github.com/microsoft/Generative-AI-for-beginners-dotnet/blob/main/README.md)

  **AI Agents Hackathon** – https://github.com/microsoft/AI_Agents_Hackathon bundles slides, code starters, and session replays from Microsoft’s three-week virtual hack, giving you community-tested blueprints (and prize-winning ideas) for building production-ready agents. [GitHub](https://github.com/microsoft/AI_Agents_Hackathon/blob/main/README.md)

  **Magma** – https://github.com/microsoft/Magma open-sources Microsoft Research’s multimodal foundation model that lets agents see, plan, and act across images, video, and text—crucial for the next wave of perceptive enterprise agents. [GitHub](https://github.com/microsoft/Magma)

  **AI Developer (Semantic Kernel Fundamentals)** – https://github.com/microsoft/ai-developer presents eight progressive challenges (C# & Python) that teach Azure AI Foundry, plugin auto-calling, RAG, and multi-agent workflows, serving as a deeper-dive companion to the beginner course. [GitHub](https://github.com/microsoft/ai-developer)

  **Agent Innovator Lab** – https://github.com/Azure/agent-innovator-lab provides modular Azure-centric labs on agentic RAG, evaluation, and optimization design patterns, making it ideal for teams refining real-world agent architectures. [GitHub](https://github.com/Azure/agent-innovator-lab)

  **Azure AI Agents Labs** – https://github.com/Azure/azure-ai-agents-labs contains notebook-style labs that showcase the brand-new Azure AI Agent Service SDK + Semantic Kernel working together, guiding you from a single tool-calling agent to a full multi-agent system. [GitHub](https://github.com/Azure/azure-ai-agents-labs)