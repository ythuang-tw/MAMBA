# Dataset info

## preprocess data
We provide all preprocess data in our experiments, and you can find it under `/data/preprocesssing_dataset/all_mist/`.
The zip file including all mist files used in our experiments.
- ### MIST Format
    The MIST should have one line per api call, and each api call should look like this:
    ```
    01 02 | b'c:\\windows\\syswow64\\ntdll.dll'
    ```
    Where:
    - `01`: the category of the api call
    - `02`: the function name of the api call
    - `b'c:\\windows\\syswow64\\ntdll.dll'`: the sets of manipulated resources from the api call
    
    To know the api call which the number indicates, you can use `/data/selected_API.xlsx - sheet2`. And the api calls related to discovering TTPs  used in this study can be find in `/data/MAMBA_selected_API_table.pdf`. 

## TTP labeling methods
To label each malware sample in datasets, we applied three label methods:
- ATT&CK dataset: 
    - MITRE: `/preprocessing_dataset/MITRE_Dataset/dataset_matrix.csv`
- Big dataset: 
    - Cuckoo: `/preprocessing_dataset/BIG_Dataset_cuckoo/dataset_matrix.csv`
    - RegExp: `/preprocessing_dataset/BIG_Dataset_regex/dataset_matrix.csv`

## Toy dataset
We provide a toy dataset for illustration. The toy dataset is a subset of the Big dataset labeled by cuckoo.
- toy dataset: 
    - cuckoo label: `/preprocessing_dataset/toy/dataset_matrix.csv`
    - trainset: `/preprocessing_dataset/toy/trainSet.txt`
      (the set of samples for training)
    - validset: `/preprocessing_dataset/toy/validSet.txt`
      (the set of samples for development)
    - testset: `/preprocessing_dataset/toy/testSet.txt`
      (the set of samples for testing)