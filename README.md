# Repolex Knowledge Graph of colcon/colcon-python-setup-py

RDF knowledge graph data for [colcon/colcon-python-setup-py](https://github.com/colcon/colcon-python-setup-py), parsed by [repolex](https://repolex.ai).

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
rlex download colcon/colcon-python-setup-py
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 2317cc933cfa792c19c2ac4cc88f41e1454b185f
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 2317cc933cfa792c19c2ac4cc88f41e1454b185f
│           └── chunk-001.nq.gz
├── blob
│   ├── 014c26922a04fe15b3ac51bc1789a1b5fc61cdfb.nq.gz
│   ├── 07c68986fd91c68328ba1da3490ced851ecef726.nq.gz
│   ├── 0f17157ed42b486a0c57cbffddd97987a4844e6b.nq.gz
│   ├── 1a87dccdb39f9e2c7debf17373416738f313afa9.nq.gz
│   ├── 2555de456750d99e59d1c4a3e0966f5526f90b16.nq.gz
│   ├── 52cfada857a437bdc63ba47b0838407f5186de8f.nq.gz
│   ├── 783803ccac92254dfe89aba0c83d33690a2cacc7.nq.gz
│   ├── 99cb7b66f1482ab885a1aa0f6d83c274e4bc58c2.nq.gz
│   ├── aa5b2fd887c8cfab65eb72320009f12ac743f2f3.nq.gz
│   ├── b7745614eac47ea349fdfc5adcf8a1054ecc3f70.nq.gz
│   ├── bd7c8693b373f16474a10254e75b502ef8389f27.nq.gz
│   ├── c4b55c480544c77ea321e84cf7eb60ca023a3858.nq.gz
│   ├── c9b3426c1ce606db4a4d832cf6c0d79d20a32388.nq.gz
│   ├── d645695673349e3947e8e5ae42332d0ac3164cd7.nq.gz
│   ├── dffe460f162da9929178a7ce342532e7ba896425.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── e82fd0b0abbf1472480d19d468efe7819276e80d.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 2317cc933cfa792c19c2ac4cc88f41e1454b185f.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 25 files
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

[colcon/colcon-python-setup-py](https://github.com/colcon/colcon-python-setup-py)

---
*Parsed on 2026-10-17 by [repolex](https://repolex.ai)*
