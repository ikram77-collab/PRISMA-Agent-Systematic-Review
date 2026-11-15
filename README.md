# PRISMA-Agent-Systematic-Review
An Autonomous Multi-Agent Pipeline for Systematic Literature Reviews using LangGraph and Europe PMC.
# PRISMA-Agent: An Autonomous Multi-Agent Pipeline for Systematic Reviews

**Course:** FDO - M1 Agentic AI & Building AI Agents  
**Institution:** FSTT  
**Team Members:** Ikram Lefhal Lalaoui & Tawfiq Moussif  

## 1. Project Overview
This project implements a modular, stateful, multi-agent AI system designed to automate the rigorous PRISMA 2020 workflow for Systematic Literature Reviews (SLRs). The system uses **LangGraph** for workflow orchestration, **LangChain** for LLM integration, and the **Europe PMC REST API** for grounded literature retrieval. It is designed to transform a raw research topic into a fully synthesized, traceable systematic review manuscript draft.

## 2. System Architecture
The pipeline is divided into 8 specialized agents, split into two independent blocks to ensure modularity:

### Block 1: Data Acquisition & Pre-processing (Ikram Lefhal Lalaoui)
- **Agent 1 (Coordinator):** Orchestrates the LangGraph workflow.
- **Agent 2 (Search Strategy):** Generates Boolean queries using prompt engineering.
- **Agent 3 (Retrieval):** Fetches real scientific literature via Europe PMC API.
- **Agent 4 (Deduplication):** Cleans the dataset by removing duplicate records.

### Block 2: Analysis, Extraction & Generation (Tawfiq Moussif)
- **Agent 5 (Screening):** Evaluates titles and abstracts (Inclusion/Exclusion).
- **Agent 6 (Extraction):** Performs PICO data extraction from full texts.
- **Agent 7 (Critic/QA):** Generates QUADAS-2 quality appraisal worksheets.
- **Agent 8 (Synthesis):** Drafts the final PRISMA-aligned review manuscript.

## 3. Technologies Used
- **Orchestration:** LangGraph, LangChain
- **LLM Backbone:** OpenRouter API (Free models)
- **Data Source:** Europe PMC REST API
- **Environment:** Python 3.10+

## 4. Installation and Setup
To run this project locally or in Google Colab, install the required dependencies:
```bash
pip install -q langgraph langchain-openai langchain-community requests pandas
