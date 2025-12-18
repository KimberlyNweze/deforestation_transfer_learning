# deforestation_transfer_learning
Transferability of an Attention U-Net for Detecting Deforestation in the Congo Basin: A Case Study in Cameroon
# Datasets 
## Baseline - Amazon 4 band 
Link to download the Amazon.rar file - https://zenodo.org/records/4498086#.YMh3GfKSmCU
## Cameroon raw 4 band satelite imagery 
Link to Ground Cover - https://drive.google.com/file/d/1Ij42CJiqiRBPEgzYitj-daHIWa3JQcdZ/view?usp=sharing

Link to Ground Truth mask - https://drive.google.com/file/d/1OH788bh1DSTjmwRI-Pt94_nHncOz6BNj/view?usp=sharing

# Repository Structure 
This repository is organised to support reproducibility, comparison, and documentation of both the baseline and adapted deforestation detection models.
## ChosenContext/
Contains contextual and methodological documentation for the adapted Cameroon study:

- Adapted Model Architecture Changes – Details modifications made to the baseline Attention U-Net architecture.

- Challenge and SDG Alignment – Discusses project challenges and alignment with relevant Sustainable Development Goals.

- Dataset Curation – Describes data sourcing, preprocessing decisions, and ethical considerations.

- Cameroon/ – Core implementation for the adapted model, including:

  * Scripts to generate image tiles

  * Generated tiles

  * Training scripts

  * Trained model weights

  * Training and evaluation results
 ## ReplicateBaseline/
 Supports full reproduction of the original baseline model:
 - environment.yml – Conda environment file listing all required dependencies.
 - Reproduce Baseline – Notebook and scripts to reproduce baseline results from the original repository.
 - Environment Setup Documentation – Detailed explanation of environment setup and dependency management.
 - Original Repository – Unmodified files from the original Attention U-Net repository, included for reference and transparency.

## Comparing The Models/
- Contains scripts and outputs used to quantitatively compare the baseline and adapted models, including per-image and aggregate performance metrics.

# How to Use the Repository
## Reproducing the Baseline Model
- Download the AMAZON.rar dataset.
- Unzip the dataset.
- Place the extracted folder into the directory specified in the baseline preprocessing scripts.
- Run the baseline preprocessing and training scripts as provided.

This will replicate the baseline Attention U-Net results reported in the original study.
## Running the Cameroon (Adapted) Model
There are two ways to run the adapted Cameroon model, depending on whether you want to reproduce the full preprocessing pipeline or use the preprocessed data provided in this repository.
### Option A: Full Data Preparation and Training (From Raw Data)
- Download the Sentinel-2 imagery and corresponding ground truth masks from the provided data source links.
- Place the files into the directory paths specified in the Cameroon preprocessing scripts.
- Run the tiling and preprocessing scripts to generate training, validation, and test tiles.
- Train the adapted Attention U-Net model using the provided training scripts.
- Evaluate the model using the included evaluation and comparison notebooks.

This option fully reproduces the data preparation workflow and is suitable for adapting the pipeline to new regions.

## Option B: Direct Model Training Using Preprocessed Tiles
- Clone this repository.
- Navigate to the dataset_split folder within the Cameroon preprocessing directory.
- Run the South Cameroon training script, which directly uses the preprocessed training, validation, and test tiles already included in the repository.
- Evaluate the model using the provided evaluation and comparison notebooks.

  
This option allows for replication of the reported results without rerunning the preprocessing steps. All file paths are defined relative to the repository root to ensure portability across systems.

 
