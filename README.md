<h1 align="center">Nadeem</h1>

<p align="center">
  <b>Senior Software Engineer</b><br>
  <sub>Full Stack &nbsp;·&nbsp; GenAI &amp; RAG &nbsp;·&nbsp; Distributed Systems</sub>
</p>

<p align="center">
  <a href="https://in.linkedin.com/in/nadeemchoudhary">LinkedIn</a> &nbsp;·&nbsp;
  <a href="mailto:ah.nadeem.choudhary@gmail.com">Email</a>
</p>

```ts
const nadeem: Engineer = {
  role:      "Senior Software Engineer",
  writes:    ["TypeScript", "Go", "Python"],
  ships:     ["retrieval pipelines", "streaming LLM APIs", "React at scale"],
  optimises: ["p99 latency", "recall@k", "time-to-first-token", "blast radius"],
  belief:    "boring infrastructure, interesting products",
};
```

<table>
<tr>
<td width="50%" valign="top">

### ⚡ What I ship

**Retrieval systems that cite their sources**<br>
<sub>Answers grounded in your own data, with the passage attached.</sub>

**Streaming LLM endpoints**<br>
<sub>Tool calls, backpressure, retries, hard cost ceilings.</sub>

**Go services that hold p99 under 50ms**<br>
<sub>While the traffic graph keeps climbing.</sub>

**React surfaces that stay smooth**<br>
<sub>After the dataset stops being a demo fixture.</sub>

</td>
<td width="50%" valign="top">

### ◆ How I operate

**Read the code before rewriting it**<br>
<sub>Most bugs are somebody's old assumption.</sub>

**Contract first**<br>
<sub>Schema, error shape, version policy. Implementation after.</sub>

**Instrument before optimising**<br>
<sub>Guessing at the hot path burns weeks, reliably.</sub>

**Ship behind a flag, roll forward**<br>
<sub>Keep every decision cheap to reverse.</sub>

</td>
</tr>
</table>

---

## Stack

<table>
<tr><td><b>Languages</b></td><td>
<kbd> TypeScript </kbd> <kbd> Go </kbd> <kbd> JavaScript </kbd> <kbd> Python </kbd> <kbd> SQL </kbd> <kbd> Bash </kbd>
</td></tr>

<tr><td><b>Frontend</b></td><td>
<kbd> React </kbd> <kbd> Next.js </kbd> <kbd> Redux Toolkit </kbd> <kbd> TanStack Query </kbd> <kbd> Tailwind </kbd> <kbd> Vite </kbd> <kbd> Playwright </kbd>
</td></tr>

<tr><td><b>Backend</b></td><td>
<kbd> Node.js </kbd> <kbd> NestJS </kbd> <kbd> Express </kbd> <kbd> Fiber </kbd> <kbd> gRPC </kbd> <kbd> GraphQL </kbd> <kbd> WebSockets </kbd>
</td></tr>

<tr><td><b>Storage &amp; streams</b></td><td>
<kbd> PostgreSQL </kbd> <kbd> pgvector </kbd> <kbd> Redis </kbd> <kbd> MongoDB </kbd> <kbd> Kafka </kbd> <kbd> ClickHouse </kbd> <kbd> OpenSearch </kbd> <kbd> S3 </kbd>
</td></tr>

<tr><td><b>GenAI &amp; RAG</b></td><td>
<kbd> LangChain </kbd> <kbd> LlamaIndex </kbd> <kbd> OpenAI </kbd> <kbd> Anthropic </kbd> <kbd> Ollama </kbd> <kbd> Qdrant </kbd> <kbd> Hybrid search </kbd> <kbd> Rerankers </kbd> <kbd> Ragas </kbd>
</td></tr>

<tr><td><b>Platform</b></td><td>
<kbd> AWS </kbd> <kbd> Docker </kbd> <kbd> Kubernetes </kbd> <kbd> Terraform </kbd> <kbd> GitHub Actions </kbd> <kbd> OpenTelemetry </kbd> <kbd> Grafana </kbd>
</td></tr>
</table>

---

## Selected work

| Project | Stack | What it does |
| :--- | :--- | :--- |
| **rag-service** | Go · Postgres/pgvector · OpenAI | Hybrid retrieval API — BM25 + dense, cross-encoder rerank, grounded citations |
| **stream-ui** | Next.js · TypeScript · SSE | Token-streaming chat surface with live tool-call rendering and cancellation |
| **eval-harness** | Python · Ragas | Regression suite for RAG: faithfulness, context precision, answer recall |
| **go-gateway** | Go · gRPC · Redis | Edge gateway — authn/z, token-bucket limiting, circuit breaking, tracing |

<details>
<summary><b>How I think about RAG</b></summary>

<br>

- **Most "hallucination" bugs are recall bugs.** If the passage never made it into context, no amount of prompt engineering saves the answer. Fix the index first.
- **Hybrid retrieval by default.** Lexical catches exact identifiers and rare tokens; dense catches paraphrase. Run both, fuse, then cross-encoder rerank the top ~50.
- **Chunking is a product decision, not a constant.** Structure-aware splits that respect headings and tables beat a fixed 512-token window nearly every time.
- **Evaluate before you tune.** Without a golden set you are not improving the system, you are just moving it. Faithfulness and context precision first, latency second.
- **Cite or abstain.** If the retrieved context does not support an answer, the correct output is saying so.

</details>

<details>
<summary><b>Engineering defaults I don't negotiate</b></summary>

<br>

- Types at every boundary — TS strict, Go generics, schema validation on the wire
- Structured logs with a request ID that survives every hop
- Idempotency keys on anything that writes
- Timeouts, retries with jitter, and a circuit breaker on every outbound call
- Migrations that are reversible, or a written reason why they aren't

</details>

---

<p align="center">
  <sub>Open to interesting problems in retrieval, platform, and developer tooling.</sub>
</p>
