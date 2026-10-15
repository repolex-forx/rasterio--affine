# Repolex Knowledge Graph of rasterio/affine

RDF knowledge graph data for [rasterio/affine](https://github.com/rasterio/affine), parsed by [repolex](https://repolex.ai).

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
rlex download rasterio/affine
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 63d1898b811956d4b38147b53ca6ef3a2314b3fd
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 63d1898b811956d4b38147b53ca6ef3a2314b3fd
│           └── chunk-001.nq.gz
├── blob
│   ├── 0d62b62676468fc880db61c71e0afdc3bb9c8965.nq.gz
│   ├── 0fee69196884621ca14d34c8cc0f84163790ac46.nq.gz
│   ├── 11d200900339b240fd62739da8dfd5b5368dc937.nq.gz
│   ├── 1e896c2d5f5ce0509224d4f31694011fe4d02890.nq.gz
│   ├── 1fa75b5de45ccb4c0d92d180e14f00524f209828.nq.gz
│   ├── 27597a7cd99ea3a5a89daa60063df05db589b95a.nq.gz
│   ├── 2c804c9e8877b562b37d42ce4381baf8585508fd.nq.gz
│   ├── 31952b883ab6b8a5b87adb193562a2a41cb91a8b.nq.gz
│   ├── 4d9490d403aecf97b5acb36b288445d9a35e7383.nq.gz
│   ├── 51c7b5918c08d0dbdc071e53ca586cc2ca9ac953.nq.gz
│   ├── 621c9f60cc09fe1495f27f6db59f591e75eb9f27.nq.gz
│   ├── 75765cc8f17aaa20858b33055e46506b71b677bd.nq.gz
│   ├── 91eaa03afe0a74b4ca7419202b071463ec41bdd9.nq.gz
│   ├── 921be472f712663c1a171a3f9a80b9e71caaa34b.nq.gz
│   ├── a64e56d8d842d8c10e59749ea733b1bd42f9431d.nq.gz
│   ├── ad7868b09a0a40bd5de87af6f9257dc3f1158a4e.nq.gz
│   ├── ad8236fd01e7e1a8333cdbc06512de906c38f7fa.nq.gz
│   ├── b5b452ab3b7a17e033f9002b103343c10716d627.nq.gz
│   ├── b81ed32d560a32b5e070394b498477f9df53f0ad.nq.gz
│   ├── baed6d7956ed947c115ff98e0b5fbf2be1337fd8.nq.gz
│   ├── bb50a0f947e7f539e054128903013fe0f648c33c.nq.gz
│   ├── c61977e2a3a25847571d3a321b504571da027785.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e92ba040ba02ce143ec734809a1e70a467d400fa.nq.gz
│   ├── edb315e4c56fcb2e91359e7b2c07ef476a54376b.nq.gz
│   └── ee230164dec3700669ff5ffb775aed068d3793ea.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 63d1898b811956d4b38147b53ca6ef3a2314b3fd.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 34 files
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

[rasterio/affine](https://github.com/rasterio/affine)

---
*Parsed on 2026-10-15 by [repolex](https://repolex.ai)*
