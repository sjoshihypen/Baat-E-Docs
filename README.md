<h1 style="font-size: 20px;"><b>Baat-E Docs</b></h1>

The project, "Chat with PDF & Word Documents using Gemini," is a Streamlit web application designed to allow users to upload PDF and Word documents, extract text from these documents, and ask questions based on the content. The application leverages Google's Generative AI models for text embedding and question answering, making it a powerful tool for document-based Q&A.

<h2 style="font-size: 5px;"><b>Project Overview</b></h2>

<h3 style="font-size: 5px;"><b>Objective:</b></h3>
The primary objective of this project is to create an interactive web application that can extract text from uploaded PDF and Word documents and provide accurate answers to user queries based on the document content.

<h3 style="font-size: 5px;"><b>Key Features:</b></h3>

<p style="font-size: 10px;"><b>1. File Upload : </b> Users can upload multiple PDF and Word documents.</p>

<p style="font-size: 10px;"><b>2. Text Extraction : </b> The application extracts text from the uploaded documents.</p>

<p style="font-size: 10px;"><b>3. Text Chunking : </b>  The extracted text is split into manageable chunks for efficient processing.</p>

<p style="font-size: 10px;"><b>4. Vector Store Creation : </b> The text chunks are converted into embeddings and stored in a FAISS vector store.</p>

<p style="font-size: 10px;"><b>5. Question Answering : </b> Users can input questions, and the application will search the vector store for relevant information to generate answers.</p>

<p style="font-size: 10px;"><b>6. User Authentication : </b> Integration with Auth0 for secure user authentication (login with Google).</p>

<h3 style="font-size: 5px;"><b>How It Works</b></h3>

<p style="font-size: 10px;"><b>1. User Interface :</b></p>

* The application is built using Streamlit, providing a simple and intuitive interface.
* Users can upload PDF and Word documents from the sidebar.
* Users can ask questions in the main interface.
  
<p style="font-size: 10px;"><b>2. Document Processing :</b></p>

* Text extraction is done using PyPDF2 for PDFs and python-docx for Word documents.
* Extracted text is split into chunks using RecursiveCharacterTextSplitter to manage large documents efficiently.

<p style="font-size: 10px;"><b>3. Vector Store:</b></p>

* The text chunks are converted into embeddings using Google's Generative AI embeddings model.
* These embeddings are stored in a FAISS vector store for efficient similarity searches.

<p style="font-size: 10px;"><b>4. Question Answering:</b></p>

* A conversational chain is created using the ChatGoogleGenerativeAI model.
* When a user asks a question, the application searches the vector store for relevant text chunks.
* The conversational chain generates an answer based on the retrieved chunks.

<p style="font-size: 10px;"><b>5. Authentication:</b></p>

* The application integrates with Auth0 for user authentication, allowing users to log in with their Google accounts.

<h3 style="font-size: 5px;"><b>How to Run the Project</b></h3>

<p style="font-size: 10px;"><b>1. Clone the Repository:</b></p>

git clone https://baat-e-docs-hdwu8f2cbhymnqwmqgucx5.streamlit.app/

cd Chat-with-Documents

<p style="font-size: 10px;"><b>2. Install Dependencies :</b></p>

pip install -r requirements.txt

<p style="font-size: 10px;"><b>3. Set Up Environment Variables :</b></p>

Create a .env file in the project root with the following content:

GOOGLE_API_KEY=your_google_api_key

<p style="font-size: 10px;"><b>4.Run the Application :</b></p>
streamlit run app.py

<h3 style="font-size: 5px;"><b>Result</b></h3>

<p style="font-size: 10px;"><b>Dashboard</b></p>
![image](https://github.com/user-attachments/assets/05278519-daf3-4135-824c-5c8902b97439)

<p style="font-size: 10px;"><b>Selecting The PDF File Asking The Questions </b></p>
![image](https://github.com/user-attachments/assets/eaa0cdd7-7e02-4340-9ca4-6f8c9a781709)

<p style="font-size: 10px;"><b>Selecting The Word File Asking The Questions </b></p>
