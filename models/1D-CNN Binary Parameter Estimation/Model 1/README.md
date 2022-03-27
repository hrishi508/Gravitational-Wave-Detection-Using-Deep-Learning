# Model Architecture :
The following model has been obtained from the paper authored by Plamen G. Krastev [1]. You can read this paper [here](/Literature%20Review/Classification/1D-CNN/krastev_1.pdf).
``` 
Model: "sequential_1"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
conv1d_4 (Conv1D)            (None, 16369, 16)         272       
_________________________________________________________________
max_pooling1d_4 (MaxPooling1 (None, 4092, 16)          0         
_________________________________________________________________
re_lu_4 (ReLU)               (None, 4092, 16)          0         
_________________________________________________________________
conv1d_5 (Conv1D)            (None, 4085, 32)          4128      
_________________________________________________________________
max_pooling1d_5 (MaxPooling1 (None, 1021, 32)          0         
_________________________________________________________________
re_lu_5 (ReLU)               (None, 1021, 32)          0         
_________________________________________________________________
conv1d_6 (Conv1D)            (None, 1014, 64)          16448     
_________________________________________________________________
max_pooling1d_6 (MaxPooling1 (None, 253, 64)           0         
_________________________________________________________________
re_lu_6 (ReLU)               (None, 253, 64)           0         
_________________________________________________________________
conv1d_7 (Conv1D)            (None, 246, 128)          65664     
_________________________________________________________________
max_pooling1d_7 (MaxPooling1 (None, 61, 128)           0         
_________________________________________________________________
re_lu_7 (ReLU)               (None, 61, 128)           0         
_________________________________________________________________
flatten_1 (Flatten)          (None, 7808)              0         
_________________________________________________________________
dense_3 (Dense)              (None, 64)                499776    
_________________________________________________________________
dense_4 (Dense)              (None, 2)                 130       
=================================================================
Total params: 586,418
Trainable params: 586,418
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
| Trial No. | Accuracy | Normalized? | Amplitude Re-Scaled? | Optimizer | lr   | Batch Size | Epochs |
| --------- | -------- | ----------- | -------------------- | --------- | ---- | ---------- | ------ |
| 1         | 100%     | No          | Yes                  | Adam      | 1e-3 | 128        | 10     |
| --------- | -------- | ----------- | -------------------- | --------- | ---- | ---------- | ------ |
```

# Trial Results :
## Trial 1:
<p align="center"> <img src="screenshots/graph_1.png"> </p>
<p align="center"> <img src="screenshots/trial_1.png"> </p>

# References :
1. Krastev, Plamen. (2019). Real-Time Detection of Gravitational Waves from Binary Neutron Stars using Artificial Neural Networks.



