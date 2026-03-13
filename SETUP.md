# Local Setup Guide

This guide shows how to run the Tracer agent locally with your Tracer account.

## Prerequisites

- Python 3.11+
- `make`

## 1. Install dependencies

```bash
make install
```

## 2. Configure Env variables

1. Copy the example env file:

   ```bash
   cp .env.example .env
   ```

2. Go to `https://app.tracer.cloud`, sign in, and create or copy your Tracer API token from settings.
3. In your local `.env`, set the tracer JWT token and other env variables(for example):

   ```bash
   JWT_TOKEN=your-tracer-token-from-app.tracer.cloud
   ANTHROPIC_API_KEY=your-anthropic-api-key
   ```

You can use `.env.example` as a reference for any other optional integrations you want to enable.

## 3. Run the LangGraph dev UI

Start the LangGraph dev server:

```bash
make dev
```

Then open `http://localhost:2024` in your browser. From there you can send alerts to the agent and inspect the graph step by step while developing.
