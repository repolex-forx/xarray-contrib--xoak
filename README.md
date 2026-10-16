# Repolex Knowledge Graph of xarray-contrib/xoak

RDF knowledge graph data for [xarray-contrib/xoak](https://github.com/xarray-contrib/xoak), parsed by [repolex](https://repolex.ai).

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
rlex download xarray-contrib/xoak
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 3aa25f5c8096ed1fbc65711d3314f6b86f371cb7
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 3aa25f5c8096ed1fbc65711d3314f6b86f371cb7
│           └── chunk-001.nq.gz
├── blob
│   ├── 0ac121876c930430fcabeb7583dbb9e129c3f532.nq.gz
│   ├── 0b5238a4bc5de40a40a14297bc6829142c165199.nq.gz
│   ├── 1270209330ea92c2aa5605a25aa012d888182742.nq.gz
│   ├── 2119f51099bf37e4fdb6071dce9f451ea44c62dd.nq.gz
│   ├── 29000dd5331eb1e207dbb4d42fd7fc9205b5f355.nq.gz
│   ├── 419b3797866cf512695779c0af88bb12cfe4dc77.nq.gz
│   ├── 499cff54ce09b753a18de14e92fb20be3b80f933.nq.gz
│   ├── 4bccbbf6a91076de482a842bbd601e1f493efd97.nq.gz
│   ├── 54de5bc76180f7923b9f9b87dc3eea4c999ed4f1.nq.gz
│   ├── 5f89818f9e63c2f6829c7706c57f223cdb5bbd38.nq.gz
│   ├── 61e72466bd90489aff9fe4d567aff68f4bdf1017.nq.gz
│   ├── 7186d182107a1b169cebf2186c00a9bf5e48db71.nq.gz
│   ├── 78444fee2b8c7a0845cea59642bb24d90e5f3e93.nq.gz
│   ├── 7d13de373a8a4dbdae2273f7a5d7516d74a2370e.nq.gz
│   ├── 8964c8369f7f82a606740927ebf4802f08d6b258.nq.gz
│   ├── 8ac6b8c4984dcd382e54c7923325af6d226ca3df.nq.gz
│   ├── 92a9c500f43ed25007688b4630284f892410ae24.nq.gz
│   ├── 98daebe52ed8b05f2303f3f08793290b13834661.nq.gz
│   ├── 99a491fd55026a400708c0819efe865088a5ad90.nq.gz
│   ├── 9aeba0ac54391b21f880ab8739b15f34120e1505.nq.gz
│   ├── 9c660d9c1f476711474177444a0dba4a9d146e3d.nq.gz
│   ├── 9d6b9cff08e222dacdf672bd1ed24e854b2956b7.nq.gz
│   ├── 9d801b1bc54025161f3ecedbec5584df97995b7b.nq.gz
│   ├── a0ae7bf5532763e9d1ff163849ce9ec1678ace49.nq.gz
│   ├── a309b18d5793412a90338c27a17ad88ed3c03c06.nq.gz
│   ├── a4b152220ba87d461a6ec0532fdcd5f6c006c971.nq.gz
│   ├── afd632e39112235fe463476e38b8b2750f36686d.nq.gz
│   ├── b16a456782e0187c39e5bb72fc72f42af1896782.nq.gz
│   ├── b5e3e71b80a529d7ae032bbe6e7ff6a1ad9216f3.nq.gz
│   ├── c28a2930ac8e9f29308781a145d7ec2b00c62af9.nq.gz
│   ├── c54721ad23d5744145f2faf3d4c3db61feef72f7.nq.gz
│   ├── d29962235604b4cd5a4a04251b989b65b02d2217.nq.gz
│   ├── d3fb976216cb7067dbbd02fa6ab327d251c7fb8a.nq.gz
│   ├── d4bb2cbb9eddb1bb1b4f366623044af8e4830919.nq.gz
│   ├── e4d1cf3c8eac246b7b63ff8a0cd0e7e9fe85944f.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f0e3fc1a0f13c283dc0258c8f917c9d0b237ce43.nq.gz
│   ├── f7d8bbb44aabb1cabb170ca7ac5f510f82987050.nq.gz
│   ├── f85a34665b3daad5f60e57cfb74a20dc108265d6.nq.gz
│   ├── f8727806232f33b718f887586518d90571f35ba8.nq.gz
│   └── fa3a26fdb34549edcc773bd3ad45bfef103f0d98.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 3aa25f5c8096ed1fbc65711d3314f6b86f371cb7.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 49 files
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

[xarray-contrib/xoak](https://github.com/xarray-contrib/xoak)

---
*Parsed on 2026-10-16 by [repolex](https://repolex.ai)*
