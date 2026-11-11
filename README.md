# GenAI Engineer Interview Handbook

An interactive, single-page study guide for AI Engineer, GenAI Engineer, ML Engineer and Research Scientist interviews. Open [`index.html`](index.html) in a browser. No build step or server is needed.

## What's inside

Eight parts, each with a concept guide, an interactive diagram or calculator, and detailed interview questions:

| Part | Topics |
| --- | --- |
| 1. Transformers & BERT | Attention maths, multi-head attention, positional encoding, BERT, GQA / MLA / MoE / SSM |
| 2. Generative AI | Model families, diffusion, multimodal models, alignment, risks |
| 3. LLMs | Training pipeline, LoRA / QLoRA, KV cache, sampling, quantization, serving |
| 4. RAG | Chunking, hybrid search, reranking, GraphRAG, agentic RAG, evaluation |
| 5. Agentic AI | Agent loop, workflow patterns, tool calling, MCP, A2A, multi-agent, safety |
| 6. Harness Engineering | Loop, tools, permissions, hooks, long-running agents |
| 7. Context Engineering | Context rot, budgets, compaction, memory, sub-agents, caching |
| 8. HSBC Manager, Data & Analytics | SQL optimisation and window functions, star/snowflake and SCD, imbalance, SHAP, drift, RAG for policy docs, 4 banking case studies, STAR stories, governance (GDPR, BCBS 239, model risk) |

Features:

- 147 interview questions (including 50 HSBC-specific) with detailed answers, tagged Basic, Intermediate or Advanced
- 9 interactive architecture diagrams (click a block, or press Play to step through)
- 6 labs: attention heat-map, KV-cache calculator, sampling, chunking, hybrid-search fusion and context budget
- 10-question self-test quiz
- Search across all questions (press `/`), light and dark themes, contents sidebar

## Project layout

| Path | Purpose |
| --- | --- |
| `index.html` | The finished page (self-contained; fonts load from Google Fonts) |
| `_build_hsbc/` | Part 8 sources (`part8.html`, `qa_hsbc.js`, `qa_hsbc2.js`); `merge.py` and `merge2.py` were one-off merges into `index.html` (do not re-run) |
| `_build/` | Source pieces `index.html` is assembled from (git-ignored) |

To rebuild `index.html` from `_build/`:

```bash
cd _build
{ cat a_head.html b_part1_2.html c_part3_7.html; echo '<script>'; cat d_qa1.js e_qa2.js f_app.js; echo '</script>'; echo '</body></html>'; } > ../index.html
```

## Sources and caveats

Part 8 topics come from candidate-reported HSBC interview guides (Dataford, Revarta, AmbitionBox, Uncodemy, LinkedIn). They are not official HSBC material. Example STAR answers use illustrative numbers: replace them with your own real results. Verify current regulation details for your jurisdiction.

Agent, harness, context-engineering and MCP material follows Anthropic's engineering posts and the MCP documentation. The Transformer and BERT section follows the supplied study notes. Web search was unavailable when this was written, so verify any 2026-specific paper claims before quoting them in an interview.

## License

See [`LICENSE`](LICENSE).
