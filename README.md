
# KnowledgeVis: Transform Text into Interactive Knowledge Networks

> Uncover hidden connections in any text corpus through powerful graph visualization

## 🧠 What is KnowledgeVis?

KnowledgeVis transforms raw text into beautiful, interactive knowledge networks that reveal the hidden connections between concepts. Unlike traditional NLP approaches that focus on entities, KnowledgeVis captures semantic relationships between complex ideas, providing deeper insights into your content.

## ✨ Key Features

- **Concept-Centric Analysis**: Extracts meaningful concepts rather than just named entities
- **Relationship Detection**: Identifies semantic connections between concepts
- **Interactive Visualization**: Explore your content through an intuitive network interface
- **Community Detection**: Automatically groups related concepts
- **Centrality Analysis**: Identifies the most important concepts in your corpus
- **Local LLM Integration**: Uses Mistral 7B locally for cost-effective processing

## 🔄 The KnowledgeVis Workflow

```mermaid
graph TD
    A[Text Corpus] --> B[Text Chunking]
    B --> C[Concept Extraction]
    C --> D[Relationship Mapping]
    D --> E[Network Construction]
    E --> F[Analysis & Visualization]
    
    C -->|LLM Processing| D
    D -->|Weight W1: Semantic| E
    D -->|Weight W2: Proximity| E
    
    style A fill:#f9d5e5,stroke:#333,stroke-width:2px
    style F fill:#eeeeee,stroke:#333,stroke-width:2px
    
    subgraph "Intelligence Layer"
    C
    end
    
    subgraph "Graph Construction"
    D
    E
    end
```

1. **Text Chunking**: Divides input text into manageable segments
2. **Concept Extraction**: Uses LLM to identify key concepts within each chunk
3. **Relationship Mapping**: Establishes connections between concepts using:
   - Semantic relationships identified by the LLM (weight W1)
   - Contextual proximity within the same chunks (weight W2)
4. **Network Construction**: Builds a weighted graph where:
   - Nodes represent unique concepts
   - Edges represent relationships with combined weights
5. **Analysis & Visualization**: Calculates network metrics and renders an interactive graph

## 🚀 Why Knowledge Networks Matter

Knowledge networks unlock capabilities beyond traditional text analysis:

- **Discover Non-Obvious Connections**: Reveal relationships between seemingly unrelated concepts
- **Identify Central Ideas**: Find the core concepts that anchor your content
- **Detect Conceptual Communities**: Understand how ideas cluster together
- **Enable Graph RAG (GRAG)**: Supercharge your retrieval-augmented generation with graph-based context

## 💻 Technology Stack

### Intelligence Layer
- **[Mistral 7B OpenOrca](https://huggingface.co/Open-Orca/Mistral-7B-OpenOrca)**: State-of-the-art open-source LLM for concept extraction
- **[Ollama](https://ollama.ai)**: Efficient local model deployment

### Data Processing
- **Pandas**: Flexible data manipulation
- **NetworkX**: Comprehensive graph analysis toolkit

### Visualization
- **[Pyvis](https://github.com/WestHealth/pyvis)**: Interactive network visualization with JavaScript export

## 🛠️ Getting Started

1. Clone this repository
2. Install Ollama from [ollama.ai](https://ollama.ai)
3. Run `ollama run mistral` to initialize the local LLM
4. Open and run `extract_graph.ipynb` to process your text
5. Explore your interactive knowledge network!

**Demo**: [Interactive Knowledge Graph Explorer](https://garimatripathi3.github.io/KnowledgeVis-Transform-Text-into-Interactive-Knowledge-Networks/)

## 📚 Learn More

- [The Theory Behind Knowledge Graphs](https://www.ibm.com/topics/knowledge-graph)
- [Graph Retrieval Augmented Generation (GRAG)](https://medium.com/towards-data-science/how-to-convert-any-text-into-a-graph-of-concepts-110844f22a1a)
- [Community Discussions](https://github.com/guneeshvats/Convert-any-Corpus-of-Text-into-a-Graph-of-Knowledge/discussions)
