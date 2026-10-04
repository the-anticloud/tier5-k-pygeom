# HF_Leaderboard_Lab_Results

**Project:** `K_PYGEOM`  
**Tier:** `TIER_5_WORLD_NEURO_EMBODIED`  
**Slug:** `pyg-team/pytorch_geometric`  
**Commit:** `79d33965a40b`  
**Run:** `2026-09-30T15:07:07.146295+00:00`  

## Isolation Environment

| Field | Value |
| ----- | ----- |
| Platform | `win32` |
| Python | `3.12.10` |
| HF model | `distilbert-base-uncased` |
| HF load time | `4.42s` |
| Inference device | `cpu` |

## Results

**Framework:** [HuggingFace Open LLM Leaderboard (proxy via distilbert-base-uncased)](https://huggingface.co/docs/leaderboards/en/open_llm_leaderboard/archive)

**Model used:** `distilbert-base-uncased`

### Inference Latency (Classification)

| Metric | Value |
| ------ | ----- |
| Avg latency | **144.14 ms** |
| Min latency | 81.67 ms |
| Max latency | 270.41 ms |
| Samples | 5 |

### Real Tokenization Results

| Field | Value |
| ----- | ----- |
| Token count | **43** |
| Tokenization latency | 0.0 ms |
| Classification label | `LABEL_0` |
| Classification score | 0.5936 |
| Classification latency | 342.39 ms |
| Status | **PASS** |

**Input text tokenized:**
```
K_PYGEOM (pyg-team/pytorch_geometric) — 1548 files, 192074 source lines, licence MIT, primary language ['Python']
```

**First 20 tokens:**
```
['[CLS]', 'k', '_', 'p', '##y', '##ge', '##om', '(', 'p', '##y', '##g', '-', 'team', '/', 'p', '##yt', '##or', '##ch', '_', 'geometric']
```

> Full MMLU/HellaSwag/TruthfulQA/ARC/Winogrande/GSM8K require dedicated GPU.
> These results are CPU inference proxy metrics using distilbert-base-uncased.

---
_Anticloud Benchmark Suite — isolation log — 2026-09-30T15:07:07.146295+00:00_