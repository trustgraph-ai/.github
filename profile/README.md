<div align="center">

<img src="./TG-fullname-logo.svg" width=100% />

[![PyPI version](https://img.shields.io/pypi/v/trustgraph.svg)](https://pypi.org/project/trustgraph/) ![E2E Tests](https://github.com/trustgraph-ai/trustgraph/actions/workflows/release.yaml/badge.svg)
[![Discord](https://img.shields.io/discord/1251652173201149994
)](https://discord.gg/sQMwkRz5GX) [![Ask DeepWiki](https://deepwiki.com/badge.svg)](https://deepwiki.com/trustgraph-ai/trustgraph)

[**Website**](https://trustgraph.ai) | [**Docs**](https://docs.trustgraph.ai) | [**YouTube**](https://www.youtube.com/@TrustGraphAI?sub_confirmation=1) | [**Configuration Builder**](https://config-ui.demo.trustgraph.ai/) | [**Discord**](https://discord.gg/sQMwkRz5GX) | [**Blog**](https://blog.trustgraph.ai/subscribe)

</div>

# The Context Operating System for AI Apps

TrustGraph is an **open-source Context Operating System** that enables organizations to **build, manage, and deploy intelligent context graphs**. Transform fragmented enterprise data into AI-optimized knowledge structures that power accurate, trustworthy AI agents.

Instead of relying on generic RAG solutions or proprietary black boxes, TrustGraph gives you a complete platform to:

- **Build Context Graphs** — Automatically extract entities, relationships, and knowledge structures from your enterprise data
- **Manage Context** — Organize, version, and govern your knowledge graphs with enterprise-grade tools
- **Deploy Intelligent Agents** — Run AI agents grounded in your own precise context with full visibility and control
- **Maintain Full Sovereignty** — Keep your data and AI stack entirely under your control, deployed on-prem, in the cloud, or on bare metal

---

## Why TrustGraph?

### Reduced Hallucinations, Higher Accuracy

Ground your AI with contextually rich intelligence built from your own data. TrustGraph's knowledge graphs provide precise context that dramatically reduces hallucinations and improves response accuracy.

### Full Stack Privacy

Deploy the entire TrustGraph platform—including your sensitive knowledge graphs and data—wherever you choose: on-premises, private cloud, public cloud, or bare metal. You maintain ultimate control over your data and AI infrastructure.

### Enterprise-Grade Context Engineering

Automatically build knowledge graphs with **ontology-driven construction**, **hybrid retrieval** combining vector and graph search, and **structured data processing** for seamless integration of XML, JSON, and CSV data from across your enterprise.

## 🏗️ Key Capabilities

### Context Graph Construction

- **Automated Entity & Relationship Extraction** — AI-powered agents automatically identify key concepts and connections in your data
- **Ontology-Driven Graphs** — Define what *should* be extracted, not just what *can* be extracted, for consistent, controlled knowledge representation
- **Multi-Format Data Support** — Process PDFs, documents, databases, APIs, and structured data sources simultaneously
- **Vector Embedding Integration** — Automatic semantic embeddings mapped to graph relationships for hybrid retrieval

### Context Management

- **Context Cores** — Package and version your processed context for reuse across projects and deployments
- **Collections** — Organize knowledge by domain, project, or dataset with enterprise governance controls
- **Flow Configuration** — Design flexible data processing pipelines with runtime control and prompt management
- **Observability & Telemetry** — Monitor processing status, costs, performance, and agent behavior in real-time

### Agent Intelligence

- **GraphRAG Queries** — Intelligent retrieval combining graph structure and semantic search for deep contextual understanding
- **Agentic Workflows** — Build sophisticated agents that understand relationships, perform reasoning, and make decisions based on your knowledge
- **Model Context Protocol (MCP)** — Connect agents to external tools, APIs, and services while maintaining grounded context
- **Multi-Model Support** — Deploy local open-source models or connect to Anthropic, OpenAI, Google, Mistral, and other LLM providers

### Enterprise Infrastructure

- **Production Deployment** — Kubernetes-native, fully containerized, ready for enterprise scale
- **Cost Observability** — Real-time tracking of token usage, inference costs, and resource consumption
- **Access Controls & Secrets Management** — Enterprise security with fine-grained permissions and credential handling
- **Flexible Storage** — Graph databases (Neo4j, Cassandra, Memgraph), vector stores (Qdrant, Pinecone, Milvus), and support for structured data

## 🔌 Integrations

TrustGraph connects seamlessly with your existing enterprise stack:

### LLM Providers
Anthropic Claude • OpenAI • Google AI Studio • Google VertexAI • Mistral • Cohere • AWS Bedrock • Azure OpenAI

### Local Model Orchestration
Ollama • LM Studio • vLLM • Hugging Face TGI • Llamafiles

### Vector Databases
Qdrant • Pinecone • Milvus • Chroma • Weaviate

### Graph Storage
Neo4j • Apache Cassandra • Memgraph • FalkorDB • ArangoDB

### Cloud Platforms
AWS • Azure • Google Cloud • OVHcloud • Scaleway • Intel Tiber Cloud

### Observability & Monitoring
Prometheus • Grafana

### External Tools & Services
Model Context Protocol (MCP) for seamless agent integration with external APIs and tools

## 🏛️ Platform Architecture

TrustGraph is built on a modular, microservices architecture designed for enterprise scale:

```
┌─────────────────────────────────────────────────────────────┐
│        Enterprise Data Sources & External Services           │
│   (Documents, Databases, APIs, LLMs, Enterprise Systems)    │
└────────────────────────┬────────────────────────────────────┘
                         │ API Gateway
┌────────────────────────┴────────────────────────────────────┐
│                    TrustGraph Platform                       │
├───────────────────────────────────────────────────────────────┤
│                                                               │
│  Context Graph Construction        Agent Intelligence        │
│  • Data Ingestion & Librarian      • GraphRAG Engine         │
│  • Entity & Relationship Extract   • Agentic Workflows       │
│  • Ontology-Driven Graphs          • MCP Integration         │
│  • Knowledge Core Management       • Agent Orchestration     │
│                                                               │
│  Context Knowledge Layer                                      │
│  • Knowledge Graph Storage (Neo4j, Cassandra, etc.)          │
│  • Vector Embeddings (Qdrant, Pinecone, etc.)               │
│  • Structured Data Stores                                     │
│                                                               │
│  Model Serving & Orchestration                               │
│  • LLM Deployment (Local & API)    • Cost Observability      │
│  • Embeddings Models               • Real-time Monitoring    │
│  • OCR & Document Processing       • Access Controls         │
│                                                               │
│  Infrastructure & Control Plane                              │
│  • Apache Pulsar (Event Streaming) • Secrets Management      │
│  • Flow Configuration              • Observability & Logging │
│  • Prompt Management               • Hardware Resource Mgmt  │
│                                                               │
└───────────────────────────────────────────────────────────────┘
```

## 📚 Resources

| Resource | Link |
|----------|------|
| **Official Website** | [trustgraph.ai](https://trustgraph.ai) |
| **Documentation** | [docs.trustgraph.ai](https://docs.trustgraph.ai) |
| **Configuration Builder** | [Build Your Deployment](https://trustgraph.ai/builder) |
| **YouTube Channel** | [@trustgraph](https://youtube.com/@trustgraph) |
| **Discord Community** | [Join the Community](https://discord.gg/trustgraph) |
| **Blog** | [Latest News & Tutorials](https://trustgraph.ai/blog) |
| **GitHub Issues** | [Report Bugs & Request Features](https://github.com/trustgraph-ai/trustgraph/issues) |
| **GitHub Discussions** | [Ask Questions & Share Ideas](https://github.com/trustgraph-ai/trustgraph/discussions) |

---

## 📄 License

TrustGraph is licensed under the **Apache License 2.0**. See [LICENSE](https://github.com/trustgraph-ai/trustgraph/blob/main/LICENSE) for details.

```
Copyright 2024-2025 TrustGraph

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```

---

## 🤝 Support & Community

- **💬 Have Questions?** [Join our Discord](https://discord.gg/trustgraph)
- **🐛 Found a Bug?** [Open an issue](https://github.com/trustgraph-ai/trustgraph/issues)
- **📖 Need Help?** [Check the documentation](https://docs.trustgraph.ai)
- **🤓 Want to Discuss?** [Start a discussion](https://github.com/trustgraph-ai/trustgraph/discussions)
- **🤝 Ready to Contribute?** [See the contributing guide](CONTRIBUTING.md)

