# OpenAI Agents SDK
<!-- Badges -->
<p align="center">
  <!-- GitHub Stars -->
  <!-- Open Issues -->
  <a href="https://github.com/Rishi-Kora/OpenAI-Agents-SDK/issues">
    <img src="https://img.shields.io/github/issues/Rishi-Kora/OpenAI-Agents-SDK" alt="Open Issues" />
  </a>
  <!-- Contributors -->
  <a href="https://github.com/Rishi-Kora/OpenAI-Agents-SDK/graphs/contributors">
    <img src="https://img.shields.io/github/contributors/Rishi-Kora/OpenAI-Agents-SDK" alt="Contributors" />
  </a>
  <!-- License -->
  <a href="https://github.com/Rishi-Kora/OpenAI-Agents-SDK/blob/main/LICENSE">
    <img src="https://img.shields.io/github/license/Rishi-Kora/OpenAI-Agents-SDK" alt="License: MIT" />
  </a>
</p>




A lightweight Python SDK providing easy-to-use abstractions and utilities to build intelligent agents on top of the OpenAI API.

##  Features

- **Agent Framework**: Quickly spin up LLM-based agents with customizable behaviors.
- **Tool Integration**: Seamless wrappers for external tools (e.g., search, calculators).
- **Memory Management**: Built-in short-term and long-term memory abstractions.
- **Asynchronous Support**: Fully async API for high-throughput applications.
- **Extensible**: Plug in your own toolkits, memory stores, and workflows.

##  Installation

Install via PyPI:

```bash
pip install OpenAI-Agents-SDK
````

Or clone and install from source:

```bash
git clone https://github.com/Rishi-Kora/OpenAI-Agents-SDK.git
cd OpenAI-Agents-SDK
pip install -e .
```

##  Quick Start

```python
from openai_agents_sdk import Agent, Tool

# Define a simple tool
class CalculatorTool(Tool):
    name = "calculator"
    def run(self, query: str) -> str:
        # implement simple calculation logic
        return str(eval(query))

# Create an agent with the tool
agent = Agent(
    name="CalcBot",
    tools=[CalculatorTool()]
)

# Ask the agent a question
response = agent.run("What is 3 * 12 + 5?")
print(response)  # ➜ 41
```

For a full tutorial and advanced examples, see [examples/](./examples) and the Jupyter notebook [OpenAI\_Agents\_SDK.ipynb](./OpenAI_Agents_SDK.ipynb).

## 📚 Documentation

* **API Reference**: [https://rishi-kora.github.io/OpenAI-Agents-SDK/](https://rishi-kora.github.io/OpenAI-Agents-SDK/)
* **Tutorials**: [https://github.com/Rishi-Kora/OpenAI-Agents-SDK/tree/main/docs](https://github.com/Rishi-Kora/OpenAI-Agents-SDK/tree/main/docs)
* **Changelog**: See [Releases](https://github.com/Rishi-Kora/OpenAI-Agents-SDK/releases).

##  Contributing

Contributions are welcome! Please:

1. Fork the repo.
2. Create a feature branch: `git checkout -b feature/YourFeature`.
3. Commit your changes: `git commit -m 'Add YourFeature'`.
4. Push to branch: `git push origin feature/YourFeature`.
5. Open a Pull Request.

See [CONTRIBUTING.md](./CONTRIBUTING.md) for more details.

##  License

This project is licensed under the **MIT License**. See [LICENSE](./LICENSE) for details.

##  Contact

* **Author**: Rishi Kora
* **Email**: [korarishi@gmail.com](mailto:rishi.kora@example.com)

---

*Made with ❤️ and ☕ in London.*

