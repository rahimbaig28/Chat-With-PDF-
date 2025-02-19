# Chat with PDF using AWS Bedrock 💁

This project enables interactive querying of PDF documents using advanced Language Models (LLMs) hosted on AWS Bedrock. It combines vector embeddings, FAISS vector store, and powerful LLMs such as **Claude v2** and **Llama2-70b** for retrieving and answering questions based on PDF content.

---

## Features

- **PDF Data Ingestion**: Easily load PDF files from the `data` directory.
- **Text Splitting**: Efficiently split documents into chunks using `RecursiveCharacterTextSplitter`.
- **Vector Embeddings**: Generate document embeddings using **Amazon Titan Embeddings**.
- **Vector Store**: Store embeddings in a FAISS index for efficient similarity search.
- **LLM Support**:
  - **Claude v2** by Anthropic.
  - **Llama2-70b Chat** by Meta.
- **Custom Prompting**: Detailed prompts designed for concise, accurate, and explanatory responses.
- **Streamlit UI**: A simple user interface for asking questions and managing the vector store.

---

## Prerequisites


### AWS Setup
1. **AWS Credentials**: Ensure your AWS credentials are configured in `~/.aws/credentials`.
2. **Amazon Bedrock Access**: Set up Bedrock with permissions to use Titan Embeddings and LLMs.

### Python Dependencies
Install the required libraries with the following command:

```bash
pip install -r requirements.txt
