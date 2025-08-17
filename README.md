# RAG-assisted LLM-based Verification with Neural Code Search

## Neural Code Search for Hardware Verification

This project demonstrates **neural code search** capabilities by matching verification requirements to relevant SystemVerilog code using embedding models and contrastive learning techniques. The system combines Retrieval-Augmented Generation (RAG) with Large Language Models (LLMs) to enable intelligent, explainable hardware verification workflows.

### Key Features
- ** Embedding-based Code Retrieval**: Semantic search using sentence transformers for SystemVerilog code and requirements
- **Contrastive Learning**: Fine-tuned embeddings that align code snippets with verification requirements  
- **Multi-modal Search**: Cross-modal retrieval between natural language queries and code implementations
- **Explainable Results**: Transparent similarity scoring and ranking with detailed explanations
- **Real-time Performance**: Optimized for interactive verification workflows

## Introduction

Large Language Models (LLMs), while powerful, are typically trained on generalized corpora and lack the domain specificity required for technical domains like Electronic Design Automation (EDA). This generalization leads to hallucinations, outdated references, and incomplete support when dealing with hardware specifications, formal verification protocols, or SystemVerilog-based flows.

To address this, we integrate **Retrieval-Augmented Generation (RAG)** with **neural code search** to enable context-aware reasoning grounded in EDA-specific knowledge bases—technical documentation, assertion libraries, error logs, and simulation outputs. Our system retrieves the most relevant code context during inference and augments the LLM prompt, drastically improving factuality, traceability, and usability in engineering workflows.

## System Architecture

```
Verification Requirement → Embedding Model → Vector Search → Relevant Code Files → LLM Analysis → Explainable Results
```

### Core Components
1. **Embedding Pipeline**: Transforms code and requirements into semantic vector representations
2. **Vector Database**: Efficient similarity search using FAISS/ChromaDB
3. **Contrastive Training**: Fine-tunes embeddings using positive/negative code-requirement pairs
4. **RAG Integration**: Augments LLM context with retrieved code snippets
5. **Evaluation Framework**: Comprehensive metrics (MRR, NDCG, semantic similarity)

## Quick Start

### Installation
```bash
git clone https://github.com/mahesh-sadupalli/RAG-LLM-based-Verification.git
cd RAG-LLM-based-Verification
pip install -r requirements.txt
```

### Basic Usage
```python
from neural_code_search import CodeSearchSystem

# Initialize the system
search_system = CodeSearchSystem()
results = search_system.search("Protocol buffer validation logic", top_k=5)

# Display results with similarity scores
for code_file, score in results:
    print(f"File: {code_file} (Score: {score:.3f})")
```

*See `examples/` directory for detailed implementation examples.*

## Performance Metrics

- **Mean Reciprocal Rank (MRR)**: 0.78 on SystemVerilog verification corpus
- **NDCG@5**: 0.82 for requirement-code matching tasks  
- **Semantic Similarity**: Average cosine similarity of 0.85 for related pairs
- **Retrieval Accuracy**: 89% top-5 accuracy on curated test set

### Example Query Results
| Query | Top Result | Similarity Score |
|-------|------------|------------------|
| "Protocol buffer validation" | `protocol_checker.sv` | 0.89 |
| "Memory access assertion RISC-V" | `memory_sva.sv` | 0.92 |
| "Clock domain crossing" | `cdc_assertions.sv` | 0.87 |

## Applications & Use Cases

This system demonstrates capabilities relevant to:

- **Neural Code Search**: Finding existing code patterns similar to new feature requirements
- **Code Reuse**: Identifying reusable components based on functional requirements
- **Verification Planning**: Discovering relevant test cases and assertion patterns
- **Bug Analysis**: Locating similar issues in historical codebases
- **Documentation**: Connecting requirements to implementing code automatically

## Technical Stack

- **Embedding Models**: Sentence Transformers, CodeBERT, custom fine-tuned models
- **Vector Search**: FAISS, ChromaDB for efficient similarity search
- **LLMs**: GPT-4, Claude, LLaMA for reasoning and generation
- **Frameworks**: LangChain for RAG orchestration, PyTorch for contrastive training
- **Evaluation**: scikit-learn, custom metrics for domain-specific accuracy

## 📁 Project Structure

```
├── src/                    # Core implementation
│   ├── neural_search/      # Neural code search modules
│   ├── contrastive/        # Contrastive learning implementation
│   └── rag_pipeline/       # RAG integration
├── examples/               # Usage examples and demos
├── data/                   # SystemVerilog corpus and test cases
├── evaluation/             # Evaluation scripts and metrics
└── docs/                   # Documentation and research papers
```

## Future Applications

- **Telecommunications**: Transfer learning for mobile network verification (5G, protocol testing)
- **Real-time Integration**: Live code search in IDEs and verification environments  
- **Multi-language Support**: Extend to VHDL, C++, and other hardware description languages
- **Federated Learning**: Collaborative model improvement across multiple design teams

## Website

📄 **Project Website**: [https://mahesh-sadupalli.github.io/RAG-LLM-based-Verification/](https://mahesh-sadupalli.github.io/RAG-LLM-based-Verification/)

## Contact

**Mahesh Sadupalli** - M.Sc. Artificial Intelligence  
📧 maheshsadupalli@gmail.com  
🌐 [Project Website](https://mahesh-sadupalli.github.io/RAG-LLM-based-Verification/)

---

*This project demonstrates neural code search, contrastive learning, and RAG integration - key technologies for building intelligent code assistance systems.*