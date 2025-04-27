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


reference link: https://github.com/NASA-IMPACT/hls-foundation-os 

```
conda activate hls_fresh

pip install torch==1.11.0+cu115 torchvision==0.12.0+cu115 --extra-index-url https://download.pytorch.org/whl/cu115

pip install -e .

pip install -U openmim

mim install mmcv-full==1.6.2 -f https://download.openmmlab.com/mmcv/dist/cu115/torch1.11.0/index.html 

```
pip install torch==1.11.0+cu115 torchvision==0.12.0+cu115 --extra-index-url https://download.pytorch.org/whl/cu115 

Sanity Check: 
```
python -c "import mmcv; print(mmcv.__version__)" 
```
pip install rasterio==1.3.10 
mim install mmcv-full==1.6.2 -f https://download.openmmlab.com/mmcv/dist/cu115/torch1.11.0/index.html  
```
mim install mmsegmentation 

pip install "numpy>=1.19.2,<1.24.0" #TypeError related to np.ndarray 
```

pip install -e . --config-settings editable_mode=compat 

