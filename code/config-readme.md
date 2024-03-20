## Params config.py 
```diff
+ Add by ktzia
+ change function by me for add lag function
```

## Model and Dataset Configuration
**My addition to the code**
* **LAG_SIZE:** You can write how many lag fields you want to add to the packet vector where 0 means one field with one interval and n means n-1 additional fields.
**End my addition to the code**

* **DATASET_SHARE:** Indicates if the dataset is shared across processes. This flag might be used when initializing data loaders or managing multiprocessing tasks.
* **PACTETCNN:** A flag to enable or disable the use of Convolutional Neural Networks (CNN) for packet analysis. This would influence the choice of architecture in functions related to feature extraction from packets.
* **TRANSFORMER:** Determines whether a Transformer model is used. This could affect model initialization and the architecture setup functions, dictating the use of attention mechanisms over other types.
* **PACKET2FLOW:** Specifies the method for converting packets to flow-level features, influencing the choice of neural network architecture or feature extraction methods in flow-related processing functions.
* **FLOW2TRACE:** Defines how flow-level features are aggregated into trace-level representations, affecting functions that operate on higher-level data aggregation.
* **K_FOLD, CORE_NUM:** These parameters control the execution of k-fold cross-validation and parallel processing, affecting functions related to model evaluation and training.
* **MAX_EPOCH, DEVICE:** Determine the maximum number of training epochs and the computation device (CPU/GPU), influencing the main training loop and device allocation for tensors.
* **DATASET_FOLDER, DATASET_NAME:** Specify the location and name of the dataset, used in data loading and preprocessing functions.
## Overfitting Handling and Model Parameters
* **Flags like ES_FLAG, LNORM_FLAG, WD_FLAG, DROPOUT_FLAG, USEBN_FLAG, USEMM_FLAG, and DATA_ENHANCEMENT_FLAG** control various strategies to handle overfitting, such as early stopping, layer normalization, weight decay, dropout, batch normalization, and data enhancement. These are crucial in the model's training process to ensure generalization.
## Experimentation and Output Configuration
* **FLOW_CUT_FLAG, FLOW_CUT_SIZE, SCALE_1dCNN, SCALE_SIZE, HU2_FLAG, FIX_M1_CNN_LENGTH, SIZE_2dCNN, TRAIN_SAMPLE_MAX, VALID_SAMPLE_MAX, WF_MIX_PAGE:** These parameters are used to tweak the model's input data structure, the size of the dataset for training and validation, and experimental features like flow cutting, scaling for 1D CNN, and handling the dataset's flow. These configurations affect data preprocessing, model architecture adjustments, and how datasets are split and utilized during training and validation.
* **USE_WARM_UP, WARM_UP:** Determine whether a warm-up phase is used in training to gradually increase the learning rate, used in the training loop to stabilize the optimization process.
* **OUTPATH:** Specifies the directory for output files, such as trained model weights and evaluation results, influencing where model artifacts are saved.
