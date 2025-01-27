[![](https://billionapps.net/wp-content/uploads/2023/11/BillionApps.svg)](https://billionapps.net/)

<div align="center">
  <h3 align="center">Conversational Chatbot</h3>

  <p align="center">
    Get started with BillionApp's Conversational Chatbot and learn about its features!
    <br />
    <a href="https://github.com/anbudamo/chatbot-readme/blob/main/README.md"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/anbudamo/chatbot-readme/blob/main/README.md">View Demo</a>
    &middot;
    <a href="https://github.com/anbudamo/chatbot-readme/blob/main/README.md">Report Bug</a>
    &middot;
    <a href="https://github.com/anbudamo/chatbot-readme/blob/main/README.md">Request Feature</a>
  </p>
</div>

## About The Project
This project is a Flask-based chat assistant built with next.js, bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app). It integrates with OpenAi's GPT models and provides flexible conversational capabilities through dynamic LLM call routing. 

Features:
- Conversational AI- Implements history-aware retrieval, which contextualizes the users prompt using the past conversation history to provide a smooth conversational flow
- RAG-Powered Retrieval- Employs FAISS within a RAG framework to deliver accurate, context-based responses
- Intelligent Workflow Routing- Directs user inputs to tailored workflows, such as consultation, requirement gathering, and summarization
- Email Notification- Sends conversation summary and follow up info via email 
  
## Getting Started

### Running the development server
First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) to automatically optimize and load Inter, a custom Google Font.

### Set up
Here is a step by step on how to do further setup
1. Install the needed dependancies in a [virtual environment](https://docs.python.org/3/tutorial/venv.html) by running
```bash
pip install -r backend/requirements.txt
```
2. Create and fill in the .env file with the appropriate keys
```bash
touch backend/.env
```
```bash
OPENAI_API_KEY='ENTER YOUR OPENAI_API_KEY'
SENDGRID_API_KEY='ENTER YOUR SENDGRID_API_KEY'
```


## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.



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

