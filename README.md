# Rag Starter

This is the completed version of the project in [Retrieval-Augmented Generation (RAG) guide](https://sdk.vercel.ai/docs/guides/rag-chatbot).

## pre-requisites

Setup the postgresql database with pgvector plugin using docker-compose
```bash
docker-compose up
```

Setup NVM and the node version
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash

NODE_VERSION=$(cat .nvmrc)
nvm install "$NODE_VERSION"
nvm alias default "$NODE_VERSION"
nvm use "$NODE_VERSION"
```

Setup the environment variables
```bash
cp .env.example .env
# then add your OPENAI_API_KEY to the .env file
```

Next - install the deps and start the app.
```bash
pnpm i
pnpm dev
```

## stack

This project will use the following stack:

- [Next.js](https://nextjs.org) 14 (App Router)
- [Vercel AI SDK](https://sdk.vercel.ai/docs)
- [OpenAI](https://openai.com)
- [Drizzle ORM](https://orm.drizzle.team)
- [Postgres](https://www.postgresql.org/) with [ pgvector ](https://github.com/pgvector/pgvector)
- [shadcn-ui](https://ui.shadcn.com) and [TailwindCSS](https://tailwindcss.com) for styling
