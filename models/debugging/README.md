# Debugging
In this section of the repository, each folder contains various testcases to determine the performance of the model in various possible scenarios. Every folder has been named after the type of models being used and the kind of classification task being performed in the testcases. 

For example, the folder named ["1D-CNN Binary Classification"](/models/debugging/1D-CNN%20Binary%20Classification/) contains all the test cases that use a 1D-CNN type of model and perform the binary classification task.

# Directory Structure
Each folder in this section has the following structure:

## Folder 1
<hr>

  - ### Signal_HIDDEN_in_strain_data
    - #### Signal_NOT_WHITENED
      - Test 1
      - Test 2
      - ....
    - #### Signal_WHITENED
      - Test 1
      - Test 2
      - ....

  - ### Signal_VISIBLE_in_strain_data
    - #### Signal_NOT_WHITENED
      - Test 1
      - Test 2
      - ....
    - #### Signal_WHITENED
      - Test 1
      - Test 2
      - ....
<hr>

```
1. Signal_HIDDEN_in_strain_data
--------------------------------
In all the test cases contained in this sub-folder, the amplitude of the noise has been adjusted such that the signal is directly visible in the generated strain data.

2. Signal_VISIBLE_in_strain_data
--------------------------------
In all the test cases contained in this sub-folder, the amplitude of the noise has been adjusted such that the signal is directly visible in the generated strain data.

3. Signal_NOT_WHITENED
--------------------------------
In all the test cases contained in this sub-sub-folder, the signal is not whitened before injecting into the noise to generate the strain data.

4. Signal_WHITENED
--------------------------------
In all the test cases contained in this sub-sub-folder, the signal is whitened before injecting into the noise to generate the strain data.

```




