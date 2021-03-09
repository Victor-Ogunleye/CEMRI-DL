# CEMRI-DL

CEMRI Documentation

https://github.com/Victor-Ogunleye/CEMRI-DL.git


Healthy_breast_MRI_Model: We need a benchmark to test against to help the neural network learn what a healthy breast MRI image looks like. Initial test data is collected from:Human Breast Cancer (Breast-MRI-NACT-Pilot) dataset.
Deep_learning_model
Contains inference code to judge the accuracy of the model.It highlights the model architecture and the implementation of the inference procedure.
The Deep Learning Model provides for a number of learning methods and some predefined model weights.
The user is prompted to select the prefered method
Unet
R2U_Net
Attu_Net
R2Attu_Net
ResAttu_Net
Tools
Data_loader.py: 
Initializes file paths and preprocessing modules. Data is loaded and prepared here.The properties of the data; like the dimensions and the slice dimensions are configured.
network.py:
Codebase for the The Neural Network and the proposed weights 
Solver.py:
Initializes the deep learning model with training data, validation data and test data. Sets up model and hyper parameters loss functions and eventually model classes.

Saved_model_weights:
The trained model weights are compiled here. 


CEMRI_scripts
Generate_new_predictions.py:
These scripts help generate predictions based on deep learning models selected,model weight required, loss function and inference benchmark.
Verify_old_new_predictions_identical.py:
Verification of generated data and old data to determine if they are identical
Visual_inspection.py:
Qualitative Evaluation of dataset reliability
Test_retest_evaluation.py:
Quantitative evaluation of dataset reliability
Test retest reliability dataset(Work in Progress) 	
Currently gathering the larger dataset to inform reproducibility and understand the limits of the reduction of gadolinium and contrast levels	 		
nonContrast
GBCAuptake
GBCApredicted
Surface_Area_Mask
tissueLabel

Environment_setup
CEMRI.yml
Simple Yaml file to help setup the environment variables and config files


