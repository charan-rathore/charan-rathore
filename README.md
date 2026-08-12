# Charan Rathore

I investigate how intelligent systems behave underneath the abstraction layer, then build the infrastructure, evaluation, and failure-handling mechanisms around them.

Retrieval, memory, closed-loop prediction, and agent reliability are not black boxes. They are pipelines with measurable failure modes. I treat them that way.

[Portfolio](https://charan-rathore.github.io) · [Substack](https://charanrathore.substack.com) · [Email](mailto:ra7hore.charan@gmail.com)

---

## Currently

**2026**

→ Production RAG systems - hybrid retrieval, evaluation, observability, CI quality gates  
→ Document intelligence and provenance-preserving memory  
→ Closed-loop IoT + forecasting (ground truth → bias → model → feedback)  
→ Agent systems with explicit trust, freshness, and knowledge versioning  
→ Performance and reliability of local inference stacks

---

## Evidence

### [IntelliRAG](https://github.com/charan-rathore/IntelliRAG)
Production-oriented RAG platform built from first principles.

Ingestion with document lifecycle tracking, Celery workers, retries and DLQ, five chunking strategies with benchmarks, dense + keyword + hybrid (RRF) retrieval, cross-encoder reranking, context assembly (dedup / MMR / budget), citation-aware generation, unified evaluation platform, adversarial probes, observability, and CI quality gates.

Benchmarks are reported on a small deterministic corpus (2 documents, golden queries) with mock embeddings/LLM for CI; real Ollama runs are supported and labeled separately. Precision numbers are intentionally not inflated.

Architecture docs and an engineering journal record the trade-offs at each layer.

### [memoRABLE](https://github.com/charan-rathore/memoRABLE)
Document → source-linked memory graph → multi-surface publish.

Preserves semantic structure and provenance while turning a document into six memory blocks (Snapshot, Signals, Timeline, Decisions, Risks, Actions). Local-first by default. Selective OCR / experimental Docling refine only when quality improves. Correctness gates and deterministic behavior are first-class concerns.

Live: [memo-rable.vercel.app](https://memo-rable.vercel.app)

### [ThermoSense](https://github.com/charan-rathore/Time-Series-Temperature-Modelling)
Closed-loop hyperlocal temperature system.

Sensor (or historical) ground truth → commercial API forecasts → learned location-specific bias → ensemble forecasting (SARIMA / LightGBM / TFT) → live accuracy leaderboard against baselines → feedback and retraining. The interesting engineering is the measurement and correction loop, not the models alone.

Live: [thermosense-black.vercel.app](https://thermosense-black.vercel.app)

### [Finsight](https://github.com/charan-rathore/agentic-finance-advisor)
Multi-agent finance research system with an explicit trust layer.

Ingest agents (prices, NAVs, macro, news), analysis agents that maintain versioned knowledge bases, storage with provenance, and a confidence score on every answer derived from data freshness, source agreement, and staleness flags. Not positioned as a black-box advisor.

---

## Writing

[The 2 seconds you never see](https://charanrathore.substack.com/p/the-2-seconds-you-never-see) - on Substack

---

## How I work

- Prefer systems that can be measured and failed in known ways over opaque frameworks.
- Document trade-offs (chunk size vs recall, local vs paid inference, when to invoke an expensive parser).
- Keep evaluation and observability in the same repository as the pipeline.
- Local-first and zero paid API keys when the goal is understanding the stack.

---

## Background

BITS Pilani (MSc Chemistry + BE Mechanical Engineering, class of 2026).  
Former Flipkart intern (Jan-Jun 2026).  
Previously worked across computer vision, quantitative finance experiments, and automated dataset generation; the current focus is the infrastructure under intelligent systems.

---

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=charan-rathore&style=for-the-badge&color=7b68ee&label=Profile+Views" alt="Profile views" />
</p>

*Repositories that no longer represent the main line of work are left public for history but are not highlighted here.*
