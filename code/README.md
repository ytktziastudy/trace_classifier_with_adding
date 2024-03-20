## Code Structure

* **main.py** the main function [main-readme add by ktzia](main-readme.md)
* **config.py** the config settings [config-readme add by ktzia](config-readme.md)
* **pytorch_warmup** Tony-Y's implementation of [pytorch_warmup](https://github.com/Tony-Y/pytorch_warmup).
* **output** the training output files
* **others** other lib py files

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
```diff
+ add by ktzia
+ dataset.py My addition to the code
```

* **dataset.py** [dataset-readme](dataset-readme.md) Functions for loading and processing datasets 
* **model.py** [model-readme](model-readme.md) Defines the neural network model (Net) used for classification.
* **mylib.py** [mylib-readme](mylib-readme.md) Contains utility functions for dataset processing and evaluation.
* **my_hilbertcurve.py**
* **draw_tsne.py** <br>
Both my_hilbertcurve.py and draw_tsne.py serve crucial roles in the preprocessing and analysis of model data, aiding both in the improvement of model input through dimensionality reduction and in the interpretation of model outputs or dataset structures through visualization.

