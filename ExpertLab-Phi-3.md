# Expert Lab — Running **Phi-3 Mini** Locally with **ONNX Runtime GenAI** (CPU Edition)

Hands-on-lab for enterprise developers to prove an LLM can run completely offline and then plug it into a Semantic Kernel agent.

------

## Why local models matter 

Running inference on-prem or at the edge gives enterprise teams…

- **Data sovereignty & privacy** – no sensitive provider/PHI ever leaves the firewall; avoids vendor lock-in. [Microsoft Tech Community](https://techcommunity.microsoft.com/blog/startupsatmicrosoftblog/optimizing-inference-performance-for-“on-prem”-llms/4358788)
- **Low, predictable latency** – tokens stream from local RAM/CPU instead of round-trips to a cloud API. [NVIDIA Developer](https://developer.nvidia.com/blog/supercharging-llm-applications-on-windows-pcs-with-nvidia-rtx-systems/?utm_source=chatgpt.com)
- **Always-on resilience** – mission-critical apps keep working during WAN or SaaS outages. [Microsoft Tech Community](https://techcommunity.microsoft.com/blog/machinelearningblog/bringing-genai-offline-running-slm’s-like-phi-2phi-3-and-whisper-models-on-mobil/4128056?utm_source=chatgpt.com)
- **Cost control** – once the hardware is bought, inference is “free”; no per-token fees. [Microsoft Tech Community](https://techcommunity.microsoft.com/blog/startupsatmicrosoftblog/optimizing-inference-performance-for-“on-prem”-llms/4358788)

You’ll prove those advantages by loading Microsoft’s **Phi-3 Mini-4K-Instruct** (INT4, ~1.8 GB) entirely on CPU.

------

## Lab goals



| What you’ll do                                              | Proof you’ll collect                                         |
| ----------------------------------------------------------- | ------------------------------------------------------------ |
| [Set up ONNX Runtime GenAI](https://onnxruntime.ai/) on CPU | `pip list` shows `onnxruntime-genai`                         |
| Pull an INT4 model with Git-LFS & HF CLI                    | Folder `phi3/…/model.onnx` exists                            |
| Chat with the model in a terminal                           | You see live responses ≈10-15 tokens/s on a 64-vCPU Xeon [GitHub](https://github.com/microsoft/onnxruntime-genai/issues/436) |
| (Optional) Hit it from C#/Semantic Kernel                   | Console app prints an answer from `serviceId:"local-phi3"`   |

------



## Overview

In this lab, you will learn how to set up and deploy Microsoft's Phi-3 language model using ONNX Runtime. By the end of this lab, you'll have a working Phi-3 model that you can interact with through a Python interface.

Phi-3 is a lightweight yet powerful language model that can be run efficiently on a CPU. ONNX Runtime provides a platform-independent way to deploy machine learning models with high performance.

## Prerequisites

- Windows, Linux, or macOS

- Python 3.10 or later

- Basic familiarity with Python and command-line interfaces

- At least 4GB of free disk space

- Administrative privileges may be required for installation

## Lab Steps

### Step 1: Create and Activate a Python Virtual Environment

First, we'll create an isolated Python environment to avoid conflicts with other packages.

*# Create a virtual environment named ort-env*

python -m venv ort-env

*# Activate the virtual environment*

*# For Windows:*

.\ort-env\Scripts\activate.ps1

You should see (ort-env) appear at the beginning of your command prompt, indicating the environment is active.

### Step 2: Install Required Packages

Now we'll install the packages needed to run Phi-3 with ONNX Runtime.

*# Install onnxruntime-genai package*

pip install onnxruntime-genai

*# Install numpy (required by onnxruntime-genai)*

pip install numpy

*# Install Hugging Face CLI tool for downloading mo**dels*

pip install huggingface-hub[cli]

### Step 3: Create a Project Directory

Create a directory for your Phi-3 project.

*# Create a directory for the Phi-3 project*

mkdir phi3-project

cd phi3-project

### Step 4: Download the Phi-3 Model

Download the Phi-3 model files from Hugging Face.

*# Download the model files (this may take a few mi**nutes depending on your internet speed)*

huggingface-cli download microsoft/Phi-3-mini-4k-instruct-onnx --include cpu_and_mobile/cpu-int4-rtn-block-32-acc-level-4/* --local-dir .

This command will download the optimized INT4 quantized version of Phi-3 mini 4k model specifically for CPU usage.

### Step 5: Create a Quick Test Script

Create a file named quick_test.py with the following code:

*import* onnxruntime_genai *as* ort, time, os

*# Using absolute path to ensure correct loading*

current_dir = os.path.dirname(os.path.abspath(__file__))

MODEL_DIR = os.path.join(current_dir, "cpu_and_mobile", "cpu-int4-rtn-block-32-acc-level-4")

print(f"Loading model from: {MODEL_DIR}")

print(f"Files in model directory: {os.listdir(MODEL_DIR)}")

model   = ort.Model(MODEL_DIR)     *# folder, not the .onnx file*

tokenizer = ort.Tokenizer(model)

prompt = "Quick test: what is ONNX?"

params = ort.GeneratorParams(model)

params.set_search_options(*max_length*=64)  *# optional cap*

gen = ort.Generator(model, params)

gen.append_tokens(tokenizer.encode(prompt))

t0 = time.time()

*while* not gen.is_done():

  gen.generate_next_token()

elapsed = time.time() - t0

answer = tokenizer.decode(gen.get_sequence(0))

print("\n--- MODEL REPLY -----------------------------------")

print(answer)

print("----------------------------------------------------")

print(f"Generated {len(answer.split())} words in {elapsed:.2f}s")

### Step 6: Run the Quick Test

Execute the quick test script to verify that the model works properly.

python quick_test.py

You should see output similar to:

text

Apply

Loading model from: ...\cpu_and_mobile\cpu-int4-rtn-block-32-acc-level-4

Files in model directory: ['added_tokens.json', 'config.json', 'configuration_phi3.py', 'genai_config.json', 'phi3-mini-4k-instruct-cpu-int4-rtn-block-32-acc-level-4.onnx', 'phi3-mini-4k-instruct-cpu-int4-rtn-block-32-acc-level-4.onnx.data', 'special_tokens_map.json', 'tokenizer.json', 'tokenizer.model', 'tokenizer_config.json']

--- MODEL REPLY -----------------------------------

Quick test: what is ONNX?

ONNX is an open standard for interchange of machine learning models.

ONNX stands for Open Neural Network Exchange.

ONNX is an open ecosystem that enables models to be trained and deployed across various frameworks.

\----------------------------------------------------

Generated 39 words in 1.52s

### Step 7: Create an Interactive Chat Script

Now, let's download a more advanced script that allows for interactive chat with the model.

*# Download the phi3-qa.py script from GitHub*

curl https://raw.githubusercontent.com/microsoft/onnxruntime-genai/main/examples/python/phi3-qa.py -o phi3-qa.py

### Step 8: Run the Interactive Chat

Run the interactive chat script with appropriate parameters:

python phi3-qa.py -m cpu_and_mobile/cpu-int4-rtn-block-32-acc-level-4 -e cpu -k 40 -p 0.95 -t 0.8 -r 1.0

Parameter explanation:

- -m: Path to the model directory

- -e: Execution provider (cpu, cuda, or dml)

- -k: Top-k value for token sampling (40)

- -p: Top-p (nucleus sampling) probability threshold (0.95)

- -t: Temperature for sampling (0.8)

- -r: Repetition penalty (1.0)

You should now be able to chat with the model. Enter prompts when prompted for "Input:" and the model will generate responses.

Example interaction:

text

Apply

Input: Tell me about climate change

Output: Climate change refers to long-term shifts in temperatures and weather patterns. These shifts may be natural, such as through variations in the solar cycle. However, since the 1800s, human activities have been the main driver of climate change, primarily due to burning fossil fuels like coal, oil, and gas, which produces heat-trapping gases.

The primary cause of climate change is the greenhouse effect. When we burn fossil fuels, we release greenhouse gases like carbon dioxide (CO2) and methane into the atmosphere. These gases trap heat from the sun, preventing it from escaping back into space, much like a greenhouse traps heat for plants.

The effects of climate change include:

1. Rising global temperatures
2. More frequent and severe weather events (hurricanes, floods, droughts)
3. Rising sea levels due to melting ice caps and glaciers
4. Loss of biodiversity and ecosystems
5. Threats to food security and water supplies
6. Health impacts due to air pollution and disease spread

Addressing climate change requires both mitigation (reducing greenhouse gas emissions) and adaptation (adjusting to climate impacts that are already happening or unavoidable). International efforts like the Paris Agreement aim to limit global warming to well below 2°C compared to pre-industrial levels.

Input:

### Step 9: Experiment with Different Parameters

Try running the chat script with different parameters to see how they affect the model's responses:

bash

Apply

Run

*# More creative outputs (higher temperature)*

python phi3-qa.py -m cpu_and_mobile/cpu-int4-rtn-block-32-acc-level-4 -e cpu -k 40 -p 0.95 -t 1.2 -r 1.0

*# More deterministic outputs (lower temperature)*

python phi3-qa.py -m cpu_and_mobile/cpu-int4-rtn-block-32-acc-level-4 -e cpu -k 40 -p 0.95 -t 0.4 -r 1.0

## Understanding the Code Components

### ONNX Runtime GenAI Components:

- ort.Model: Loads the model from the specified directory

- ort.Tokenizer: Handles text tokenization and detokenization

- ort.GeneratorParams: Sets parameters for text generation

- ort.Generator: Manages the text generation process

### Key Parameters:

- max_length: Maximum number of tokens to generate

- temperature: Controls randomness (higher = more random)

- top_k: Limits sampling to the k most likely tokens

- top_p: Limits sampling to tokens comprising the top p probability mass

- repetition_penalty: Discourages repetition of the same tokens

## Conclusion

Congratulations! You have successfully deployed the Phi-3 language model using ONNX Runtime. You can now use this setup to:

- Build conversational AI applications

- Generate creative text content

- Develop educational tools

- Experiment with different prompt engineering techniques



------

## 6. Integrate with Semantic Kernel (C#) *(10 min)*

```
dotnet new console -n PhiLocal
cd PhiLocal
dotnet add package Microsoft.SemanticKernel
dotnet add package Microsoft.SemanticKernel.Connectors.OnnxRuntimeGenAI
dotnet add package Microsoft.ML.OnnxRuntimeGenAI       # CPU EP
csharpCopyEditusing Microsoft.SemanticKernel;

IKernelBuilder kb = Kernel.CreateBuilder();

kb.AddOnnxChatCompletion(
    modelPath: @"phi3\cpu_and_mobile\cpu-int4-rtn-block-32-acc-level-4\model.onnx",
    tokenizerPath: @"phi3\cpu_and_mobile\cpu-int4-rtn-block-32-acc-level-4\tokenizer.json",
    serviceId: "local-phi3");

var kernel = kb.Build();

var chat = kernel.GetRequiredService<IChatCompletionService>();
var reply = await chat.GetChatMessageContentAsync("List three benefits of local LLMs");
Console.WriteLine(reply.Content);
```

> **Take-away:** your existing SK plugins, planners, and function-calling code stay unchanged—only the `serviceId` switches from OpenAI to `local-phi3`.

------

## 7. Clean-up / next steps

```
deactivate          # if you used the venv
```

- Re-quantize with **Olive** for <1 GB models or GPU builds.
- Wire the model into your RealActivity Copilot’s agent loop.
- Benchmark latency vs. your cloud endpoint.

------

### Review questions for students

1. **Which enterprise concerns make on-prem LLMs attractive for mission-critical apps?**
2. **What does INT4 quantization trade off, and why is it acceptable here?**
3. **How would you hot-swap a GPU provider (`onnxruntime-genai-cuda`) later?**