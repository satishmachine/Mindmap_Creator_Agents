# 🧠 Multi-Agent Knowledge Graph Builder

A powerful application that generates detailed, AI-powered knowledge graphs and learning roadmaps from any topic or question.

## 📋 Overview

The Multi-Agent Knowledge Graph Builder is an intelligent system that leverages multiple specialized AI agents working together to create comprehensive visual knowledge maps. Simply input a topic or question, and the system will automatically research, synthesize, and visualize the information as an interactive knowledge graph.

## ✨ Features

- **🔍 Intelligent Research**: Automatically gathers information from multiple sources including Google and Wikipedia
- **🧩 Smart Synthesis**: Processes and organizes raw information into structured knowledge
- **📊 Visual Mapping**: Transforms structured knowledge into beautiful, interactive knowledge graphs
- **🔄 Multi-Agent Architecture**: Uses a LangGraph-powered workflow with specialized agents for each task
- **🌐 Web Interface**: Clean, user-friendly Streamlit interface for easy interaction

## 🏗️ Architecture

The system uses a multi-agent architecture with three specialized agents:

1. **Researcher Agent**: Gathers raw information from multiple sources
2. **Synthesizer Agent**: Processes and structures the raw information
3. **Mapper Agent**: Transforms the structured information into a visual knowledge graph

These agents work together in a sequential workflow managed by LangGraph.

## 📁 Project Structure

```
knowledge_graph_builder/
├── agents/                  # Specialized AI agents
│   ├── researcher.py        # Agent for gathering information
│   ├── synthesizer.py       # Agent for processing information
│   └── mapper.py            # Agent for creating knowledge graphs
├── tools/                   # External API integrations
│   ├── serpapi_tool.py      # Google search integration
│   ├── wikipedia_tool.py    # Wikipedia integration
│   └── research_api_tool.py # AI model integration
├── workflows/               # Process orchestration
│   └── langgraph_router.py  # LangGraph workflow definition
├── utils/                   # Utility functions
│   ├── graphviz_exporter.py # Graph visualization
│   └── config.py            # Configuration settings
├── data/                    # Data storage
│   └── outputs/             # Generated graphs
└── app.py                   # Streamlit web application
```

## 🚀 Getting Started

### Prerequisites

- Python 3.9+
- Graphviz (for visualization)

### Installation

1. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

2. Set up environment variables:
   Create a `.env` file in the root directory with the following variables:
   ```
   SERP_API_KEY=your_serpapi_key
   EURI_API_KEY=your_euriai_key
   ```

### Running the Application

Start the Streamlit application:
```bash
streamlit run app.py
```

Then open your browser and navigate to `http://localhost:8501`.

## 🔧 How It Works

1. **Input**: User enters a topic or question
2. **Research**: The Researcher Agent gathers information from Google and Wikipedia
3. **Synthesis**: The Synthesizer Agent processes and structures the information
4. **Mapping**: The Mapper Agent creates a visual knowledge graph
5. **Visualization**: The graph is rendered using Graphviz and displayed to the user

## 📊 Example Output

When you input a topic like "Roadmap for Machine Learning", the system generates a comprehensive knowledge graph showing the learning path, key concepts, and estimated time frames.

The output is a visual SVG graph that can be viewed in the browser and downloaded for future reference.

## 🛠️ Technologies Used

- **Streamlit**: Web interface
- **LangGraph**: Multi-agent workflow orchestration
- **Graphviz**: Graph visualization
- **SerpAPI**: Google search integration
- **EuriAI**: AI model integration
- **Python-dotenv**: Environment variable management
- **Requests**: HTTP requests
- **Pillow**: Image processing

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.
