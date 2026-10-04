# Ledger Status

**Project:** `K_PYGEOM`  
**Tier:** TIER_5_WORLD_NEURO_EMBODIED  
**Identity:** Upstream `pyg-team/pytorch_geometric` @ `79d33965a40b` (MIT)

## Chain state

| Fact | Value |
| --- | --- |
| Upstream | `pyg-team/pytorch_geometric` |
| Commit | `79d33965a40b7fa83616a9f598a0f8619f25d939` |
| Upstream licence | MIT |
| Licence class | permissive |
| Clone size | 10.39 MB |
| Ledger | 0 blocks, chain verified |
| Current TRL | NOT YET MEASURED |
| Post-optimisation TRL | NOT YET MEASURED |
| II budget cap | 1000.0 IIU |
| Verified upstream edits | 1 |

- Blocks: **0**
- Head digest: `None`
- Chain verification: **verified**

## Independent verification

The chain is verifiable without trusting this project's tooling:

```
anticloud ledger verify
anticloud ledger export > ledger.jsonl
```

Each block carries the previous block's digest, so removing or reordering an
entry invalidates every block after it. That property is the reason the
ledger can stand in for a claim of what happened.
