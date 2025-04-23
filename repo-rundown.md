## Repo Rundown

We’ll be coding against two freshly minted Microsoft repos that showcase the same agentic patterns from two angles:

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