# LLMebots: From Natural Language to Validated Webots Worlds

Anonymous supplementary material for a submission to DATE 2027.

This repository documents experimental inputs and qualitative examples that
could not be included in the main paper.

## Contents

- [models/README.md](models/README.md): evaluated model names, exact API
  identifiers, and inference conventions; `models/models.json` provides the same
  information in machine-readable form.
- [prompts/README.md](prompts/README.md): prompt composition and strategy definitions;
- [datasets/README.md](datasets/README.md): YAML scene requests and evaluation
  specifications for T1-T3 and the held-out T4 benchmark.
- [qualitative/README.md](qualitative/README.md): prompts and
  before/after images used for qualitative illustration.

## Scope

The dataset files contain both the natural-language request and its evaluator
specification. T1, T2, and T3 contain 20 scenes each. T4 contains only the
30-scene held-out benchmark used for headline evaluation. The separate T4
development set is deliberately excluded.