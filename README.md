# Geospatial-Land-Use-Classification<div style="text-align:center">

![transformation-31d49ea5fedf3443](https://github.com/phreak1703007/Geospatial-Land-Use-Classification/assets/62479964/a51010c8-d6f8-4685-bd89-f5f6c1937364)


The goal of this notebook is to develop a basic data pipeline that can be easily applied to new image recognition projects. Some concepts developed here:

- Use of generators for data loading using *flow_from_dataframe*.
- Triple splitting of the dataset (training, validation and test sets) for model training and evaluation.
- Usage of predefined CNN architectures.
- Evaluation of the model performance.

# Dataset Description

## Context
This dataset is used for classifying land use in geospatial images. The classification aims to identify the top two land use categories within each image.

## Content
The dataset contains images sourced from the EuroSat dataset, organized into two folders:

1. **EuroSAT**: This folder contains RGB images collected from the Sentinel Dataset.

2. **EuroSATallBands**: This folder contains .tif files that include all bands of the electromagnetic spectrum, as collected from the Sentinel-2 satellite.

### Image Specifications
- Each image is 64x64 pixels in size.
- The Ground Sampling Distance (GSD) is 10 meters.
- The images were collected from the Sentinel-2 satellite.

### Class Labels
The dataset includes the following class labels:

1. AnnualCrop
2. Forest
3. HerbaceousVegatation
4. Highway
5. Industrial
6. Pasture
7. PermanentCrop
8. Residential
9. River
10. SeaLake
### Link: https://www.kaggle.com/datasets/apollo2506/eurosat-dataset

### Samples:
  
![Samples](https://github.com/phreak1703007/Geospatial-Land-Use-Classification/assets/62479964/29e93830-8477-4dcc-ba0c-794849a97081)


# Results and Evaluation of VGG-16 Based Transfer Learning Model:

## Accuracy & Loss Curve: 

![result](https://github.com/phreak1703007/Geospatial-Land-Use-Classification/assets/62479964/92917e35-9eb2-499b-a9c6-757d197d47d2)

## Wrong Predictions by the model:

![wrongs](https://github.com/phreak1703007/Geospatial-Land-Use-Classification/assets/62479964/d9fdeba4-db34-44c6-9fc7-3e54e8bc9dbc)


## Correct Predictions by the model:


![Corrects](https://github.com/phreak1703007/Geospatial-Land-Use-Classification/assets/62479964/c77778c2-a8ad-40a4-83f0-1e71a7a25d1a)



# Conclusions

- Standard Data augmentation techniques did not add significant value to the models.
- The VGG16 architecture performs really well on this dataset.
- The value of the non-visible light bands is minor in these data.


