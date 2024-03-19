## Code Dataset.py Structure 
```diff
+ Add by ktzia
```

The main script combines all the previous steps to execute the model training and evaluation. It configures the model, preprocesses the dataset, trains the model on the training dataset, evaluates it on the validation and test datasets, and optionally visualizes the results.

list function in main.py
* **main**
  -----
  The primary entry point of the script. It orchestrates the overall process, including setting up the environment, initiating model training, performing     evaluations, and optionally visualizing the results. It determines which training and evaluation functions to call based on the configuration.
* **one_of_k_fold_test** 
  -------------
   Performs a single fold of k-fold cross-validation. This function is responsible for dividing the dataset into training, validation,and test sets for one specific fold, training the model on this fold, and evaluating its performance <br>
  **Configurations Used:** 
  Configuration settings related to dataset splitting (K_FOLD), training sample limits (TRAIN_SAMPLE_MAX, VALID_SAMPLE_MAX)
* **read_dataset**
  ------------------
  Loads the dataset from the specified source and preprocesses it according to the requirements of the model. It converts raw data into a format suitable for     training and evaluation, including feature extraction and normalization.
  
* **one_fold_test**
  ------------
  Executes the training and evaluation process using a single fold, i.e., without performing k-fold cross-validation. This is useful for quick testing or when the dataset is too small to be divided into multiple folds
  
* **k_fold_test**
  ------------------
  Orchestrates the k-fold cross-validation process by calling one_of_k_fold_test for each fold. It ensures that every data point is used for both training and validation exactly once, providing a robust estimate of the model's performance.
  
* **one_round_test**
  ------------------
  Facilitates a complete round of training and evaluation without dividing the dataset. It preprocesses the data, trains the model on the entire training set, and evaluates it on the whole validation set. This function is suitable for initial model assessments or when cross-validation is not required.



