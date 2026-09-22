<div align="center">

<img src="../TG-fullname-logo.svg" width=100% />

[**Website**](https://trustgraph.ai) | [**Docs**](https://docs.trustgraph.ai) | [**YouTube**](https://www.youtube.com/@TrustGraphAI?sub_confirmation=1) | [**Launch TrustGraph**](https://config-ui.demo.trustgraph.ai/) | [**Discord**](https://discord.gg/sQMwkRz5GX) | [**Blog**](https://blog.trustgraph.ai/subscribe)

# The Semantic Intelligence Layer

</div>


[TrustGraph](https://trustgraph.ai) is an open-source Semantic Intelligence Layer. It transforms raw, unstructured data into formally defined, ontology-grounded knowledge making that knowledge retrieval-ready with natural language, fully traceable, and portable across any standards-compliant system.

AI applications fail without shared, unambiguous semantics. LLMs and agents operating on vector proximity across isolated text chunks can hallucinate, lose provenance, and produce non-deterministic outcomes. TrustGraph is the missing layer, a semantic substrate where every fact is typed, every relationship is defined, every agent action is traced back to its source knowledge stored in standards-compliant interoperable formats.

## The Problem: "Common Semantic Understanding"
To understand why AI struggles in complex use cases, consider Abbott and Costello’s classic ["Who's on First?"](https://www.youtube.com/watch?v=sYOUFGfK4bU) routine.

Abbott explains the baseball lineup: `Who` is on first base, `What` is on second base, and `I Don't Know` is on third base. Costello is driven mad because he assumes Abbott is asking questions rather than stating the names of the players: `Who`, `What`, and `I Don't Know`.

Two agents cannot communicate if they do not share the same context understanding.

## Why Vector Embeddings and Keyword Search Fail Here
If you feed this scenario into a standard RAG pipeline using vector embeddings or keyword search, it breaks completely.

If a user asks: "*Who is playing on first base?*"

1. The vector database converts the query into an embedding.
2. Cosine similarity searches for vectors close to "playing," "first base," and "who."
3. Because "Who" is a common pronoun, the embedding space maps it to general inquiries about identity, not the specific name of a baseball player.
4. The LLM retrieves irrelevant documents and hallucinates, failing to understand that "Who" is an entity (a Person), not a question.

Cosine similarity operates on fuzzy, statistical probability. It cannot distinguish between the linguistic usage of a word as a pronoun and its usage as a proper noun within a specific, localized context.

## The Semantic Intelligence Layer
A semantic intelligence layer built using standards like RDF and OWL, establishes explicit, unambiguous semantics. It doesn't rely on "guessing" based on word proximity; it relies on defined relationships.

Here is the "Who's on First" routine modeled in RDF with an OWL ontology. By structuring data this way, the LLM knows exactly what "Who" means in this context:

```turtle
@prefix : <http://trustgraph.ai/baseball#> .
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .
@prefix owl: <http://www.w3.org/2002/07/owl#> .

# Ontology Classes
:Player a owl:Class ;
    rdfs:subClassOf owl:Thing .

:BaseballPosition a owl:Class .

# Object Properties
:playsPosition a owl:ObjectProperty ;
    rdfs:domain :Player ;
    rdfs:range :BaseballPosition .

# Data (The Context)
:Who a :Player ;
    rdfs:label "Who" .

:What a :Player ;
    rdfs:label "What" .

:IDontKnow a :Player ;
    rdfs:label "I Don't Know" .

:FirstBase a :BaseballPosition ;
    rdfs:label "First Base" .

:SecondBase a :BaseballPosition ;
    rdfs:label "Second Base" .

:ThirdBase a :BaseballPosition ;
    rdfs:label "Third Base" .

# The Explicit Relationships
:Who :playsPosition :FirstBase .
:What :playsPosition :SecondBase .
:IDontKnow :playsPosition :ThirdBase .
```

When an agent queries the TrustGraph semantic intelligence layer, it uses SPARQL or GraphRAG to traverse these explicit paths. The agent knows that `:Who` is a `:Player` whose `:playsPosition` is `:FirstBase`. Hallucination is eliminated because context is structured, not inferred via probability.

## Core Components
- **Semantic Intelligence Layer** — An RDF 1.2‑compliant named graph system with automated natural language retrieval, semantic filtering, and reranking, so queries return grounded, contextually relevant answers rather than raw search hits.
- **Semantic Compliance** — Native support for OWL ontologies, enabling formal class hierarchies, property constraints, and logical inference over your knowledge graph.
- **Agent Runtime** — Bring your own agent framework and integrate via the TrustGraph API Gateway, or use the native TrustGraph Agent Runtime, which traces all agent behavior and links every decision back to its source semantic intelligence with full provenance.
- **Semantic Intelligence Management** — Workspaces, Collections, Flows, and Knowledge Cores give you multiple independent degrees of freedom for isolating, accessing, and versioning semantic knowledge over time.
- **Semantic Interoperability** — Built on open standards (RDF 1.2, OWL, PROV-O), TrustGraph stores intelligence in interoperable serializations like Turtle that can be exported or migrated to any RDF-compliant system.
- **Unstructured Data Ingest** — Converts PDF, DOCX, XLSX, PPTX, HTML, Markdown, CSVs, and images into structured semantic intelligence.
- **Full LLM Inference Stack** — Connect to all major LLM provider APIs, or self-host open-weight models on Nvidia, AMD, or Intel hardware.

## TrustGraph vs. Conventional Graph Systems
| Dimension                      | TrustGraph                                                                                                                       | Conventional Graph Databases (e.g., Neo4j)                                                             |
| ------------------------------ | -------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| Primary purpose                | Semantic Intelligence Layer purpose-built for AI: make knowledge unambiguous, traceable, and retrieval-ready for LLMs and agents | General-purpose property graph database for transactional workloads and graph analytics                |
| Data model                     | RDF 1.2 named graphs (quads) with reification — statements are first-class, addressable resources enabling n-ary relationships   | Labeled property graph — nodes and edges with key-value properties; no native statement reification    |
| Semantic rigor                 | OWL ontology enforcement: typed entities and properties with formally defined meaning                                            | Schema-optional; semantics live in application code or conventions, not the data model                 |
| Provenance                     | Built-in, standards-based (W3C PROV-O); extraction lineage, query traces, and agent behavior stored as queryable graph triples   | Not native; provenance must be hand-modeled as ordinary nodes/edges with no standard vocabulary        |
| Natural language retrieval     | Automated NL-to-graph retrieval with semantic filtering and reranking                                                            | Requires manual Cypher queries or add-on vector search with no semantic grounding                      |
| Agent integration              | Native Agent Runtime with full behavioral tracing linked to source intelligence, plus API Gateway for bring-your-own-framework   | None; agents access the graph as an external data source with no behavioral traceability               |
| Knowledge lifecycle management | Workspaces, Collections, Flows, and Knowledge Cores for isolation, access control, and versioning of semantic intelligence       | Database-level separation only; versioning and lifecycle management are application concerns           |
| Unstructured data ingest       | Integrated pipeline converts PDF, DOCX, XLSX, PPTX, HTML, Markdown, CSV, and images into ontology-typed knowledge                | Not included; requires external ETL and custom extraction pipelines                                    |
| LLM stack                      | Full inference stack: all major provider APIs or self-hosted open-weight models on Nvidia, AMD, or Intel                         | None; LLM integration is entirely external                                                             |
| Interoperability               | Open standards throughout (RDF 1.2, OWL, PROV-O); exports to Turtle portable to any RDF-compliant system                         | Proprietary property graph model; Cypher is not a W3C standard; migration requires data transformation |
| Query paradigm                 | SPARQL + semantic graph patterns with automated natural language access                                                          | Cypher / GQL pattern matching requiring graph expertise                                                |
          
## No API Keys Required

How many times have you cloned a repo and opened the `.env.example` to see the dozens of API keys for 3rd party dependencies needed to make the services work? There are only 3 things in TrustGraph that might need an API key:

- 3rd party LLM services like Anthropic, Cohere, Gemini, Mistral, OpenAI, etc.
- 3rd party OCR like Mistral OCR
- The API key *you set* for the TrustGraph API gateway

Everything else is included.
- [x] Managed Multi-model storage in [Cassandra](https://cassandra.apache.org/_/index.html)
- [x] Managed Vector embedding storage in [Qdrant](https://github.com/qdrant/qdrant)
- [x] Managed File and Object storage in [Garage](https://github.com/deuxfleurs-org/garage) (S3 compatible)
- [x] Managed High-speed Pub/Sub messaging fabric with [Pulsar](https://github.com/apache/pulsar) or [RabbitMQ](https://www.rabbitmq.com/)
- [x] Complete LLM inferencing stack for open LLMs with [vLLM](https://github.com/vllm-project/vllm), [TGI](https://github.com/huggingface/text-generation-inference), [Ollama](https://github.com/ollama/ollama), [LM Studio](https://github.com/lmstudio-ai), and [Llamafiles](https://github.com/mozilla-ai/llamafile) 

## Support & Community

- **Have Questions?** [Join our Discord](https://discord.gg/sQMwkRz5GX)
- **Found a Bug?** [Open an issue](https://github.com/trustgraph-ai/trustgraph/issues)
- **Need Help?** [Check the documentation](https://docs.trustgraph.ai)
- **Ready to Contribute?** [See the contributing guide](CONTRIBUTING.md)
