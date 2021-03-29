```
CEMRI Documentation

https://github.com/Victor-Ogunleye/CEMRI-DL.git


```



1. <code>Healthy_breast_MRI_Model: We need a benchmark to test against to help the neural network learn what a healthy breast MRI image looks like. Initial test data is collected from:<em>Human Breast Cancer (Breast-MRI-NACT-Pilot)</em> dataset.</code>
2. <code>Deep_learning_model</code>

    ```
    Contains inference code to judge the accuracy of the model.It highlights the model architecture and the implementation of the inference procedure.
    The Deep Learning Model provides for a number of learning methods and some predefined model weights.
    The user is prompted to select the prefered method
    Unet
    R2U_Net
    Attu_Net
    R2Attu_Net
    ResAttu_Net
    Tools
    ```


*   `Data_loader.py: `

        ```
        Initializes file paths and preprocessing modules. Data is loaded and prepared here.The properties of the data; like the dimensions and the slice dimensions are configured.
        ```


*   `network.py:`

        ```
        Codebase for the The Neural Network and the proposed weights 
        ```


*   `Solver.py: \
Initializes the deep learning model with training data, validation data and test data. Sets up model and hyper parameters loss functions and eventually model classes.`
*   `Saved_model_weights:`

        ```
        The trained model weights are compiled here. 

        ```


3. `CEMRI_scripts`

    ```
    Generate_new_predictions.py:
    These scripts help generate predictions based on deep learning models selected,model weight required, loss function and inference benchmark.

    Verify_old_new_predictions_identical.py:
        Verification of generated data and old data to determine if they are identical
        Visual_inspection.py:
        Qualitative Evaluation of dataset reliability
    Test_retest_evaluation.py:
    Quantitative evaluation of dataset reliability

    ```



4. `Test retest reliability dataset(Work in Progress) 	`

    ```
    Currently gathering the larger dataset to inform reproducibility and understand the limits of the reduction of gadolinium and contrast levels	 		
    ```


    1. `nonContrast`
    2. `GBCAuptake`
    3. `GBCApredicted`
    4. `Surface_Area_Mask`
    5. `tissueLabel`
5. `Environment_setup`

    ```
    CEMRI.yml
    Simple Yaml file to help setup the environment variables and config files


    Getting Started

    ```



1. `Environment Setup`
*   `Download Anaconda`
*   `Setup Anaconda with the details in CEMRI.yml`


```
Manual Config
If you can't install with the YAML file. Consider installing from scratch
Conda env create -f Cemricontrast.yml
conda create -n CemriContrast

conda activate CemriContrast
conda install python=3.7 numpy scipy scikit-image scikit-learn seaborn -c anaconda
conda install pytorch torchvision cudatoolkit=10.2 -c pytorch
conda install nibabel tqdm -c conda-forge
conda install cudatoolkit=10.2 -c pytorch

```



2. `Setup Data Files`
*   `Download Model Weights`
*   `Place them in the right folder`
*   <code>Now run `<strong>conda activate`</strong></code>
3. <strong><code>Generate New Predictions</code></strong>

    ```
    Run the following scripts in the python 
    ```


*   `Python generate_new_predictions.py`
*   `Python verify_old_new_predictions_identical.py`
