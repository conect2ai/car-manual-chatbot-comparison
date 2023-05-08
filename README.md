# Comparing Three AI-Powered Solutions for Car Manual Queries 🤖🚗

Welcome to the **Comparing Three AI-Powered Solutions for Car Manual Queries** project! This repository contains a comprehensive analysis and comparison of three leading AI-based solutions for answering technical questions related to car manuals in PDF format. Our goal is to help you make an informed decision on the best solution for your specific needs.

## 🤖 Solutions Overview

We've evaluated the following three AI-powered solutions:

1. **Doc Chatbot with LlamaIndex**: A chatbot that uses LlamaIndex and LangChain libraries to connect large language models (LLMs) to external data sources like PDF car manuals, enabling the creation of chatbots that can learn from diverse data sources and deliver good answers at an affordable cost. The code for this solution can be found in the [doc-chatbot-with-llamaindex](./doc-chatbot-with-llamaindex) folder.

2. **Ask your PDF**: A graphical interface that combines Streamlit and Langchain to allow users to upload a PDF file and ask questions about its content. The application extracts text from the PDF, creates embeddings using the OpenAIEmbeddings library, and stores them in a FAISS database for similarity search. The code for this solution can be found in the [ask-your-pdf](./ask-your-pdf) folder.

3. **Question and answer system**: A system that combines LangChain and Large Language Models, such as OpenAI’s GPT-3, and uses React/Typescript for the frontend and Python FastAPI for the backend. QDrant is used to store embeddings and text documents for fast search. The code for this solution can be found in the [QA-system-for-car-manuals](./QA-system-for-car-manuals) folder.

## 📚 Documentation and Resources

Below are the official documentation and resources for each solution:

- **Doc Chatbot with LlamaIndex**
  - [Getting Started Guide](https://levelup.gitconnected.com/how-to-create-a-doc-chatbot-that-learns-everything-for-you-in-15-minutes-364fef481307)

- **Ask your PDF**
  - [GitHub Repository](https://github.com/alejandro-ao/langchain-ask-pdf)

- **Question and answer system**
  - [GitHub Repository](https://github.com/mallahyari/drqa)
  - [Getting Started Guide](https://github.com/mallahyari/drqa/blob/main/README.md)

## 💻 How to run 

Follow the instructions below to run each one of these applications in your machine:

- **Doc Chatbot with LlamaIndex**

1. Download the `index.ipynb` file, located in the `chatbot_llama_index` folder and open it in Visual Studio Code;

2. Create an account at [OpenAi API](https://openai.com/blog/openai-api). You will need OpenAi credits to run the application, and in general, new users get $5 credits to test the API. This is enough to run the application;

3. Create an API key in the OpenAI API. To do this, click on the `View API keys` option and create a new API key. Copy the value from the key that was created;

4. In the same directory where the `index.py` file is located on your machine, create the `.env` file and paste in this file the following code snippet, replacing `your-api-key` with the key you generated in step 3:

```
OPENAI_API_KEY='your-api-key'
```

5. In the same directory, now create a folder called `data` and put the pdf with the car manual, called `ford_ka.pdf`;

6. Run the `index.py` notebook, replacing the variable `query_str` with the question you wish to ask the chatbot.

```
from langchain.callbacks import get_openai_callback

query_engine = index.as_query_engine()

with get_openai_callback() as cb:
    query_str = "How does the air recycle button work?"
    response = query_engine.query(query_str)
    print(cb)
```

- **Ask your PDF**

1. Clone the repository to your local machine:
```
git clone https://github.com/alejandro-ao/langchain-ask-pdf.git 
```

2. Navigate to the cloned repository:
```
cd langchain-ask-pdf
```

3. Install the required packages and dependencies using pip:
```
pip install -r requirements.txt
```

4. Create a file named ".env" in the root directory of the cloned repository and add the following environment variable:
```
OPENAI_API_KEY=<your_openai_api_key>
```
Replace `<your_openai_api_key>` with your actual OpenAI API key. If you don't have an API key, you can sign up for one  [here](https://beta.openai.com/signup/).

5. Run the code using the following command:
```
streamlit run main.py
```
A new tab will be opened in your default web browser, showing the "Ask your PDF" app. Upload a PDF file by clicking the "Upload your PDF files" button, and enter a question about the uploaded file in the text box below it. Then click the "Submit" button to see the answer to your question.

- **Question and answer system**

1. Clone the application repository from github using the following command:
```
git clone https://github.com/mallahyari/drqa.git
```

2. Create an account in [Qdrant Cloud](https://qdrant.tech/documentation/cloud/) to get your`API_KEY` and `HOST_URL`.

3. Create an account at (OpenAi API)[https://openai.com/blog/openai-api]. You will need OpenAi credits to run the application, and in general, new users get $5 credits to test the API. This is enough to run the application.

4. Create an API key in the OpenAI API. To do this, click on the `View API keys` option and create a new API key. Copy the `OPENAI_API_KEY` value from the key that was created.

5. Go to `/drqa/backend/app` and create a `.env` file with the following structure replacing `<YOUR_KEY>` to your key:
```
QDRANT_HOST="<YOUR_KEY>"
QDRANT_API_KEY="<YOUR_KEY>"
OPENAI_API_KEY="<YOUR_KEY>"
```

6. For running the backend, first create a virtual environment and execute the following commands:
```
pip install -r requirements.txt
python main.py
```

7. In other terminal, go to `/drqa/frontend` and execute the following commands to run the frontend:
```
npm install
npm start
```

## 📊 Analysis and Comparison

Our analysis and comparison of the three solutions focused on the following criteria:

1. Performance
2. Cost
3. Answer Accuracy
4. User Experience

| Criteria        | Doc Chatbot with LlamaIndex | Ask your PDF | Question and answer system
| :---------:     |:---------------------------:|:------------:|:-------------------------:|
| Performance     | Good                        | Good         | Good
| Cost            | $$                          | $            | $
| Answer Accuracy | High                        | High         | Medium
| User Experience | Fair                        | Good         | Good

You can find a detailed report of our analysis [here](./analysis_report.md).  

## ✉️ Contact Information

If you have any questions or feedback, please feel free to reach out to the authors of this analysis:

- [Mariana Azevedo](mailto:mariana.brito.110@ufrn.edu.br)
- [Morsinaldo Medeiros](mailto:morsinaldo.medeiros.075@ufrn.edu.br)
- [Thaís Medeiros](mailto:thais.araujo.707@ufrn.edu.br)

And don't hesitate to contact the developers of the solutions analyzed:

- [Chatbot with LlamaIndex](https://medium.com/@wenbohuang0307)
- [Ask your PDF](https://github.com/alejandro-ao)
- [Question and answer system](https://github.com/mallahyari)
