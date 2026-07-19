<p align="center"> <img src="https://capsule-render.vercel.app/api?type=waving&color=58A6FF&height=200&section=header&text=CoderGogh&fontSize=50&fontColor=ffffff"/> </p>

<p align="center">
  <img src="./typing-cursor.svg" width="500" height="160" alt="Backend Engineer / Kafka + Spring Batch / Elasticsearch + Data Pipelines">
</p>

---

## About

**Hi there👋🏻, I'm Haram Jeong — Backend Developer.**<br>
I build data-intensive backend systems: batch pipelines, event-driven messaging, and search infrastructure.

I've led three projects end-to-end, usually owning the data flow design, recovery logic, and failure handling — not just the feature itself:

- **Settlement batch** — Kafka-based pipeline handling 5M+ daily transactions
- **AI-assisted CRM** — consultation search & analytics system
- **EON** — geospatial EV charging platform built on PostGIS

| | |
|:---|:---|
| <img src="https://skillicons.dev/icons?i=kafka" width="22" /> &nbsp;**Messaging & Batch** | Kafka, Spring Batch, chunk processing, DLQ/retry design |
| <img src="https://skillicons.dev/icons?i=elasticsearch" width="22" /> &nbsp;**Search & Data** | Elasticsearch, MongoDB, CQRS, denormalized storage |
| <img src="https://skillicons.dev/icons?i=spring" width="22" /> &nbsp;**Backend** | Java, Spring Boot, FastAPI, PostgreSQL/PostGIS |
| <img src="https://skillicons.dev/icons?i=docker" width="22" /> &nbsp;**Ops** | Redis caching, Docker, Grafana monitoring |

---

## Stack

<table>
  <tr>
    <td><b>Backend</b></td>
    <td>
      <img src="https://skillicons.dev/icons?i=java" />
      <img src="https://skillicons.dev/icons?i=spring" />
      <img src="https://skillicons.dev/icons?i=hibernate" />
      <img src="https://skillicons.dev/icons?i=kafka" />
    </td>
  </tr>
  <tr>
    <td><b>Data</b></td>
    <td>
      <img src="https://skillicons.dev/icons?i=mysql" />
      <img src="https://skillicons.dev/icons?i=postgres" />
      <img src="https://skillicons.dev/icons?i=mongodb" />
      <img src="https://skillicons.dev/icons?i=redis" />
      <img src="https://skillicons.dev/icons?i=elasticsearch" />
    </td>
  </tr>
  <tr>
    <td><b>Infra</b></td>
    <td>
      <img src="https://skillicons.dev/icons?i=docker" />
      <img src="https://skillicons.dev/icons?i=aws" />
      <img src="https://skillicons.dev/icons?i=gcp" />
    </td>
  </tr>
  <tr>
    <td><b>AI/ML</b></td>
    <td>
      <img src="https://skillicons.dev/icons?i=python" />
      <img src="https://skillicons.dev/icons?i=pytorch" />
    </td>
  </tr>
</table>

---

## Main Projects

### Async Settlement System
#### *Kafka & Spring Batch settlement platform · 2026.01 · 3 weeks · Batch team lead*

Settlement batch and message delivery for 1M users / 5M+ usage records, built as one controlled pipeline instead of a simple data transfer. Settlement and delivery are split into separate modules connected asynchronously through Kafka.

- Chunk-based (Reader-Processor-Writer) processing to avoid OOM and connection exhaustion on large batches
- Manual ack commit (`AckMode.MANUAL_IMMEDIATE`) instead of auto-commit, to stop silent failures during consumer rebalancing — settlement data loss rate: 0%
- Failed messages retry up to 3 times, then move to a DLQ for manual review
- JDBC bulk insert for the settlement writer step — write time cut by ~50%
- Settlement/delivery progress tracked via Spring Batch meta tables for near real-time bottleneck visibility

<p>
  <img src="https://skillicons.dev/icons?i=java" width="32" style="margin-right:6px" />
  <img src="https://skillicons.dev/icons?i=spring" width="32" style="margin-right:6px" />
  <img src="https://skillicons.dev/icons?i=kafka" width="32" style="margin-right:6px" />
  <img src="https://skillicons.dev/icons?i=mysql" width="32" style="margin-right:6px" />
  <img src="https://skillicons.dev/icons?i=redis" width="32" style="margin-right:6px" />
  <img src="https://skillicons.dev/icons?i=docker" width="32" style="margin-right:6px" />
  <img src="https://skillicons.dev/icons?i=gcp" width="32" />
