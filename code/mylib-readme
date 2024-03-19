## Code Mylib Structure 
```diff
+ Add by ktzia
```


list function in mylib.py
* **process_final_results**
  -----
  The primary entry point of the script. It orchestrates the overall process, including setting up the environment, initiating model training, performing     evaluations, and optionally visualizing the results. It determines which training and evaluation functions to call based on the configuration.
* **name_generator** 
  -------------
   Performs a single fold of k-fold cross-validation. This function is responsible for dividing the dataset into training, validation,and test sets for one specific fold, training the model on this fold, and evaluating its performance <br>
 
* **cut_dataset2**
  ------------------
  Loads the dataset from the specified source and preprocesses it according to the requirements of the model. It converts raw data into a format suitable for     training and evaluation, including feature extraction and normalization.
  
* **cut_dataset**
  ------------
  Executes the training and evaluation process using a single fold, i.e., without performing k-fold cross-validation. This is useful for quick testing or when the dataset is too small to be divided into multiple folds
  
* **pre_process**
  ------------------
  Orchestrates the k-fold cross-validation process by calling one_of_k_fold_test for each fold. It ensures that every data point is used for both training and validation exactly once, providing a robust estimate of the model's performance.
  
* **pre_process_1**
  ------------------
  Facilitates a complete round of training and evaluation without dividing the dataset. It preprocesses the data, trains the model on the entire training set, and evaluates it on the whole validation set. This function is suitable for initial model assessments or when cross-validation is not required.

 
* **drop_empty_data**
  ------------------
  Facilitates a complete round of training and evaluation without dividing the dataset. It preprocesses the data, trains the model on the entire training set, and evaluates it on the whole validation set. This function is suitable for initial model assessments or when cross-validation is not required.

 
* **tailoring_dataset**
  ------------------
  Facilitates a complete round of training and evaluation without dividing the dataset. It preprocesses the data, trains the model on the entire training set, and evaluates it on the whole validation set. This function is suitable for initial model assessments or when cross-validation is not required.


* **dataset2flow**
  ------------------
  Facilitates a complete round of training and evaluation without dividing the dataset. It preprocesses the data, trains the model on the entire training set, and evaluates it on the whole validation set. This function is suitable for initial model assessments or when cross-validation is not required.

* **dataset_use_hilbertcurve**
  ------------------
  Facilitates a complete round of training and evaluation without dividing the dataset. It preprocesses the data, trains the model on the entire training set, and evaluates it on the whole validation set. This function is suitable for initial model assessments or when cross-validation is not required.



