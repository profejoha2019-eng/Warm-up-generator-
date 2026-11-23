# Warm-up Generator

A small Node.js + HTML app that generates student-facing English warm-ups using the Gemini API.

## What you need
- Node.js 18 or newer
- A Gemini API key from https://aistudio.google.com/app/apikey
- Internet access while generating activities

## Run locally
1. Install Node.js from https://nodejs.org/ if it is not already installed.
2. Extract this ZIP folder.
3. Open a terminal in this folder and run: `npm install`
4. Copy `.env.example` and rename the copy to `.env`.
5. Open `.env` and replace the example value with your Gemini API key:
   `GEMINI_API_KEY=your_actual_key`
6. Run: `npm start`
7. Open http://localhost:3000 in your browser.

## Security
- Never paste your API key into `public/index.html`.
- Never share the `.env` file or upload it to a public repository.
- `.env` is excluded by `.gitignore`.
- The free tier has usage limits and Google's free-tier data-use terms apply. Do not enter student names or personal information.

## Deploying online
This app needs a Node.js host (not a static-only HTML host). Deploy the folder to a Node-compatible service and set `GEMINI_API_KEY` as a private environment variable in that service's dashboard. Set the start command to `npm start`.

## Model
Default model: `gemini-3.8-flash`. If your AI Studio account does not have access to that model, set `GEMINI_MODEL` in `.env` to a model currently available in your free tier.
