Medical ChatBot

It is a user friendly tool to ask for any disease related queries 
which can be helpful for common people.

Developed application using Langchain framewrodk and Meta Llama2 quantised model

Features:

--Knowledge Base created using a Medical Science book

--The data is divided into chunks and embedded before storing them in Pinecone
  vector database

-- User can ask any query which is first embedded into a vector and then 
  searched in the database for the best match(k best matches considered)

--Best match is then forwarded to LLM model LLama2 for exact answer


Execution Steps:

1)Clone the repository
Project repo: https://github.com/arka57/LLM_Medical_Chatbot

2) Create a virtual environment after opening the repository
conda create -n mchatbot python=3.8 -y
conda activate mchatbot

3) Install the requirements
pip install -r requirements.txt

4)Create a .env file in the root directory and add your Pinecone credentials as follows:
PINECONE_API_KEY = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
PINECONE_API_ENV = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"


5)Download the quantize model from the link provided in model folder
 and create a folder model and store the downloaded model inside:

Download the Llama 2 Model:llama-2-7b-chat.ggmlv3.q4_0.bin
Link:https://huggingface.co/TheBloke/Llama-2-7B-Chat-GGML/tree/main

6)Run the following command
python store_index.py

7)Finally run the following command
python app.py 

8)Give the query and answer will be returned


Example

Technologies Used:

--Langchain
--Meta Llama2
--Pinecone Vector Database
--Python
--Flask