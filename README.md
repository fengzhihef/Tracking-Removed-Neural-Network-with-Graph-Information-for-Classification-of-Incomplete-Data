# Tracking-Removed-Neural-Network-with-Graph-Information-for-Classification-of-Incomplete-Data
This repository is the official implement of the paper "Tracking-Removed Neural Network with Graph Information for Classification of Incomplete Data," which leverages graph information to tackle the challenges of classifying incomplete datasets.

## Information of the paper
```latex
@article{lai2025tracking,
  title={Tracking-removed neural network with graph information for classification of incomplete data},
  author={Lai, Xiaochen and Zhang, Zheng and Chen, Hui and Zhang, Liyong and Li, Zhuohan and Lu, Wei},
  journal={Applied Intelligence},
  volume={55},
  number={3},
  pages={1--20},
  year={2025},
  publisher={Springer}
}
```

## Description
The codebase includes implementations of three models discussed in the aforementioned paper: `AE-MTL.ipynb`, `TRAE-MTL.ipynb`, and `TGAN-MTL.ipynb`, each serving a unique role:
1. **Autoencoder-based Multi-task Learning Classification (AE-MTL)**: During training and prediction, incomplete data are input to the network, and the estimation of sample data and the probabilities of class labels are calculated based on the network. The values corresponding to the missing data are selected for imputation and the label corresponding to the maximum probability is used as the sample label.
2. **Tracking-Removed Autoencoder-based Multi-task Learning Classification (TRAE-MTL)**: Built upon the TRAE model, this follows a similar approach to AE-MTL for handling incomplete data during training and prediction.
3. **Tracking-Removed Graph Aggregated Autoencoder Network-based Multi-task Learning Classification (TGAN-MTL)**: The method proposed in this paper. During the training period, the network parameters are updated using incomplete datasets and graph information, and the estimations of missing values are continuously adjusted as the variables. During the prediction period, the imputation and the classification of missing values and sample labels are calculated using the trained network.

## How to Run
The project inputs incomplete datasets and outputs completed datasets along with classification results. Example datasets can be found in the datasets folder. Follow these steps to execute the models:
1. Configure the dataset parameters and run `Incomplete_data_producer.ipynb` to induce random missingness in the complete datasets located in the `datasets` folder, thereby creating an incomplete dataset.
2. Set the parameters for the dataset and execute `TGAN-MTL.ipynb` to perform data imputation and classification. The results will be stored in the `zz_result` folder.
