# chatbot-readme

[![](https://billionapps.net/wp-content/uploads/2023/11/BillionApps.svg)](https://billionapps.net/)

## Soure code for AI chatbot
Here is simple chatbot using OpenAI's gpt3.5, built directly in JS.
Download the folder and open the index.html file to know more about the bot, asking questions relating to BillionApps

## Setting up Environment 
Create a python venv
```bash
python -m venv env
source env/bin/activate
```
Install the project's dependancies
```bash
pip install -r backend/requirements.txt
```

## company_chat_create_db.py:
> Creates vector DB by reading the contents of the provided company background information, and saves it locally as faiss_company_index

## app.py:
> Loads the db created in above step,

> Receives the user's query and contextualizes it with the chat_history, 
> Retrives the matching content and sends final query to gpt server

