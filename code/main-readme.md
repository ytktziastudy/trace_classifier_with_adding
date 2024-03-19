## Code Main Structure 
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
  **Description:**
  Performs a single fold of k-fold cross-validation. This function is responsible for dividing the dataset into training, validation, and test sets for one     
  specific   fold, training the model on this fold, and evaluating its performance
  **Configurations Used:**_ _
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


## How to Config it?
All the configurations are set in [config.py](./config.py).
Here we list some of the configurations.

```
PACKET2FLOW = 'LSTM+ATT' # 'ATT, LSTM, TREE, LSTM+ATT,1dCNN, 2dCNN' 1dCNN can be used only if one flow has a fixed length of packet vectors. if 1dCNN/2dCNN, PACTETCNN should = False.   
                      # 2dCNN uses hilbertcurve2d to transfer a flow into a matrix.
FLOW2TRACE = 'LSTM+ATT' # 'ATT, LSTM, TREE, LSTM+ATT'

# the program uses k-fold
K_FOLD = 10     # k of k-fold
CORE_NUM = 1    # multi-process worker number, 1 - n

# epochs
MAX_EPOCH = 100 * 1

# paras
EMB_NUM = 100           # EMBEDDING TOKENS
F_EMB_NUM = 100         # VECTOR SIZE OF ONE EMBEDDING TOKEN
FEATURE_SIZE = 100      # HIDDEN LAYER FEATRUE SIZE
LEARNING_RATE = 0.001   # MAX LEARNING RATE
BATCH_SIZE = 16         # BATCH SIZE

# output path
OUTPATH = './output/20230505_test/'

```

Change the config file and run main.py.
