<h1 style="font-size: 20px;"><b>Baat-E Docs</b></h1>

The project, "Chat with PDF & Word Documents using Gemini," is a Streamlit web application designed to allow users to upload PDF and Word documents, extract text from these documents, and ask questions based on the content. The application leverages Google's Generative AI models for text embedding and question answering, making it a powerful tool for document-based Q&A.

<h1 style="font-size: 18px;"><b>Project Overview</b></h1>
<h1 style="font-size: 15px;"><b>Objective:</b></h1>
The primary objective of this project is to create an interactive web application that can extract text from uploaded PDF and Word documents and provide accurate answers to user queries based on the document content.

<h1 style="font-size: 16px;"><b>Key Features:</b></h1>

**1. File Upload :** Users can upload multiple PDF and Word documents.

**2. Text Extraction :** The application extracts text from the uploaded documents.

**3. Text Chunking :** The extracted text is split into manageable chunks for efficient processing.

**4. Vector Store Creation :** The text chunks are converted into embeddings and stored in a FAISS vector store.

**5. Question Answering :** Users can input questions, and the application will search the vector store for relevant information to generate answers.

**6. User Authentication :** Integration with Auth0 for secure user authentication (login with Google).

**How It Works**

**1. User Interface:**

* The application is built using Streamlit, providing a simple and intuitive interface.
* Users can upload PDF and Word documents from the sidebar.
* Users can ask questions in the main interface.
  
**2. Document Processing:**

* Text extraction is done using PyPDF2 for PDFs and python-docx for Word documents.
* Extracted text is split into chunks using RecursiveCharacterTextSplitter to manage large documents efficiently.

**3. Vector Store:**

* The text chunks are converted into embeddings using Google's Generative AI embeddings model.
* These embeddings are stored in a FAISS vector store for efficient similarity searches.

**4. Question Answering:**

* A conversational chain is created using the ChatGoogleGenerativeAI model.
* When a user asks a question, the application searches the vector store for relevant text chunks.
* The conversational chain generates an answer based on the retrieved chunks.

**5. Authentication:**

* The application integrates with Auth0 for user authentication, allowing users to log in with their Google accounts.

**How to Run the Project**

**1. Clone the Repository:**

git clone https://baat-e-docs-hdwu8f2cbhymnqwmqgucx5.streamlit.app/

cd Chat-with-Documents

**2. Install Dependencies:**

pip install -r requirements.txt

**3. Set Up Environment Variables:**

Create a .env file in the project root with the following content:
