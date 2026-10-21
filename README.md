# Repolex Knowledge Graph of explosion/curated-tokenizers

RDF knowledge graph data for [explosion/curated-tokenizers](https://github.com/explosion/curated-tokenizers), parsed by [repolex](https://repolex.ai).

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
rlex download explosion/curated-tokenizers
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── e11413cfb56ddf1c42cc6c003d1e1f3b6a3e7993
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── e11413cfb56ddf1c42cc6c003d1e1f3b6a3e7993
│           └── chunk-001.nq.gz
├── blob
│   ├── 0ecb2ab8f2005c89dae121906f5b9751c67ccad8.nq.gz
│   ├── 15ed99bd893cc5e0cab028faa4f22096ca2c104f.nq.gz
│   ├── 21e0acf6c5246b25ee72641b3012c166124f03b6.nq.gz
│   ├── 396014a3b3242364ec72d9a224afaf3739b2d98f.nq.gz
│   ├── 3af8060dba870aac31bba2badb5c2ad1f3847bbc.nq.gz
│   ├── 412d6b8b5d3fd68be47fd1ccfd388a100e12a1a2.nq.gz
│   ├── 4c5e8410a7a2213096b2efd32e5fd1b223ea7917.nq.gz
│   ├── 4fdeaf1e992e39254527f0e92b94c349eb0fb491.nq.gz
│   ├── 527949ab540bc260cf84de7f66e3e4ca23825b57.nq.gz
│   ├── 5713ee060fcdc64d5c2062e300aa6142d5ac5bfc.nq.gz
│   ├── 5ada135e88b78b3c9126ff53d7e06eacff31b099.nq.gz
│   ├── 6bd1bcf123ec19d714726a5d0946fb323262400f.nq.gz
│   ├── 6e6ec22c90a0907641d875ce4b30d85815bff5d0.nq.gz
│   ├── 72618d7e98f396c4182f816c44b07a50bf88dcc3.nq.gz
│   ├── 729e5a055e0002dbb9b89d0f519ab9dba56e3448.nq.gz
│   ├── 7877c125c098541edd5d54de7f41badd05d05bd6.nq.gz
│   ├── 78d2aa13295ed39491a41558eea0752f883c88c4.nq.gz
│   ├── 7b1d0cd323c8c15101ab2f5d8e9397569428db1b.nq.gz
│   ├── 7b8d799ee5e0106118627bda52bf0ffe5a3edd15.nq.gz
│   ├── 7ba059caef01967cc8781c123ab83d139321b3b6.nq.gz
│   ├── 81c6e7d61b5c56ba365801778226151a30dbb4a9.nq.gz
│   ├── 892d27d381f1c81063dbf7414a0f0086996c8980.nq.gz
│   ├── 96350ae32eacc698a5bae5df6e7ffe8ec827975d.nq.gz
│   ├── 97eaada38ccc2f89f8be8d8f2c92d8d04253eaf1.nq.gz
│   ├── ae3d97d7d63a9ef90a56d1ba183915362720e44f.nq.gz
│   ├── b0e1243b02106c0b4b945a4be867e4ccf4e72c8a.nq.gz
│   ├── b9a8080b68755a16b46fd75a547031a6cd1d2dd1.nq.gz
│   ├── bd2a1576cb308d49f85941cd708f36fa8f1d264a.nq.gz
│   ├── c00097a7cb17118731258c8d25ea9a8dbffde151.nq.gz
│   ├── c2d5b4c10f5e406b5566e59e787840cbbfe6f65e.nq.gz
│   ├── cb0f70dcb490df1eaf73af01daf69bec80e43e16.nq.gz
│   ├── d6dbd3317f4f58078084639bc9a8653f57176593.nq.gz
│   ├── ddc0fcc52af8c335d1ebe3581d450e2ffc9a23ba.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e83adbab141cbb33025ee92beb80edae48d817e2.nq.gz
│   ├── eb64284f9b71a7043ee7b142008153ba78ef1891.nq.gz
│   ├── f2aaf9d77e60e05ccc0f3e4843c5bce4e59c3623.nq.gz
│   ├── f3ca38a3f42a31fe81bbd65904b20bdb2fb170bc.nq.gz
│   ├── fb4808a9151a95e3f4c3a455e711b41b2cd8b5ae.nq.gz
│   └── fbc8e7e73a6b6739439d6238b884c442cc4bd048.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── e11413cfb56ddf1c42cc6c003d1e1f3b6a3e7993.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 48 files
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

[explosion/curated-tokenizers](https://github.com/explosion/curated-tokenizers)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
