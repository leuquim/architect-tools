# architect-tools

Claude Code plugin that bundles public-data MCP servers for Lenovo HPC/AI architects:

| Server | Source | What it answers |
|---|---|---|
| `lenovo-press` | dependency plugin | Product guides, part lookup across guides, guide comparison, OS support, benchmarks |
| `lenovo-dcsc` | dependency plugin | List prices and solution blueprints |
| `nvidia-dsx` | remote, `https://docs.nvidia.com/dsx/_mcp/server` | NVIDIA AI-factory reference designs: rack power and cooling basis, network roles |

`lenovo-xconfig` (the x-config engine, the authority on parts and rules) is a separate plugin in the same marketplace for licensed internal users; it is not a dependency because its repository is private. When installed and sources disagree on a part, believe x-config. DSX answers are generated summaries with source URLs; confirm figures on the linked page.

Install (Node 22+):

```bash
claude plugin marketplace add leuquim/lenovo-architect
claude plugin install architect-tools@lenovo-architect
```

MIT licensed.
