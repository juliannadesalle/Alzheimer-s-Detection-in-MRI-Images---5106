# Alzheimer-s-Detection-in-MRI-Images---5106
This ipynb file was made with Google Colab in mind.

The code unzips the dataset from the storage path and stores it in the Google Colab workspace.
The dataset contains 4 classes: Mild Demented, None Demented, Moderate Demented, and Very Mild Demented.
After the dataset is loaded into the workspace, 3 dataloaders are created after augmenting the images in the dataset.
The training, validation, and test dataloaders uses 85%, 10%, and 5% of the augmented images respectively.

There are 4 models used in this file: ResNet-50, GoogLeNet, DenseNet-161, and MobileNetV3-Large.
There is a training boolean flag to either train or use pre-trained weights for each model.
Any pre-trained weights and checkpoints are saved to Google Drive.
During training, a checkpoint is created after 50 epochs and when the process is completed the weights 
are saved in a tar file and shows the training loss, validation loss, and test confusion matrix.
If training is not done, the test confusion matrix is created instead.

Dataset:
Alzheimer MRI Preprocessed Dataset
https://www.kaggle.com/datasets/sachinkumar413/alzheimer-mri-dataset
