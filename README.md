# Repolex Knowledge Graph of purpleprotocol/mimalloc_rust

RDF knowledge graph data for [purpleprotocol/mimalloc_rust](https://github.com/purpleprotocol/mimalloc_rust), parsed by [repolex](https://repolex.ai).

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
rlex download purpleprotocol/mimalloc_rust
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── a5a76fd2c5a3a7c7b24d4765d53c71e41b32df74
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── a5a76fd2c5a3a7c7b24d4765d53c71e41b32df74.nq.gz
│   └── repolex
│       └── a5a76fd2c5a3a7c7b24d4765d53c71e41b32df74
│           └── chunk-001.nq.gz
├── blob
│   ├── 01d2c742bbd96ac90d156bc01579aeaf80fc47fe.nq.gz
│   ├── 05e116694e260d68ecf09049ab57243df9ec3001.nq.gz
│   ├── 11588aeb17150b67dfc1b0608a22752e14f1acca.nq.gz
│   ├── 2f88dbac54e76e79bf1619d109f0efbf9a4268e9.nq.gz
│   ├── 383f0dcb3c431136c725d254d022be2eb10ca796.nq.gz
│   ├── 385a34d8d240c3b43712bdf189c4f08f7225056c.nq.gz
│   ├── 4288b2f5109c6ce0f871bc3a7569def418b81608.nq.gz
│   ├── 4ab43736a839dad0625345ac8ae37355254e3078.nq.gz
│   ├── 4de01ea7cb2a0ff38dd88b61cd19806b3b1ea0a3.nq.gz
│   ├── 5148cec1e41daff63ec5d987e36d415bf90bd7bb.nq.gz
│   ├── 67eeb4c1968e397c062e4b9380a74574aa995e1d.nq.gz
│   ├── 9a3377d9ceafb733860ab47bd5ddd412dd5c11a8.nq.gz
│   ├── be9614c9006cc846a8881275a0cc94f16b73e87a.nq.gz
│   ├── cb3fa2e19c26afbd78f901e583ec985eaa6088c1.nq.gz
│   ├── de9e80e3078a7be994954b8edd0c1e222f74adbc.nq.gz
│   ├── e059bfdeef79f384f46d62ee5cda5ecd97d7f7b1.nq.gz
│   └── ecc9f3ade5049a94f7dadca84040317291bfc366.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── a5a76fd2c5a3a7c7b24d4765d53c71e41b32df74.nq.gz
├── filetree
│   └── a5a76fd2c5a3a7c7b24d4765d53c71e41b32df74.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 27 files
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

[purpleprotocol/mimalloc_rust](https://github.com/purpleprotocol/mimalloc_rust)

---
*Parsed on 2026-11-22 by [repolex](https://repolex.ai)*
