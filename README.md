# UAV Land-Cover Classification with Object-Based SVM

Object-based supervised classification of five-band UAV multispectral imagery over Cass Field, New Zealand, into five land-cover classes: **built-up areas, grassland, forest, roads, and water**.

<img width="590" height="566" alt="image" src="https://github.com/user-attachments/assets/76e605a1-fc90-48c9-8ff1-5b7369bdba2e" />

## Overview

The imagery has very high spatial resolution, so individual pixels contain substantial local variation from vegetation texture, shadows, bare ground, and building materials. A purely pixel-based classifier therefore produced fragmented results and visible salt-and-pepper noise.

To improve spatial consistency, the image was first segmented into meaningful objects and then classified with a Support Vector Machine (SVM) in ArcGIS Pro. SVM was selected because it can work effectively with limited training samples and multi-band input data.

## Study Area and Imagery

The study focused on Cass Field in Canterbury, New Zealand. The input was five-band multispectral imagery collected by a DJI UAV at approximately 0.05 m spatial resolution. The very high resolution captured detailed vegetation texture, buildings, roads, shadows and bare ground, but also increased within-class spectral variation and pixel-level noise.

The classification mapped five land-cover classes: built-up areas, grassland, forest, roads and water.

## Method

1. Used all five spectral bands without dimensionality reduction.
2. Segmented the UAV image into spatially coherent objects.
3. Manually labelled representative samples for each land-cover class.
4. Trained an object-based SVM classifier.
5. Reviewed the output and corrected clear spectral-confusion errors with raster-based rules.

![Pixel-based and object-based comparison](pixel_vs_object_classification.png)

The object-based result forms more continuous land-cover patches, while the pixel-based output is more fragmented and sensitive to small spectral variations.

## Key Results

The final map clearly separates the dominant forest and grassland areas while preserving smaller features such as buildings, roads, and water.

The main classification errors were caused by similar spectral responses:

- bright building surfaces were sometimes confused with grassland;
- bare ground was sometimes classified as road;
- building shadows were sometimes classified as water.

Targeted post-classification refinement reduced these obvious errors and produced a cleaner final map.

## Workflow

- Reviewed the five-band UAV multispectral imagery and defined the target land-cover classes.

- Manually created representative training samples for built-up areas, grassland, forest, roads and water.

- Produced a pixel-based supervised classification as a baseline.

- Segmented the imagery into spatially coherent objects.

- Trained an object-based Support Vector Machine classifier using all five spectral bands.

- Compared the spatial coherence of the pixel-based and object-based outputs.

- Reviewed spectral-confusion errors and applied raster-based post-classification refinement.

- Produced the final land-cover map and documented limitations.


## Limitations

Independent ground-truth data were not available, so a formal external accuracy assessment is not reported. The final map should therefore be interpreted as a supervised-classification workflow and spatial interpretation exercise rather than a production-ready land-cover dataset.

The refinement stage also included analyst review, meaning that some corrections depend on visual interpretation and local knowledge of the study area.

## Tools and Methods

**ArcGIS Pro · Object-Based Image Analysis · Support Vector Machine · UAV Multispectral Imagery · Image Segmentation · Raster Calculator**

## Project Context

I prepared the training samples, performed the object-based SVM classification in ArcGIS Pro, reviewed spectral-confusion errors, refined the classified raster and produced the final land-cover map. The broader theoretical review and coursework report were completed collaboratively as part of a University of Canterbury group project.


