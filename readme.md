# Assignment 4 - Age Prediction
## _Problem Description_
#### Age prediction as a CV task is useful for various real-world applications, such as age-restricted content filtering, personalized marketing targeting specific age demographics, enhancing security systems with age verification, and assisting in medical diagnostics and age-related research.

## _DataSet Description_
### Files
        train - contains the training set images.
        test - contains the test set images.
        train.csv - contains the ground truth age for the training set images.
        submission.csv - a sample submission file in the correct format.

## _Solution Description_
### Trained different pre-trained models (Transfer Learning) like ResNet18, ResNet50, ResNet101 separately. Hyperparameters like learning rate, SGD momentum were also fine tuned. Extracted best model based on least validation error (0.1 times size of train data). ResNet18 had high bias and upon increasing epochs, variance increased, MAE of 6.2947. ResNet50 was able to produce decent results as it captured the patterns effectively and least validation error of 4.65 and MAE of 5.795. ResNet101 was able to produce terrific results, least validation error of 4.47 and MAE of 5.635. Upon combining the results of ResNet50 and ResNet101, taking mean of predicted ages since this is a regression task. Ensemble methods (bagging) gave better results than both the models, MAE of 5.3594.