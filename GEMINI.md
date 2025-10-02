##  Core Principles (High Priority)

### 1. Readability & Maintainability
- Prioritize **clear, maintainable code** over clever micro-optimizations.
- Code should be easy to read and understand at a glance.
- Every new function must begin with **two short comment lines**:
  1. **Input & Output Parameters**  
  2. **What the function does**

### 2. Explicit Typing
- Use **explicit types** (TypeScript types, Java types, Python type hints) for all public APIs and library boundaries.
- Avoid implicit “magic” typing whenever possible.

### 3. Security First
- **Never hardcode secrets** (API keys, passwords, tokens).
- Always use environment variables or config placeholders  
  (e.g. `process.env.MY_SECRET`, `ENV_MY_SECRET`).

### 4. Async for I/O
- Use **async/await (or equivalent)** for network, file, or database I/O.
- Avoid blocking calls in request handlers or main loops.

### 5. Hallucination Reduction
- When producing factual claims (versions, API behavior, release dates, benchmarks, legal text, metrics) include a short **source** comment or mark the claim as **[UNVERIFIED]** if a reliable source isn't known.
- If a claim cannot be confidently produced from local repo context, return a clear placeholder: `// TODO: verify` or `[UNVERIFIED]` rather than inventing facts.
- For external API behavior, prefer returning a minimal, conservative example and add `// SOURCE: <url>` comment when known.

### 6. Keep Examples Local / Repo-first
- Prefer to rely on files in the repository (package.json, pyproject.toml, README) to answer questions about the project. If repository lacks the info, mark as [UNVERIFIED] rather than guessing.




