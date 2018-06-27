# Deepl Learning usin h2o

### set path include library and start h2o cluster
```markdown
setwd('set your scripts directory')
library('h2o')
h2o.init()
```
### load data and divide ito train valid test
_Download thw dataset from kaggle mnisit_
```markdown
digits.data<-read.csv("train.csv")
train<-digits.data[1:5000,]
valid<-digits.data[5000:10000,]
test<-digits.data[10001:15000,]
```
### convert to h2o Variables
```markdown
train$label<-factor(train$label)
train_h2o<-as.h2o(train)
test_h2o<-as.h2o(test)
```

### train the model 
_it take colnums as input labels will be y=column 1 and input x=columns 2:785 hidden wll take a vector of no of hidden units in each layer in sequence_
```markdown
model<-h2o.deeplearning(x=2:785,
                        y=1,
                        training_frame = train_h2o,
                        seed = 0,
                        hidden = c(10,10))
```
### predictions
```markdown
> preds<-h2o.predict(model,test_h2o)
  |==============================================================================================================| 100%
> h2o.confusionMatrix(model,test_h2o)
Confusion Matrix: Row labels: Actual class; Column labels: Predicted class
         0   1   2   3   4   5   6   7   8   9  Error          Rate
0      429   0   3   5   3   6   2   2   7   1 0.0633 =    29 / 458
1        0 576   3   8   0   4   4   4   7   1 0.0511 =    31 / 607
2        3   2 388   9   9   9  20  18   9   2 0.1727 =    81 / 469
3        3   2  31 419   1  28   2  10  19   3 0.1911 =    99 / 518
4        1   5   2   3 454   2  14   3   1  24 0.1081 =    55 / 509
5       10   2   8  20   4 377  11   4   9   7 0.1659 =    75 / 452
6        8   2  10   4   5  20 438   0   0   0 0.1006 =    49 / 487
7        2   4   9  10   6   2   0 455   4  19 0.1096 =    56 / 511
8        5  27  11  10   4  12   4   4 414   7 0.1687 =    84 / 498
9        6   2   2   6  22   3   1  23   6 420 0.1446 =    71 / 491
Totals 467 622 467 494 508 463 496 523 476 484 0.1260 = 630 / 5,000
```
