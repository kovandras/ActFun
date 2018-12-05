# ActFun
## Deep Learning Homework 2018 autumn

Team name: ActFun
Team members: Karz Gergely (greg[dot]karz[at]gmail[dot]com), Kovács András(kovacsandras[dot]kat[at]com)

First and second milestones can be found in the `DeepLearning_HW_ActFun.ipynb` file.

Tests and the evaluated activation functions can be found in the `WSGAF_evaluation.ipynb` file. This file can be run to reproduce the results found in the `results` directory.

The `results` directory has the following structure:
 - `accuracy_all.ods` file containing all of the accuracies for each training
 - four directories containing results for WSGAF-1/2 both with and without passing the weights through sigmoid

Each of these four directories contain the following:
 - The five tests that were run
 - an `accuracy.ods` file containing accuracy values for all five tests and their avarages

Each test directory contains:
 - Three directories, one for each dataset (cifar-10, MNIST, Fashion-MNIST)
 - an `accuracy.csv` file containing accuracy values for each tested activation function (different weight initializations)
 - and the `accuracy.png` visualizing the data represented in the `accuracy.csv` table

Each dataset directory contains:
 - `training_loss.csv` containing loss values on the training batch and the validation dataset for all of the tested activation functions, measured at 10 step intervals. Note that for the cifar-10 dataset, validation loss values are calculated for 500 samples instead of the entire validation set, so these values will have considerable jitter
 - `train_loss.png` showing loss values on the training batches
 - `valid_loss.png` showing loss values on the validation data

Runing the `WSGAF_evaluation.ipynb` file generates one test directory, based on the selected `model_groups` value. We recommend runing this notebook in google colaboratory, as we were only able to test it using this tool.
