''' 

The task is predicting categories of leaf images. This dataset contains 176 categories, 18353 training images, 8800 test images. Each category has at least 50 images for training. The test set is split evenly into the public and private leaderboard. 

''' 

In this competition, I used pre-trained resnet50 in timm package as the baseline. Then I implemented label smoothing as a method of normalization, and augmentation and some other transform tricks (like mixup and cutmix) were applied on the train data to imporve generalization.
Besides those, I found a theory that after each batch is trained, we increase the learning rate. Then the best learning rate is the one with lowest loss. More detail in the essay 'Cyclical Learning Rates for Training Neural Networks'
