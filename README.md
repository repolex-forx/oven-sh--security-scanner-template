# Repolex Knowledge Graph of oven-sh/security-scanner-template

RDF knowledge graph data for [oven-sh/security-scanner-template](https://github.com/oven-sh/security-scanner-template), parsed by [repolex](https://repolex.ai).

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
rlex download oven-sh/security-scanner-template
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── a18eb0889a31e25199d6acbcf3b7ace83429aee5
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── a18eb0889a31e25199d6acbcf3b7ace83429aee5
│           └── chunk-001.nq.gz
├── blob
│   ├── 10465cdaf603f70e435a9453075f25f05da89d2a.nq.gz
│   ├── 17e3afcc1fdba02dc1c2725a21a2ab6fae4200ae.nq.gz
│   ├── 28f1ba7565f46fb5074ad9a4f07c4cfc86dff4cc.nq.gz
│   ├── 2c6649c21b4fb3eef63cc308a12ce5feb63541ce.nq.gz
│   ├── 3f5f86abc73dda8ff28dfed132a2edc85be2943a.nq.gz
│   ├── 74ed34d29940699ac2ffab00c41925acac0f3d71.nq.gz
│   ├── a91aec6dbed21e920b85d1667c86559a8a120b36.nq.gz
│   ├── bcc9986605a12c0985456a2d087ae5263abf8fdf.nq.gz
│   └── c08129e6b253bf956d460c3bdd63d897df70e9f6.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── a18eb0889a31e25199d6acbcf3b7ace83429aee5.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 17 files
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

[oven-sh/security-scanner-template](https://github.com/oven-sh/security-scanner-template)

---
*Parsed on 2026-10-10 by [repolex](https://repolex.ai)*
