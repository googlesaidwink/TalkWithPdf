# Talk with PDF using Gemini

This Streamlit application enables users to interact with PDF documents through natural language queries, leveraging Google Generative AI for embeddings and conversational responses. The application extracts text from uploaded PDF files, processes it into manageable chunks, and creates a searchable vector store for efficient question answering.

## Features

- Upload multiple PDF documents.
- Extract text from PDFs and split it into manageable chunks.
- Create a vector store using Google Generative AI embeddings.
- Perform similarity searches for user questions against the processed PDF data.
- Provide detailed and accurate answers to user queries using conversational AI.

## Requirements

The following dependencies are required to run the application:

- `streamlit`
- `google-generativeai`
- `python-dotenv`
- `langchain`
- `PyPDF2`
- `chromadb`
- `faiss-cpu`
- `langchain_google_genai`

Install the dependencies using the command:

```bash
pip install -r requirements.txt
```

## Environment Setup

1. Create a `.env` file in the project root and add your Google API key:

```
GOOGLE_API_KEY=your_google_api_key_here
```

2. Ensure that your Google Generative AI is configured correctly for embeddings and conversational models.

## How to Run

1. Clone the repository and navigate to the project directory.
2. Install the required dependencies:

```bash
pip install -r requirements.txt
```

3. Run the Streamlit app:

```bash
streamlit run app.py
```

4. Open the application in your browser and follow these steps:

   - Upload PDF files using the sidebar uploader.
   - Click the "Submit & Process" button to process the files.
   - Enter your question in the input box and view the AI-generated response.

## Code Overview

# Key Functions

1. `get_pdf_text(pdf_docs)`: Extracts text from uploaded PDF files.
2. `get_text_chunks(text)`: Splits extracted text into chunks for easier processing.
3. `get_vector_store(text_chunks)`: Creates a vector store using Google Generative AI embeddings and saves it locally.
4. `get_conversational_chain()`: Configures the conversational AI chain with a custom prompt template.
5. `user_input(user_question)`: Searches the vector store for relevant context and generates a response using the conversational AI chain.

# Main Workflow

- The application uses Streamlit for the user interface and input handling.
- PDFs are uploaded via the sidebar and processed for text extraction and vector storage.
- Users can ask questions related to the PDFs, and the AI model provides accurate, context-aware responses.

# Acknowledgments

- Google Generative AI: for providing powerful embeddings and conversational models.
- **LangChain** for the integration of chain-based workflows.
- **Streamlit** for a seamless user interface experience.

## License

This project is licensed under the MIT License. Feel free to use and modify it as needed.

