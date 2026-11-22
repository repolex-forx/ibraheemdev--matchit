# Repolex Knowledge Graph of ibraheemdev/matchit

RDF knowledge graph data for [ibraheemdev/matchit](https://github.com/ibraheemdev/matchit), parsed by [repolex](https://repolex.ai).

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
rlex download ibraheemdev/matchit
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 4b5a2c356022f544187d6e67325d8e98dd7f11ca
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 4b5a2c356022f544187d6e67325d8e98dd7f11ca.nq.gz
│   └── repolex
│       └── 4b5a2c356022f544187d6e67325d8e98dd7f11ca
│           └── chunk-001.nq.gz
├── blob
│   ├── 0587fdb2d270d78e468440c6c1b2088520f08401.nq.gz
│   ├── 1c18afcd284514bcbc2081ce229c3335e75624b7.nq.gz
│   ├── 26929e3c089439c4a9175b92f986f6d6e05cbad2.nq.gz
│   ├── 32bd3cd760cd5249863b7628db5f3109ba777777.nq.gz
│   ├── 50292d5068ef024d418480c6ff6fa06641df12af.nq.gz
│   ├── 572e03bdf321b6cc3a99488183436905cefd086d.nq.gz
│   ├── 6118b68f720ae977b46ebe33d0699a9c4e3832fc.nq.gz
│   ├── 6d0bec4ebdf3d2bf36b17ca3d7aac3c299ff652b.nq.gz
│   ├── 6ef310b7ab7152a329efae12e13858fcc101cbb3.nq.gz
│   ├── 7abbab7f170059d4a41ef1ca7150c4eb5e0b65c1.nq.gz
│   ├── 7edcdf984ebca7379587fdb5f182cd150bd5c80f.nq.gz
│   ├── 82859ff17154adbcd2069483b1b1ccac61e394d6.nq.gz
│   ├── 82e9b038b6c58f768750f54fdf3e5ec0b3148081.nq.gz
│   ├── 875308f5235f5b8f91a7b6513c82ed171c9b3af2.nq.gz
│   ├── 90aefd42c075f5ccb672276351f4ef4d4267788a.nq.gz
│   ├── 939b767eb0268f459f1eec0cdca96719272437cf.nq.gz
│   ├── 96ef6c0b944e24fc22f51f18136cd62ffd5b0b8f.nq.gz
│   ├── 97b20f76d2bc9935306d71d630bc5f0876b4bda0.nq.gz
│   ├── b76a2064642b11563c3c53668e1a599beeeb4e9b.nq.gz
│   ├── d39a0d6f419a885d19289043ace4b60f81e47060.nq.gz
│   ├── e8cb498cedf0426474972ec403e60fd63b1c0a27.nq.gz
│   ├── f11ec284696df6f79d4128066f81d7014a0dd43b.nq.gz
│   ├── f7c9a2d3f836acf8e583626c86ddb1589de25f5b.nq.gz
│   ├── f7f5ec45f3fe6c7459962e891179dde4960bb817.nq.gz
│   └── fed5385bf1ca2f7524a96de0e68bb3ab72bc58f5.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 4b5a2c356022f544187d6e67325d8e98dd7f11ca.nq.gz
├── filetree
│   └── 4b5a2c356022f544187d6e67325d8e98dd7f11ca.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 35 files
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

[ibraheemdev/matchit](https://github.com/ibraheemdev/matchit)

---
*Parsed on 2026-11-22 by [repolex](https://repolex.ai)*
