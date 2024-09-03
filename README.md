# Tracking-Removed-Neural-Network-with-Graph-Information-for-Classification-of-Incomplete-Data
This repository contains the implementation of the "Tracking-Removed Neural Network with Graph Information for Classification of Incomplete Data," which leverages graph information to tackle the challenges of classifying incomplete datasets.

## Description
The codebase includes implementations of three models discussed in the aforementioned paper: AE-MTL.ipynb, TRAE-MTL.ipynb, and TGAN-MTL.ipynb, each serving a unique role:
(1) Autoencoder-based multi-task learning classification (AE-MTL). During training and prediction, incomplete data are input to the network, and the estimation of sample data and the probabilities of class labels are calculated based on the network. The values corresponding to the missing data are selected for imputation and the label corresponding to the maximum probability is used as the sample label.
(2) Tracking-removed autoencoder-based multi-task learning classification (TRAE-MTL). TRAE-MTL is built based on TRAE. Similar to AE-MTL, during training and prediction, incomplete data are input to the network, and the estimation of sample data and the probabilities of class labels are calculated based on the network.
(3) Tracking-removed graph aggerated autoencoder network-based multi-task learning classification (TGAN-MTL). The method proposed in this paper. During the training period, the network parameters are updated using incomplete datasets and graph information, and the estimations of missing values are continuously adjusted as the variables. During the prediction period, the imputation and the classification of missing values and sample labels are calculated using the trained network.

## How to Run
The project inputs incomplete datasets and outputs completed datasets along with classification results. Example datasets can be found in the datasets folder. Follow these steps to execute the models:
（1）Configure the dataset parameters and run Incomplete_data_producer.ipynb to induce random missingness in the complete datasets located in the datasets folder, thereby creating an incomplete dataset.
（2）Set the parameters for the dataset and execute TGAN-MTL.ipynb to perform data imputation and classification. The results will be stored in the zz_result folder.
