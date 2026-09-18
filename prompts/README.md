# Prompt Templates

The prompt package records source assets and human-readable rendered
components. Dynamic values such as the scene description and retrieved catalog
entries are inserted at runtime.

## Direct generation

The direct pipeline asks the model to emit a complete Webots `.wbt` world.

| Strategy | Model-visible content |
|---|---|
| S0 | Task only |
| S1 | Task + structural rules |
| S2 | Task + structural rules + retrieved catalog definitions |
| S3 | Task + structural rules + fixed demonstrations |
| S4 | Task + structural rules + retrieved catalog definitions + demonstrations |

## Structured generation

The structured pipeline first compiles natural language into JSON and then
uses a JSON-to-WBT prompt. The rendered compiler template and structured
demonstrations document the model-visible content of these two stages.

## Prompt artifacts

- `assets/structural_rules.txt`: source rules with research comments;
- `assets/fewshot_examples*.yaml`: direct and structured demonstrations;
- `rendered/structural_rules_model_visible.txt`: exact rules after comment
  filtering;
- `rendered/retrieved_catalog_example.txt`: catalog block retrieved for held-out
  scene `t4h_01_kitchen_cabinet_variant`;
- `rendered/fewshot_*_model_visible.txt`: formatted demonstrations;
- `rendered/compiler_user_template.txt`: compiler presentation template with
  dynamic values replaced by placeholders;
- `rendered/s4_cot_instructions.txt`: separate direct S4-CoT ablation text,
  not part of ordinary headline S4.

For ordinary S4 the direct user-message order is rules, retrieved schema,
examples, then the scene task. Retrieval is scene-dependent; therefore the
provided rendered catalog is one concrete example rather than a universal
static prompt.
