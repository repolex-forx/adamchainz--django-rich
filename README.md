# Repolex Knowledge Graph of adamchainz/django-rich

RDF knowledge graph data for [adamchainz/django-rich](https://github.com/adamchainz/django-rich), parsed by [repolex](https://repolex.ai).

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
rlex download adamchainz/django-rich
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 1009f109322770ea3234b77f6ee902d271ad02bd
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 1009f109322770ea3234b77f6ee902d271ad02bd
│           └── chunk-001.nq.gz
├── blob
│   ├── 11e75696348297482abe5d9bb5e75f75dbed0bba.nq.gz
│   ├── 205ab9ad9df4ab629d1b7b8d8a72b41f44d8824c.nq.gz
│   ├── 22ddbb118475b52ce8ecba56d9ec45009923da58.nq.gz
│   ├── 2529ff0b60f07945525434cfebf01fa3d5a8a330.nq.gz
│   ├── 2a7f84f54867d02714727f82eef95d3be939d666.nq.gz
│   ├── 3967597c5d8a594ed7e40cd370714b4aeba2af9c.nq.gz
│   ├── 3ba13e0cec6cbbfd462e9ebf529dd2093148cd69.nq.gz
│   ├── 40f4ac757715bb1a8c355eda9124141fdda3aeff.nq.gz
│   ├── 438d629c3ce988e3afffa71110b9660853d38549.nq.gz
│   ├── 483e3e0fb3b1c3d02fef00e80958fc2d65d4eaa2.nq.gz
│   ├── 49155131e360ff10184d1237d992d311f01ed2d6.nq.gz
│   ├── 59794dfb75563dc5fc8298696de383c777490956.nq.gz
│   ├── 60fd03dc3bda76b5169f762461875007c4f10c47.nq.gz
│   ├── 664ee9bd0d35471c753883c28536b7078c38bb02.nq.gz
│   ├── 7f1d007c01048570d774e58f46203d3e92056c39.nq.gz
│   ├── 8bcb5b8cbbd2acbf534ec8dd9eadc639585bd1d4.nq.gz
│   ├── 8e62c9fa5583994ce153cb9644385a98c5f5c27e.nq.gz
│   ├── 93acb639926ccf42e9a2f76f02419eeaf0405c3a.nq.gz
│   ├── b8f1930ec1c2e2320b2118170fa6b46a870aae3f.nq.gz
│   ├── c02d394525d974ed4038e9acf12dbdd06982488a.nq.gz
│   ├── d31c208152af9f4d517d17b53e6d110e2ef4d9f7.nq.gz
│   ├── dea0450b9829c75c1a4e0bf11c38488d54aaea7d.nq.gz
│   ├── e071ef3df0aa1b4a1f21b07531701a61d1b881a4.nq.gz
│   ├── e537603cadd1cc1dcb09783c3f6748e43298355a.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ed8bc198c0a6049cbd2833630f15fe2a1d203399.nq.gz
│   ├── f7d2a333a29452eef990294fdfd2075059d0adb1.nq.gz
│   ├── f9ddafeccdf1e7ed716b57b33fa236462bab2e16.nq.gz
│   └── fc800c6d9c6aac568df8a66ad391bfa8bce43a56.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 1009f109322770ea3234b77f6ee902d271ad02bd.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 37 files
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

[adamchainz/django-rich](https://github.com/adamchainz/django-rich)

---
*Parsed on 2026-10-18 by [repolex](https://repolex.ai)*
