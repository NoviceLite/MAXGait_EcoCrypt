# FYP2
This repository consists of Python Notebooks and Datasets for Final Year Project 2

## "dataset" folder
This folder consists of the training, validation and testing dataset used for the experiments conducted. The data are in 3D SMPL format (24 joints) which can be directly read and processed using the models in Jupyter Notebook.

## "src" folder
This folder consists of all Jupyter Notebook used, including the proposed MAXGait, EcoCrypt and comparison models.
Note: The "MAXGait.weights.h5" file is the pretrained weights to be loaded by MAXGait + EcoCrypt model.

## Note
The components in this repository does not worked directly after cloning to the local computer. This repository only serves as a storage of FYP 2's materials.

## Steps to execute (MAXGait)
1. Download the train, validation and testing set from the folder "dataset".
2. Download the "MAXGait (Best 3).ipynb" for MAXGait model.
3. (Optional) Upload the downloaded notebook to Google Drive.
4. (Optional if not using Google Drive) Install MAXGait's necessary modules.
   ```
   pip install tensorflow numpy scipy matplotlib scikit-learn einops typing-extensions
   ```
5. Change the directory of dataset input folder.
6. Execute the notebook.

Note: If there is an error occured in the data preprocessing stage (more specifically, "extract_data" function), please kindly comment out the lines:
```
from drive.MyDrive.model_preprocessing import process
age = process(file)
```
and uncomment the following line:
```
age = int(file.split("_")[3])
```
