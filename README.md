<div align="center">

# Onyx · AI Knowledge Workspace

### Search documents. Build AI agents. Explore enterprise RAG.

A personal development fork maintained by **[Rohith](https://github.com/rohithpk12)**.

[Explore the code](backend/) · [Development guide](CONTRIBUTING.md) · [Deployment guide](https://docs.onyx.app/deployment/overview) · [Original project](https://github.com/onyx-dot-app/onyx)

</div>

---

## Overview

Onyx connects documents and applications to an AI workspace. It combines document retrieval, chat, research, and custom agents.

This repository is Rohith's fork of Onyx. It provides a base for learning, experiments, and future extensions.

**Current fork changes:** repository presentation and documentation. The application features below come from upstream Onyx. Custom application features and a hosted demo are not yet included.

## Product preview

![Upstream Onyx interface showing document-grounded chat](docs/assets/onyx-chat-use-cases.png)

*Interface preview from the original Onyx project.*

## Core capabilities

| Capability | What it provides |
| --- | --- |
| Document search and RAG | Retrieve relevant content through keyword and vector search. |
| AI chat | Ask questions using connected knowledge and a chosen model provider. |
| Custom agents | Configure instructions, knowledge sources, and external actions. |
| Deep research | Run multi-step research tasks and produce reports. |
| App connectors | Ingest content and permissions from connected applications. |
| Web search and MCP | Add external information and tools to agent workflows. |
| Multiple model providers | Connect hosted models or self-hosted model services. |

Feature availability depends on the edition, configuration, and deployment mode.

## Technology stack

| Layer | Technologies |
| --- | --- |
| Backend | Python, FastAPI, SQLAlchemy, Alembic |
| Web application | Next.js, React, TypeScript, Tailwind CSS |
| Background jobs | Celery |
| Data and storage | PostgreSQL, Redis, MinIO |
| Search | OpenSearch keyword and vector index |
| Model integration | LangChain, LiteLLM, embedding models |
| Deployment | Docker Compose, Kubernetes, Helm, Terraform |

## Architecture

The system ingests source documents and prepares them for retrieval. The application uses retrieved context to support model responses.

![Upstream Onyx system architecture](docs/assets/architecture.png)

*Architecture illustration from upstream Onyx. Services vary by deployment mode.*

## Explore the repository

| Directory | Purpose |
| --- | --- |
| [backend/](backend/) | API, retrieval logic, model services, and background workers |
| [web/](web/) | Web interface |
| [deployment/](deployment/) | Deployment configuration |
| [docs/](docs/) | Technical documentation and assets |
| [examples/](examples/) | Integration examples |
| [desktop/](desktop/) | Desktop application |
| [mobile/](mobile/) | Mobile application |

## Get started

Clone this fork:


```bash
git clone https://github.com/rohithpk12/onyx.git
cd onyx
```

Then choose a setup path:

| Goal | Guide |
| --- | --- |
| Run the application with Docker | [Docker instructions](CONTRIBUTING.md#running-in-docker) |
| Edit and run the source | [Development setup](CONTRIBUTING.md#development-setup) |
| Configure a hosted deployment | [Deployment documentation](https://docs.onyx.app/deployment/overview) |

Source development uses Python 3.13, uv, Bun, and Docker. Follow the linked guide for service configuration and model setup.

**Standard mode** includes document indexing and RAG services. **Lite mode** supports a smaller chat-focused setup without document indexing.

Model and search providers can require API keys and usage fees. Keep credentials outside version control.

## Possible next extensions

These are ideas for future work, not completed features:

- A financial-document workspace with public sample documents.
- A retrieval evaluation set with repeatable accuracy checks.
- A dashboard for response latency and model usage.
- A recorded walkthrough of a configured deployment.

## Attribution and license

This fork is based on **[Onyx](https://github.com/onyx-dot-app/onyx)**, originally developed by DanswerAI, Inc. and its contributors.

Community code is covered by the MIT license, subject to the repository's license terms. Code under `ee` directories has separate Onyx Enterprise License terms. Third-party components retain their original licenses.

See [LICENSE](LICENSE) for the full scope and notices. Original copyright notices and source history remain intact.

---

<div align="center">

Maintained as a personal development fork by [Rohith](https://github.com/rohithpk12).

</div>
