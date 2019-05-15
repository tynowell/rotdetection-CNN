### Master's Thesis 2019

# Detection and Quantification of Rot in Harvested Trees using Convolutional Neural Networks


# Tyrone Carlisle Nowell

Master of Science in Data Science

Faculty of Science and Technology

Norwegian University of Life Sciences

## Abstract

Root and Butt-Rot (RBR) is having a significant economic impact on the forest industry and is expected to increase with climate change. The current management strategies are becoming less effective, and little data on RBR distribution is available to develop new ones. In Europe, approximately half of the timber production is using Cut-To-Length timber harvesters which store a considerable amount of data on each tree. Being able to supplement this data with the presence and quantity of RBR in the tree would add significant value to both the forest industry and to the scientific community in developing new strategies for RBR management. 

This Master's thesis explored the feasibility of embedding a computer vision system on the harvester for autonomous rot detection and quantification using state of the art Convolutional Neural Networks (CNNs). Among the potential applications of this system, this study assessed the possibilities to (1) provide real time feedback of this information to the harvester operator for faster, more accurate categorisation of the timber quality and (2) enable the collection of big data on RBR distribution for high spatial resolution mapping for the development of new management strategies.

The model developed to detect RBR achieved an F1 score of 97.1% accuracy (precision of 95.2% and recall of 99.0%) which is a significant improvement over previous techniques with an F1 score of 90.8% accuracy (precision of 90.8% and recall of 90.8%). Prediction of the RBR quantity as a percentage of the surface area attained an RMSE of 6.88%, and was reduced to 6.17% when aggregated with the RBR detector. 

Evaluating the misclassifications of the detection system indicated that the model performance is at least on par with that of the author. These results indicate that there is significant potential in developing this technology further for both economic and environmental gains.

## Repository contents

This repository contains the original thesis and the code used. The thesis can be found in pdf form [here](Detection%20and%20Quantification%20of%20Rot%20in%20Harvested%20Trees%20using%20Convolutional%20Neural%20Networks.pdf).

The code is broken down into five notebooks:
- [Data preprocessing](Data%20preprocessing.ipynb)
- [Data selection and cross-validation](Data%20selection%20and%20cross-validation.ipynb)
- [Classification task](Classification%20task.ipynb)
- [Regression task](Regression%20task.ipynb)
- [Combined model](Combined%20model.ipynb)

## File directory structure

The following directory structure is used in the code for storing the data and dataframes, and saving logs and models.

### rotdetection-CNN/
#### data/
* orig/ (original images)
* orig_mask/ (original masks)
* crop/ (cropped images)
* crop_mask/ (cropped masks)
* equ_crop/ (histogram equalised images)
#### dataframes/ (storing dataframes for training, validation and test sets)
#### logs/
* cls/ (classifier logs)
  * comp/ (comparison of all models on unaltered images)
  * enhanced/ (comparison of all models on histogram equalised images)
  * select/ (comparison of selected models)
  * optim/ (hyperparameter tuning of final model)
  * final/ (final model with validation and without)
* reg/ (regressor logs)
  * comp/ (comparison of all models on unaltered images)
  * enhanced/ (comparison of all models on histogram equalised images)
  * select/ (comparison of selected models)
  * optim/ (hyperparameter tuning of final model)
  * final/ (final model with validation and without)
#### models/ (final models)
