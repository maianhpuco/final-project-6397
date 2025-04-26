# final-project-6397
Dataset:  Sen1Floods11 dataset 

## Input Data: Single-timestamp Sentinel-2 images in GeoTIFF format, utilizing six spectral bands:
1. Blue
2. Green
3. Red
4. Narrow Near-Infrared (NIR)
5. Short-Wave Infrared 1 (SWIR 1)
6. Short-Wave Infrared 2 (SWIR 2)

## Output: A segmentation map classifying each pixel as:

0: No water
1: Water/Flood
-1: No data/Clouds 


Architecture: Based on a Vision Transformer (ViT) with a Masked Autoencoder (MAE) framework, the model was initially pre-trained on Harmonized Landsat and Sentinel-2 (HLS) data, then fine-tuned for flood mapping tasks. 

Note: 
Chip = a small cut-out or patch from a much larger satellite image.
512×512 = the chip has 512 pixels width × 512 pixels height. 
