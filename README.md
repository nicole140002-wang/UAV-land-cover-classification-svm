# UAV Land Cover Classification using SVM (ArcGIS Pro)
Supervised object-based land cover classification using drone multispectral imagery and Support Vector Machine (SVM) in ArcGIS Pro.

<img width="679" height="590" alt="image" src="https://github.com/user-attachments/assets/b10308ec-ad1f-412a-809f-ff162590e0b2" />

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
Data used in this project was provided for educational purposes as part of GISC412 coursework of University of Canterbury.

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
<img width="487" height="398" alt="image" src="https://github.com/user-attachments/assets/6c8071c8-4c9b-4507-ad29-7c3eb21b4b7a" />

#### 2. Training Samples
<img width="506" height="370" alt="image" src="https://github.com/user-attachments/assets/50bdfcf1-7993-4291-a8c0-7674fa887bb0" />

<img width="695" height="298" alt="image" src="https://github.com/user-attachments/assets/90806905-207a-439a-90e7-5ae89ccb18fd" />

<img width="474" height="341" alt="image" src="https://github.com/user-attachments/assets/677a7599-1039-4118-8a6b-c4ebcd738b03" />

<img width="513" height="390" alt="image" src="https://github.com/user-attachments/assets/20f5ceb2-b2c2-463a-9f87-531948b31d9c" />

<img width="432" height="555" alt="image" src="https://github.com/user-attachments/assets/97e29dab-d589-4be0-9258-520eb80f6aee" />


#### 3. Raw Classification Output
<img width="653" height="508" alt="image" src="https://github.com/user-attachments/assets/7c6d8b47-bec5-4ba3-988d-19169ac98d8e" />

#### 4. Final Corrected Classification Map
<img width="679" height="590" alt="image" src="https://github.com/user-attachments/assets/b10308ec-ad1f-412a-809f-ff162590e0b2" />

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

