# RAG-assisted LLM-based Verification

## Introduction

Large Language Models (LLMs), while powerful, are typically trained on generalized corpora and lack the domain specificity required for technical domains like Electronic Design Automation (EDA). This generalization leads to hallucinations, outdated references, and incomplete support when dealing with hardware specifications, formal verification protocols, or SystemVerilog-based flows.

To address this, we integrate Retrieval-Augmented Generation (RAG) with LLMs to enable context-aware reasoning grounded in EDA-specific knowledge bases—technical documentation, assertion libraries, error logs, and simulation outputs. Our system retrieves the most relevant context during inference and augments the LLM prompt, drastically improving factuality, traceability, and usability in engineering workflows.

This project demonstrates how a RAG-enhanced LLM pipeline, combined with Explainable AI (XAI) techniques, can support intelligent debugging and verification tasks in EDA. From querying design errors to interpreting waveform outputs, the system provides accurate, interpretable responses backed by domain-grounded evidence.

> Use case: Querying assertion failures in SystemVerilog, generating testbench snippets, or explaining waveform anomalies using retrieved knowledge from formal verification documents.



This project explores the integration of Retrieval-Augmented Generation (RAG) with Large Language Models (LLMs) for hardware verification tasks such as:

- Formal Verification
- Bug Detection and Fixing
- Mutation Testing
- SystemVerilog & RISC-V Integration
- Explainable AI (XAI)

## Website
The project is also showcased at: [GitHub Pages](https://mahesh-sadupalli.github.io/RAG-LLM-based-Verification/)

## Key Papers
We build upon these foundational papers:
- LLM-guided Formal Verification
- Bug Fixing with LLMs
- Scalable Semantic Change Detection
*(Full references listed in the website)*

## 📦 Tools & Stack
- LangChain, OpenAI APIs
- RISC-V test cases
- Z3 SMT Solver
- GitHub Pages



