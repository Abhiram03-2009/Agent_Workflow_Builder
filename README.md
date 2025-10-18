<h1 align="center">
Agent Workflow Builder
</h1>

<h3 align="center">Build and deploy AI agent workflows in minutes.</p>

## Quickstart

#### Note
Docker must be installed and running on your machine.

Access the application at [http://localhost:3000/](http://localhost:3000/)

#### Using Local Models with Ollama

Run Sim with local AI models using [Ollama](https://ollama.ai) - no external APIs required:

```bash
# Start with GPU support (automatically downloads gemma3:4b model)
docker compose -f docker-compose.ollama.yml --profile setup up -d

# For CPU-only systems:
docker compose -f docker-compose.ollama.yml --profile cpu --profile setup up -d
```

Wait for the model to download, then visit [http://localhost:3000](http://localhost:3000). Add more models with:
```bash
docker compose -f docker-compose.ollama.yml exec ollama ollama pull llama3.1:8b
```

### Self-hosted: Dev Containers

1. Open VS Code with the [Remote - Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)
2. Open the project and click "Reopen in Container" when prompted
3. Run `bun run dev:full` in the terminal
   - This starts both the main application and the realtime socket server

### Self-hosted: Manual Setup

**Requirements:**
- [Bun](https://bun.sh/) runtime
- PostgreSQL 12+ with [pgvector extension](https://github.com/pgvector/pgvector) (required for AI embeddings)

## Tech Stack

- **Framework**: [Next.js](https://nextjs.org/) (App Router)
- **Runtime**: [Bun](https://bun.sh/)
- **Database**: PostgreSQL with [Drizzle ORM](https://orm.drizzle.team)
- **Authentication**: [Better Auth](https://better-auth.com)
- **UI**: [Shadcn](https://ui.shadcn.com/), [Tailwind CSS](https://tailwindcss.com)
- **State Management**: [Zustand](https://zustand-demo.pmnd.rs/)
- **Flow Editor**: [ReactFlow](https://reactflow.dev/)
- **Docs**: [Fumadocs](https://fumadocs.vercel.app/)
- **Monorepo**: [Turborepo](https://turborepo.org/)
- **Realtime**: [Socket.io](https://socket.io/)
- **Background Jobs**: [Trigger.dev](https://trigger.dev/)
- **Remote Code Execution**: [E2B](https://www.e2b.dev/)

<h2 align="center">Made by Abhiram Kaakarla </h2>
