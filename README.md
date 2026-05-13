# LangChain & LangGraph End-to-End Tutorials

## Overview

This repository contains two comprehensive tutorials for building intelligent applications with Python:

1. **LangChain Tutorial** - Framework for developing applications powered by language models
2. **LangGraph Tutorial** - State machines and multi-agent orchestration patterns

## Table of Contents

- [LangChain Tutorial](#langchain-tutorial)
- [LangGraph Tutorial](#langgraph-tutorial)
- [Installation](#installation)
- [Quick Start](#quick-start)

---

## LangChain Tutorial

### What is LangChain?

LangChain is a framework that simplifies developing applications with large language models (LLMs). It provides tools for:
- **Prompt management** and templating
- **Memory** and conversation history
- **Chains** for combining multiple operations
- **Agents** for autonomous decision-making
- **Integration** with external APIs and databases

### Key Concepts

#### 1. **Language Models**
- Working with OpenAI, Anthropic, local models
- Prompt engineering best practices
- Temperature, tokens, and sampling strategies

#### 2. **Prompt Templates**
- Dynamic prompt construction
- Variable interpolation
- Few-shot examples
- Output parsing and validation

#### 3. **Chains**
A sequence of operations combining LLMs with other tools:
- **LLMChain**: Simple LLM + prompt template
- **SequentialChain**: Multiple chains in sequence
- **RouterChain**: Conditional routing based on input
- **SQLDatabaseChain**: SQL generation and execution

#### 4. **Memory**
Maintain conversation context:
- **BufferMemory**: Store all messages
- **ConversationSummaryMemory**: Summarize for efficiency
- **EntityMemory**: Track specific entities
- **VectorStoreMemory**: Semantic search over history

#### 5. **Agents**
Autonomous systems that decide which tools to use:
- **ReAct**: Reasoning and acting
- **Chain-of-Thought**: Step-by-step reasoning
- **Self-Ask**: Recursive question answering

#### 6. **Tools & Utilities**
- Web search integration
- Calculator tools
- Database queries
- API integrations
- File operations

### Processes Covered

| Process | Description |
|---------|-------------|
| **Model Selection** | Choose appropriate LLM for your use case |
| **Prompt Design** | Create effective prompts with examples and instructions |
| **Chain Building** | Combine operations into workflows |
| **Memory Management** | Maintain conversation state and context |
| **Agent Development** | Build autonomous systems with tool access |
| **Error Handling** | Graceful degradation and retry logic |
| **Evaluation** | Measure accuracy, latency, and cost |

### Use Cases

- **Chatbots**: Conversational AI with context
- **Q&A Systems**: Document search and question answering
- **Summarization**: Long document condensation
- **Content Generation**: Creative writing and coding
- **Data Analysis**: Converting natural language to SQL
- **Customer Support**: Automated response generation

---

## LangGraph Tutorial

### What is LangGraph?

LangGraph is a framework for building stateful, multi-step applications with language models. It provides:
- **State graphs** for complex workflows
- **Multi-agent coordination** patterns
- **Checkpointing** for fault tolerance
- **Streaming** for real-time updates
- **Production metrics** and monitoring

### Key Concepts

#### 1. **State Management**
Every node maintains and updates application state:
- Initial state definition
- State updates during execution
- Terminal state conditions

#### 2. **Nodes**
Processing units in the graph:
- Read current state
- Execute operations
- Update state
- Return next node (routing)

#### 3. **Edges**
Connections between nodes with routing logic:
- Static edges for fixed connections
- Conditional edges for runtime decisions
- Loop edges for feedback

#### 4. **State Graphs**
Declarative workflow definition connecting nodes and edges

#### 5. **Multi-Agent Patterns**

**Supervisor Pattern**: Central coordinator with worker agents
**Hierarchical Pattern**: Nested agent hierarchies
**Team Pattern**: Peer agents with shared memory

#### 6. **Checkpointing**
Fault tolerance and recovery:
- Thread-level checkpoints
- Batch operation snapshots
- Versioned state history

#### 7. **Production Metrics**
Monitor and optimize:
- **Latency**: Time per node execution
- **Token Usage**: LLM token consumption
- **Success Rate**: Operation completion rate
- **Cost**: Total API costs
- **Throughput**: Operations per second

### Processes Covered

| Process | Description |
|---------|-------------|
| **State Definition** | Define application state schema |
| **Node Creation** | Implement processing logic |
| **Graph Construction** | Connect nodes with routing |
| **Multi-Agent Setup** | Coordinate multiple agents |
| **Error Handling** | Retry and recovery logic |
| **Checkpointing** | Enable fault tolerance |
| **Monitoring** | Track metrics and performance |
| **Optimization** | Improve latency and cost |

### Use Cases

- **Research Workflows**: Collaborative multi-agent research
- **Data Processing**: Complex ETL pipelines
- **Decision Systems**: Multi-stage decision making
- **Content Creation**: Coordinated content generation
- **Quality Assurance**: Automated testing workflows
- **Customer Support**: Escalation and routing

### Architecture Patterns

#### 1. Sequential Processing
Input flows through agents in sequence

#### 2. Parallel Processing
Multiple agents process simultaneously

#### 3. Looping/Iteration
Agents process with conditional loops

#### 4. Branching
Conditional routing to different agents

---

## Installation

### Prerequisites
- Python 3.8+
- pip or conda
- Jupyter Notebook or JupyterLab

### Setup

```bash
# Clone repository
git clone https://github.com/analyticswithharry/lang-chain-and-lang-graph.git
cd lang-chain-and-lang-graph

# Create virtual environment
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Install Jupyter
pip install jupyter jupyterlab
```

### Dependencies

```
langchain
langgraph
openai
python-dotenv
jupyter
matplotlib
```

---

## Quick Start

### Running LangChain Tutorial

```bash
jupyter notebook langchain-end-to-end.ipynb
```

### Running LangGraph Tutorial

```bash
jupyter notebook langgraph-end-to-end.ipynb
```

---

## Key Differences: LangChain vs LangGraph

| Aspect | LangChain | LangGraph |
|--------|-----------|-----------|
| **Purpose** | LLM application components | Stateful workflows |
| **Abstraction** | Chains, agents, memory | State graphs, nodes, edges |
| **State Management** | Memory objects | Explicit state dict |
| **Complexity** | Simple to moderate | Moderate to complex |
| **Multi-agent** | Limited | Built-in support |
| **Checkpointing** | Not primary | Central feature |
| **Use Case** | Chatbots, Q&A | Complex workflows, research |

---

## Resources

### Documentation
- [LangChain Docs](https://python.langchain.com/)
- [LangGraph Docs](https://langchain-ai.github.io/langgraph/)
- [LLM Concepts](https://platform.openai.com/docs/concepts)

### Tools & APIs
- [OpenAI API](https://platform.openai.com/)
- [Anthropic Claude](https://www.anthropic.com/)
- [Local Models](https://ollama.ai/)

---

## License

MIT License - See LICENSE file for details

---

**Last Updated**: May 2026
**Author**: Analytics with Harry
**Version**: 1.0

