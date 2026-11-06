<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:512BD4,100:0078D4&height=180&section=header&text=Faysil%20Alshareef&fontSize=46&fontColor=ffffff&animation=fadeIn&fontAlignY=36&desc=Senior%20.NET%20Backend%20Engineer&descAlignY=56&descSize=18" alt="Faysil Alshareef" width="100%" />

<a href="https://github.com/FaysilAlshareef">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&pause=1200&color=512BD4&center=true&vCenter=true&width=620&lines=Event+Sourcing+%C2%B7+CQRS+%C2%B7+Distributed+Systems;Secure+APIs+for+payments+and+commerce;Systems+at+hundreds+of+millions+of+records;From+requirements+to+production" alt="Typing SVG" />
</a>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/faysil-alshareef-a23978263/)
[![Email](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:faysilalshareef@gmail.com)
[![NuGet](https://img.shields.io/badge/NuGet-Anis.Partners-004880?style=for-the-badge&logo=nuget&logoColor=white)](https://www.nuget.org/packages/Anis.Partners)
[![Profile Views](https://komarev.com/ghpvc/?username=FaysilAlshareef&color=512BD4&style=for-the-badge)](https://github.com/FaysilAlshareef)

📍 **Tripoli, Libya**

</div>

---

## 🧑‍💻 About Me

I'm a **Senior .NET Backend Engineer** at **ANIS**, where I design and run the backend for financial and commerce systems: partner APIs, card sales, payments and reporting at the scale of **hundreds of millions of records**.

I take requirements directly from management, design the system, build it, and run it in production. I also run technical interviews when we hire backend engineers.

<div align="center">

| 🏗️ Design | 🔐 Security | ⚡ Performance | 🤖 AI Engineering |
|:---:|:---:|:---:|:---:|
| Event sourcing, CQRS, DDD | Signed APIs, managed keys | Query and storage redesign | Multi-agent workflows with review gates |

</div>

---

## 🚀 Selected Work

### 🔐 Partner API Platform: Security by Design

The public API that partner companies use to buy cards and move money, built security-first from the design up.

- ✍️ **Signed in both directions.** Partners sign every request. Answers that move money or deliver card codes are signed with [RFC 9421](https://www.rfc-editor.org/rfc/rfc9421) HTTP Message Signatures.
- 🗝️ **Hardware-backed keys** with planned rotation and revocation.
- 🪪 **Key enrollment with proof of possession.** A partner proves it holds its private key before access is granted.
- 👥 **Maker-checker on access.** Narrowing access applies immediately. Widening it needs an approved proposal, and an approval expires if anything changed after it was made.
- 🧾 **Tamper-evident configuration.** Policies are hashed with RFC 8785 canonical JSON, and timestamped evidence is kept for signed answers.
- 🛡️ **Defense in depth.** Network allow-lists, spend limits, rate limits and mandatory idempotency.
- 📦 **Public .NET SDK:** [`Anis.Partners`](https://www.nuget.org/packages/Anis.Partners) on NuGet. Response verification can't be turned off, and tests prove no secret reaches logs or telemetry.

<p>
<img src="https://img.shields.io/badge/.NET%2010-512BD4?style=flat-square&logo=dotnet&logoColor=white" />
<img src="https://img.shields.io/badge/Event%20Sourcing-CQRS-6E40C9?style=flat-square" />
<img src="https://img.shields.io/badge/gRPC-244C5A?style=flat-square&logo=grpc&logoColor=white" />
<img src="https://img.shields.io/badge/RFC%209421-Signatures-2EA44F?style=flat-square" />
</p>

### 📊 Sales Reporting Platform: Azure SQL → PostgreSQL

Redesigned the company's sales reporting databases and moved them from Azure SQL to self-hosted PostgreSQL.

<div align="center">

| Metric | Before | After |
|:---|:---:|:---:|
| 💰 Database cost | Azure SQL | **85%+ lower** |
| 🐢 5-year grouped report | 173 s | **1.8 s** |
| 📤 Deepest export page | 1,266 ms | **55 ms** (23× faster) |

</div>

- Range-partitioned schema, connection pooling, and automated server provisioning.
- A parallel, resumable rebuild over the full sales history.
- Verified record by record against the source before cutover.

<p>
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" />
<img src="https://img.shields.io/badge/pg__partman-336791?style=flat-square" />
<img src="https://img.shields.io/badge/PgBouncer-336791?style=flat-square" />
<img src="https://img.shields.io/badge/Ansible-EE0000?style=flat-square&logo=ansible&logoColor=white" />
</p>

### 💳 Owned Cards: Card Ownership at Scale

Rebuilt customer card ownership as event-sourced **Command / Query / Processor** services over a sales source of hundreds of millions of records.

- Planned database partitioning from real data volumes instead of guessing.
- Designed an ordered producer with hash-routed parallel workers for the full rebuild, tested against crash and resume.
- Made the sale-to-ownership flow safe under concurrency, so no purchased card goes missing.

<p>
<img src="https://img.shields.io/badge/Azure%20Cosmos%20DB-0078D4?style=flat-square&logo=microsoftazure&logoColor=white" />
<img src="https://img.shields.io/badge/SQL%20Server-CC2927?style=flat-square&logo=microsoftsqlserver&logoColor=white" />
<img src="https://img.shields.io/badge/Azure%20Service%20Bus-0078D4?style=flat-square&logo=microsoftazure&logoColor=white" />
</p>

### ⚡ Meter Charging

Electricity meter top-ups, integrated with the national electricity provider.

---

## 📦 Open Source

<div align="center">

| Project | What it is |
|:---|:---|
| 🔐 [**Anis.Partners SDK**](https://github.com/anis-ly/anis.partners-sdk-dotnet) | .NET SDK for the ANIS Partner API: signed requests, verified responses, typed operations |
| 🤖 [**dotnet-ai-kit**](https://github.com/FaysilAlshareef/dotnet-ai-kit) | AI plugin for the full .NET lifecycle: skills, agents and commands |
| 🧪 [**Rig.TUnit**](https://github.com/FaysilAlshareef/Rig.TUnit) | TUnit-first integration-testing rig for SQL, NoSQL, messaging, caching and more |
| 📗 [**ExcelGenerator**](https://github.com/FaysilAlshareef/ExcelGenerator) | Lightweight Excel generation from `IEnumerable` with ClosedXML, used in production |
| 👀 [**claude-workflow-tracker**](https://github.com/FaysilAlshareef/claude-workflow-tracker) | Live viewer for multi-agent Claude workflow runs (ASP.NET Core 10 + Angular) |

</div>

---

## 🛠️ Tech Stack

<div align="center">

### Backend & Architecture
![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=csharp&logoColor=white)
![.NET 10](https://img.shields.io/badge/.NET%2010-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![ASP.NET Core](https://img.shields.io/badge/ASP.NET%20Core-5C2D91?style=for-the-badge&logo=dotnet&logoColor=white)
![gRPC](https://img.shields.io/badge/gRPC-244C5A?style=for-the-badge&logo=grpc&logoColor=white)
![Blazor](https://img.shields.io/badge/Blazor-512BD4?style=for-the-badge&logo=blazor&logoColor=white)
![EF Core](https://img.shields.io/badge/EF%20Core-5C2D91?style=for-the-badge&logo=dotnet&logoColor=white)

### Data & Messaging
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![SQL Server](https://img.shields.io/badge/SQL%20Server-CC2927?style=for-the-badge&logo=microsoftsqlserver&logoColor=white)
![Cosmos DB](https://img.shields.io/badge/Cosmos%20DB-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![Azure Service Bus](https://img.shields.io/badge/Azure%20Service%20Bus-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)

### Cloud & DevOps
![Azure](https://img.shields.io/badge/Azure-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![Ansible](https://img.shields.io/badge/Ansible-EE0000?style=for-the-badge&logo=ansible&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)

### Testing & AI
![TUnit](https://img.shields.io/badge/TUnit-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![Testcontainers](https://img.shields.io/badge/Testcontainers-291A3F?style=for-the-badge&logo=docker&logoColor=white)
![Claude Code](https://img.shields.io/badge/Claude%20Code-D97757?style=for-the-badge&logo=anthropic&logoColor=white)
![Codex](https://img.shields.io/badge/Codex-000000?style=for-the-badge&logo=openai&logoColor=white)

</div>

---

## 🧭 How I Work

<div align="center">

| ✅ Correctness first | 🔍 Root cause, not retries | 🤖 AI with guardrails |
|:---|:---|:---|
| Idempotency, outbox delivery, and data checked against the source before release | A failing test gets a proven cause before it gets a rerun | Multi-agent workflows with Claude Code and Codex behind review, build and test gates. Nothing ships without review. |

</div>

---

## 💼 Experience

| Role | Company | Period |
|:---|:---|:---|
| **Senior Backend Engineer** | ANIS | Jul 2023 – Present |
| **Software Engineer** | Growth Tech | Apr 2023 – Jul 2023 |

🌐 **Arabic** (native) · **English** (professional)

---

<div align="center">

## 📊 GitHub Stats

<img src="https://github-readme-stats.vercel.app/api?username=FaysilAlshareef&show_icons=true&theme=radical&hide_border=true&include_all_commits=true" alt="GitHub Stats" height="170" />
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=FaysilAlshareef&layout=compact&theme=radical&hide_border=true" alt="Top Languages" height="170" />

[![GitHub Streak](https://github-readme-streak-stats.herokuapp.com/?user=FaysilAlshareef&theme=radical&hide_border=true)](https://github.com/FaysilAlshareef)

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0078D4,100:512BD4&height=110&section=footer" width="100%" />

</div>
