## 👋 Welcome, I'm Andrew Pleeter

[<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linkedin/linkedin-original.svg" alt="LinkedIn" width="12"/> Linkedin](https://www.linkedin.com/in/ahp2002/) •
[📧 Email](mailto:andrewpleeter@gmail.com) •
[🌐 Website](https://andrewpleeter.us) •
[📄 Resume](https://andrewpleeter.us/resume)

---

### 🔧 About Me

Software engineer working mostly on backend and fullstack systems.

- Recent focus: agent runtimes in **Rust**, real-time streaming systems in **Go**, recommendation and ranking, LLM tooling and MCP servers, and web apps on Next.js and FastAPI.
- Experience with cryptographic systems, packet-level inspection, and secure system design.
- Comfortable at the hardware level too, from embedded C on STM32 boards to a pipelined RISC-V CPU model.

---

### 🚀 Public Projects

- **[AgentOS](https://github.com/anpl1623/AgentOS)** (Rust)  
  A local-first agent runtime for executing AI-driven tasks on your own machine, built around an explicit trust boundary rather than a blanket grant.
  - Capability-scoped permissions, a tamper-evident **audit chain**, and OS keychain credential storage
  - Browser automation and screen control, scoped to the application in the foreground
  - CLI plus a **Tauri** desktop app, cross-platform CI, and [tagged release builds](https://github.com/anpl1623/AgentOS/releases) with SHA-256 checksums for macOS, Linux, and Windows

- **[Sharpline](https://github.com/anpl1623/sharpline)** (Go / TypeScript)  
  A real-time sports odds platform: ingest from a licensed feed, price, and stream live to the browser, all on self-hosted compute. A production-shaped sportsbook _simulation_ — play money only, no wagering, no custody of funds.
  - Six Go services over **Kafka** (KRaft, `franz-go`): ingest, pricer, stream, api, settle, migrate
  - Pricing engine doing devig, no-vig fair value, EV%, Kelly sizing, and arbitrage detection, with property-based tests over the odds math
  - **WebSocket** gateway with snapshot/delta, resync, and per-client backpressure; **Next.js 16** live odds board
  - Double-entry ledger where every stake, payout, and void is two rows summing to zero
  - Postgres + Timescale, Helm and Terraform, integration tests on real containers via `testcontainers-go`
  - The whole stack comes up with one command: `make up`

- **[X Recommendation System](https://github.com/anpl1623/XRECSYSTEM)** (Python / TypeScript)  
  A reimplementation of the X (Twitter) ranking pipeline, built to make feed construction inspectable and tunable.
  - **FastAPI** backend with separate ranking and semantic scoring modules
  - **Next.js** frontend for browsing the feed and adjusting algorithm parameters live
  - Simulation harness that generates synthetic users and posts with **Gemini** or **OpenAI** models

- **[MCP Web Scraper](https://github.com/anpl1623/MCP_WEBSCRAPER)** (Python)  
  An MCP server exposing a `scrape_url` tool that fetches a page, strips navigation and ad clutter, and returns clean text.
  - Runs over stdio transport, drops into any MCP client config

- **[Connect Four on STM32F429i](https://github.com/anpl1623/Connect4-STM32F429i)** (C / Assembly)  
  Connect Four for the STM32F429i Discovery board, written in embedded C with a Makefile and linker script build.

- **[RISC-V Processor](https://github.com/anpl1623/RISCV-PROCESSOR)** (Assembly / C)  
  A cycle-accurate 32-bit RV32I CPU model covering 40 instructions.
  - 5-stage pipeline with **branch prediction**, **hazard detection**, and **data forwarding**

- **[DAO Dashboard](https://github.com/anpl1623/explaining_daos)** (JavaScript)  
  A dashboard comparing decentralized and traditional governance models, live at [daos.andrewpleeter.us](https://daos.andrewpleeter.us).
  - Built with **React.js** and Web3 APIs

---

### 🌍 Open Source Contributions

Patches sent upstream to projects I don't own. Both are **open** and under review — linked so the work can be read, not because they've landed.

- **[git/git#2388](https://github.com/git/git/pull/2388)** — `builtin/whoami: add new 'whoami' command`  
  A new builtin for Git itself, submitted through the standard `Documentation/SubmittingPatches` process.

- **[shiyu-coder/Kronos#393](https://github.com/shiyu-coder/Kronos/pull/393)** — KV cache and cached autoregressive inference  
  Adds a cached decode path to a financial-markets foundation model, with regression tests pinning output equivalence against the uncached path.

---

### 🚧 Current Projects _(Code Not Public Yet)_

- **Social Playlist Media**  
  A social app that lets listeners on any music provider rate, collaborate on, and upvote playlists.
  - Written in **Swift**, independent work, not affiliated with any organization
  - Shipping to TestFlight for demos

---

### 💼 Experience

**Software Engineer, [4URSPACE](https://4urspace.com)** (March 2026 to present, New York, NY)

- Designed and shipped the Location/Projects Map, a geospatial dashboard with a filterable data grid and team-configurable pins, now the default landing experience for enterprise accounts
- Implemented FIDO2/WebAuthn passkey authentication across web and mobile on **AWS Cognito**, adding a passwordless login path alongside the existing auth flows
- Built an ETL pipeline integrating **ServiceNow** and **Autodesk Construction Cloud**, mapping vendor-specific schemas into the 4URSPACE data model for an enterprise client
- Built in-app photo markup for punch lists, so field users can shoot or upload a photo and annotate it with freehand drawing, shapes, and text
- Cut roughly 300KB gzipped from the initial bundle by tracing a runtime-branched static import and converting it to lazy loading

**Founding Software Engineer, [Monovalley](https://monovalley.co)** (May 2025 to March 2026, Scottsdale, AZ)

- Built and shipped Monovalley's site as founding engineer, authoring 167 of 184 commits across **Next.js**, **TypeScript**, and **MySQL** via **Prisma**
- Designed a schema-driven survey engine of sections, typed questions, and submissions, absorbing peaks of 500 weekly responses, with restrict-on-delete preserving answers as questions change
- Built role-based admin on **NextAuth** JWT sessions with bcrypt credentials, plus a session-guarded results endpoint exporting long-format CSV

**Full Stack Developer Intern, [Fyndme](https://fyndme.net)** (May 2025 to September 2025, Elmont, NY)

- Shipped a serverless social graph on **Azure Functions**, eight HTTP endpoints spanning follow and unfollow, follower and following lists, and the full connection request lifecycle
- Designed the portfolio repository layer with injected models, conflict detection on duplicate titles, no-op updates, and status-based soft deletes, backed by functional tests
- More on the company at [FindMe on LinkedIn](https://www.linkedin.com/company/findmeee)

---

### 🎓 Education

**University of Colorado Boulder** (August 2021 to May 2025, Boulder, CO)  
Bachelor's degree in Computer Science, minors in Computer Engineering and Business

---

### 📚 Tech Stack

```text
Languages:   Go • Rust • TypeScript • JavaScript • Python • Swift • C • C++ • SQL • Scala • Assembly • Bash
Frameworks:  React • React Native • Next.js • Vite • Node.js • Express • FastAPI • Tauri • TailwindCSS
Data:        Postgres • TimescaleDB • MySQL • MongoDB • Redis • Prisma ORM
Streaming:   Apache Kafka • WebSocket
Infra:       Docker • Kubernetes • Helm • Terraform • GitHub Actions • Caddy
Cloud:       AWS (Cognito, Lambda, S3) • Azure (Functions, Blob Storage) • Vercel
Systems:     Linux CLI • Git • MCP • STM32
```
