## Code Main Structure 
```diff
+ Add by ktzia
```

The main script combines all the previous steps to execute the model training and evaluation. It configures the model, preprocesses the dataset, trains the model on the training dataset, evaluates it on the validation and test datasets, and optionally visualizes the results.

list function in main.py
* **main** the main function
  
* **one_of_k_fold_test** 
* **read_dataset** 
* **one_fold_test** 
* **k_fold_test** 
* **one_round_test**


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
