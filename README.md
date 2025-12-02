# deforestation_transfer_learning
Transferability of an Attention U-Net for Detecting Deforestation in the Congo Basin: A Case Study in South Cameroon


# Environment setup and Dependencies Documentation 
This project uses a dedicated Conda environment to ensure reproducibility and compatibility with the Attention U-Net architecture implemented in the original deforestation detection paper.

**Environment name:** attunet

**Operating System:** macOS Sequoia 15.7.1

**Architecture:** Apple Silicon (ARM64 — M-series)

**Python version:** 3.9

## 1. Create the Conda Environment
*conda create -n attunet python=3.9*

*conda activate attunet*

Python 3.9 is required for compatibility with TensorFlow 2.8 and the segmentation-models package.

## 2. Install Geospatial Dependencies
*conda install -c conda-forge gdal rasterio rioxarray*

These libraries depend on GDAL and must be installed through Conda on macOS.

## 3. Install Apple-Optimised TensorFlow & Keras
Apple Silicon machines require the unqiue Apple TensorFlow build:

*pip install tensorflow-macos==2.8* - official Apple version

*pip install keras==2.8*

*pip install tensorflow-metal* - GPU acceleration using the Metal backend

## 4. Install Remaining Python Dependencies
*pip install numpy pillow segmentation-models rarfile pyunpack patool matplotlib pandas pathlib scikit-learn*

From teh original requiremnets PIL and sklearn were replaced with pillow and scikit-learn repectively becasue they were outdated 

## 5. Full list of Depenedencies 
|Package|Version|Purpose
|--------|-------|----------|
|Package|	Version	|Purpose|
|tensorflow-macos	|2.8	|Apple TensorFlow build|
|keras	|2.8|	Model API|
|tensorflow-metal	|—	|GPU acceleration|
|numpy|	—	|Array operations|
|pillow|	—	|Image reading and preprocessing|
|segmentation-models	|—	|U-Net / Attention U-Net blocks|
|matplotlib|	—	|Visualisation|
|pandas	|—	|Data handling|
|scikit-learn	|—	|Metrics (F1-score, IoU|
|gdal	|—	|Geospatial data processing|
|rasterio|	—|	Satellite raster handling|
|rioxarray	|—	|GeoTIFF & metadata|
|rarfile|	—	|Archive handling|
|pyunpack	|—	|Decompression utilities|
|patool	|—|	Archive extraction|
|pathlib	|—	|File system utilities|
