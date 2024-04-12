# Multiple PDF Interacter 💁

This Streamlit app allows users to interactively ask questions from uploaded PDF files using the Gemini conversational model. The application processes the PDF files, extracts text, generates embeddings, and creates a conversational chain for answering user queries based on the provided context.

## How to Use

1. **Upload PDF Files**: Use the file uploader in the sidebar to upload one or more PDF files containing the information you want to query.
2. **Ask a Question**: Enter your question in the text input box provided. Ensure that your question is relevant to the content of the uploaded PDF files.
3. **Submit & Process**: Click the "Submit & Process" button to start processing the uploaded PDF files and generate responses to your questions.

## Installation and Setup

1. Clone the repository to your local machine:

   ```bash
   git clone https://github.com/your/repository.git
   ```

2. Install the required dependencies:

   ```bash
   pip install streamlit PyPDF2 langchain google google-cloud genai dotenv
   ```

3. Set up your Google API key in a `.env` file:

   ```plaintext
   GOOGLE_API_KEY=your_api_key_here
   ```

4. Run the Streamlit app:

   ```bash
   streamlit run app.py
   ```

## Code Overview

### Libraries Used

- `streamlit`: For creating the interactive web application.
- `PyPDF2`: For extracting text from PDF files.
- `langchain`: For text splitting, embeddings generation, and conversational chain creation.
- `google`, `genai`: For Google AI services and generative AI models.
- `dotenv`: For loading environment variables.

### Functions

1. **`get_pdf_text(pdf_docs)`**: Extracts text from PDF files and concatenates them.
2. **`get_text_chunks(text)`**: Splits the text into smaller chunks for processing.
3. **`get_vector_store(text_chunks)`**: Generates embeddings and creates a vector store using FAISS.
4. **`get_conversational_chain()`**: Sets up a conversational chain for answering user questions.
5. **`user_input(user_question)`**: Processes user input question and provides a response using the conversational chain.
6. **`main()`**: Main function to run the Streamlit application, handle user input, and display the interface.

### Running the Application

- The `main()` function sets up the Streamlit interface with a header, input field for questions, and a sidebar for uploading PDF files.
- Upon uploading PDF files and submitting a question, the application processes the files, generates embeddings, and provides a response based on the context and question.

## Additional Notes

- Ensure that your Google API key is valid and has access to the required services for the application to function properly.
- You can customize the Gemini conversational model parameters and other settings based on your requirements by modifying the code accordingly.

Feel free to explore and enhance the application further based on your needs and use cases!
