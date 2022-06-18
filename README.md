# Self_Supervised_Learning
SSL, Transfer Learning, Fine Tuning

In this repository we implemented a simple example of learning visual features using a self-supervised learning approach. We performed the following steps on the CIFAR10 dataset.

In this experiment, we kept only 20 labeled training data from each class and used the rest of the data unlabeled. In other words, we generated a total of 200 labeled training data and 49,800 unlabeled training data for training, and retained 10,000 labeled test data for model evaluation.

Part A) We trained our model only using labeled training data and evaluated it on test data.

Part B) Using unlabeled training data, we solved the problem of image angle detection as a pre-training problem. Then, we removed the end layers of the network and instead placed a layer with 10 neurons for classification. Then the model trained with these initial weights using labeled training data.

Part C) We changed our model to have two outputs: one output for angle classification and one output for 10-class classification. Then, we trained the model with all 50,000 training data. 49,800 sample data are not labeled Therefore, for this data, we set the output of the 10-class classification equal to the zero vector so as not to affect its loss function.

  In this case, the effect of each loss function must be set correctly. Due to the small number of labeled data, their effect will be low overall. We evaluated the trained model on test data and compared it with previous results.

* Note that in our case, it's not just the input of the two issues in common, but the bulk of the CNN network for the two issues are in common.
