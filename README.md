# Repolex Knowledge Graph of aio-libs/idna-ssl

RDF knowledge graph data for [aio-libs/idna-ssl](https://github.com/aio-libs/idna-ssl), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download aio-libs/idna-ssl
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 24f54514182c3530fb18d602963337edcadfd377
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 24f54514182c3530fb18d602963337edcadfd377
│           └── chunk-001.nq.gz
├── blob
│   ├── 0aa739061fc27465a622735e3a80173d81c68025.nq.gz
│   ├── 12ae75549102b8aa82059c585978ffbeb96d2b34.nq.gz
│   ├── 13ff0bb0c757e3ba1e16a903177e77466c7b5503.nq.gz
│   ├── 1ceacd84c8cdf25987d2b402d71b4366d1bbb086.nq.gz
│   ├── 47a466b65336bc871e4f87d1d937a58a47d1ec15.nq.gz
│   ├── 59db9bd469c63ce49cc6d4f5c0b05be08a47d20b.nq.gz
│   ├── 676a73785d520ea15df14fbe53a10005f5b28b8f.nq.gz
│   ├── 687e8b674a9753b2e038684ecf5f58650d6ff465.nq.gz
│   ├── 8c5d85da41560a313493c34ca630b47abfff5144.nq.gz
│   ├── 9e97e50ea67845c61bdbd42791a3f385853c149a.nq.gz
│   ├── b551b97744546a4438d7eae24df98ca0d0e8231f.nq.gz
│   ├── ce96d83fb6630825b404968cee1091b02096d17b.nq.gz
│   ├── da180db2c5b38ab42b71c7258696a655b3ef5061.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── f06dc5f40bff570fb8f7550b9faed8803eac64c2.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 24f54514182c3530fb18d602963337edcadfd377.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 23 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[aio-libs/idna-ssl](https://github.com/aio-libs/idna-ssl)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
