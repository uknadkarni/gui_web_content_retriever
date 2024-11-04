# Query System with Optional Retrieval Augmentation
## Setup Instructions:
* Install Python 3.12 or higher.
* Clone the repository or download the source code.
* Install the required dependencies by running:
```pip install -r requirements.txt```
* Set up environment variables for API keys:
OPENAI_API_KEY: Your OpenAI API key
GROQ_API_KEY: Your Groq API key
* Ensure you have a stable internet connection.
## Usage Instructions:
Run the Streamlit app:  
```streamlit run gui_web_content_retriever.py``` . 
Open the provided URL in your web browser.  
Use the sidebar to adjust settings:  
Set the temperature for the language model (0.0 to 2.0).  
Optionally, enter a web path for retrieval-augmented generation.  
Enter your query in the text input field.  
View the generated response below the input field.  
## Program Description:
This program is a query system that uses language models to answer user questions. It offers two modes of operation:  
* Simple LLM: Answers questions using a language model without additional context.
* Retrieval Augmented Generation (RAG): Fetches relevant information from a specified web page, creates a searchable database, and uses this context to enhance the language model's responses.
The program allows users to adjust the temperature of the language model and optionally provide a web path for context retrieval. It handles errors gracefully and provides informative messages about the current operating mode.  
## Requirements:
```pip install ``` the packages listed below  
```
streamlit
langchain-openai
langchain-groq
langchain-community
langchain-core
chromadb
beautifulsoup4
requests
```
Alternatively, install the packages listed in the ``requirements.txt``
```
pip install -r requirements.txt
```
## Technologies Used:
* Chroma: A vector database used for storing and retrieving document embeddings. It enables efficient similarity search for relevant context during retrieval-augmented generation.
* OpenAI: Utilized for generating text embeddings through the OpenAIEmbeddings class. These embeddings are crucial for creating searchable vector representations of documents.
* GroqChat: Employed as the primary language model through the ChatGroq class. It processes user queries and generates responses, with the ability to incorporate retrieved context when using RAG mode.

These technologies work together to provide a flexible and powerful query system that can operate with or without additional context, adapting to user needs and available resources.
