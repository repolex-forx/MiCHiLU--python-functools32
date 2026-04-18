# Repolex Knowledge Graph of MiCHiLU/python-functools32

RDF knowledge graph data for [MiCHiLU/python-functools32](https://github.com/MiCHiLU/python-functools32), parsed by [repolex](https://repolex.ai).

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
lexq download MiCHiLU/python-functools32
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 756d0820a3956829baabc28c6e3685487d7e8ef5
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 756d0820a3956829baabc28c6e3685487d7e8ef5.nq.gz
│   └── repolex
│       └── 756d0820a3956829baabc28c6e3685487d7e8ef5
│           └── chunk-001.nq.gz
├── blob
│   ├── 03b9855fdd476202fe4dce327065f60de1015a38.nq.gz
│   ├── 03ceaf13fc94792b30db1cd5ed109a8652840a1a.nq.gz
│   ├── 3784af7eaf7a062d7ed4940e56896c718af8520e.nq.gz
│   ├── 43388e7e13a2f38c07b717f64f8f7d01c7099820.nq.gz
│   ├── 45f2c10684d90cf3ef8c920dc7c38235c743bc27.nq.gz
│   ├── 4eff2cb513c7c7edca2bbc902a560bc3d2afecd0.nq.gz
│   ├── 524e74120578612e6603d950434d06cd33283879.nq.gz
│   ├── 687201c938edec555290fa9e435e71412aee3854.nq.gz
│   ├── 7f4037cbc936819428a9fa2d9516dab527dadd78.nq.gz
│   ├── 8b85f1c877ffd586ac975d8d3cd1087e7c9f0d6b.nq.gz
│   ├── bf895c72e122d244dff69d2d9264e7dea93e18e0.nq.gz
│   ├── ddd17a243b0bd9bcbd4e8ebfcd974b655917ee82.nq.gz
│   ├── df05db1c8d15777a0a567892322efd9d57740b6d.nq.gz
│   └── ed50520ab322ada9a701e500c00091e0a93de521.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 756d0820a3956829baabc28c6e3685487d7e8ef5.nq.gz
├── filetree
│   └── 756d0820a3956829baabc28c6e3685487d7e8ef5.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 24 files
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

[MiCHiLU/python-functools32](https://github.com/MiCHiLU/python-functools32)

---
*Parsed on 2026-04-18 by [repolex](https://repolex.ai)*
