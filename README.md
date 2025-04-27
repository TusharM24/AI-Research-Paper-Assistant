# AI-Research-Paper-Assistant
AI Research Paper Assistant: An offline-capable RAG-powered chatbot for secure, efficient summarization and Q&amp;A on academic papers. Leverages FAISS, Llama 3.2, and prompt engineering to deliver context-aware insights while preserving data privacy.

## Repository Structure

This project includes the following primary files:

1. **`practicum_project.ipynb`**  
   A Jupyter notebook containing the full data-analysis pipeline: data ingestion, preprocessing, EDA, prompt engineering, model benchmarking, statistical analysis, and all source code with outputs displayed inline.

2. **`exit_exam_presentation.pptx`**  
   PowerPoint slides used for the university exit-exam presentation, covering project motivation, architecture, results, and live demo.

3. **`Final_Report_Group4.pdf`**  
   The comprehensive project report submitted as part of the practicum (same as the PDF you provided).

4. **`app5.py`**  
   The Streamlit application code (front-end and back-end) that powers the interactive research-assistant interface.

5. **`requirements.txt`** (optional)  
   Lists all Python dependencies needed to install and run the notebook and app.

## Overview

This repository contains an end-to-end AI agent for automated analysis of scientific literature.  
- **Secure & Offline**: Fully local deployment—no third-party servers or internet required.  
- **Semantic Retrieval**: Uses FAISS for high-performance vector search over embedded document chunks.  
- **Retrieval-Augmented Generation (RAG)**: Dynamically augments prompts with relevant passages before passing to a lightweight LLM.  
- **Streamlit UI**: Intuitive interface for uploading PDFs, viewing extracted text, and querying the system. :contentReference[oaicite:2]{index=2}&#8203;:contentReference[oaicite:3]{index=3}

## Features

- **PDF Ingestion & Duplication Check**: Extracts text with PyMuPDF and uses SHA-256 hashing to prevent redundant processing. :contentReference[oaicite:4]{index=4}&#8203;:contentReference[oaicite:5]{index=5}  
- **Chunking & Embedding**: Splits documents into manageable chunks; generates 384-dimensional embeddings via Sentence-BERT. :contentReference[oaicite:6]{index=6}&#8203;:contentReference[oaicite:7]{index=7}  
- **FAISS Vector Store**: Indexes embeddings for approximate nearest-neighbor search using L2 distance. :contentReference[oaicite:8]{index=8}&#8203;:contentReference[oaicite:9]{index=9}  
- **Dynamic RAG Pipeline**: Retrieves top-k relevant chunks, appends them to user queries, and forwards to the selected LLM via Ollama API. :contentReference[oaicite:10]{index=10}&#8203;:contentReference[oaicite:11]{index=11}  
- **Model Benchmarking**: Supports multiple open-source LLMs (Llama 3.2, Gemma 3, Mistral, Qwen 2.5, DeepSeek-R1) with automated evaluation (ROUGE, BERTScore, latency). :contentReference[oaicite:12]{index=12}&#8203;:contentReference[oaicite:13]{index=13}  
- **Web Interface**: Built with Streamlit—users can upload papers, preview extracted text, submit queries, and view citation-backed responses. :contentReference[oaicite:14]{index=14}&#8203;:contentReference[oaicite:15]{index=15}  


