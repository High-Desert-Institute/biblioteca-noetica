# Biblioteca Noetica
**The library of intellectual apprehension.**

Biblioteca Noetica is a pre-build blueprint for a multimodal knowledge library that ingests memes, short-form and long-form videos, movies, documentaries, TV episodes, and document corpora (PDFs, academic papers, books). For every source, the system generates structured sidecar artifacts (transcript/OCR text, markdown-normalized text, argument maps, and multi-lens analyses) and uses those artifacts to build a semantic web and wiki of claims, perspectives, evidence, and open questions.

## 1. Core Relationship Between Projects

### Biblioteca Memetica (Current System)

Biblioteca Memetica is a **memetic knowledge system** built around:

* A large corpus of images (memes)
* Rich **sidecar metadata** per artifact
* Locally-run AI pipelines (e.g., SBC-class hardware)
* Multi-perspective analysis layers:

  * Descriptive summaries
  * Feminist critique
  * Marxist critique
  * Foucauldian analysis
* A structured taxonomy (topic category -> content -> sidecars)

It functions as:

> A *semantic library of cultural artifacts* where each item is analyzed across ideological and descriptive dimensions.

---

### Biblioteca Noetica (Proposed System)

The new project extends this paradigm from **static image artifacts -> multimodal media** and from **categorization -> argument mapping + topic synthesis**.

It introduces:

* Time-based media (short-form + long-form video, movies, documentaries, TV)
* Document media (PDF papers, books, reports, essays)
* Transcription and OCR as first-class primitives
* Markdown-normalized text artifacts across media types
* Argument extraction and classification
* Cross-document semantic linking
* Multi-user, opt-in corpus aggregation
* Wiki-like synthesis layer across topics

---

### Relationship Summary

| Dimension  | Biblioteca Memetica         | Biblioteca Noetica                            |
| ---------- | --------------------------- | --------------------------------------------- |
| Media Type | Images (memes)              | Video, film, TV, and document corpora         |
| Core Unit  | Meme                        | Source artifact + sections/segments/arguments |
| Metadata   | Sidecar files               | Unified sidecars + graph nodes                |
| Analysis   | Ideological critique layers | Critique + argument extraction + topic indexing |
| Structure  | Taxonomy                    | Knowledge graph + taxonomy + wiki             |
| Scope      | Individual archive          | Federated, opt-in network                     |
| Output     | Categorized meme library    | Semantic map + topic articles + evidence links |

---

## 2. Conceptual Shift

### From Classification -> Relational Knowledge

Biblioteca Memetica primarily answers:

> "What is this artifact and how can it be categorized?"

The new system answers:

> "What arguments are being made, how do they relate, and where do related arguments appear across the media in the local library?"

---

### From Static Artifacts -> Multimodal + Logical Structures

Memes are often:

* Atomic
* Context-light

Multimodal sources are often:

* Temporal (video/film/TV)
* Long-form textual (papers/books/PDFs)
* Multi-argument
* Context-rich

This requires:

* Segment/chapter/page-level analysis
* OCR + transcription + text normalization
* Argument boundaries
* Temporal and structural indexing

---

## 3. Required New System Components

### 3.0 Semantic RAG and Question Intelligence Layer

A central addition to the project is a **semantic retrieval-augmented generation layer (SemRAG)** that sits on top of the archive, sidecars, argument graph, topic indexes, and topic pages.

This layer enables:

* Chatbots to answer complex user questions grounded in the actual library
* Retrieval across memes, videos, films, TV, documents, transcript/OCR segments, arguments, and synthesized topic pages
* Better navigation of the corpus through natural language queries
* Analytics about what users are asking
* Feedback to creators about missing, emerging, or highly demanded topics
* Explicit artifacts for unresolved questions and low-evidence zones

This is not just a UI convenience. It turns the archive into a **queryable knowledge system**.

#### Core functions

* Accept natural language questions
* Retrieve relevant source material semantically
* Rank evidence from multiple layers:

  * original artifacts
  * transcript/OCR segments
  * markdown-normalized documents
  * extracted arguments
  * topic indexes
  * synthesized topic pages
