**CrewAI** is a framework used to build systems where multiple AI agents collaborate to complete tasks—kind of like a team of specialized assistants working together instead of a single chatbot doing everything.

### 🧠 What CrewAI does

CrewAI lets you define:

* **Agents** → individual AIs with specific roles (e.g., researcher, writer, coder)
* **Tasks** → what each agent is responsible for
* **Crew** → the full team working together toward a goal

These agents can communicate, delegate work, and combine their outputs to solve more complex problems than a single AI could handle.

---

### ⚙️ How it works (simple example)

Imagine you want to write a blog post:

1. **Research Agent** → gathers information
2. **Writer Agent** → drafts the article
3. **Editor Agent** → refines and improves it

CrewAI orchestrates this workflow automatically.

---

### 🚀 Key features

* Multi-agent collaboration
* Role-based AI behavior
* Task delegation and sequencing
* Integration with tools (APIs, databases, etc.)
* Custom workflows

---

### 🧩 Where it's used

* Content creation pipelines
* Automated research systems
* Customer support workflows
* Coding assistants with multiple roles
* Business process automation

---

### 🛠️ Tech context

CrewAI is typically used with:

* Python
* LLMs like GPT models
* Tools like APIs, vector databases, or search systems

---

### 🧭 In one sentence

CrewAI = **a way to build a team of AI agents that work together to solve complex tasks.**

---

Here’s a **clear, step-by-step guide** to install and run **CrewAI** locally 👇

---

# ⚙️ 1. Prerequisites

Make sure you have:

* **Python 3.10–3.12**
* **pip** installed
* An API key (usually from OpenAI or another LLM provider or Ollama)



# 📦 2. Install CrewAI

Create a virtual environment (recommended):

```bash
uv tool install crewai==0.130.0 --python 3.12
```

Activate it:

**Windows:**

```bash
crewai-env\Scripts\activate
```

# 3. Project

Debate system

created two ajents -> one deabtere and one jude debater:
  role: >
    A compelling debater
  goal: >
    Present a clear argument either in favor of or against the motion. The motion is: {motion}
  backstory: >
    You're an experienced debator with a knack for giving concise but convincing arguments.
    The motion is: {motion}
  llm: "ollama/llama3.2:1b"

judge:
  role: >
    Decide the winner of the debate based on the arguments presented
  goal: >
    Given arguments for and against this motion: {motion}, decide which side is more convincing,
    based purely on the arguments presented.
  backstory: >
    You are a fair judge with a reputation for weighing up arguments without factoring in
    your own views, and making a decision based purely on the merits of the argument.
    The motion is: {motion}
  llm: "ollama/llama3.2:1b"


  task -> propose and oppose -> based on disuccsion choose which is best

  
