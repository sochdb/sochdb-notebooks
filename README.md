# SochDB Notebooks

This repository contains interactive Jupyter notebooks for exploring SochDB from a few different angles:

- first-touch product evaluation
- local embedded retrieval workflows
- database and transaction basics
- advanced AI-oriented patterns

## Laptop Learning Path

If someone just installed SochDB on their laptop and wants a clear progression,
start here:

- [Laptop Learning Path](./LAPTOP_LEARNING_PATH.md)

It groups the notebooks into:

- `Basic`
- `Intermediate`
- `Advanced`

and gives concrete tasks to complete at each level.

The notebook set is intentionally uneven in scope. Some notebooks are part of the validated public `pip install sochdb` path today, while others show broader platform capabilities or external-API-dependent workflows.

## Show This Product First

If you are showing SochDB to someone for the first time, use this order:

1. **SochDB 101** (`13_sochdb_101.ipynb`) — Broad first impression and platform framing
2. **Local Knowledge Retrieval** (`14_local_knowledge_retrieval.ipynb`) — Strongest current Python-first wedge
3. **Transactions, KV, and Data Modeling** (`6_transactions_kv.ipynb`) — Shows the embedded database side clearly
4. **SQL Engine** (`8_sql_engine.ipynb`) — Shows the richer packaged SQL/querying surface
5. **Local Admin and Maintenance** (`9_backup_admin.ipynb`) — Shows checkpoint/admin/operational concepts

## Start Here

If you are new to SochDB, start with these notebooks first:

0. **Local Knowledge Search Walkthrough** (`0_local_knowledge_search_walkthrough.ipynb`): Clean local-only walkthrough for the first Python-first retrieval wedge.
13. **SochDB 101** (`13_sochdb_101.ipynb`): Broad first-touch notebook showing basic storage, local retrieval, and the all-in-one local workflow story.
14. **Local Knowledge Retrieval** (`14_local_knowledge_retrieval.ipynb`): Focused evaluator notebook for SochDB's strongest current local retrieval wedge, including fast and quality presets.
6. **Transactions, KV, and Data Modeling** (`6_transactions_kv.ipynb`): Runnable notebook covering the embedded database side of SochDB.
8. **SQL Engine** (`8_sql_engine.ipynb`): Runnable notebook covering the richer packaged SQL/querying surface.
9. **Local Admin and Maintenance** (`9_backup_admin.ipynb`): Runnable notebook covering checkpoint, fsync, garbage collection, and local on-disk inspection.

## Validated Public-Package Path

These notebooks are the best current fit for a user starting with:

```bash
pip install sochdb
```

- `0_local_knowledge_search_walkthrough.ipynb`
- `6_transactions_kv.ipynb`
- `8_sql_engine.ipynb`
- `9_backup_admin.ipynb`
- `13_sochdb_101.ipynb`
- `14_local_knowledge_retrieval.ipynb`

## Advanced or External-API-Dependent Notebooks

These notebooks are still useful, but they are not the best first evaluator path. Many depend on external APIs, richer SDK surfaces, or more advanced setup:

1. **RAG Hybrid Search** (`1_rag_hybrid_search.ipynb`)
2. **CAG Semantic Cache** (`2_cag_semantic_cache.ipynb`)
3. **Agent Memory** (`3_agent_memory.ipynb`)
4. **Agentic Workflows** (`4_agentic_workflows.ipynb`)
7. **Multitenant Isolation** (`7_multitenant_isolation.ipynb`)
10. **Advanced RAG** (`10_advanced_rag.ipynb`)
11. **Agentic Tool Use** (`11_agentic_tool_use.ipynb`)
12. **Conversational RAG Memory** (`12_conversational_rag_memory.ipynb`)

## Broader Capability Notebooks

These notebooks are useful for understanding the broader SochDB vision, but they may not match the currently validated public Python evaluator path exactly:

5. **Knowledge Graph** (`5_knowledge_graph.ipynb`)

## Usage

Clone this repository and run the notebooks in Jupyter Notebook, JupyterLab, or VS Code.

For the validated local-first path, start with:

```bash
pip install sochdb
```

Then open one of the notebooks in the **Start Here** section above.
