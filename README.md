### Medical ChatBot

It is a user friendly tool to ask for any disease related queries 
which can be helpful for common people.

Developed application using Langchain framework and Meta Llama2 quantised model

## Features:

--Knowledge Base created using a Medical Science book

--The data is divided into chunks and embedded before storing them in Pinecone
  vector database

-- User can ask any query which is first embedded into a vector and then 
  searched in the database for the best match(k best matches considered)

--Best match is then forwarded to LLM model LLama2 for exact answer


## Execution Steps:

1)Clone the repository<br>
Project repo: https://github.com/arka57/LLM_Medical_Chatbot
<br><br>
2) Create a virtual environment after opening the repository
<br>conda create -n env_name python=3.8 -y
<br>conda activate env_name<br><br>

3)Install the requirements<br>
pip install -r requirements.txt<br><br>

4)Create a .env file in the root directory and add your Pinecone credentials as follows:
PINECONE_API_KEY = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
PINECONE_API_ENV = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"<br><br>


5)Download the quantize model from the link provided in model folder
 and create a folder model and store the downloaded model inside:<br>

Download the Llama 2 Model:llama-2-7b-chat.ggmlv3.q4_0.bin<br>
Link:https://huggingface.co/TheBloke/Llama-2-7B-Chat-GGML/tree/main<br><br>

6)Run the following command<br>
python store_index.py<br><br>

7)Finally run the following command<br>
python app.py <br><br>

8)Give the query and answer will be returned<br><br>


## Example<br>
<img width="708" alt="LLM_Medical_Chatbot" src="https://github.com/arka57/LLM_Medical_Chatbot/assets/36561428/e347b147-3dfd-46a3-bcb2-bf131008f407">
<br><br>

## Technologies Used:<br>

--Langchain<br>
--Meta Llama2<br>
--Pinecone Vector Database<br>
--Python<br>
--Flask<br>
