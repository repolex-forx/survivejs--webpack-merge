# Repolex Knowledge Graph of survivejs/webpack-merge

RDF knowledge graph data for [survivejs/webpack-merge](https://github.com/survivejs/webpack-merge), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download survivejs/webpack-merge
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 2f610b9c2da066cc5d035ee83db84e22b7d42fb3
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 2f610b9c2da066cc5d035ee83db84e22b7d42fb3.nq.gz
│   └── repolex
│       └── 2f610b9c2da066cc5d035ee83db84e22b7d42fb3
│           └── chunk-001.nq.gz
├── blob
│   ├── 0967ef424bce6791893e9a57bb952f80fd536e93.nq.gz
│   ├── 2944dbcabb17ad966608c5342ec4d3ab3811db22.nq.gz
│   ├── 29a76c45b9a7e3f153173f6dc9ecd0e7c80cec52.nq.gz
│   ├── 2cedc8a6534bb53861466acc9d81f8381bb3131a.nq.gz
│   ├── 352d9040288ec57560e8539e7309722716509ab3.nq.gz
│   ├── 36f9c42b8de42f27328ab1f52ee82460f5234963.nq.gz
│   ├── 3c032078a4a21c5c51d3c93d91717c1dabbb8cd0.nq.gz
│   ├── 5eaceffb3418bf2f41c506660eb289beaba54172.nq.gz
│   ├── 6161b4eba4d8551d243e5a25e60a34dea65ec883.nq.gz
│   ├── 6328b5b889f8a57b088cb042543af5c53c97e662.nq.gz
│   ├── 65cd50a95f5e06484d209996c6259fe066a5169b.nq.gz
│   ├── 6c42f0d6bf2bb28cbc43afd25e15b054d5530bb0.nq.gz
│   ├── 70f43eec46ffc745e374e4bbfed83b13fc70fe93.nq.gz
│   ├── 71fb3773479e47de38162cc92ce1c009c8a04fc4.nq.gz
│   ├── 756375f5fa1e1616c9fd31e50ed9d51dc9250802.nq.gz
│   ├── 8276559873861a0d3872592b4e28c9088f97c805.nq.gz
│   ├── 83049b2a3cdb9517bb9a1f8928ac3ba7660d06c1.nq.gz
│   ├── 85cea6b3f1ba91bfc37fb970ac4fcf29a6a43ecb.nq.gz
│   ├── 90ea10185a23d1b06cb47686c2ca4947fa3570cb.nq.gz
│   ├── 95d9c3d78ad21afcc0e8027a1806cb6154a33d60.nq.gz
│   ├── 9913567c2f36187a75bcc52302a0b3db44512271.nq.gz
│   ├── 99ef75256f30dd6bd3468d96497776422d4ff239.nq.gz
│   ├── a0cc94f257e4d2ac2f90c36e142d9b934c2feb41.nq.gz
│   ├── aa7ed37ad4632845c11520b611624c59d9d7048e.nq.gz
│   ├── bd26163b28757934a414d8b9ee6af7d173add1db.nq.gz
│   ├── cad9cf73acb4565d68bbf2e2cbb07e09c3bc8c1a.nq.gz
│   ├── ce85075f9ce1abd5793bc915fd5a62ea9937467a.nq.gz
│   ├── e2c2ed6af8c51a08533e1a84aea6292eeed3da80.nq.gz
│   ├── e5af475296c6386041dc3ce8b0e7b70ccb94ec87.nq.gz
│   ├── f5ec2a9a9419cfb01f93e37af24cbf460df7065a.nq.gz
│   └── fdff191fd6eec65eedc3036d41aac1465e534045.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 2f610b9c2da066cc5d035ee83db84e22b7d42fb3.nq.gz
├── filetree
│   └── 2f610b9c2da066cc5d035ee83db84e22b7d42fb3.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 41 files
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

## Source repository

[survivejs/webpack-merge](https://github.com/survivejs/webpack-merge)

---
*Parsed on 2026-04-19 by [repolex](https://repolex.ai)*
