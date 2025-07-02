# Crew-AI Demo

This project demonstrates how to use [CrewAI](https://github.com/joaomdmoura/crewAI) to orchestrate a team of AI agents for researching and writing a blog post on a given topic. The agents collaborate sequentially to research and generate content, showcasing the power of agentic workflows.

---

## Features

- **Tech-focused AI Crew:**  
  Two agents (`blog_researcher` and `blog_writer`) work together to research and write about a specified topic.
- **Sequential Task Execution:**  
  Tasks are executed in order, ensuring research is completed before writing.
- **Enhanced Configurations:**  
  Includes memory, caching, rate limiting, and crew sharing options.

---

## Requirements

- **Python 3.10-3.12** (Recommended: Python 3.12)
- **pip** (Python package manager)
- **Microsoft C++ Build Tools** (Windows only, for some dependencies)
- **OpenAI API Key** (for agent LLM access)

---

## Getting an OpenAI API Key

1. Go to [OpenAI Platform](https://platform.openai.com/signup) and sign up or log in.
2. Navigate to your [API Keys page](https://platform.openai.com/api-keys).
3. Click **Create new secret key** and copy the generated key.

**Keep your API key safe and do not share it publicly.**

---

## Setting Your OpenAI API Key

Set your API key as an environment variable so CrewAI and its agents can access it.

- **Windows (Command Prompt):**
  ```cmd
  set OPENAI_API_KEY=your-api-key-here
  ```
- **Windows (PowerShell):**
  ```powershell
  $env:OPENAI_API_KEY="your-api-key-here"
  ```
- **macOS/Linux:**
  ```bash
  export OPENAI_API_KEY=your-api-key-here
  ```

You can also add this line to your `.env` file if your project uses [python-dotenv](https://pypi.org/project/python-dotenv/).

---

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/arun250492/crewai-demo.git
cd crewai-demo/Crew-AI-demo
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
```

Activate the virtual environment:

- **Windows:**
  ```bash
  venv\Scripts\activate
  ```
- **macOS/Linux:**
  ```bash
  source venv/bin/activate
  ```

### 3. Install Dependencies

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

> **Note:**  
> If you see errors about `Microsoft Visual C++ 14.0 or greater is required`, [download and install Build Tools](https://visualstudio.microsoft.com/visual-cpp-build-tools/) and restart your terminal.

---

## Usage

1. **Set your OpenAI API key** as described above.
2. Run the main script:

```bash
python crew.py
```

This will start the crew, execute the research and writing tasks,
