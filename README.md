# FAQ Chatbot for PDF Documents
This project is a Retrieval-Augmented Generation (RAG) chatbot that answers questions based on the content of a PDF document. It demonstrates how modern language models can transform static documents into dynamic, interactive assistants.

## Project Goal
To build an interactive chatbot that allows users to ask questions and receive accurate answers drawn directly from a PDF file. This simulates the functionality of a smart assistant that understands your documents.

## Features
  *  Parses any PDF document and converts it into machine-readable text.
  *  Splits the text into chunks and generates vector embeddings for semantic search.
  *  Uses FAISS to retrieve the most relevant information from the document.
  *  Utilizes OpenAI GPT to generate natural language answers.
  *  Includes a command-line Q&A loop for quick testing.

## Tech Stack
  *  PDF Parsing: **PyMuPDF** enables accurate and fast text extraction from PDF files.
  *  LLM Framework: **LangChain** orchestrates the retrieval and response generation.
  *  Embeddings: OpenAI’s **text-embedding-ada-002** is used for high-quality vector representations.
  *  Vector Store: **FAISS** allows efficient similarity search over embedded document chunks.
  *  LLM: **GPT-3.5 from OpenAI** provides the language understanding and response generation.

## Data Source
Title: "Extending Human Creativity with AI"

Authors: Katherine O’Toole & Emőke-Ágnes Horvát

Published in: Journal of Creativity, 2024

License: CC BY-NC-ND (Open Access)

This publication is available at the [following link](https://www.sciencedirect.com/science/article/pii/S2713374524000062?via%3Dihub).

## How It Works
1.  Download a PDF and extract the raw text using PyMuPDF.
2.  Split and embed the text using LangChain’s text splitter and OpenAI embeddings.
3.  Store embeddings in FAISS, which enables fast and accurate vector search.
4.  Use RetrievalQA from LangChain to match user questions with relevant document content.
5.  Answer questions using GPT, returning responses grounded in the original document.
