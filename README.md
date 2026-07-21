# Sigma GPT

A ChatGPT clone built from scratch using the MERN stack and the OpenAI API. No boilerplate, no starter templates — just React, Node, Express, and MongoDB wired together to actually understand how a chat app like this works under the hood.

This started as a learning project, but it turned into a fully working chat application with a real backend, a database, and a UI that feels close to the real thing.

## What it does

- Chat with GPT in a clean, ChatGPT-style interface
- Messages are sent to OpenAI's API and streamed back with a typing effect
- Conversations are saved to MongoDB, so chats persist
- Sidebar to manage and switch between different chats
- Loading states while waiting for a response
- Responses are formatted properly (code blocks, markdown, etc.)

## Tech stack

**Frontend:** React
**Backend:** Node.js, Express
**Database:** MongoDB
**AI:** OpenAI API

## How it's built

The backend exposes a couple of core routes — one to test the setup, and one that actually handles the chat logic (sending the prompt to OpenAI and returning the reply). Models are defined for storing chats in MongoDB, and everything is connected through a database layer set up early on.

On the frontend, the sidebar and chat window were built as separate components and styled individually, then connected to the backend so prompts actually get a response. From there it was mostly about polish — adding a loader while waiting on OpenAI, displaying past chats, formatting the GPT replies properly, and adding a typing effect so responses don't just appear all at once.

## Running it locally

1. Clone the repo
   ```bash
   git clone https://github.com/Anjani-Sarawagi/Sigma-Gpt.git
   cd Sigma-Gpt
   ```

2. Install dependencies for both frontend and backend
   ```bash
   cd backend && npm install
   cd ../frontend && npm install
   ```

3. Run the backend
   ```bash
   cd backend
   npm start
   ```

5. Run the frontend
   ```bash
   cd frontend
   npm start
   ```

## Why I built this

I wanted to actually understand what's happening behind a tool like ChatGPT — not just use it, but build the plumbing myself. Setting up the routes, connecting OpenAI's API properly, handling state on the frontend, getting the typing effect to feel right — all of it taught me a lot more than just reading about how these apps work.
