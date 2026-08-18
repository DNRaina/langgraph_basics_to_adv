# LangGraph & LangChain: From Basics to Advanced Labs 🚀

A comprehensive, hands-on collection of progressive labs exploring **LangGraph** and **LangChain** concepts, design patterns, architectures, and real-world agentic workflows — from foundational state graphs to advanced multi-agent systems, human-in-the-loop, and MCP integrations.

---

## 📚 Curriculum & Lab Directory

The repository is structured into sequential labs, each targeting a specific core concept or design pattern:

| Lab | Topic / Design Pattern | Key Concepts Covered |
|---|---|---|
| **[Lab 1: Basic State Graph](lab_1.ipynb)** | Foundational Graph & State | • `StateGraph`, `START`, `END`<br>• Defining typed states with `TypedDict`<br>• Sequential node execution & state transitions |
| **[Lab 2: LLM Node Integration](lab_2.ipynb)** | Single LLM Node Execution | • Integrating Chat Models into graph nodes<br>• Invoking LLMs within stateful functions |
| **[Lab 3: Prompt Chaining Pattern](lab_3.ipynb)** | Sequential Prompt Chaining | • Outline generation ➔ Full blog generation<br>• Multi-step prompt pipelines passing structured context |
| **[Lab 4: Parallel Execution Pattern](lab_4.ipynb)** | Parallel Branching (Fan-Out / Fan-In) | • Running parallel computation nodes simultaneously<br>• Aggregating independent branch states into a summary node |
| **[Lab 5: Parallel Evaluation & Structured Output](lab_5.ipynb)** | Multi-Aspect Evaluation & Schema Parsing | • Parallel evaluator nodes (Language, Analysis, Thought)<br>• Structured output parsing using Pydantic `BaseModel`<br>• Multi-criteria decision scoring |
| **[Lab 6: Deterministic Branching](lab_6.ipynb)** | Math & Logic Branching | • Conditional execution based on numerical state (discriminant calculation)<br>• Branching between real and imaginary root paths |
| **[Lab 7: Routing & Conditional Edges](lab_7.ipynb)** | Router Pattern | • Dynamic routing using `add_conditional_edges`<br>• Sentiment analysis with structured schema<br>• Conditional resolution flows (positive acknowledgement vs. negative diagnosis) |
| **[Lab 8: Evaluator-Optimizer Pattern](lab_8.ipynb)** | Feedback & Self-Correction Loops | • Iterative generation, evaluation, and optimization cycles<br>• Cyclic graphs with conditional termination criteria (score thresholds) |
| **[Lab 9: Conversational State & Message Reducers](lab_9.ipynb)** | Chat State Management | • Managing chat history using `BaseMessage`, `HumanMessage`, `AIMessage`<br>• Utilizing message reducers (`add_messages`) in LangGraph |
| **[Lab 10: Checkpointing & Fault Tolerance](lab_10.ipynb)** | Persistence & State Recovery | • Checkpointing with `InMemorySaver` / `MemorySaver`<br>• Thread-level isolation (`thread_id`)<br>• Resuming interrupted or crashed workflows from persisted states |
| **[Lab 11: Tool Calling & ReAct Agent Pattern](lab_11.ipynb)** | Tool Integration & ReAct Architecture | • Binding custom tools (Calculator, Stock Price, Web Search) to LLM<br>• `ToolNode` and `tools_condition` for autonomous tool execution loops |
| **[Lab 12: Model Context Protocol (MCP) Integration](lab_12.ipynb)** | External Tool Ecosystems via MCP | • Connecting LangGraph agents to MCP servers<br>• Dynamic tool discovery and async tool execution |
| **[Lab 13: Agentic RAG](lab_13.ipynb)** | Retrieval-Augmented Generation Tool Pattern | • Vector stores and retrieval workflows as tools<br>• Enabling LLM agents to autonomously retrieve and synthesize external knowledge |
| **[Lab 14: Human-in-the-Loop (HITL)](lab_14.ipynb)** | Human Approval & Interruptions | • Dynamic pausing with `interrupt()`<br>• State inspection and approval workflows<br>• Resuming execution with human feedback via `Command(resume=...)` |
| **[Lab 15: Subgraphs & Hierarchical Graphs](lab_15.ipynb)** | Modular Graph Architecture | • Composing graphs within graphs (Subgraphs)<br>• Encapsulating domain-specific sub-workflows (e.g. translation, validation) inside parent state graphs |

---

## 🛠️ Key Design Patterns Demonstrated

- **Chaining Pattern**: Sequential pipeline where each node refines or adds to state.
- **Parallelization Pattern (Fan-Out / Fan-In)**: Concurrently processing independent tasks and combining results.
- **Router Pattern**: Directing inputs to specialized handlers or workflows using conditional logic.
- **Evaluator-Optimizer Loop**: Iterative refinement with self-critique until quality benchmarks are met.
- **ReAct Agent Pattern**: Reasoning, tool selection, action execution, and observation feedback loops.
- **Human-in-the-Loop (HITL)**: Integrating human review, safety approvals, or guidance into automated flows.
- **Hierarchical / Subgraph Pattern**: Modularizing complex multi-agent logic into reusable subgraphs.

---

## 🚀 Getting Started

### 1. Prerequisites & Installation

Clone the repository and install the required dependencies:

```bash
git clone https://github.com/DNRaina/langgraph_basics_to_adv.git
cd langgraph_basics_to_adv

# Install core packages
pip install langchain langchain-openai langchain-community langgraph
```

### 2. Environment Setup

Create a `.env` file or export your API keys in your terminal:

```bash
export OPENAI_API_KEY="your-openai-api-key"
# Optional: Add any search/MCP keys if required by specific labs
```

### 3. Running the Labs

Launch Jupyter Notebook / JupyterLab and open the labs sequentially:

```bash
jupyter lab
```

---

## 📖 Suggested Learning Path

1. **Foundations (Labs 1–6)**: Master core graph mechanics, typed states, parallel node execution, and deterministic branching.
2. **Dynamic Workflows & Loops (Labs 7–10)**: Implement conditional routing, evaluator-optimizer loops, chat state handling, and persistent checkpoints.
3. **Agentic Workflows & Tool Use (Labs 11–13)**: Build ReAct agents, integrate MCP tools, and construct agentic RAG systems.
4. **Production Patterns (Labs 14–15)**: Implement human-in-the-loop gates and composite hierarchical subgraphs.