# Developer Cookbook — K_PYGEOM
**Stack:** Python 3.11, PyTorch Geometric 2.5+, PyTorch 2.10+, PAX 27B, AIOSS_FORMAT
**Domain:** PyGeom: geometric deep learning on graphs for molecular and spatial Anticloud data

## Molecular graph GNN
```python
from k_pygeom import GeometricModel

model = GeometricModel(
    task="drug_interaction_prediction",
    checkpoint="./pygeom_drug_checkpoint/",
    aioss_chain="./pygeom.aioss"
)

# SMILES to graph, then GNN inference
result = model.predict(
    smiles_a="CC(=O)Oc1ccccc1C(=O)O",  # aspirin
    smiles_b="CN1C=NC2=C1C(=O)N(C(=O)N2C)C"  # caffeine
)
print(f"Interaction: {result.interaction_type}, severity: {result.severity}")
```

## Spatial scene graph
```python
from k_pygeom import SceneGraphGNN
scene_model = SceneGraphGNN(checkpoint="./scene_graph_model/")
navigation_cost = scene_model.estimate_path_cost(scene_graph, start, goal)
```

## AIOSS Chain Append
```python
import hashlib, time

def aioss_append(chain_path, payload: bytes, module_id: str):
    entry_hash = hashlib.sha3_256(payload).digest()
    ts = int(time.time_ns()).to_bytes(8, 'big')
    with open(chain_path, 'rb') as f:
        f.seek(-32, 2); prev_hash = f.read(32)
    new_hash = hashlib.sha3_256(prev_hash + entry_hash + ts).digest()
    with open(chain_path, 'ab') as f:
        f.write(ts + entry_hash + new_hash)
    return new_hash.hex()
```
