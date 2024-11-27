🤖 Retrieval-Augmented Generation with Ollama

forthebadge

This project is a Retrieval-Augmented Generation (RAG) application built with Streamlit and Ollama. The app enables users to upload PDF documents, which are split into chunks and embedded in a vector database for efficient document retrieval. Users can then interact with the content through a language model using customized parameters. The application can process new documents, change embedding models, and adjust chunk sizes, with all settings dynamically configurable through a sidebar.

This project can also act as a tool to chat with LLM without uploading a document.

Features

    Document Upload: Supports uploading PDF documents and automatically processes them into text chunks.
    Side-by-side comparison: Allow direct comparison of the uploaded PDF file and the parsed content that got fed to the Embedding model.
    Dynamic Vector Database Creation: Automatically re-creates the vector database when a new document is uploaded, a different embedding model is selected, or chunking parameters are updated.
    Embedding Models: Allows users to select from various embedding models for document chunk embeddings.
    LLM Interaction: Provides a custom LLM chat interface where users can retrieve document-relevant information.
    Configurable LLM Parameters: Users can adjust parameters like temperature, top-p and top-k to tailor model outputs.
    Efficient Text Retrieval: Uses a vector database to enable efficient similarity-based search within document contents.

Getting Started
Pre-requisites

    Ollama
    Python 3

Installation
Install pre-requisites

pip install -r requirements.txt

Run the app

streamlit run app.py

Usage

    Access the app
        Visit the URL: localhost:8501
    Upload a PDF Document
        Select a PDF document to upload. The application will parse the content and split it into chunks.
    Choose Model and Embedding Options
        Select an LLM model and an embedding model from the sidebar.
        Adjust the Chunk Size and Overlap Size to control how the document is divided into chunks.
    Configure LLM Parameters
        In the sidebar, adjust LLM parameters like temperature, top_k, top_p, and penalties to customize the output.
    Run Retrieval-Augmented Generation
        Enter prompts to interact with the document content. The model generates responses based on document information.
    Chat with LLM
        If you don't want to upload a document - you can and simply chat with the app.

Examples

After uploading a PDF (sample used) and selecting embedding parameters, use prompts like:

Summarise the document in 200 words with bullet points in a tone and language that even a high school student can understand.

Having a chat with LLM

Why is the sky blue? Respond in one sentence.

Configuration

All settings are available in the Streamlit sidebar:

    Model Selection: Choose an embedding model and an LLM model.
    Chunk Size and Overlap Size: Adjust these values to split documents effectively.
    LLM Parameters: Configure options such as temperature, top_k and top_p to influence LLM output.
