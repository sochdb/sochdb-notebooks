# SochDB Laptop Learning Path

This guide is for someone who just installed SochDB on their laptop and wants
to build confidence step by step.

The goal is not to try every feature on day one. The goal is to complete a few
useful tasks in the right order.

## Before You Start

Recommended baseline:

```bash
pip install sochdb jupyterlab notebook
```

Then launch Jupyter:

```bash
jupyter lab
```

If you also cloned the main SochDB repository, you can pair these notebooks
with the Python examples under `sochdb/examples/python/`.

## Level 1: Basic

This is the best first session for a new evaluator.

### Outcome

By the end of this level, you should be able to:

- explain what SochDB is good at
- store local documents
- run local retrieval
- understand the local-first workflow

### Recommended order

1. `13_sochdb_101.ipynb`
2. `0_local_knowledge_search_walkthrough.ipynb`
3. `14_local_knowledge_retrieval.ipynb`

### Tasks to complete

#### Task 1. Build a first mental model

Open:

- `13_sochdb_101.ipynb`

Try to answer:

- What is embedded/local mode?
- What is the retrieval wedge?
- Why is local-first a strong entry point?

#### Task 2. Run a local retrieval walkthrough

Open:

- `0_local_knowledge_search_walkthrough.ipynb`

Complete:

- load a small local corpus
- build a vector index
- run a few retrieval queries
- inspect which results come back and why

#### Task 3. Tune for speed vs quality

Open:

- `14_local_knowledge_retrieval.ipynb`

Complete:

- run the default setup
- compare a faster setup vs a higher-quality setup
- note what changes in retrieval quality and latency

### Optional companion script

If you cloned the main repo too:

```bash
python3 sochdb/examples/python/07_local_knowledge_search.py
```

That is the strongest current local Python-first wedge.

## Level 2: Intermediate

This is where someone moves from “interesting demo” to “I can build with this.”

### Outcome

By the end of this level, you should be able to:

- model local data clearly
- use transactions and SQL
- understand admin/maintenance basics

### Recommended order

1. `6_transactions_kv.ipynb`
2. `8_sql_engine.ipynb`
3. `9_backup_admin.ipynb`

### Tasks to complete

#### Task 1. Model data with KV and transactions

Open:

- `6_transactions_kv.ipynb`

Complete:

- create a small dataset
- write and read records
- try a transaction
- intentionally test what rollback means

#### Task 2. Query with SQL

Open:

- `8_sql_engine.ipynb`

Complete:

- create a small table
- insert rows
- run a few `SELECT` queries
- test a filtered query
- understand when SQL is easier than raw KV paths

#### Task 3. Learn local operations

Open:

- `9_backup_admin.ipynb`

Complete:

- inspect checkpoint/admin concepts
- understand what local maintenance looks like
- learn what a healthy local workflow should feel like

### Optional companion scripts

If you cloned the main repo too:

```bash
python3 sochdb/examples/python/01_basic_database.py
python3 sochdb/examples/python/02_vector_search.py
python3 sochdb/examples/python/06_sql_queries.py
```

## Level 3: Advanced

This level is for someone exploring SochDB as an AI application platform, not
just a local embedded database.

### Outcome

By the end of this level, you should be able to:

- evaluate AI-oriented workflows on top of SochDB
- understand where semantic cache, memory, and agent workflows fit
- identify which advanced flows are product-ready vs exploratory

### Recommended order

1. `2_cag_semantic_cache.ipynb`
2. `3_agent_memory.ipynb`
3. `4_agentic_workflows.ipynb`
4. `12_conversational_rag_memory.ipynb`
5. `10_advanced_rag.ipynb`
6. `11_agentic_tool_use.ipynb`
7. `7_multitenant_isolation.ipynb`
8. `5_knowledge_graph.ipynb`

### Tasks to complete

#### Task 1. Evaluate semantic cache

Open:

- `2_cag_semantic_cache.ipynb`

Complete:

- understand what gets cached
- compare exact vs semantic reuse
- decide whether this helps your workload

#### Task 2. Evaluate memory and retrieval patterns

Open:

- `3_agent_memory.ipynb`
- `12_conversational_rag_memory.ipynb`

Complete:

- understand what is stored as memory
- inspect how retrieval is used across turns
- decide if the memory model is useful for your product

#### Task 3. Evaluate agent workflows carefully

Open:

- `4_agentic_workflows.ipynb`
- `11_agentic_tool_use.ipynb`

Complete:

- identify which parts are core SochDB value
- identify which parts depend on broader orchestration stacks
- avoid treating these as the first product evaluation path

#### Task 4. Explore advanced architecture areas

Open:

- `10_advanced_rag.ipynb`
- `7_multitenant_isolation.ipynb`
- `5_knowledge_graph.ipynb`

Complete:

- decide whether you need multi-tenant separation
- decide whether graph-like modeling is central or optional
- decide whether advanced RAG is a fit after the local retrieval wedge

## Best Pitch Path

If someone only has 30 to 45 minutes, do this:

1. `13_sochdb_101.ipynb`
2. `0_local_knowledge_search_walkthrough.ipynb`
3. `14_local_knowledge_retrieval.ipynb`
4. `6_transactions_kv.ipynb`

That gives the cleanest story:

- local-first
- retrieval-oriented
- practical
- easy to explain

## What Not To Do First

Avoid leading with:

- the most complex agent notebook
- external-API-dependent workflows
- broad “SochDB does everything” claims
- every notebook in one session

Instead:

- start with one wedge
- complete one task at a time
- expand only after the basic path feels solid