* Generate grounded answers with explicit source links
* Log and analyze question patterns over time
* Flag unanswered questions and insufficiently covered topics

#### Why this matters

Without SemRAG, the project is primarily a library and graph.
With SemRAG, it becomes an **interactive epistemic interface** that can:

* answer questions
* expose uncertainty
* identify missing coverage
* help contributors understand what the audience is seeking
* produce research backlogs from unresolved questions

#### Creator-facing value

Question analytics can be used to show:

* what people most want explained
* where the corpus is weak or fragmented
* what themes are rapidly becoming salient
* what adjacent topics users repeatedly connect together

This creates a loop:

1. creators publish content
2. the system analyzes and indexes it
3. users ask questions
4. the system observes demand patterns
5. creators use that signal to shape future work

#### Required subcomponents

* Embedding-based retrieval over all indexed objects
* Cross-layer ranking strategy
* Citation / provenance system for answers
* Query logging and aggregation
* Dashboard for creator analytics
* Controls for privacy, opt-in analytics, and corpus boundaries

#### Important design principle

The chatbot should not answer from a generic model memory when the corpus can answer. It should prefer grounded retrieval and make the difference between:

* sourced answer
* inferred synthesis
* insufficient evidence

---

### 3.1 Transcription Pipeline

New foundational layer:

* ASR (e.g., local models)
* OCR/document text extraction
* Speaker segmentation (optional but valuable)
* Timestamp + page/chapter alignment

Outputs:

* Full transcript and/or extracted document text
* Timestamped segments and page/chapter segments
* Markdown-normalized text representation

---

### 3.2 Argument Extraction Layer

Core new capability:

* Identify claims, premises, conclusions
* Classify argument types
* Detect rhetorical strategies

Possible approaches:

* LLM-based structured extraction
* Rule + embedding hybrid

Outputs:

* Argument objects:

  * Claim
  * Supporting evidence
  * Confidence
  * Position (pro/anti/neutral)

---

### 3.3 Semantic Linking Engine

Moves beyond taxonomy into graph structure:

* Embed all artifacts (memes, video segments, document segments, arguments, topic pages)
* Compute semantic similarity plus support/contradiction relationships
* Link:

  * Video <-> Video
  * Video <-> Document
  * Document <-> Document
  * Media <-> Meme
  * Argument <-> Argument

Graph structure:

* Nodes: artifacts, segments, arguments, topics, unresolved questions
* Edges: similarity, citation, contradiction, support, evidence-gap

---

### 3.4 Topic Synthesis (Wiki Layer)

A new emergent layer with two outputs:

* Topic argument indexes (machine-readable)
* Topic articles (human-readable wiki pages)

Topic argument indexes aggregate all arguments about each topic across all media:

* Claims, premises, conclusions, counter-claims
* Position clusters (support/challenge/neutral)
* Linked evidence references to original media locations
* Confidence and provenance metadata

Topic articles synthesize those indexes and include:

  * Summary of topic
  * Variety of competing perspectives
  * Areas of agreement and disagreement
  * Unanswered questions and weak-evidence areas
  * Source references to original media artifacts

This transforms the system into:

> A *collective epistemic map* rather than just an archive.

---

### 3.5 Federated / Opt-In Corpus System

Critical architectural expansion:

* Users contribute their own content
* Maintain ownership boundaries
* Opt-in inclusion in global graph

Requirements:

* Identity + attribution system
* Permissioning
* Content ingestion pipelines

---

### 3.6 Extended Sidecar Schema

The sidecar model must evolve:

From:

* Description
* Critiques

To:

* Transcript/OCR output
* Markdown-normalized text
* Segment/page/chapter index
* Topic-by-topic argument ledger for the source
* Multi-lens analytical outputs
* Embeddings
* Graph relationships
* Provenance pointers to exact source locations

---

## 4. Integration with Existing System

### Reuse

* Existing critique pipelines (feminist, Marxist, Foucauldian)
* Sidecar-based architecture
* Local inference philosophy

### Extend

* Apply critique layers to:

  * Entire videos
  * Individual arguments

### Unify

* Memes become nodes in the same graph
* Memes can:

  * Represent arguments
  * Link to video arguments

