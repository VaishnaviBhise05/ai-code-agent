# AI Code Agent Code Generation, Execution & Debugging

An AI-powered multi-agent project using AutoGen to generate Python code, execute it, detect errors, and iteratively improve solutions through agent-to-agent communication.

## Overview

This project demonstrates how two AI agents work together to solve programming and data-analysis tasks.

- **AssistantAgent:** Generates Python code, analyzes execution feedback, and suggests corrections.
- **UserProxyAgent:** Executes generated code, captures results, and returns feedback to the assistant.

The agents continue communicating until the task is completed or the configured reply limit is reached.

## Features

- Automated Python code generation
- Code execution using AutoGen's local command-line executor
- Error feedback and iterative debugging
- Stock price data retrieval using Yahoo Finance
- Stock price comparison and visualization
- CSV data export and PNG chart generation
- AI-generated data analysis and blog summaries
- Chat history, conversation summary, and API cost reporting

## Technology Stack

- Python
- AutoGen AgentChat 0.2
- OpenAI API
- Matplotlib
- yfinance
- Jupyter Notebook

## Project Workflow

1. The user provides a task.
2. AssistantAgent generates Python code.
3. UserProxyAgent executes the code.
4. The execution result or error is returned to the assistant.
5. The assistant can revise the code based on the feedback.
6. The workflow produces results such as stock data, charts, and a written analysis.

## Project Structure

```text
ai-code-agent/
├── agentchat_auto_feedback_from_code_execution.ipynb
├── README.md
├── requirements.txt
├── .gitignore
└── .env.example
```

## Setup and Installation

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/ai-code-agent.git
cd ai-code-agent
```

Replace `YOUR_USERNAME` with your GitHub username.

### 2. Create a virtual environment

Windows:

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
```

### 3. Install dependencies

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### 4. Configure your OpenAI API

Create your local AutoGen configuration file named `OAI_CONFIG_LIST` and configure a valid OpenAI API key. Follow the configuration format supported by AutoGen 0.2.

**Never upload API keys, passwords, or private credentials to GitHub.**

### 5. Run the notebook

```bash
jupyter notebook agentchat_auto_feedback_from_code_execution.ipynb
```

Run the notebook cells in order after completing the configuration.

## Generated Outputs

The notebook is designed to generate:

- `coding/stock_price_ytd.csv` — collected stock price data
- `coding/stock_price_ytd.png` — stock price comparison chart
- Chat history and a generated data-analysis summary

The output files are created only if the relevant notebook cells execute successfully.

## Safety Notice

This project executes AI-generated Python code locally. Generated code should be reviewed before execution. Do not run untrusted code on your main system. Use a properly isolated environment with appropriate time and resource limits for safer experimentation.

## Future Improvements

- Add a Streamlit web interface
- Add user-defined coding tasks
- Display execution logs and errors
- Add safer, isolated code execution
- Support additional data-analysis tasks
- Add automated tests