</p>

[repo →](https://github.com/CoderGogh/async-settlement-system)

---

### AI-based CRM
#### *AI-assisted consultation record platform · 2026.02–2026.03 · 7 weeks · Team lead, search & AI summary*

Consultation logs are summarized automatically via the Gemini API, then split into read/write paths (CQRS) so the stored data stays reusable for analysis, not just archived. Long, inconsistent-format transcripts are chunked before indexing to keep search relevant.

- CQRS split: writes go through summarization/storage, reads go through Elasticsearch
- Elasticsearch full-text search with N-gram analyzer for autocomplete/suggestions
- Denormalized document storage in MongoDB to avoid join overhead on combined queries
- External Gemini API calls decoupled from internal storage/query flow, so API latency doesn't propagate
- Result: search response time improved ~300%, infra cost reduced ~25%

<p>
  <img src="https://skillicons.dev/icons?i=java" width="32" style="margin-right:6px" />
  <img src="https://skillicons.dev/icons?i=spring" width="32" style="margin-right:6px" />
  <img src="https://skillicons.dev/icons?i=elasticsearch" width="32" style="margin-right:6px" />
  <img src="https://skillicons.dev/icons?i=mongodb" width="32" style="margin-right:6px" />
  <img src="https://skillicons.dev/icons?i=redis" width="32" style="margin-right:6px" />
  <img src="https://skillicons.dev/icons?i=kafka" width="32" style="margin-right:10px" />
  <img src="https://img.shields.io/badge/Gemini_API-8E75B2?style=for-the-badge&logo=googlegemini&logoColor=white" height="26" />
</p>

[repo →](https://github.com/4Ureca)

---

### EON — EV Charging Info System
#### *EV subsidy & charging station platform · 2025.08–2025.10 · 9 weeks · Sole backend*

Unifies scattered regional EV subsidy data and real-time charging station status into one service, so users can check an actual purchase price and nearby chargers in one place.

- FastAPI async I/O for concurrent subsidy calculations across regions/trims
- PostGIS spatial queries (`ST_DWithin` + GiST index) with a dynamic radius correction (±10%) to fix a boundary bug where edge-of-radius stations were missing — missing-station rate: 0%
- Redis caching layer for repeated KEPCO API lookups — response time and throughput improved ~6x
- API contract auto-documented via FastAPI's OpenAPI/Swagger UI to keep frontend/backend in sync

<p>
  <img src="https://skillicons.dev/icons?i=python" width="32" style="margin-right:6px" />
  <img src="https://skillicons.dev/icons?i=fastapi" width="32" style="margin-right:6px" />
  <img src="https://skillicons.dev/icons?i=postgres" width="32" style="margin-right:6px" />
  <img src="https://skillicons.dev/icons?i=redis" width="32" style="margin-right:6px" />
  <img src="https://skillicons.dev/icons?i=docker" width="32" style="margin-right:10px" />
  <img src="https://img.shields.io/badge/Poetry-60A5FA?style=for-the-badge&logo=poetry&logoColor=white" height="26" style="margin-right:6px" />
  <img src="https://img.shields.io/badge/Alembic-DBAB09?style=for-the-badge" height="26" />
</p>

[frontend →](https://github.com/CoderGogh/Eon-FrontEnd-Server) · [backend →](https://github.com/CoderGogh/Eon-BackEnd-Server)

---

## GitHub Stats

<table align="center">
  <tr>
    <td align="center" style="border: none;">
      <img src="https://github-stats-alpha.vercel.app/api?username=CoderGogh&cc=22272e&tc=79c0ff&ic=79c0ff&bc=00000000" alt="GitHub Stats" height="170" />
    </td>
    <td align="center" style="border: none;">
      <img src="https://github-readme-streak-stats.herokuapp.com/?user=CoderGogh&background=22272e&currStreakNum=79c0ff&sideNums=79c0ff&sideLabels=79c0ff&dates=79c0ff&fire=79c0ff&stroke=00000000&hide_border=true" alt="GitHub Streak" height="170" />
    </td>
  </tr>
</table>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=CoderGogh&theme=tokyo-night&hide_border=true" alt="Activity Graph" />
</p>

![Metrics](./github-metrics.svg)
