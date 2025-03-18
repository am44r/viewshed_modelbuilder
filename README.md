# 📍 GGR321 - Viewshed & Least Cost Path Analysis  

## 📖 Overview  
This project is a Geographic Information Processing assignment for GGR321. The objective is to conduct **Viewshed Analysis** to determine the best sightseeing location on a mountain and perform a **Least Cost Path Analysis** to design an optimal hiking trail connecting the urban area to the sightseeing spot.  

## 🎯 Objectives  
- Conduct **Viewshed Analysis** to determine which candidate location provides the best visibility of the urban area.  
- Perform **Least Cost Path Analysis** to design a hiking trail considering elevation and land cover.  
- Use Digital Elevation Model (DEM) and Land Use data for spatial analysis.  

## 🗺️ Data Used  
The dataset is stored in a File Geodatabase (`Data/Data.gdb`) and includes:  
- **Candidate Spots**:  
  - `CandidateSpot_A`  
  - `CandidateSpot_B`  
  - `CandidateSpot_C`  
- **LandUse**: Urban and other land cover types.  
- **DEM (Digital Elevation Model)**: Elevation data of the region.  

## 🔧 Tools & Software  
This project was implemented using ArcGIS Pro and the built-in tools 
- **Python Libraries**:  
  - `Viewshed`
  - `Con`  
  - `Reclassify` 
  - `Times` 
  - `Raster to poly`  
- **Other Tools**:  
  - **QGIS Processing Toolbox** (for Viewshed & Cost Path Analysis)
 
## 📌 Implementation Steps  

### 1️⃣ Viewshed Analysis  
1. Load the **Digital Elevation Model (DEM)** and **Candidate Spots** from `Data/Data.gdb`.  
2. Run **Viewshed Analysis** for each of the three candidate spots (`CandidateSpot_A`, `CandidateSpot_B`, `CandidateSpot_C`).  
3. Generate three maps displaying:  
   - The elevation background.  
   - The visible areas from each candidate spot.  
   - The urban area visible from each spot.  
4. Compare the viewshed results to determine which candidate offers the **largest urban visibility**.  
5. Justify the selected sightseeing spot using visibility coverage calculations.  

### 2️⃣ Least Cost Path Analysis  
1. Load the **DEM** and **Land Use** data.  
2. Calculate the **Slope Raster** from the DEM to account for terrain difficulty.  
3. Reclassify land cover types to assign movement costs:  
   - Urban areas (high cost).  
   - Forested areas (moderate cost).  
   - Open land (low cost).  
4. Compute the **Cost Surface** by combining slope and land cover cost rasters.  
5. Use **Least Cost Path Analysis** to determine the optimal hiking trail from the **urban area to the selected sightseeing location**.  
6. Generate a final **Least Cost Path Map** showing the best trail option.  



