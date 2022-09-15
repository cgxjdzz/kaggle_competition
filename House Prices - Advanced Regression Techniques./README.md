In this competition, I learn and implement some tricks. Firstly, in preprocessing part, I divide a validation dataset which is pretreated respectively from train dataset in case of Data leakage.
Besides this, I also get zscore of the label instead of the oringinal price data, because the numbers of them are in a wide range. And in prediction, I use the mean and standard deviation calculated from train data to get the final price of the test dataset. 
Noticalbely, after zscore are used, there will be a obvious flucuation in learing-line plot if drop-out layers are activated.
In training part, I save the model which has the best behaviour in validation test.
About the learning rate, there isn't anything large difference whether the number decease like cos does with the increase of epoch. 
####################
And in machine learning, there are some trick in feature processing, just like apply log1p on both features and labels to transform them to normal distribution. 
Turn qualitative features to  quantitative things by implementing encode function sort one feature according to the mean price in each type and use 1:n to replace them
Then create new features in 2 ways. The first one is add some related features together, while the other is 1 or 0 for some features.
Count the most frequnt values in each feature, then delete those who have almost same values in all samples.
Commercing with the model construction, they used RobustScaler before some specific models, and sum RidgeCV, LassoCV, ElasticNetCV, SVR, GradientBoostingRegressor, LGBMRegressor, XGBRegressor and StackingCVRegressor result together to predict final answer.
I use h2o autoML to replace these complex model, however, the model obviously overfit and give a prediction with quite a large bias.
