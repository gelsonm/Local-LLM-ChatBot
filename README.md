# Local-LLM-ChatBot
## Personal Assistant with Streamlit and Ollama LLM

This project implements a personal assistant using Streamlit, LangChain, and a locally downloaded Llama 3.2 model via Ollama. The assistant is designed to engage in interactive conversations, where user input is processed, and responses are generated by the language model. This assistant supports a continuous chat history, providing a conversational experience.

## Features
- Chat interface powered by Streamlit.
- Integration with LangChain for prompt handling and response generation.
- Use of a locally downloaded Llama 3.2 model through Ollama.
- Session-based message history to maintain context across interactions.

## Installation

### Prerequisites

- Python 3.7+
- Streamlit
- LangChain
- Ollama

You will need to install the following dependencies:

```bash
pip install streamlit langchain langchain_ollama
```

## Setup
1. Create a config.py file in your project directory and define the CHAT_PROMPT_TEMPLATE variable. Example:
2. CHAT_PROMPT_TEMPLATE = "Your predefined chat prompt template goes here"

Ensure that you have the Llama 3.2 model downloaded using Ollama and make sure the configuration for it is set up correctly.

## Usage
To run the personal assistant application:
```bash
streamlit run app.py
```
## How it Works

- The application displays a chat interface where the user can input messages.
- The input is processed using a predefined chat prompt template and passed to the Llama 3.2 model for generating a response.
- Both user and assistant messages are stored in `st.session_state` to maintain the chat history.
- The assistant responds based on the input and the context stored in the session history.

## Code Breakdown:

### Streamlit Interface:
- Displays the title and chat interface on the page.
- Messages are retrieved from `st.session_state` and displayed dynamically.

### LangChain Integration:
- The `ChatPromptTemplate` processes the user input using a template.
- The `OllamaLLM` connects to the local Llama 3.2 model to generate responses.

### Message History:
- The chat history is maintained across sessions using `st.session_state`.

## Contributing

If you would like to contribute to this project, feel free to fork the repository, create a branch, and submit a pull request.

## License

This project is open source and available under the MIT License.

