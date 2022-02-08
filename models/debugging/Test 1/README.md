# Classes :
```
1. Noise 
2. BBH signal + Noise
```

# Dataset :
```
| S.No. | Data Type          | Mode of Generation | No. of Samples | Noise Label | Signal Label   |
| ----- | ------------------ | ------------------ | -------------- | ----------- | -------------- |
| 1     | Noise              | Gaussian           | 5000           | N1          | Not Applicable |
| ----- | ------------------ | ------------------ | -------------- | ----------- | -------------- |
| 2     | BBH signal + Noise | SEOBNRv2           | 5000           | N1          | S1             |
| ----- | ------------------ | ------------------ | -------------- | ----------- | -------------- |
```

# Model Architecture :
The following model has been obtained from the paper authored by Plamen G. Krastev [1]. You can read this paper [here](/Literature%20Review/Classification/1D-CNN/krastev_1.pdf).
``` 
Model: "sequential"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
conv1d (Conv1D)              (None, 16369, 16)         272       
_________________________________________________________________
max_pooling1d (MaxPooling1D) (None, 4092, 16)          0         
_________________________________________________________________
re_lu (ReLU)                 (None, 4092, 16)          0         
_________________________________________________________________
conv1d_1 (Conv1D)            (None, 4085, 32)          4128      
_________________________________________________________________
max_pooling1d_1 (MaxPooling1 (None, 1021, 32)          0         
_________________________________________________________________
re_lu_1 (ReLU)               (None, 1021, 32)          0         
_________________________________________________________________
conv1d_2 (Conv1D)            (None, 1014, 64)          16448     
_________________________________________________________________
max_pooling1d_2 (MaxPooling1 (None, 253, 64)           0         
_________________________________________________________________
re_lu_2 (ReLU)               (None, 253, 64)           0         
_________________________________________________________________
conv1d_3 (Conv1D)            (None, 246, 128)          65664     
_________________________________________________________________
max_pooling1d_3 (MaxPooling1 (None, 61, 128)           0         
_________________________________________________________________
re_lu_3 (ReLU)               (None, 61, 128)           0         
_________________________________________________________________
flatten (Flatten)            (None, 7808)              0         
_________________________________________________________________
dense (Dense)                (None, 7808)              60972672  
_________________________________________________________________
dense_1 (Dense)              (None, 64)                499776    
_________________________________________________________________
dense_2 (Dense)              (None, 2)                 130       
=================================================================
Total params: 61,559,090
Trainable params: 61,559,090
Non-trainable params: 0
_________________________________________________________________
```

# Trial Hyperparameters :
```
| Trial No. | Normalized? | Amplitude Re-Scaled? | Val split(in %) | Optimizer | lr   | Batch Size | Epochs |
| --------- | ----------- | -------------------- | --------------- | --------- | ---- | ---------- | ------ |
| 1         | No          | No                   | 0               | Adam      | 1e-3 | 1          | 2      |
| --------- | ----------- | -------------------- | --------------- | --------- | ---- | ---------- | ------ |
| 2         | Yes         | Yes (Due to Norm)    | 0               | Adam      | 1e-3 | 1          | 2      |
| --------- | ----------- | -------------------- | --------------- | --------- | ---- | ---------- | ------ |
| 3         | No          | Yes                  | 0               | Adam      | 1e-3 | 1          | 2      |
| --------- | ----------- | -------------------- | --------------- | --------- | ---- | ---------- | ------ |
```

# Trial Results :
## Trial 1:
<p align="center"> <img src="screenshots/graph_1.png"> </p>
<p align="center"> <img src="screenshots/trial_1.png"> </p>

## Trial 2:
<p align="center"> <img src="screenshots/graph_2.png"> </p>
<p align="center"> <img src="screenshots/trial_2.png"> </p>

## Trial 3:
<p align="center"> <img src="screenshots/graph_3.png"> </p>
<p align="center"> <img src="screenshots/trial_3.png"> </p>

# References :
1. Krastev, Plamen. (2019). Real-Time Detection of Gravitational Waves from Binary Neutron Stars using Artificial Neural Networks.



