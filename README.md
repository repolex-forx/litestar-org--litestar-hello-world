# Repolex Knowledge Graph of litestar-org/litestar-hello-world

RDF knowledge graph data for [litestar-org/litestar-hello-world](https://github.com/litestar-org/litestar-hello-world), parsed by [repolex](https://repolex.ai).

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
rlex download litestar-org/litestar-hello-world
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 907643553944c242ba9a50fa8e12baaf3d0253e6
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 907643553944c242ba9a50fa8e12baaf3d0253e6
│           └── chunk-001.nq.gz
├── blob
│   ├── 02b4dd0c499a3222d225dfda03ac6177d984b8c6.nq.gz
│   ├── 05cd4665fd76781b5040964b8f97958c42e783c9.nq.gz
│   ├── 123014908bebbfb7ecfa1d15daaceb272fabe05b.nq.gz
│   ├── 144908a7aa3cb62657b66cb93861524a9f8722b3.nq.gz
│   ├── 1509ac9241d931605407797bc6f800a58cfb6dbe.nq.gz
│   ├── 1d27fd298befe01c50206e70480a41bdad0b8269.nq.gz
│   ├── 37d8731ad036726a8d0854b9d2959139516de927.nq.gz
│   ├── 3ba13e0cec6cbbfd462e9ebf529dd2093148cd69.nq.gz
│   ├── 4e58f77a5603d469b738db232743e40442dbc96d.nq.gz
│   ├── 583bd0b8438c99f1c9b5876e9fc470720f77c05b.nq.gz
│   ├── 60a9dfa85ba7e43bc0788c70f0d9349cefccce5b.nq.gz
│   ├── 90446afc3da119a8cdeadaee892c7a70768b84d9.nq.gz
│   ├── 90d78aa1fd4410ff4ffac3c03125525906bd9557.nq.gz
│   ├── 9e8af479a967b3b385ef6ab1a8f0fa26a98cbb09.nq.gz
│   ├── 9f96b553eddd0727ed5e45fb68c3aad92dd88179.nq.gz
│   ├── c627f2a16cf6695e4fb349b2a7f7a765968584c7.nq.gz
│   ├── cd4c9447c13618786c2dde4ea810cb859b4b5c8f.nq.gz
│   ├── d0ae548fa6a1e5c2baf682904dfdd9954948ad21.nq.gz
│   ├── d130a5f6ca2559f3da059001e5888eba93dbffe2.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f9bd8eeb20747650d002e27c9299057b2b0d0153.nq.gz
│   └── fa74339259984f5301a28673017e6bb8a7e40230.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 907643553944c242ba9a50fa8e12baaf3d0253e6.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 30 files
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

[litestar-org/litestar-hello-world](https://github.com/litestar-org/litestar-hello-world)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
