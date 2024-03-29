# Model Architecture :
The following model has been obtained from the paper authored by Yash Chauhan [1]. You can read this paper [here](/Literature%20Review/Classification/1D-CNN/yash_chauhan.pdf).
```
Model: "sequential"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
conv1d (Conv1D)              (None, 16353, 64)         2112      
_________________________________________________________________
max_pooling1d (MaxPooling1D) (None, 4088, 64)          0         
_________________________________________________________________
re_lu (ReLU)                 (None, 4088, 64)          0         
_________________________________________________________________
conv1d_1 (Conv1D)            (None, 4025, 128)         524416    
_________________________________________________________________
max_pooling1d_1 (MaxPooling1 (None, 1006, 128)         0         
_________________________________________________________________
re_lu_1 (ReLU)               (None, 1006, 128)         0         
_________________________________________________________________
conv1d_2 (Conv1D)            (None, 943, 256)          2097408   
_________________________________________________________________
max_pooling1d_2 (MaxPooling1 (None, 235, 256)          0         
_________________________________________________________________
re_lu_2 (ReLU)               (None, 235, 256)          0         
_________________________________________________________________
conv1d_3 (Conv1D)            (None, 108, 512)          16777728  
_________________________________________________________________
max_pooling1d_3 (MaxPooling1 (None, 27, 512)           0         
_________________________________________________________________
re_lu_3 (ReLU)               (None, 27, 512)           0         
_________________________________________________________________
flatten (Flatten)            (None, 13824)             0         
_________________________________________________________________
dense (Dense)                (None, 128)               1769600   
_________________________________________________________________
dense_1 (Dense)              (None, 64)                8256      
_________________________________________________________________
dropout (Dropout)            (None, 64)                0         
_________________________________________________________________
dense_2 (Dense)              (None, 2)                 130       
=================================================================
Total params: 21,179,650
Trainable params: 21,179,650
Non-trainable params: 0
_________________________________________________________________
```

# Classes :
```
1. Noise 
2. BBH signal + Noise
```

# Dataset :
To generate this dataset, use the "IMPORTS" section (code cell no. 1) and the "BBH Data Generation" section (code cell no. 2-6) of the [Data Generation](/scripts/Data%20Generation.ipynb) script.
```
| S.No. | Data Type          | Mode of generation   | No. of Samples |
| ----- | ------------------ | -------------------- | -------------- |
| 1     | Noise              | Gaussian             | 5000           |
| ----- | ------------------ | -------------------- | -------------- |
| 2     | BBH signal + Noise | SEOBNRv2             | 5000           |
| ----- | ------------------ | -------------------- | -------------- |
```

# Trial Hyperparameters :
```
| Trial No. | Accuracy | Normalized? | Amplitude Re-Scaled? | Dropout rate | Optimizer | lr   | Batch Size | Epochs |
| --------- | -------- | ----------- | -------------------- | ------------ | --------- | ---- | ---------- | ------ |
| 1         | 49.31%   | No          | No                   | 0.2          | Adam      | 1e-3 | 128        | 10     |
| --------- | -------- | ----------- | -------------------- | ------------ | --------- | ---- | ---------- | ------ |
| 2         | 49.32%   | Yes         | Yes (Due to Norm)    | 0.2          | Adam      | 1e-3 | 128        | 10     |
| --------- | -------- | ----------- | -------------------- | ------------ | --------- | ---- | ---------- | ------ |
| 3         | 100%     | No          | Yes (by 1e19)        | 0.2          | Adam      | 1e-3 | 128        | 5      |
| --------- | -------- | ----------- | -------------------- | ------------ | --------- | ---- | ---------- | ------ |
```
 
# Trial Results :
## Trial 1:
<p align="center"> <img src="screenshots/graph_1.png"> </p>
<p align="center"> <img src="screenshots/1dcnn_binary_class_model_11.png"> </p>

## Trial 2:
<p align="center"> <img src="screenshots/graph_2.png"> </p>
<p align="center"> <img src="screenshots/1dcnn_binary_class_model_12.png"> </p>

## Trial 3:
<p align="center"> <img src="screenshots/graph_3.png"> </p>
<p align="center"> <img src="screenshots/1dcnn_binary_class_model_13.png"> </p>

# Conclusions :

+ Batch size = 128 is ideal since it has a faster runtime than batch size = 256 and it also does not cause the runtime  to crash due to exhaustion of RAM resources on colab. 
+ 10 epochs are enough to determine whether the model is able to learn any features. 
+ Normalization of the dataset caused the training time to increase significantly, and the results were still baseline, so it is not feasible to try out further combinations with normalization. 

# References :
1. Chauhan, Y., 2020. Deep Learning Techniques to Make Gravitational Wave Detections from Weak Time-series Data. arXiv preprint arXiv:2007.05889.


