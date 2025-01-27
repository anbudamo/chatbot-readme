[![](https://billionapps.net/wp-content/uploads/2023/11/BillionApps.svg)](https://billionapps.net/)

<div align="center">
  <h2 align="center">Best-README-Template</h2>

  <p align="center">
    An awesome README template to jumpstart your projects!
    <br />
    <a href="https://github.com/othneildrew/Best-README-Template"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/othneildrew/Best-README-Template">View Demo</a>
    &middot;
    <a href="https://github.com/othneildrew/Best-README-Template/issues/new?labels=bug&template=bug-report---.md">Report Bug</a>
    &middot;
    <a href="https://github.com/othneildrew/Best-README-Template/issues/new?labels=enhancement&template=feature-request---.md">Request Feature</a>
  </p>
</div>

## About
The chatbot is a RAG application that performs call routing to maintain a conversational flow with the user. 
It's capabilities are as follows:
- Conversing- Greets and answers specific questions about the company
- Requirement gathering- Inquires about client needs, specifications, and information
- Conversation summarization- Concludes the conversation effectively, and sends a follow up email to the user

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

This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

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

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.




