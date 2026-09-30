# AeroCAD v0.11

AeroCAD is an AI-assisted urban cadastral mapping and verification prototype.

Core workflow:

Data ingestion → geospatial preflight → building/road extraction → land-use evidence → multi-source parcel evidence → candidate parcel generation → topology QC → human editing → field verification → GIS export.

## Run locally

### Backend
```bat
start-backend.bat
```

### Frontend
```bat
start-frontend.bat
```

Backend: `http://127.0.0.1:8000`
Frontend: `http://127.0.0.1:5174`

V0.11 adds a complete GIS export package (GeoJSON, GeoPackage and Shapefile sets) plus validation/QC/audit records, and uses optional DTM data in the terrain-aware baseline signal.

**Important:** outputs are preliminary cadastral candidates and QC evidence; human survey verification remains required before authoritative cadastral use.
