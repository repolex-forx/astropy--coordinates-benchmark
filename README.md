# Repolex Knowledge Graph of astropy/coordinates-benchmark

RDF knowledge graph data for [astropy/coordinates-benchmark](https://github.com/astropy/coordinates-benchmark), parsed by [repolex](https://repolex.ai).

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
rlex download astropy/coordinates-benchmark
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 34ee5cd04d3abf770307f6f78451712768cce117
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 34ee5cd04d3abf770307f6f78451712768cce117
│           └── chunk-001.nq.gz
├── blob
│   ├── 01ba15846c5465f9d6b2ecfe6e2d9d0c9af66c2d.nq.gz
│   ├── 0a2c4bdec19c56fbbaa412056167e2ad890ff948.nq.gz
│   ├── 0dc220c4e4d2e06391f54caad5dfd0300017b17d.nq.gz
│   ├── 1a218f5e5bc6f6fcf957402a14d721e762095351.nq.gz
│   ├── 207baf7c52487ce9d5016e6e9b885aa76aab0422.nq.gz
│   ├── 30468a72571c2c6c6c39f60d3ff0a2a0cbff4450.nq.gz
│   ├── 3e453d60bad06acce94fb4b97839e4f38a7ab4a4.nq.gz
│   ├── 3f35cc0a5234f91e0e661c6a7b65871a06cc179a.nq.gz
│   ├── 498b93f91cb492af872492a9bda0d8f24e42c358.nq.gz
│   ├── 4b09eebe9972b3cb3a631394e4b664fa968d52e3.nq.gz
│   ├── 5862d08aba57aec1d4c48142812e6d96dd515ec4.nq.gz
│   ├── 6aeef4708292ebbc894165f877ac73170881ea16.nq.gz
│   ├── 6ca9a1a3ec53559b6a9d4c551a46bab74e64fd00.nq.gz
│   ├── 7084748eb9bb7ac5ea26d4cc933d4a31758d3529.nq.gz
│   ├── 769bb43de5bb26e9e4154c30231186aba6adf3bc.nq.gz
│   ├── 7c8fa0b3d9d4a148748d992b1e8553f0329e0501.nq.gz
│   ├── 82878daf16bfbd99107a775b6ce8f3419842c8b1.nq.gz
│   ├── 8c6b9f50d2a3550ed7cdecf11af046961d71471f.nq.gz
│   ├── 8ece07c04dfd6228b74d4ddfdedc8347e5fdae6e.nq.gz
│   ├── 9babe3292cde2afbd1af1082bcc9786c9d854c42.nq.gz
│   ├── 9c8e824724496b270c7de7994501970c342d95c9.nq.gz
│   ├── 9da41a7c7696a2577f6f57bad88c070aed1ebc5f.nq.gz
│   ├── a898e30a6567e861e48dd0ad488fda810357ad0b.nq.gz
│   ├── ac5fbde91613b91d2a58f5dd6bdc3d91c1b2dfbd.nq.gz
│   ├── bb1cdebdee5250fad4dd322e28afce4d08a2b075.nq.gz
│   ├── bb8afad41b28b9f46b115ee88031589ef1f9ed35.nq.gz
│   ├── cb9886b7559c245bac99919f82cf55a0dde8a3f4.nq.gz
│   ├── cf416704f9cf38fbb6273af03b7ce6a1b866e5b9.nq.gz
│   ├── d1b6896b9738e539ea830af77ff69756fcd6423d.nq.gz
│   ├── d605ed2b12742c4d5bc0ce52d7530f0576580a1d.nq.gz
│   ├── e023ddf57bf9874830097990c01996259e6c4fa3.nq.gz
│   ├── e0bf5adc042b2665dcd0554de6b74e08098f3dc0.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e97b46d0b4755bde49798821f6ab46f25b6d06bc.nq.gz
│   ├── ea47bd49e96e97f2ffe730e6931345b263ae6666.nq.gz
│   ├── f37ea48b529e7fec3c04bab139fc329eb1def0f0.nq.gz
│   └── fceb62a3de199c2dfcd54356667e7bb56bddf604.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 34ee5cd04d3abf770307f6f78451712768cce117.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 45 files
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

[astropy/coordinates-benchmark](https://github.com/astropy/coordinates-benchmark)

---
*Parsed on 2026-11-07 by [repolex](https://repolex.ai)*
