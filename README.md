# 3D-mapping-using-qgis
# 🛰️ 3D Terrain Mapping Using Drone Imagery and QGIS

This project explains the end-to-end process of creating 3D terrain models using aerial imagery captured via drones and processed using **QGIS** and **open-source photogrammetry tools**.

Due to company confidentiality, raw image and DEM data are not included—but all procedures are thoroughly documented so this workflow can be reproduced independently.

---

## 🌍 Objective

Generate 3D topographic maps and elevation models using drone-acquired imagery and visualize them in QGIS for analysis and presentation.

---

## 🧰 Tools & Software Used

| Tool         | Purpose                              |
|--------------|---------------------------------------|
| **Drone**    | Aerial image acquisition              |
| **QGIS**     | GIS processing and visualization      |
| **OpenDroneMap / WebODM** | Photogrammetry & DEM/Orthomosaic generation |
| **MeshLab / CloudCompare** | 3D point cloud editing (optional) |

---

## 🚁 Step-by-Step Workflow

### 1. **Drone Flight & Image Capture**
- Plan your flight using apps like **Pix4Dcapture**, **DroneDeploy**, or **DJI GS Pro**.
- Maintain at least **60–80% image overlap** (front & side).
- Ensure consistent altitude and lighting.

### 2. **Geotagging**
- Use onboard GPS or log coordinates during capture.
- If available, use RTK/PPK for higher accuracy.

### 3. **Photogrammetry Processing (OpenDroneMap / WebODM)**
- Input: Raw drone images.
- Output:
  - **Orthophoto (GeoTIFF)**
  - **Digital Elevation Model (DEM)**
  - **3D point cloud (LAZ/PLY)**

Steps in WebODM:
```bash
# Example WebODM CLI command (if not using GUI)
./webodm.sh start