---

## 5. Data Model Evolution

### Current

```
Meme
  |- Image
  `- Sidecar (metadata + analyses)
```

### Future

```
Artifact
  |- Type (meme | video | film | episode | document | segment | argument | topic)
  |- Content
  |- Sidecar
  `- Graph Links
```

---

## 6. Pipeline Architecture Overview

### Ingestion Pipeline

* Input: media file / URL / document bundle
* Steps:

   1. Download / normalize
   2. Transcribe or OCR/extract text
   3. Normalize text into markdown artifacts
   4. Segment by time/page/chapter
   5. Extract arguments by topic
   6. Run critique lenses
   7. Generate embeddings
   8. Insert into graph
   9. Update topic argument indexes
  10. Regenerate affected topic articles

---

### Analysis Pipeline

* Periodic re-analysis
* Improved models refine:

  * Arguments
  * Links
  * Topic indexes
  * Topic pages

---

## 7. Key Challenges

### 7.1 Argument Detection Accuracy

* Ambiguity in natural language
* Implicit arguments

### 7.2 Scale

* Multimodal corpora are orders of magnitude larger than meme-only corpora
* Requires efficient pipelines + storage

### 7.3 Ontology Design

* Defining:

  * What counts as an "argument"
  * Topic boundaries

### 7.4 Trust / Moderation

* Conflicting interpretations
* Ideological framing differences

---

## 8. Strategic Framing

This project becomes:

> A decentralized, AI-assisted system for mapping the structure of discourse across media.

Where Biblioteca Memetica is:

> A curated memetic archive

The new system is:

> A living, federated knowledge graph of arguments and ideas.

---

## 9. Potential Extensions

* Real-time ingestion (live streams)
* Debate mapping visualizations
* AR/graph interfaces (ties to your spectrum visualization ideas)
* Integration with mesh networks (offline knowledge sync)

---

## 10. Minimal Viable Expansion Path

1. Add multimodal ingestion (video + PDF/doc)
2. Generate transcript/OCR and markdown sidecars for each source
3. Add embedding + similarity search across all media
4. Extract topic-tagged arguments per source
5. Build topic argument indexes from all matching sources
6. Generate first topic articles with linked evidence
7. Enable SemRAG chat over indexes, topic pages, and source sidecars

---

## 11. Primary Goal and Educational Foundation: Solving Bloom's 2 Sigma Problem

The primary goal is to build a wiki/index of arguments for every topic across the full indexed corpus, plus a semantic map that SemRAG chat systems can use to represent the range of perspectives during fluent conversation. The system should also emit explicit artifacts that identify unanswered questions and domains where evidence is insufficient to answer what users are asking.

A core philosophical and practical foundation of this project is addressing **Bloom's 2 Sigma Problem**: the finding that students receiving one-on-one tutoring perform two standard deviations better than those in conventional classroom settings.

### Reframing the Project Through This Lens

This system is not just a media archive or analysis engine. It is intended to function as a **scalable, personalized tutor** across domains of knowledge represented in the corpus.

Where traditional systems provide:

* static content
* passive consumption

This system aims to provide:

* adaptive explanation
* argument-aware guidance
* context-sensitive responses grounded in real media

---

### How the System Approaches 2 Sigma Outcomes

#### 1. Personalized SemRAG-Based Tutoring

* Users ask questions in natural language
* The system retrieves relevant content from:

  * videos, films, documentaries, and TV
  * PDFs, papers, books, and other documents
  * transcripts/OCR text and markdown sidecars
  * extracted arguments and topic indexes
  * memes and topic pages
* Responses are generated with:

  * citations
  * multiple perspectives
  * clarification of disagreements

This approximates:

> a tutor who selects the right examples and explanations for the learner

---

#### 2. Argument-Level Understanding

Unlike traditional educational tools, the system operates at the level of:

* claims
* reasoning structures
* competing interpretations

This enables:

* explaining *why* something is argued
* comparing viewpoints
* identifying logical gaps

---

#### 3. Iterative Dialogue

The chatbot interface allows:

* follow-up questions
* refinement of understanding
* exploration of adjacent concepts

