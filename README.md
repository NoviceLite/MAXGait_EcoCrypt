# MAXGait: A Hybrid Mamba-Attentions Solution for Soft Biometrics Analysis using Gait Patterns
This repository consists of Python Notebooks and Dataset for proposed MAXGait model.

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

## Steps to execute (EcoCrypt)
1. Download the testing set from the folder "dataset".
2. Download the "MAXGait + EcoCrypt (CPU).ipynb" for combination of MAXGait and EcoCrypt model.
3. Download the "MAXGait.weights.h5" from the folder "src".
4. (Optional) Upload the downloaded notebook to Google Drive.
5. (Optional if not using Google Drive) Install MAXGait's necessary modules.
   ```
   pip install cryptography pandas
   ```
   Meanwhile, another two modules, `nummaster` and `tinyec` will be downloaded during the notebook execution.
6. Change the directory of dataset and pretrained weights input folder.
7. Execute the notebook.

Note: If there is an error occured in the data preprocessing stage similar to the execution of MAXGait, the similar solution is used to allow smooth execution of the program.
