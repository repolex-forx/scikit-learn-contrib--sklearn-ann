# Repolex Knowledge Graph of scikit-learn-contrib/sklearn-ann

RDF knowledge graph data for [scikit-learn-contrib/sklearn-ann](https://github.com/scikit-learn-contrib/sklearn-ann), parsed by [repolex](https://repolex.ai).

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
rlex download scikit-learn-contrib/sklearn-ann
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── c105475ab0bc6dfcdb2239a38273d6895c5fe281
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── c105475ab0bc6dfcdb2239a38273d6895c5fe281
│           └── chunk-001.nq.gz
├── blob
│   ├── 00b9591a4438b6e96ab9936089bf93a2b7dda305.nq.gz
│   ├── 1119bf2ffccb9ae380b4e1dc445b7133974fe4c2.nq.gz
│   ├── 11cd49b7bcc859d0117e31252fc0dcffb2f36677.nq.gz
│   ├── 25ef0a7651e5d815bfb4eff5f5bc1a806e2906d4.nq.gz
│   ├── 27fa661622c0b3099204b74ffdce68ef812577bd.nq.gz
│   ├── 41b781fff51cdd73417175c1e07fec2c1d6e7120.nq.gz
│   ├── 4927c45bf30bca9f1f81169ae96ce20f7454e6d0.nq.gz
│   ├── 5bfd7a0273c2b4ab6ea179759b47e7b8b27e438e.nq.gz
│   ├── 6284376272f391b91b774f0eeca9008fbf5b9573.nq.gz
│   ├── 6c26cc4e8b6a5ff4e262427dcc7a4833c24d283f.nq.gz
│   ├── 75906b9919b8b94e171bef804a6045bd2d21e942.nq.gz
│   ├── 88fe723d8574b8cf1e47f433cba8747aa315132c.nq.gz
│   ├── 8db98d61f3d1a56d746587eea17871d16c37f21e.nq.gz
│   ├── 9c6009516f46a0dd296b85e77b2c23cef59b51fc.nq.gz
│   ├── a6bc6db81474f4343392cd3a85432b879944ff12.nq.gz
│   ├── aed524d8d0496ec3da08c96d2e8c13218ab52af8.nq.gz
│   ├── b4e7370aa318122a87d48c4d6264bdbb73d84bf7.nq.gz
│   ├── b6c88a9b1c309cec8a5535274b57b23cd425d9d0.nq.gz
│   ├── c9214961091bcb4d3d3170203d4c01a1d7c3dadd.nq.gz
│   ├── cb312dcdd6632b394c74b32effa5a40170b39389.nq.gz
│   ├── cc6687ba44f2a2b3a670ba908fe4cf0113fa69e7.nq.gz
│   ├── d338908fadf77ce04227d78fe09199e76202d42d.nq.gz
│   ├── d9157c7b47fd48f5491aad14e32d8f8daed217f0.nq.gz
│   ├── dbc17770cdbd33271265aec733076da5dd3d0a9d.nq.gz
│   ├── e1cff94f432309e7a31ba3fcbe81be9f633437e6.nq.gz
│   ├── e39086b44f5b5bd136d457ebab5def83751cd985.nq.gz
│   ├── e684e5b24ade5e35d4de6f942bae338cfc615400.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e79648df50eac49cbcc3f587b0e381e99b390523.nq.gz
│   ├── e8a2a63f6779fbca58598887a8e6e7ab251f8b3e.nq.gz
│   ├── ec1f3cd3570cd2179fd359a36033cc30e332ee2a.nq.gz
│   ├── f85c1bd3b01aa2c7c1d4677bf21a76290d2a67cd.nq.gz
│   └── fcc30324e4eeffd99447506b12948d176fed3986.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── c105475ab0bc6dfcdb2239a38273d6895c5fe281.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 41 files
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

[scikit-learn-contrib/sklearn-ann](https://github.com/scikit-learn-contrib/sklearn-ann)

---
*Parsed on 2026-10-15 by [repolex](https://repolex.ai)*
