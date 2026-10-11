# Repolex Knowledge Graph of pytest-dev/pytest-localserver

RDF knowledge graph data for [pytest-dev/pytest-localserver](https://github.com/pytest-dev/pytest-localserver), parsed by [repolex](https://repolex.ai).

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
rlex download pytest-dev/pytest-localserver
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 673ef31f7a9aedee47cbbda54089d535aecbca0a
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 673ef31f7a9aedee47cbbda54089d535aecbca0a
│           └── chunk-001.nq.gz
├── blob
│   ├── 0ca48bb7b11f4569f1ade8936f0e8d8d4d176535.nq.gz
│   ├── 270ec6ff31a89d09b7fb0eaf88a1e785bdeb55c8.nq.gz
│   ├── 29f351ddb045e05c01a24fe8252825417c12d0d0.nq.gz
│   ├── 31a498ede09fa8cb17e7b873526539b745b3679b.nq.gz
│   ├── 35f68f9affcf85d154000ac978caef567f9a0aab.nq.gz
│   ├── 389ab1c743510207c404a18895c8f6910d3a4e51.nq.gz
│   ├── 3dc59942e952b44e6a2b1e7f9664d32b2813465b.nq.gz
│   ├── 464744132a07a668eb288083fd16b14774c7d4d5.nq.gz
│   ├── 482058b8229a2d4ede5937296eeab2fc3443575f.nq.gz
│   ├── 4a2de5d543fe7172d48a76dcd7d7339de1fa5cf2.nq.gz
│   ├── 577716d2b8db12747c9d616fefa0930309bf3705.nq.gz
│   ├── 622d480ae85423fdf501e0a62b8d4d4fe9f0a91f.nq.gz
│   ├── 77e2f6e055384ed898f1d17321df35cf845f68d6.nq.gz
│   ├── 7a4e5574b1afcb5251d06b12ed4b86303f5ab33b.nq.gz
│   ├── 8850d5af5621ed40502a0ac730bf983a35ac12bf.nq.gz
│   ├── 94f804c513860e6e7e887e6e5de2be6a42138a76.nq.gz
│   ├── ac3ac9b199939ac1414690ebad97f4fd812691b1.nq.gz
│   ├── b603eb0075998d37f84ac5ef1cbf6a08d4a681b0.nq.gz
│   ├── cc7246fb52887bdf2e9930f51cd43668a1eece83.nq.gz
│   ├── ce975965d53450a2c9dd2bcdd40431afcce847cf.nq.gz
│   ├── dc59b43a7b7f76c5428c45c902be0992b2d1ff82.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ef0136d864282cebcc8d63887f0a93fe5bce452a.nq.gz
│   ├── efc55a4dd91592027b1c73a05ab6207415faa761.nq.gz
│   └── fbc1a7788bfda8fb87bae07010187198716a2135.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 673ef31f7a9aedee47cbbda54089d535aecbca0a.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 33 files
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

[pytest-dev/pytest-localserver](https://github.com/pytest-dev/pytest-localserver)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
