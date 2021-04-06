# CarClassifierDeTectTechnologies
Used Transfer Learning(VGG16) to classify between two cars. Basically, It was an assignment given by Detect Technologies to test my Machine Learning skills.


Solution -
Just to make you aware before explaining the code and my approach, I am basically classifing two cars( Namely - Hyundai i10 & Hyundai i20) using Pretrained Model- VGG 16 [Transfer Learning].

My approach -
Loading all the data from google drive as a zip folder, then carefully unzipping it and making two different folders[namely train and test]. So, the exact numbers taken for each class in training and testing are

Training -> Hyundai i10 - 311 & Hyundai i20 - 330

Testing -> Hyundai i10 - 24 & Hyundai i20 - 27

Here, to classify between the cars I have used VGG16 Pretrained model. Additionally, I have removed the top layers and added mine because I have only 2 unique classes(i10 & i20).

I must say, that I have tweak the hyperparameters and fine tuned, so that I can achieve 83.4% accuracy which was earlier 70%.

The hyperparameters which I have tweaked are -

optimizer = optimizers.SGD(lr=0.0001, momentum=0.9) before it was Adam.
Dense(units=4096,activation="relu") before it was not too dense(512).
activation="softmax" before it was "sigmoid".
Used ModelCheckPoint so I wont loss the weight of best accuracy.
I have also drawn graph that represent "Loss vs Validation_Loss" & "Accuracy vs Validation_Accuracy"

