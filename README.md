# 🧠 Research AI Agent

A Python-based intelligent research assistant powered by LLMs (Large Language Models) and tool-calling capabilities via LangChain. This agent automatically searches, summarizes, and structures research information on any topic using external tools like web search and Wikipedia.

---

## 📌 Features

- 🤖 LLM-powered content generation with **Groq’s LLaMA 3**, Mixtral, or Gemma models
- 🔍 Web and Wikipedia search tools for grounded research
- 📄 Structured output using **Pydantic models**
- 🛠️ Extensible tool system via LangChain’s `create_tool_calling_agent`
- 💾 Optional saving of results with `save_tool`

---

## 🛠️ Tech Stack

- Python 3.10+
- [LangChain](https://www.langchain.com/)
- [Groq](https://groq.com/)
- OpenAI / Anthropic (optional)
- Pydantic for structured output
- `dotenv` for environment variable handling

---

## 🧩 Project Structure

```text
.
├── main.py              # Entry point of the agent
├── tools.py            # Custom tool definitions (search, wiki, save, etc.)
├── .env                # API keys and environment variables
└── README.md           # You're reading it!

```





🚀 Getting Started
1. Clone the repository
``` bash
    git clone https://github.com/Sophie-Muchiri12/Research_AI_Agent.git
    cd Research_AI_Agent
```

2. Create a virtual environment

   ```bash
    python -m venv venv
    source venv/bin/activate     # On Linux/macOS
    venv\Scripts\activate        # On Windows

   ```

3. Install dependencies

   ``` bash

    pip install -r requirements.txt

   ```

4. Set up your .env file
   Create a .env file in the root directory:

```bash

    GROQ_API_KEY=your_groq_api_key

```

🧪 How to Run

``` bash


    python3 main.py or python main.py

```

When prompted 

``` bash


    What do you want to research?

```

Type your topic (e.g. Kenya's independence) and let the AI agent do the work.

The agent will:

1. Query the tools

2. Use the LLM to generate a summary

3. Print structured output including:

      Topic, Summary, Sources, Tools used




# 🧰 Built-in Tools

You can customize or extend tools in tools.py. Current tools include:

1. search_tool: Performs online search queries.

2. wiki_tool: Pulls summaries from Wikipedia.

3. save_tool: Optionally saves results to disk or a file.

   

# 🧠 Sample Output

``` bash

{
  "topic": "Kenya's independence",
  "summary": "Kenya gained independence from Britain in 1963 after years of anti-colonial struggle...",
  "sources": [
    "https://en.wikipedia.org/wiki/History_of_Kenya",
    "https://www.britannica.com/place/Kenya"
  ],
  "tools_used": ["wiki_tool", "search_tool"]
}



```



