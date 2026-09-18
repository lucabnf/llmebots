# Benchmark Datasets

Each YAML file contains a natural-language `prompt` and a machine-readable
`spec` used only by the evaluator (and by the explicitly labelled gold-JSON
diagnostic). Dataset membership is fixed.

| Tier | Directory | Scenes | Role |
|---|---|---:|---|
| T1 | `T1/` | 20 | Basic objects, attributes, support, and simple relations |
| T2 | `T2/` | 20 | Pairwise and compound spatial constraints |
| T3 | `T3/` | 20 | Multi-object compositional scenes |
| T4 | `T4/` | 30 | Held-out realistic scenes, including facing constraints |

T1--T3 are copied from the canonical `main` benchmark split. T4 is copied
exclusively from the canonical `heldout/T4` split. No T4 development,
ablation, calibration, or tuning scenes are included.

## YAML structure

Typical fields are:

- `id`: stable scene identifier;
- `tier`: benchmark tier;
- `prompt`: natural-language generation request;
- `spec.objects`: requested object instances and support relations;
- `spec.attributes`: requested field/value constraints;
- `spec.relations`: requested spatial or facing relations.

The generator receives the natural-language prompt. Except for the explicit
gold-JSON diagnostic, evaluator specifications are not exposed to generation.
