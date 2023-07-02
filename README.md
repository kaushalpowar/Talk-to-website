# Talk-to-website 🎙🧑‍💻
Retrieve any information from a Website without having to visit all pages.
<br/>
This code is written in Python and utilizes several frameworks and libraries to perform document processing and question-answering tasks. The main frameworks used in this code are LangChain, OpenAI, and Pinecone.
<br/>
# Frameworks
## LangChain
LangChain is a framework used for document processing, including document loading, text splitting, embeddings, and vector indexing. It provides various utilities and models for natural language processing tasks.

## Apify
Apify is used for web scraping, data extraction, and RPA. 

## OpenAI
OpenAI is a powerful language model that offers a range of natural language processing capabilities. In this code, OpenAI is used for question-answering and conversational retrieval tasks.

## Pinecone
Pinecone is a vector database that is used for vector similarity search that allows fast and efficient querying of vectorized data. It is used in this code for indexing and retrieval of document embeddings.

# Flow of Work
- Install the required packages using the pip package manager.
- Import the necessary modules and libraries.
- Define a function called split_docs to split a list of documents into chunks based on specified chunk size and overlap.
- Set up environment variables for the OpenAI API key and Apify API token.
- Initialize the ApifyWrapper and OpenAIEmbeddings objects for data loading and embeddings, respectively.
- Initialize the Pinecone vector store with the API key and environment.
- Create an instance of the Apify website content crawler and load the data from the crawler into a variable called data.
- Split the loaded documents into chunks using the split_docs function.
- Optionally, create embeddings of the data and index them using Pinecone (this line is commented out in the code).
- Extract the URLs of the scraped documents and print them.
- Load the saved embeddings from Pinecone into an index.
- Initialize a ConversationBufferMemory object for storing chat history.
- Create a ConversationalRetrievalChain model for question-answering using the OpenAI language model and the Pinecone index as a retriever.
- Define a chat history list and a query.
- Perform a question-answering task using the defined query and chat history.
- Handle and process the result as needed.
