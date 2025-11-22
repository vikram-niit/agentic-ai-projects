LangChain Multi-Tool Agent Example



This repository demonstrates how to build a LangChain agent that can use multiple tools—including a Python REPL, Wikipedia search, and math utilities—to answer complex, multi-step questions using OpenAI’s gpt-4o-mini model.



Features



Loads OpenAI API Key from a local file (openai\_key.txt)



Uses ChatOpenAI as the LLM



Integrates several LangChain tools:



llm-math — mathematical reasoning



wikipedia — factual lookup



PythonREPLTool — execute Python code safely inside an agent loop



Sets up a Zero-Shot ReAct agent, enabling reasoning loops



Runs an example query combining factual lookup and numeric computation



Requirements



Install dependencies:



pip install langchain langchain-openai langchain-experimental wikipedia





Ensure you have an OpenAI API key stored in:



openai\_key.txt





The file must contain only the API key.



How to Run

python main.py





The agent will:



Look up the current Prime Minister of India (via Wikipedia)



Count letters in their first name



Multiply by 3



Take the square root



Produce a final answer



Verbose mode is enabled so the full reasoning steps are printed.



File Structure

.

├── main.py

└── openai\_key.txt



Notes



The script uses AgentType.ZERO\_SHOT\_REACT\_DESCRIPTION to enable step-by-step reasoning.



The Python REPL tool is included for dynamic computation when needed.



For production use, avoid storing API keys in plaintext files.

