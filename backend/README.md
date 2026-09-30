# AeroCAD GeoAI Backend v0.5

Endpoints:
- `GET /api/health`
- `POST /api/projects/validate`
- `POST /api/projects/{project_id}/process`
- `GET /api/projects/{project_id}/process`
- `GET /api/projects/{project_id}/outputs/{filename}`

Processing tiles the ORI, reads aligned DSM windows when available, runs a configurable semantic-segmentation adapter, polygonizes the masks, and persists `buildings.geojson` and `roads.geojson`.

When the optional model cannot be loaded, the service reports `baseline` mode and uses a conservative fallback instead of claiming that a trained cadastral model ran.
