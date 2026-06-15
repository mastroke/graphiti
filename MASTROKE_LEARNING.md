# Mastroke Learning Notes

Personal study notes while building [memory-layer-rnd](https://github.com/mastroke/memory-layer-rnd).

## Patterns extracted from Graphiti

- Facts need `valid_at` and `invalid_at`, not just latest value wins
- Episodes carry `reference_time` and provide provenance
- Contradictions invalidate old facts instead of deleting them
- Retrieval must support as-of queries

## Implemented in memory-layer-rnd

- `TemporalFact`
- `episodes_before()`
- `active_facts_at()`
- invalidation in `add_fact()`

## Suggested upstream reading

- `graphiti_core/graphiti.py`
- `graphiti_core/edges.py`
- `graphiti_core/utils/maintenance/edge_operations.py`
