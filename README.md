# LLM-Powered Data Analysis Agent

An AI-powered data analysis project that demonstrates how **Large Language Models (LLMs), LangChain, and Pandas** can work together to answer natural-language questions about structured datasets.

The project uses an OpenAI language model with a LangChain Pandas DataFrame agent to explore the Titanic dataset, perform basic data analysis, and interact with multiple DataFrames.

## Project Overview

Traditional data analysis often requires users to write Python or Pandas code for every operation. This project explores a more intuitive approach: allowing users to ask questions in natural language and letting an LLM-powered agent assist with data analysis.

The notebook demonstrates how to connect an LLM to Pandas DataFrames and investigate data through natural-language prompts.

## Objectives

- Understand the role of LLMs in AI-powered applications.
- Explore LangChain agents and their interaction with structured data.
- Query Pandas DataFrames using natural language.
- Analyze a dataset using an LLM-powered workflow.
- Handle missing values and compare transformed DataFrames.
- Explore how agents can work with multiple DataFrames.

## Technologies Used

- **Python** — Core programming language.
- **OpenAI LLM** — Natural-language understanding and response generation.
- **LangChain** — Framework for connecting the language model to an agent workflow.
- **LangChain Experimental** — Pandas DataFrame agent implementation used in the notebook.
- **Pandas** — Data manipulation, cleaning, and analysis.
- **Jupyter Notebook** — Interactive development and experimentation.
- **Titanic Dataset** — Sample dataset for data-analysis experiments.

## Key Concepts Implemented

### 1. Large Language Models (LLMs)

An LLM is an AI model trained on large amounts of data to understand and generate language. In this project, the language model helps interpret natural-language questions and supports the agent's data-analysis workflow.

### 2. LangChain Agents

The project uses a LangChain Pandas DataFrame agent to connect the language model with DataFrame operations. The agent processes user questions and uses its available data-analysis capabilities to generate answers.

### 3. Natural-Language Data Analysis

The notebook demonstrates queries such as:

- How many rows are there?
- How many people have more than three siblings?
- How many rows in the age column are different?
- Are the numbers of columns the same across all DataFrames?

### 4. Data Cleaning and Transformation

The project creates a copy of the original DataFrame and fills missing values in the `Age` column using the column's mean.

### 5. Multiple DataFrame Analysis

The notebook explores passing multiple DataFrames to the agent, comparing the original and transformed data, and examining differences in their structures.

It also creates a derived column named `Age_Multiplied` by multiplying age values by two.

## Project Workflow

1. Import the required Python libraries.
2. Configure access to the OpenAI language model.
3. Load the Titanic dataset into a Pandas DataFrame.
4. Create a LangChain Pandas DataFrame agent.
5. Submit natural-language questions for data exploration.
6. Handle missing age values using mean imputation.
7. Create additional DataFrames and transformed columns.
8. Explore questions involving multiple DataFrames.

## Installation

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/llm-powered-data-analysis-agent.git
cd llm-powered-data-analysis-agent
```

Create and activate a virtual environment:

```bash
python -m venv venv
```

On Windows:

```bash
venv\Scripts\activate
```

Install the required libraries:

```bash
pip install pandas openai langchain langchain-experimental jupyter
```

**Compatibility note:** The notebook uses older LangChain APIs, including `langchain.llms.OpenAI` and `agent.run()`. Depending on the installed versions, these may require an older compatible environment or migration to current LangChain APIs. Pin and test compatible dependency versions before running the original notebook.

## API Configuration

Set your OpenAI API key through an environment variable instead of writing it directly into the notebook.

Windows PowerShell:

```powershell
$env:OPENAI_API_KEY="your-api-key"
```

Python:

```python
import os

api_key = os.environ.get("OPENAI_API_KEY")
if not api_key:
    raise ValueError("Set the OPENAI_API_KEY environment variable.")
```

Never commit API keys, passwords, or other secrets to GitHub.

## Run the Project

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open `Langchain_Agents.ipynb`, configure your API key, update the dataset path to match your system, and execute the notebook cells in order.

The notebook expects a local Titanic dataset CSV file. Ensure the file exists at the configured path before running the data-loading cell.

## Practical Applications

This approach can serve as a starting point for:

- Natural-language dataset exploration.
- Business data analysis and reporting.
- Exploratory data analysis (EDA).
- Data quality checks and dataset comparisons.
- AI-assisted analytical workflows.

The current project is a notebook-based prototype, not a production-ready analytics platform.

## Future Enhancements

- Build a Streamlit interface for interactive data analysis.
- Add automated charts and data visualizations.
- Connect SQL databases for querying larger datasets.
- Add Retrieval-Augmented Generation (RAG) for document-grounded analysis.
- Introduce input validation, restricted tool access, and execution safeguards.
- Add error handling, logging, and automated tests.
- Explore multi-agent workflows for specialized analytical tasks.
- Evaluate answer accuracy and reliability against known results.

## Learning Outcomes

Through this project, I explored the integration of LLMs with Python data-processing tools, LangChain agent workflows, natural-language querying, data cleaning, and multi-DataFrame analysis.

## Author

**Pavan Kumar Torlapati**

GitHub: https://github.com/PavanTorlapatiCodes

LinkedIn: https://www.linkedin.com/in/pavan-torlapati-7543732ba/

---

*This project was developed for hands-on learning and experimentation with LLM-powered data analysis.*
