# UAV Land Cover Classification using SVM (ArcGIS Pro)
Supervised object-based land cover classification using drone multispectral imagery and Support Vector Machine (SVM) in ArcGIS Pro.

<img width="342" height="291" alt="image" src="https://github.com/user-attachments/assets/b10308ec-ad1f-412a-809f-ff162590e0b2" />

## Project Overview
This project performs land cover classification using UAV multispectral imagery in ArcGIS Pro.
The goal is to classify the study area into five land cover types:
1) Buildings
2) Grassland
3) Forest
4) Roads
5) Water bodies

The workflow uses object-based image analysis (OBIA) and a supervised Support Vector Machine (SVM) classifier, followed by post-processing refinement.

## Study Data
1) UAV multispectral imagery (5 bands)
2) Training samples created manually
3) NDVI derived from multispectral bands
Data used in this project was provided for educational purposes as part of GISC401 coursework of University of Canterbury.

## Methodology
#### 1. Data Preparation
1) Loaded UAV multispectral imagery in ArcGIS Pro
2) Generated NDVI from multispectral bands
3) Inspected spectral characteristics of land cover types

### 2. Training Samples
Created training samples for 5 classes: Buildings/Grass/Forest/Roads/Water
Approximately 10 samples per class

### 3. Object-Based Classification
1) Applied image segmentation (OBIA)
2) Extracted object features from 5 spectral bands
3) Used Support Vector Machine (SVM) classifier
4) Model trained automatically in ArcGIS Pro using training samples

### 4. Post-processing
1) Identified misclassified objects (e.g., shadows, road edges, vegetation overlap)
2) Applied raster calculator for correction
3) Improved classification accuracy

## Results

#### 1. NDVI Map
<img width="342" height="291" alt="image" src="https://github.com/user-attachments/assets/8a38b009-7ab0-4b80-9072-7fe960e90b18" />


#### 2. Training Samples
<img width="342" height="291" alt="image" src="https://github.com/user-attachments/assets/1a4875d6-e4d2-444d-a114-e83f8608bfeb" />
<img width="342" height="291" alt="image" src="https://github.com/user-attachments/assets/c4ac8af4-83a9-4b6a-a835-3465843505b0" />
<img width="342" height="291" alt="image" src="https://github.com/user-attachments/assets/2f491fa2-a914-491f-b8f6-a213a577bc98" />
<img width="342" height="291" alt="image" src="https://github.com/user-attachments/assets/6e4f980e-f5b6-4cbb-b380-8491d207bdb9" />
<img width="342" height="291" alt="image" src="https://github.com/user-attachments/assets/460c20bd-4bcf-4751-a47d-89aae0c16d6f" />



#### 3. Raw Classification Output
<img width="342" height="291" alt="image" src="https://github.com/user-attachments/assets/a2d80aa0-09be-41cf-b7c9-6c84124f0dc0" />


#### 4. Final Corrected Classification Map
<img width="342" height="291" alt="image" src="https://github.com/user-attachments/assets/ebdcc005-86fc-4c7e-9389-98251b9ebc13" />


## Key Findings
1) SVM achieved good separation between vegetation, built-up areas, and water bodies.
2) Misclassification mainly occurred in: Shadows vs water bodies / Road edges vs bare soil / High-reflectance building surfaces vs grass
3) Post-processing significantly improved visual classification quality.

## Limitations
1) Limited number of training samples per class
2) Spectral similarity between roads and bare soil caused errors
3) UAV image resolution leads to shadow-related misclassification

## Skills Demonstrated
1) Remote Sensing Image Classification
2) Object-Based Image Analysis (OBIA)
3) Supervised Machine Learning (SVM)
4) ArcGIS Pro Workflow
5) Raster Post-processing
6) NDVI Analysis
7) Cartographic Visualization

