# automating-lulc-classification-using-python
Compute Land Use Land Cover (LULC) for any area of your choice, using the model trained
in the [lulc_classification_using_deep_learning](https://github.com/Nirzaree/lulc_classification_using_deep_learning)
repo. 

This repo is built on the part 2 of the [lulc tutorial](https://github.com/climatechange-ai-tutorials/lulc-classification/blob/main/land_use_land_cover_part2.ipynb) in CCAI Summer school. 

High level flow: 
1. Select region of interest and get the boundary of the region
2. Get sentinel2 data (R,G,B) (preferably a median image for a time period of interest) for the region of interest
3. Generate 64x64 tiles within the region of interest (as required by the model in this case)
4. Run predictions (of the fine tuned Resnet50 model) on each of the tiles in the region. 
5. Visualize the predictions 

I computed LULC of 2024 of Bangalore, India where I live: 
![](/images/Bangalore_LULC_2024.png)

TODO : I plan to compute change of LULC for a few Indian cities, to quantify the reduction in green cover 
in the cities, in the last few years. 