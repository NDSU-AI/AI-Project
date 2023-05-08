## Machine learning & Deep learning application on genomic data for early cancer prediction

### Workflow Overview

We used Google Collab to share and run our machine learning and deep learning code. There are two main Jupyter Notebook files ***feature_selection.ipynb*** and ***dl_model.ipynb***.
***feature_selection.ipynb*** consists code that we used to select features using different machine learning algorithms and their combination to train and test the DL model and ***dl_model.ipynb*** consists code that build DL model and train and perform evaluation of it's performance using various metrics such as accuracy, recall, precision and so on.

Our workflow can be broken down into two major steps:
````
Step 1. Extracts the features from dataset using ML models and saves it into separate csv file. The generated csv is then used to train and test model. This step is perfomed by executing the code in feature_selection.ipynb.
````

```
Step 2. Build deep learning model and train, validate and test the model against the dataset (obtained from Step 1) fed into the DL model. This step is performed by executing the code in dl_model.ipynb.
````



### Getting Started

To run the project, python should be installed on your machine.
Check if it is installed or not using

```
python --version
```

If it is not installed, download and install python from https://www.python.org/downloads/


You need to install Jupyter to run notebook files in your system.
You can install Jupyter notebook using pip as follows

````
pip install jupyterlab
````

You can also install Jupyter using Anoconda and conda https://docs.jupyter.org/en/latest/install/notebook-classic.html#installing-jupyter-using-anaconda-and-conda


**However we recommend to import the project in the Google Collab https://colab.research.google.com and run it in the browser interface as we used in as our primary platform to test and execute our code**

>First of all, you will need to download origin data before smote from https://drive.google.com/file/d/1EPNf_KymdfyjfXrsAXKgSK97SPRcMkfy/view?usp=share_link and place it inside files directory.

>Now to run the code execute code in code blocks in serial manner. Please, do not forget to change the file path of the csv files as they might throw **FileNotFound** exception. After running the code in ***feature_selection.ipynb***, you will get a csv file containing markers selected using your prefered Machine Learning Model as Feature Selection Method.

>Then, use the markers file obtained to feed into the DL model in ***dl_model.ipynb*** file. Please, execute the code in this file in the sequetial order and do not forget to change the file path in this file as well. After you have successfully excecuted the code blocks in this file, you will get two files: one containing the saved weights of DL model and another containing the performance metrics.

**Keep performing step 1 for different machine learning algorithms and used the markers file generated to see DL model results using step 2.**
