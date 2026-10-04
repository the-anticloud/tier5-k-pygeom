# How to Operate — K_PYGEOM
**Platform:** Anticloud | **IP:** USPTO pending 2026, Anticloud FZ LLE, 0-1.gg

## Module Overview
K_PYGEOM — PyGeom: geometric deep learning on graphs for molecular and spatial Anticloud data
Stack: Python 3.11, PyTorch Geometric 2.5+, PyTorch 2.10+, PAX 27B, AIOSS_FORMAT

## Daily Operations
1. `aioss verify --chain ./k_pygeom.aioss`
2. Check service health via api-oss-monitor
3. Review api-oss-logging for error-level events
4. Confirm PAX 27B is loaded and responding

## Incident Response
- Chain tamper: halt, notify compliance, restore from backup
- GPU OOM: reduce batch size, check memory leak
- High latency >2s P99: check queue depth, scale workers
- Compliance gap: run api-oss-compliance report

## Backup (nightly)
```bash
python -m api_oss_backup backup --sources ./k_pygeom.aioss --output ./backups/
```
