# Deploy Guide — K_PYGEOM
**Tier:** TIER_5_WORLD_NEURO_EMBODIED | **Stack:** Python 3.11, PyTorch Geometric 2.5+, PyTorch 2.10+, PAX 27B, AIOSS_FORMAT
**Air-gap capable after initial setup.**

## Prerequisites
Python 3.11+, torch-geometric 2.5+, PyTorch 2.10+, T4 GPU. CUDA 12.x.

## Environment
T4 GPU. 16GB RAM. torch-geometric requires CUDA for GPU-accelerated message passing.

## AIOSS Integration
```bash
aioss init --module K_PYGEOM --output ./k_pygeom.aioss
aioss append --chain ./k_pygeom.aioss --payload ./output.bin --module K_PYGEOM
aioss verify --chain ./k_pygeom.aioss
```

## Air-Gap Setup
```bash
pip download -r requirements.txt -d ./wheels/
pip install --no-index --find-links ./wheels/ -r requirements.txt
```

## PAX 27B Harness Wiring
```python
from anticloud_pax import PAXHarness
harness = PAXHarness(
    model_path="./pax-27b-q4.gguf",
    module="K_PYGEOM",
    aioss_chain="./K_PYGEOM.aioss",
    classification="L5_NARROW_L2_GENERAL"
)
result = harness.process(input_data)
```

## Verification
```bash
aioss verify --chain ./K_PYGEOM.aioss --verbose
python -m K_PYGEOM.tests.smoke
```
