<div align="center">

<img src="TG-fullname-logo.svg" width=100% />

[![PyPI version](https://img.shields.io/pypi/v/trustgraph.svg)](https://pypi.org/project/trustgraph/) ![E2E Tests](https://github.com/trustgraph-ai/trustgraph/actions/workflows/release.yaml/badge.svg)
[![Discord](https://img.shields.io/discord/1251652173201149994
)](https://discord.gg/sQMwkRz5GX) [![Ask DeepWiki](https://deepwiki.com/badge.svg)](https://deepwiki.com/trustgraph-ai/trustgraph)

[**Website**](https://trustgraph.ai) | [**Docs**](https://docs.trustgraph.ai) | [**YouTube**](https://www.youtube.com/@TrustGraphAI?sub_confirmation=1) | [**Configuration Builder**](https://config-ui.demo.trustgraph.ai/) | [**Discord**](https://discord.gg/sQMwkRz5GX) | [**Blog**](https://blog.trustgraph.ai/subscribe)

</div>

# The Context Operating System for AI Apps
---

## About TrustGraph

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

---

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

---

## 🚀 Getting Started

### Deploy TrustGraph in Minutes

```bash
# Clone the repository
git clone https://github.com/trustgraph-ai/trustgraph.git
cd trustgraph

# Use the Configuration Builder for your deployment
# Visit: https://trustgraph.ai/builder

# Deploy locally with Docker Compose
docker compose up -d
```

### Access the Workbench

Once deployed, the **TrustGraph Workbench** is available at `http://localhost:8888`:

- **Load & Manage Data** — Add documents and manage knowledge
- **Design Flows** — Create processing pipelines and configure how data becomes knowledge
- **Build Agents** — Test agents and GraphRAG queries
- **Monitor Progress** — Track processing status and system performance
- **Manage Ontologies** — Define custom ontologies for structured knowledge extraction

### Learn & Explore

- **[Quickstart Guide](https://docs.trustgraph.ai/getting-started/quickstart.html)** — Get running in 5 minutes
- **[Core Concepts](https://docs.trustgraph.ai/getting-started/concepts.html)** — Understand knowledge graphs, GraphRAG, and vectors
- **[Architecture Guide](https://docs.trustgraph.ai/overview/architecture.html)** — Deep dive into system design
- **[Configuration Builder](https://trustgraph.ai/builder)** — Visually assemble your deployment
- **[Example Notebooks](https://github.com/trustgraph-ai/trustgraph-examples)** — Real-world use cases
- **[API Documentation](https://docs.trustgraph.ai)** — CLI, REST APIs, and SDK reference

---

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

---

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

---

## 💡 Use Cases

### Enterprise Data Integration & Knowledge Management
Connect fragmented data silos—databases, documents, APIs—and transform them into a unified knowledge graph that powers accurate AI systems.

### Agentic RAG at Enterprise Scale
Deploy sophisticated agents that perform deep contextual reasoning across your knowledge graphs, reducing hallucinations and providing grounded answers.

### Intelligent Document Processing
Automatically extract structured information from diverse document types (PDFs, emails, reports) and build searchable knowledge graphs.

### Fleet & Logistics Intelligence
Process vehicle telematics, maintenance records, and operational data into actionable insights with knowledge graphs that understand relationships and context.

### Compliance & Audit Intelligence
Maintain complete control and transparency over how enterprise data is processed and used by AI systems, with full audit trails and access controls.

### Customer & Product Intelligence
Build knowledge graphs from customer data, product information, and market intelligence to power personalized AI experiences.

---

## 🛠️ For Developers

### Key Repositories

| Repository | Purpose |
|-----------|---------|
| **[trustgraph](https://github.com/trustgraph-ai/trustgraph)** | Core platform codebase |
| **[trustgraph-docs](https://github.com/trustgraph-ai/trustgraph-docs)** | Documentation and guides |
| **[trustgraph-examples](https://github.com/trustgraph-ai/trustgraph-examples)** | Example projects and notebooks |
| **[mcp-servers](https://github.com/trustgraph-ai/mcp-servers)** | Model Context Protocol integrations |


### Contributing

We welcome contributions from developers, data engineers, and researchers:

1. **[Read the Contributing Guide](https://github.com/trustgraph-ai/trustgraph/blob/main/CONTRIBUTING.md)** — Guidelines and process
2. **[Check Open Issues](https://github.com/trustgraph-ai/trustgraph/issues)** — Find opportunities to contribute
3. **[Join the Discord](https://discord.gg/trustgraph)** — Discuss ideas with the community
4. **[Submit a PR](https://github.com/trustgraph-ai/trustgraph/pulls)** — Contribute improvements

---

## 📊 Community & Stats

- **⭐ 632 Stars** — Growing community of data engineers and AI practitioners
- **📦 50 Forks** — Actively extended and customized by organizations
- **🌐 Open Source** — Apache 2.0 licensed, no vendor lock-in
- **💬 Active Community** — Discord, GitHub discussions, and regular updates

---

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

## 🔐 Security & Enterprise Readiness

- **Data Sovereignty** — Complete control over where your data lives and how it's processed
- **Open Source Transparency** — Audit every component; no hidden algorithms or proprietary black boxes
- **Enterprise Authentication** — MCP authentication, access controls, and secrets management
- **Production Ready** — Kubernetes-native, horizontally scalable, built for mission-critical workloads
- **Compliance Support** — Full audit logging, data governance, and transparency for regulatory requirements

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

---

**Built by data engineers, for data engineers. Transform your data into intelligent context.**

[Get Started](https://docs.trustgraph.ai/getting-started/quickstart.html) • [Explore Examples](https://github.com/trustgraph-ai/trustgraph-examples) • [Join the Community](https://discord.gg/trustgraph)
