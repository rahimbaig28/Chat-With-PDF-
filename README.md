# Chat with PDF using AWS Bedrock 💁

This project allows you to interact with PDF documents using advanced Language Models (LLMs) hosted on AWS Bedrock. It leverages vector embeddings, a FAISS vector store, and LLMs such as Claude v2 and Llama2-70b for retrieving and answering questions based on PDF content.  

---

## Features

- **PDF Data Ingestion**: Load PDF files from the `data` directory.
- **Text Splitting**: Efficiently split documents into chunks using `RecursiveCharacterTextSplitter`.
- **Vector Embeddings**: Generate document embeddings using Amazon Titan Embeddings.
- **Vector Store**: Store embeddings in a FAISS index for efficient similarity search.
- **LLM Support**:
  - **Claude v2** by Anthropic.
  - **Llama2-70b Chat** by Meta.
- **Custom Prompting**: Detailed prompts to provide concise, accurate, and explanatory responses.
- **Streamlit UI**: Simple user interface for asking questions and managing the vector store.

---

## Prerequisites

### AWS Setup
- **AWS Credentials**: Ensure your AWS credentials are configured (`~/.aws/credentials`).
- **Amazon Bedrock Access**: Set up Bedrock with permission to use Titan Embeddings and LLMs.

Python Dependencies
To install the required libraries, use the following command:

pip install -r requirements.txt  

## Required Files
Add your PDF files to the data directory for ingestion.(create a folder name it as data and add your pdf files)







