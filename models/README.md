# Evaluated Models

All model calls used the OpenRouter OpenAI-compatible API. Friendly names map
to the following exact OpenRouter identifiers.

| Paper name | Internal key | Exact model identifier |
|---|---|---|
| Gemma-3 4B | `gemma-4b` | `google/gemma-3-4b-it` |
| Gemma-3 12B | `gemma-12b` | `google/gemma-3-12b-it` |
| Gemma-3 27B | `gemma-27b` | `google/gemma-3-27b-it` |
| Gemini-2.5-Flash | `gemini-flash` | `google/gemini-2.5-flash` |
| Gemini-2.5-Pro | `gemini-pro` | `google/gemini-2.5-pro` |

Generation used temperature 0 and an 8,192-token WBT output budget. The
structured compiler used a 4,096-token output budget. No seed was supplied.
Full-system experiments allowed at most three diagnostic LLM repair rounds,
with deterministic correction and validation after every revision.

OpenRouter may select an available backend provider for a requested model.
Accordingly, the requested model identifier is the stable experimental
identifier; returned model and provider metadata were recorded per API call
in the experiment logs. Local Webots evaluation does not contribute to the
reported provider cost.
