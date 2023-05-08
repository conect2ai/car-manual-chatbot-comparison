# Question and answer system
The Question and answer system is a system that combines LangChain and Large Language Models, such as OpenAI’s GPT-3, and uses React/Typescript for the frontend and Python FastAPI for the backend. QDrant is used to store embeddings and text documents for fast search.

## 📚 Documentation and Resources
- [FastAPI Documentation](https://fastapi.tiangolo.com/)
- [React Documentation](https://reactjs.org/docs/getting-started.html)
- [Typescript Documentation](https://www.typescriptlang.org/docs/)
- [Qdrant Documentation](https://qdrant.tech/documentation/)
- [LangChain Documentation](https://langchain.readthedocs.io/en/latest/)
- [Application Source Repository](https://github.com/mallahyari/drqa)

## 💻 How to Run

1. Clone the repository from github using the following command:
```
git clone https://github.com/conect2ai/car-manual-chatbot-comparison.git
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