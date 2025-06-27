# LangChain Agent with Gemini Pro

This project demonstrates a simple LangChain agent powered by Google Gemini Pro. It is designed to answer questions based on a text document and perform basic arithmetic using a custom tool.

## Features

- Conversational agent built with LangChain
- Uses Gemini Pro as the LLM via `langchain-google-genai`
- Supports document-based question answering
- Retrieves context using FAISS and Hugging Face embeddings
- Includes a custom calculator tool for simple math operations
- Runs entirely in Google Colab

## How it works

A `.txt` file is uploaded and processed using LangChain’s text loader and splitter. The text is broken into chunks, embedded using a sentence-transformer model, and stored in FAISS for semantic search. Two tools are defined: one for retrieving document information, and another for basic calculations. These tools are then passed to a LangChain agent that uses Gemini Pro to respond intelligently.

## Usage

1. Upload a `.txt` file when prompted in the notebook
2. Set your Gemini API key securely in the environment
3. Run the notebook cells in order
4. Ask the agent questions like:
   - What are the key takeaways from the document?
   - What is 1000 divided by 25?
   - Combine document info and math in a single query

## Requirements

- Python (Google Colab)
- LangChain
- langchain-google-genai
- langchain-community
- sentence-transformers
- faiss-cpu
- pymupdf

## Notes

Avoid hardcoding your API key. Use environment variables or load it from a secure location. This project is meant for experimentation and learning purposes.
