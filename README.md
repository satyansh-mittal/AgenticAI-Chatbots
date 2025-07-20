# 🤖 LangGraph AgenticAI ChatBots

An intelligent, multi-purpose chatbot application built with LangGraph and Streamlit that provides three distinct use cases: Basic Chatbot, Web-Enhanced Chatbot, and AI News Explorer.

## ✨ Features

- **Basic Chatbot**: Simple conversational AI using Groq models
- **Chatbot With Web**: Enhanced chatbot with web search capabilities using Tavily
- **AI News Explorer**: Automated AI news fetching, summarization, and reporting
- **Multiple LLM Models**: Support for various Groq models (gemma2-9b-it, llama3-8b-8192, qwen3-32b)
- **Interactive UI**: Clean and intuitive Streamlit interface
- **Configurable**: Easy configuration management through INI files

## 🚀 Quick Start

### Prerequisites

- Python 3.8+
- Groq API Key ([Get it here](https://console.groq.com/keys))
- Tavily API Key ([Get it here](https://app.tavily.com/home)) - Required for web search features

### Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd "Agentic Chatbot"
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Create necessary directories:
```bash
mkdir AINews
```

### Configuration

The application uses configuration files located in `src/langgraphagenticai/ui/`:
- `uiconfigfile.ini` - Contains UI settings and model options
- Modify these files to customize available models and use cases

### Running the Application

```bash
streamlit run -m src.langgraphagenticai.main
```

## 🎯 Use Cases

### 1. Basic Chatbot
- Simple conversational AI
- Direct interaction with Groq LLM models
- No external tools required

### 2. Chatbot With Web
- Enhanced chatbot with web search capabilities
- Uses Tavily search API for real-time information
- Provides source URLs and detailed responses

### 3. AI News Explorer
- Fetches latest AI technology news from India and globally
- Summarizes news in markdown format
- Supports different time frames (Daily, Weekly, Monthly)
- Saves summaries to local files

## 🛠️ Project Structure

```
src/
├── langgraphagenticai/
│   ├── graph/
│   │   └── graph_builder.py     # Graph construction logic
│   ├── LLMs/
│   │   └── groqllm.py          # Groq LLM integration
│   ├── nodes/
│   │   ├── basic_chatbot_node.py
│   │   ├── chatbot_with_tool_node.py
│   │   └── ai_news_node.py     # News fetching & summarization
│   ├── state/
│   │   └── state.py            # State management
│   ├── tools/
│   │   └── search_tool.py      # Tavily search integration
│   ├── ui/
│   │   ├── streamlitui/
│   │   │   ├── loadui.py       # UI components
│   │   │   └── display_result.py
│   │   ├── uiconfigfile.py     # Configuration loader
│   │   └── uiconfigfile.ini    # Configuration settings
│   └── main.py                 # Application entry point
├── AINews/                     # Generated news summaries
└── requirements.txt
```

## ⚙️ Configuration

### API Keys
- **Groq API Key**: Required for all use cases
- **Tavily API Key**: Required for "Chatbot With Web" and "AI News" use cases

### Model Options
Currently supported Groq models:
- gemma2-9b-it
- llama3-8b-8192
- qwen/qwen3-32b

## 📊 Dependencies

- **LangChain**: Core framework for LLM applications
- **LangGraph**: Graph-based workflow orchestration
- **Streamlit**: Web UI framework
- **Groq**: LLM provider integration
- **Tavily**: Web search API
- **FAISS**: Vector similarity search