This recreates a key feature of tutoring:

> interactive clarification and guided inquiry

---

#### 4. Multi-Perspective Analysis

Because each artifact is processed through multiple lenses (e.g., feminist, Marxist, Foucauldian), the system can:

* expose users to different interpretive frameworks
* explain how conclusions change under different assumptions

This supports:

* deeper critical thinking
* epistemic awareness

---

#### 5. Feedback Loop from Question Analytics

The question intelligence layer provides:

* insight into what learners struggle with
* identification of knowledge gaps in the corpus

Creators can then:

* produce targeted content
* refine explanations

This mirrors:

> a tutor adapting lessons based on student confusion patterns

---

### Key Insight

Bloom's original result depended on human tutors.

This project attempts to approximate that effect by combining:

* semantic retrieval (finding the right material)
* structured argument understanding
* adaptive generation (SemRAG)
* continuous feedback from user queries
* explicit unresolved-question and low-evidence artifacts

---

### Strategic Framing

The system becomes:

> A distributed, AI-mediated tutoring infrastructure built on real-world media and collective knowledge.

Rather than replacing educators, it:

* amplifies creators
* organizes discourse
* makes high-quality explanation accessible at scale

---

## Final Summary

The project goal is to build a multimodal argument index and wiki that maps perspectives across media, then expose that map through SemRAG chat systems that can support Bloom 2 Sigma-style learning even on esoteric topics.

You are not just scaling media types.

You are transitioning from:

* Archive -> System
* Classification -> Epistemology
* Content -> Discourse

This is effectively a **multimodal argumentative operating system for knowledge**, with explicit outputs for both answered and unanswered questions.

---

## 12. Roadmap to Completion

### Phase 1: Foundation, Scope, and Success Criteria

* Deliverable 1.1: Vision-to-spec package (MVP scope, non-goals, glossary, architecture boundaries)
* Deliverable 1.2: Bloom 2 Sigma-aligned outcome metrics and evaluation protocol
* Deliverable 1.3: Canonical data contracts for `artifact`, `segment`, `argument`, `topic`, and `question`
* Deliverable 1.4: Initial executable plan set in `plans/future/`

### Phase 2: Multimodal Ingestion and Sidecar Core

* Deliverable 2.1: Ingestion adapters for video/audio/document inputs and Memetica compatibility bridge
* Deliverable 2.2: Unified sidecar schema v1 with provenance pointers
* Deliverable 2.3: Deterministic storage/index layout for raw media and derived artifacts
* Deliverable 2.4: Re-runnable ingestion jobs with idempotency and failure recovery

### Phase 3: Transcription, OCR, and Structural Segmentation

* Deliverable 3.1: ASR pipeline with timestamps and optional speaker segmentation
* Deliverable 3.2: OCR/document extraction with page/chapter anchors
* Deliverable 3.3: Markdown-normalized text artifacts for all supported media
* Deliverable 3.4: Quality checks and confidence scoring for extracted text

### Phase 4: Argument and Lens Analysis

* Deliverable 4.1: Argument extraction (claim, premise, conclusion, stance, confidence)
* Deliverable 4.2: Topic tagging and rhetorical strategy classification
* Deliverable 4.3: Multi-lens analysis outputs (descriptive + feminist/Marxist/Foucauldian)
* Deliverable 4.4: Evaluation dataset and benchmark thresholds for extraction quality

### Phase 5: Semantic Graph and Linking Engine

* Deliverable 5.1: Embedding pipeline across artifacts, segments, arguments, and topics
* Deliverable 5.2: Graph schema and edge types (similarity, support, contradiction, citation, gap)
* Deliverable 5.3: Link-ranking and graph update jobs
* Deliverable 5.4: Query APIs for graph traversal and evidence retrieval

### Phase 6: Topic Synthesis and Wiki Layer

* Deliverable 6.1: Topic argument indexes (machine-readable)
* Deliverable 6.2: Topic pages (human-readable) with competing perspectives and disagreement maps
* Deliverable 6.3: Explicit unresolved-question and low-evidence artifacts
* Deliverable 6.4: Regeneration workflow when new evidence changes topic state

