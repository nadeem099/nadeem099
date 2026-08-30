<!--
  ─────────────────────────────────────────────────────────────────
  SETUP
  1. Repo name must EXACTLY equal your GitHub username. Public.
  2. Commit this as README.md at the repo root.
  3. Commit the assets/ folder alongside it:
        <repo>/README.md
        <repo>/assets/header.svg
        <repo>/assets/focus.svg
        <repo>/assets/stack.svg
        <repo>/assets/divider.svg
  4. Fill in the Connect links at the bottom.

  Every image is a relative path into your own repo. No shields.io,
  no vercel.app, no third-party CDN — nothing to rate-limit, expire,
  or get blocked by a corporate proxy. Edit the SVGs directly to
  change any wording; they are plain text files.
  ─────────────────────────────────────────────────────────────────
-->

<img src="/assets/header.svg" alt="Nadeem — Senior Software Engineer" width="100%" />

<img src="assets/divider.svg" alt="" width="100%" />

```ts
const nadeem: Engineer = {
  role:     "Senior Software Engineer",
  writes:   ["TypeScript", "Go", "Python"],
  ships:    ["retrieval pipelines", "streaming LLM APIs", "React at scale"],
  optimises: ["p99 latency", "recall@k", "time-to-first-token", "blast radius"],
  belief:   "boring infrastructure, interesting products",
};
```

<img src="assets/focus.svg" alt="What I ship / How I operate" width="100%" />

<img src="assets/divider.svg" alt="" width="100%" />

## Stack

<img src="assets/stack.svg" alt="Technology stack" width="100%" />

<img src="assets/divider.svg" alt="" width="100%" />

## Selected work

| Project | Stack | What it does |
| :--- | :--- | :--- |
| **rag-service** | Go · Postgres/pgvector · OpenAI | Hybrid retrieval API — BM25 + dense, cross-encoder rerank, grounded citations |
| **stream-ui** | Next.js · TypeScript · SSE | Token-streaming chat surface with live tool-call rendering and cancellation |
| **eval-harness** | Python · Ragas | Regression suite for RAG: faithfulness, context precision, answer recall |
| **go-gateway** | Go · gRPC · Redis | Edge gateway — authn/z, token-bucket limiting, circuit breaking, tracing |

<details>
<summary><b>How I think about RAG</b></summary>

<br/>

- **Most "hallucination" bugs are recall bugs.** If the passage never made it into context, no amount of prompt engineering saves the answer. Fix the index first.
- **Hybrid retrieval by default.** Lexical catches exact identifiers and rare tokens; dense catches paraphrase. Run both, fuse, then cross-encoder rerank the top ~50.
- **Chunking is a product decision, not a constant.** Structure-aware splits that respect headings and tables beat a fixed 512-token window nearly every time.
- **Evaluate before you tune.** Without a golden set you are not improving the system, you are just moving it. Faithfulness and context precision first, latency second.
- **Cite or abstain.** If the retrieved context does not support an answer, the correct output is saying so.

</details>

<details>
<summary><b>Engineering defaults I don't negotiate</b></summary>

<br/>

- Types at every boundary — TS strict, Go generics, schema validation on the wire
- Structured logs with a request ID that survives every hop
- Idempotency keys on anything that writes
- Timeouts, retries with jitter, and a circuit breaker on every outbound call
- Migrations that are reversible, or a written reason why they aren't

</details>

<img src="assets/divider.svg" alt="" width="100%" />

<p align="center">
  <a href="https://linkedin.com/in/YOUR-LINKEDIN"><b>LinkedIn</b></a>
  &nbsp;·&nbsp;
  <a href="mailto:YOUR@EMAIL.COM"><b>Email</b></a>
  &nbsp;·&nbsp;
  <a href="https://x.com/YOUR-HANDLE"><b>X</b></a>
  &nbsp;·&nbsp;
  <a href="https://YOUR-SITE.dev"><b>Portfolio</b></a>
</p>
