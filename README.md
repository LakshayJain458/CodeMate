# 🛠️ CodeMate

**CodeMater** is an AI-powered coding assistant inspired by multi-agent systems. Built using LangGraph and open-source LLMs, it acts as an automated development team that can transform natural language requests into full software projects—file by file—mimicking real developer workflows.

***

## 🏗️ Architecture

- **Planner Agent:** Analyzes project requests and develops a detailed technical roadmap.
- **Architect Agent:** Decomposes the plan into actionable engineering tasks with file-specific instructions.
- **Coder Agent:** Executes each engineering task, writes code, refactors, and creates files autonomously.

***

## 🚀 Getting Started

### Prerequisites

- Install [uv](https://docs.astral.sh/uv/getting-started/installation/) for environment management.
- Obtain your API key from your preferred LLM provider (e.g. GROQ, OpenRouter, etc), and keep it available.

### ⚙️ Installation and Startup

```bash
# Create and activate a virtual environment
uv venv
source .venv/bin/activate

# Install dependencies
uv pip install -r requirements.txt

# Configure environment variables
cp .sample_env .env
# Edit .env with your values
```

To start the application:
```bash
python graph.py
```

***

## ✨ Features

- Converts **natural language prompts into real code projects**
- Supports multiple **project templates** (e.g. web apps, APIs, utilities)
- Multi-agent design for **planning, architecture, and coding**
- Modular and extensible codebase

***

## 🧪 Example Prompts

- Build a personal blog app using React and Express.js.
- Create a RESTful API for a TODO application using FastAPI.
- Scaffold an e-commerce store's backend with authentication using Django.

***

## 📂 agent Module Structure
- `graph.py`  
  Main orchestration: Defines the multi-agent workflow (planner, architect, coder) and their interactions using LangGraph. Sets up and compiles the agent graph.

- `prompts.py`  
  Prompt templates for each agent; specifies system instructions for the planning, architectural breakdown, and coding stages.

- `states.py`  
  Typed data models and state representations for plans, tasks, and agent progress (using Pydantic).

- `tools.py`  
  Utility tools and wrappers for the agents (file I/O, file listing, shell execution, working directory access).


***

## 👥 Credits

Developed by Lakshay Jain. Inspired by [codebasics/coder-buddy].

***

## 📝 License

MIT License. See `LICENSE` for details.
