# Neural Network Hotel Recommender System
Neural Network Recommender system for the hotel reservation. The goal of this project was to achieve the best HR@10 score in the final evaluation.

Author: [Jakub Fiturski](https://github.com/kabix09/)

Link to [project](https://github.com/kabix09/HotelRecommender/)

## Table of contents
* [Project description](#project-description)
* [Aim of the project](#aim-of-the-project)
* [Used Technologies](#used-technologies)
* [Installing](#installing)
* [Net Models](#net-models)
* [Recommenders](#recommenders)
* [Scores](#scores)

## Project description
Project contains two Jupyter notebooks. First one `project_1_data_preparation.ipynb` which contains data preparation. Second one `project_2_recommender_and_evaluation.ipynb` which contains **Neural Network Recommenders** body and tuning methods.

Project also contains data preprocessing files:
* data_preprocessing/data_preprocessing_toolkit.py
* data_preprocessing/dataset_specification.py
* data_preprocessing/people_identifier.py

In the project **data/hotel_data/hotel_data_original.csv** file was used as data source.

Also, there are generated HTML files containing the results of running the code.

## Aim of the project
The aim of the project is to create hotel room recommender using given dataset which returns the best result in HR@10. Created recommender is tuned and evaluated. Then the results are compared to those given by Amazon recommender.

## Used Technologies
Project is created with:
* [python](https://pl.python.org/)
* [pandas](https://pandas.pydata.org/)
* [numpy](https://numpy.org/)
* [matplotlib](https://matplotlib.org/)
* [torch](https://pytorch.org/)
* [seaborn](https://seaborn.pydata.org/)
* [jupyter notebook](https://jupyter.org/)

## Installing
To run the code on your local machine, you must install the following libraries:
* Anaconda with Python 3.8
* Dependencies listed in the `environment.yml` file 

Then go to your project directory.
The best way to [prepare the environment](https://www.machinelearningplus.com/deployment/conda-create-environment-and-everything-you-need-to-know-to-manage-conda-virtual-environment/) is use:
```
$ conda env create --name your-env-name -f environment.yml
$ conda activate your-env-name
```

Finally, in order to open the project use:
```
$ jupyter notebook
```

Now everything is prepared. Use notebooks in the given order: 
 * project_1_data_preparation.ipynb
 * project_2_recommender_and_evaluation.ipynb


## Recommenders
This project has two different recommenders using neural networks but build based on other assumptions.

First one **NNRecommender** is type of `Collaborative Recommender` which is based on the assumption that similar users like similar products.

Last one **HybridNNRecommender** is type of `Content-Based Recommender` which is based on the product contents. If products are similar and have similar features then if user likes one product he could also like second with simmilar features.

## Net Models

To build recommenders the network models below were used:

- `MLPModel`
    * https://machinelearningmastery.com/when-to-use-mlp-cnn-and-rnn-neural-networks/
    * https://scikit-learn.org/stable/modules/neural_networks_supervised.html
- `GMFModel`
    * https://pyecore.readthedocs.io/en/develop/user/gmf_notation.html
- `NeuMFModel`
    * https://d2l.ai/chapter_recommender-systems/neumf.html
- **MyContentBaseNet** - which is my own model prepared for the purposes of the project

## Scores
![final score](https://raw.githubusercontent.com/kabix09/NeuralNetworkHotelRecommender/master/img/recommender_score_final_evaluation.PNG)