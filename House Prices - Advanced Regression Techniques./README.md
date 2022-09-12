In this competition, I learn and implement some tricks. Firstly, in preprocessing part, I divide a validation dataset which is pretreated respectively from train dataset in case of Data leakage.
Besides this, I also get zscore of the label instead of the oringinal price data, because the numbers of them are in a wide range. And in prediction, I use the mean and standard deviation calculated from train data to get the final price of the test dataset. 
Noticalbely, after zscore are used, there will be a obvious flucuation in learing-line plot if drop-out layers are activated.
In training part, I save the model which has the best behaviour in validation test.
About the learning rate, there isn't anything large difference whether the number decease like cos does with the increase of epoch. 
