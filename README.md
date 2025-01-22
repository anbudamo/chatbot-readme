[![](https://billionapps.net/wp-content/uploads/2023/11/BillionApps.svg)](https://billionapps.net/)

# Conversational chatbot [feedback for heading]
The chatbot is a RAG application that performs call routing to maintain a conversational flow with the user. 
It's capabilities are as follows:
- Conversing- Greets and answers specific questions about the company
- Requirement gathering- Inquires about client needs, specifications, and information
- Conversation summarization- Concludes the conversation effectively, and sends a follow up email to the user

## company_chat_create_db.py:
> Creates vector DB by reading the contents of the provided company background information, and saves it locally as faiss_company_index

## app.py:
>- Loads the db created in above step,
>- Receives the user's query and contextualizes it with the chat_history, 
>- Retrives the matching content and sends final query to gpt server

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
Create a .env file in backend folder 
```bash
touch backend/.env
```
Paste following into .env file and enter keys
```bash
OPENAI_API_KEY=
SENDGRID_API_KEY=
```

## Getting started 
user table needs to be created, so run 
```bash
sqlite3 backend/chat_history.db
```
Enter following sql command to create table
```bash
CREATE TABLE IF NOT EXISTS "users" (
session_id TEXT PRIMARY KEY,
content TEXT,
name TEXT,
email TEXT,
timestamp TEXT,
count INTEGER default 0,
category TEXT,
summary TEXT,
reqs_asked INTEGER default 0,
consul_asked INTEGER default 0);
```