### Phase 7: SemRAG Tutoring Interface

* Deliverable 7.1: Retrieval orchestration across sidecars, arguments, graph, and topic pages
* Deliverable 7.2: Grounded answer generation with citation/provenance output
* Deliverable 7.3: Response mode labeling (`sourced`, `inferred`, `insufficient evidence`)
* Deliverable 7.4: Conversational UX for follow-up and clarification loops

### Phase 8: Question Intelligence and Creator Feedback

* Deliverable 8.1: Query logging pipeline and question taxonomy
* Deliverable 8.2: Analytics dashboards for demand patterns and content gaps
* Deliverable 8.3: Backlog generation from unanswered/high-friction topics
* Deliverable 8.4: Privacy controls and opt-in analytics boundaries

### Phase 9: Federation, Trust, and Governance

* Deliverable 9.1: Identity, attribution, and permissioning model for contributor corpora
* Deliverable 9.2: Opt-in federation rules and corpus-boundary controls
* Deliverable 9.3: Moderation/dispute workflow for conflicting interpretations
* Deliverable 9.4: Policy docs and operational governance runbooks

### Phase 10: Hardening, Scale, and Launch

* Deliverable 10.1: Observability stack (logging, tracing, job diagnostics, cost/perf metrics)
* Deliverable 10.2: End-to-end test harness and regression suite for pipeline + SemRAG
* Deliverable 10.3: Deployment profiles (local-first baseline, higher-scale profile)
* Deliverable 10.4: Alpha/Beta launch criteria and phased rollout plan

---

## 13. Technical Stack and Archive Hierarchy (v1)

### Archive Root Contract

The archive is rooted at `./archive/` and organized by service, then account name:

* `./archive/youtube/cjtrowbridge`
* `./archive/youtube/treeisalive`
* `./archive/tiktok/cjtrowbridge`
* `./archive/tiktok/treeisalive`

These account folders are populated only by contributors who explicitly opt in.

### Content and Sidecar Processing Model

All source content for each opted-in account is stored under its service/account path in `./archive/`.

For each artifact, sidecar generation should be idempotent:

* each sidecar script scans relevant archive files
* checks whether its target sidecar already exists
* creates the sidecar only when missing (or when explicitly forced)
* Simple-description sidecars should be generated from both `qwen-3.5-4b` and `gemma4-e4b` to preserve multiple model perspectives
* Complex multi-lens analysis sidecars should be generated with larger models, including `gemma4-31b` and `qwen3.5-35b-a3b`

This allows safe reruns and incremental backfill as the archive grows.

### Main Pipeline Orchestration

A single main run script orchestrates the full workflow:

1. Discover/sync content into `./archive/<service>/<account>/...`
2. Execute sidecar scripts (one script per sidecar type) to fill missing artifacts
3. Run semantic linking and topic indexing using sidecar contents
4. Build wiki/topic pages from indexes
5. Emit static wiki output to `./wiki/` (Jekyll-style static build target)

The architecture should support stage-level reruns so operators can run only sidecars, indexing, or wiki build when needed.

### Proposed v1 Tech Stack

* **Language/runtime**: Python 3.12 for pipeline scripts
* **Acquisition/normalization**: `yt-dlp` and `ffmpeg`
* **ASR**: `faster-whisper`
* **Simple-description models**: `qwen-3.5-4b` and `gemma4-e4b` (dual-model perspective baseline)
* **Complex multi-lens analysis models**: `gemma4-31b` and `qwen3.5-35b-a3b` (deeper interpretive synthesis)
* **Embeddings**: `sentence-transformers`
* **Metadata/provenance store**: SQLite
* **Vector search**: FAISS
* **Static publishing target**: generated pages in `./wiki/` (Jekyll-compatible output approach)

### Script Layout Direction

Suggested high-level script layout:

* `./scripts/run_pipeline.py` (main orchestrator)
* `./scripts/sidecars/` (one script per sidecar type)
* `./scripts/indexing/` (semantic linking + topic index generation)
* `./scripts/wiki/` (topic page/static wiki build pipeline)

This keeps ingestion, analysis, indexing, and publishing decoupled while preserving a single-command operator workflow.


