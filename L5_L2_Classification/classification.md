# L5 Narrow / L2 General Classification — K_PYGEOM
**Platform:** Anticloud | **Tier:** TIER_5_WORLD_NEURO_EMBODIED | **PAX:** 27B
**IP:** USPTO pending 2026, Anticloud FZ LLE, 0-1.gg | **License:** Apache-2.0

## L5 Narrow
K_PYGEOM applies graph neural networks (GNNs) to Anticloud geometric data: molecular graphs for TIER_7 drug interaction analysis, spatial graphs for TIER_9 robot environment mapping, and knowledge graphs for TIER_4 inference. Narrow scope: Anticloud geometric AI tasks.

## L2 General
L2 General: K_PYGEOM's GNN capabilities benefit any tier with graph-structured data. Molecular graphs in TIER_7 and spatial scene graphs in TIER_9 both use the same PyTorch Geometric infrastructure.

## PAX 27B Integration
PAX 27B provides graph construction from natural language: given a molecular SMILES or a scene description, PAX extracts the graph structure that K_PYGEOM then processes with GNNs.

## AIOSS Audit Chain
Every GNN inference (graph hash + node/edge feature hash + model output hash + task-specific metric) is chained: H_n = SHA3-256(H_{n-1} || entry_hash_n || timestamp_n).
Offline-verifiable, tamper-evident, zero cloud dependency.

## Regulatory / Compliance
No external regulatory. ISO/IEC 42001 (AI system documentation for GNN applications).
