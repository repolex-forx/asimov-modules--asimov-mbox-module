# Repolex Knowledge Graph of asimov-modules/asimov-mbox-module

RDF knowledge graph data for [asimov-modules/asimov-mbox-module](https://github.com/asimov-modules/asimov-mbox-module), parsed by [repolex](https://repolex.ai).

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
rlex download asimov-modules/asimov-mbox-module
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 31de201485f5ac45955497f9fce95fc27928158d
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 31de201485f5ac45955497f9fce95fc27928158d.nq.gz
│   └── repolex
│       └── 31de201485f5ac45955497f9fce95fc27928158d
│           └── chunk-001.nq.gz
├── blob
│   ├── 02a7d41959378b441ecf388da1f8b77f081b90f5.nq.gz
│   ├── 035a91beb91023c660e8c1d1a05fc43618f84e6f.nq.gz
│   ├── 10b359dd05935c73efb064470f9ecda90f6d28aa.nq.gz
│   ├── 1dfe80692fc1a039e15fcb2a667f86dad7708f91.nq.gz
│   ├── 2471f9cd86450acc3dbc97a8a6f5635fce5fd7cc.nq.gz
│   ├── 2b232591fb21989eb9d0c6d00052061ab008bab4.nq.gz
│   ├── 2decf5cca776b4ae98a1ae4752fffe1660b59432.nq.gz
│   ├── 6b23d61018f43b840f8d2ff3b45a1c02d76df38d.nq.gz
│   ├── 6e8bf73aa550d4c57f6f35830f1bcdc7a4a62f38.nq.gz
│   ├── 75e3b65f99b29f48ab230e3eab3de8d0b7a9229f.nq.gz
│   ├── 7fa8bd5c1da10eb25a2508e8403788816976724f.nq.gz
│   ├── 8abe2141531a4e5bf55032b9d1975900ed717489.nq.gz
│   ├── 92a9201676689ea30431ea1966e1c18efc282232.nq.gz
│   ├── 9fe50de16e59d550235aa6d7d15ee12ddf054414.nq.gz
│   ├── a36fedab8db68b26a76fbbf1de1f549e4a12261b.nq.gz
│   ├── af9908b08f4b33c32a0080af73f53bc0fa0cdce4.nq.gz
│   ├── c75adc198325c7b0b9fa484617e2a7e9df1ff9f5.nq.gz
│   ├── cf42f6893594e2f8be2b722de51123d65e4d61c4.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── ee4d9362508d63f9e156fe9ee1b11ebc1a3e86d6.nq.gz
│   ├── efb09ab35e26518cd883156ec35c03576eb2b193.nq.gz
│   ├── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
│   └── fa4373b26e25eb49c2539e6881bb03afef6da525.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 31de201485f5ac45955497f9fce95fc27928158d.nq.gz
├── filetree
│   └── 31de201485f5ac45955497f9fce95fc27928158d.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 31 files
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

[asimov-modules/asimov-mbox-module](https://github.com/asimov-modules/asimov-mbox-module)

---
*Parsed on 2026-09-28 by [repolex](https://repolex.ai)*
