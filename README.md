# Repolex Knowledge Graph of jupyter/cookiecutter-docker-stacks

RDF knowledge graph data for [jupyter/cookiecutter-docker-stacks](https://github.com/jupyter/cookiecutter-docker-stacks), parsed by [repolex](https://repolex.ai).

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
rlex download jupyter/cookiecutter-docker-stacks
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 68410a7827ca33e8126bb31a9fb3bc93287d55ac
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 68410a7827ca33e8126bb31a9fb3bc93287d55ac
│           └── chunk-001.nq.gz
├── blob
│   ├── 00841af17780d8e4309ddf722fa5e511295610a0.nq.gz
│   ├── 11ee22634326f08bd28581fb10b11415ec3d0982.nq.gz
│   ├── 11eec270a81f86917fb7a938bbdb0bfc743d16eb.nq.gz
│   ├── 1882f2a623eaa533050d5b378ed5bb63f0295563.nq.gz
│   ├── 1b3d5259ec61e0d017b0408d593c35057e6b3823.nq.gz
│   ├── 20b6bb1b78204406a976cd19235ceffb412b46a8.nq.gz
│   ├── 247e5e32a38d3cff2d379d2d51d26e2ae5d8b503.nq.gz
│   ├── 2919f296e568b46c246ca76094975702619f52fe.nq.gz
│   ├── 2d51385a7df329a5b16089d08f01e4400fa7576e.nq.gz
│   ├── 468abc3814cd720872b968358e6816eefb0f2056.nq.gz
│   ├── 54ec1a9521b77790a57dd68bb1af5f1493351dac.nq.gz
│   ├── 55ad0a0af60f2c8838c4f59b3416acadc01ae614.nq.gz
│   ├── 5d1d7e16df13d5a5b6dd86cfe328e61da6917159.nq.gz
│   ├── 6263da99b5b8c4f78776eb4719d420c9b0f2d24f.nq.gz
│   ├── 6313b56c57848efce05faa7aa7e901ccfc2886ea.nq.gz
│   ├── 6dd457c29d04bac53128996d69d2560ec5ddf501.nq.gz
│   ├── 798b58f426416d69cf6f7342901bb37bdffc5b25.nq.gz
│   ├── 7e79756d5c803de45d392ef52edf6be59e800a50.nq.gz
│   ├── 7f9d6b07b1cc4364b45d632a12063302f9853979.nq.gz
│   ├── 80623aebad99a3168302998beac552122593d6e0.nq.gz
│   ├── 813748c3394824e4093e1249dc88c5e81d246ea0.nq.gz
│   ├── 92c562e38764e53162e84c36e75af900d8177b0d.nq.gz
│   ├── a609f12d9c57488766bb65b2672e70f4cb29376f.nq.gz
│   ├── a6b401d3462a20755c9514d553f1abff483d53f0.nq.gz
│   ├── a7ba2e95e3fe8bd2b04ac17a651305db9d13a1f8.nq.gz
│   ├── b65928871eb5210d025a33403243469ad3c7fd04.nq.gz
│   ├── b9915ec5ca2ad2fb84696e07776fe473df416448.nq.gz
│   ├── c8e988bc24cdfa6a60bd309ffb5002df61845b29.nq.gz
│   ├── ca2174588d6fb2bd390b7b31bccb08e4057b442c.nq.gz
│   ├── ce15813043a3c07953fe644b4024f4c065cbe50d.nq.gz
│   ├── ce8b17f64c6ee444c5f45a1647eb7401d150923f.nq.gz
│   ├── d2df882e8955560a1e558c69d22f97b0400d7b50.nq.gz
│   ├── d8fe003789d9d090085d2db0eb5b95d54d59bc27.nq.gz
│   ├── e1946d50a613037dbabe46da899b40dac406c112.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f65191c5b3416438692f203c68a6ede9376e2ebb.nq.gz
│   ├── f703d8458f2bafc4ca4528945f61ab2c834bb5f4.nq.gz
│   ├── f78cb91e46981fd6e08c94e2c5547fcb574504b2.nq.gz
│   └── f9d501e3b03ccde442a5fa57f23848184c1fb5a1.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 68410a7827ca33e8126bb31a9fb3bc93287d55ac.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 46 files
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

[jupyter/cookiecutter-docker-stacks](https://github.com/jupyter/cookiecutter-docker-stacks)

---
*Parsed on 2026-10-28 by [repolex](https://repolex.ai)*
