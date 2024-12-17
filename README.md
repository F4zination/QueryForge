# QueryForge
A powerful foundry where user questions are shaped into precise, context-enriched queries for smarter responses.


**Key Points:**

1. **Front-End Choice:**
   - **SvelteKit** for minimalistic UI, simplicity, and fast development.
   - Alternatively, **Next.js** if you prefer React and existing familiarity.

2. **Styling:**
   - Use **Tailwind CSS** for quick, consistent, and minimalistic styling.

3. **LLM Integration (Ollama) & RAG:**
   - Containerize **Ollama** alongside your application.
   - Integrate **LangGraph** to build the retrieval-augmented generation flow.
   - Use a vector store (e.g., **Qdrant** or `pgvector` with Postgres) for document retrieval.

4. **Streaming Responses:**
   - Implement **Server-Sent Events (SSE)** in the backend.
   - Frontend consumes the stream to display live LLM responses.

5. **Authentication & Role Management:**
   - Use **Keycloak** for LDAP integration and user/role management.
   - Start with a simple JWT-based approach if not fully integrating LDAP initially.
   - Ensure secure authentication flow with session tokens stored as HTTP-only cookies.

6. **Backend Stack:**
   - **Node.js** for faster development and compatibility with LangGraph and streaming.
   - Consider **Fastify** or the built-in SvelteKit/Next.js server for backend routes.
   - Use **Prisma** as an ORM for a Postgres database and integrate vector search if needed.

7. **Deployment:**
   - Use **Docker/Docker Compose** to define and run all services (frontend, backend, Ollama, Keycloak, database, vector store).
   - This provides isolated, reproducible environments and simplifies scaling.

8. **Performance & Scalability:**
   - Scale horizontally with multiple Node.js instances if needed.
   - Use Redis or another session store if load balancing becomes necessary.

9. **Timeline (2 Weeks):**
   - Week 1: Set up authentication (Keycloak+LDAP), integrate Ollama and LangGraph, configure database.
   - Week 2: Implement frontend UI, SSE streaming, role checks, and initial testing.

10. **Maintainability:**
    - Clear project structure, proper documentation, and CI/CD pipelines.
    - Tooling choices (Node, SvelteKit/Next.js, Prisma) ensure a strong ecosystem and ease for future maintainers.
