# Hi, I'm João 👋

### 🤖 AI & Software Engineer

I design and build **AI agents and the platforms they run on**. That covers the agent harness, the data pipelines that feed it and the product people actually use.

![Core stack](https://skillicons.dev/icons?i=rust,py,ts,react,django,docker,linux)

---

## 🧭 About me

- 🧠 Deep into **harness engineering**: the code around an LLM that decides whether an agent can be trusted.
- 🤖 I build **autonomous agents** with **deepagents** and **LangGraph** on self-hosted models, so data never leaves the infrastructure.
- 🦀 I write **high-throughput data engines in Rust** and expose them to Python with **PyO3 / maturin**.
- ⚙️ I work full stack: Rust and Python on the backend, React and TypeScript on the frontend.
- 🌱 Currently learning **Apache Kafka** and going deeper into **Axum**.
- ⭐ My favourite language is somewhere between **Python** and **Rust**.
- 📚 Doing a Master's degree in Computer Science at the **University of Évora**.

---

## 🧠 Harness engineering & agents

The model is only part of an agent. The rest is the **harness**: the tools, context, budgets, checks and feedback loops around the model. That is the part I enjoy building. Most of my agent work runs on **[deepagents](https://github.com/langchain-ai/deepagents)** (LangGraph).

**🏗️ Agent architecture**
- Lead agents that plan the work, delegate to **specialist subagents** and keep their own scratch filesystem
- **Tiered runs**, where each tier gets its own tool surface, step budget and definition of "done"
- Custom deepagents **middleware**, such as summarisation and context editing, tuned to keep long runs inside the context window
- A **"System One / System Two"** split: a small, fast model answers narrow questions so the slow, deliberate agent doesn't have to
- **Skills**: procedural knowledge that is loaded only when it applies. Skills describe *how* to work a case and never *what* to conclude.

**🛡️ Trust & guardrails**
- **Deterministic guardrails** written as pure functions over the finished trace, which catch confident conclusions that the evidence doesn't support
- An **independent verifier** that re-reads the evidence *without* seeing the first agent's conclusion
- An **evidence score** computed from the trace, so confidence is earned rather than self-reported by the model
- **Human-in-the-loop memory**: agents propose lessons, people approve them, and rejected memories never reach a run

**📈 Evaluation & improvement**
- **Harness fingerprinting**, which hashes prompts, tools, guardrails and model settings so every run says which harness produced it
- Benchmarks that score agent decisions **against human decisions** on the same cases
- A **harness-improvement loop** that proposes one change, measures it fairly and keeps it only if the gain is real
- Full **tracing** of every step, tool call and model response, plus a **24/7 autopilot** mode for unattended operation

**🔒 Private by default.** Models are self-hosted behind **llama.cpp / LiteLLM**, with **RAG** and vector search on our own infrastructure.

---

## 🛠️ What else I build

**⚡ Real-time data & ETL**
- A Rust ETL engine that parses, normalises and correlates high volumes of events into an open schema
- Streaming consumers over **AMQP / RabbitMQ** using Tokio
- Analytical storage on **ClickHouse** (MergeTree engines, batched writes, multi-tenant data)

**🏗️ Platform & backend**
- One **Django REST** codebase deployed as several independent services
- **Celery** with dedicated queues, **Channels** websockets and **Axum** microservices
- Enterprise auth: **JWT, MFA** (TOTP, WebAuthn, YubiKey), **SSO**, **RBAC** and audit trails

**🎨 Frontend**
- **React 19**, **TypeScript**, **Vite**, **Tailwind 4** and **shadcn/ui**, plus visual node editors, maps and 3D

---

## 💻 Languages

![Languages](https://skillicons.dev/icons?i=rust,py,ts,js,go,java,scala,c,cpp,cs&perline=10)
![Languages](https://skillicons.dev/icons?i=php,dart,kotlin,swift,html,css,md&perline=10)

## 🧰 Frameworks & tools

![Frameworks](https://skillicons.dev/icons?i=django,fastapi,react,vite,tailwind,nodejs,svelte,graphql,flutter,electron&perline=10)
![Tools](https://skillicons.dev/icons?i=dotnet,spring,laravel,kafka,rabbitmq,nginx,docker,git,githubactions,pnpm&perline=10)
![Tools](https://skillicons.dev/icons?i=threejs,sklearn,gradle,maven,postman,bootstrap&perline=10)

## 🗄️ Databases & messaging

![Databases](https://skillicons.dev/icons?i=postgres,mongodb,redis,mysql,rabbitmq,kafka)

## 🔌 Having fun with

![Hardware](https://skillicons.dev/icons?i=raspberrypi,arduino)

## 🖥️ Like to work on

![OS](https://skillicons.dev/icons?i=apple,ubuntu,linux)

---

## 📊 GitHub stats

<img height="170" src="https://github-readme-stats-sigma-five.vercel.app/api?username=jcondeco207&count_private=true&show_icons=true&theme=tokyonight&hide_border=true" />
<img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=jcondeco207&layout=compact&count_private=true&theme=tokyonight&langs_count=8&hide_border=true" />

<!---
jcondeco207/jcondeco207 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
--->
