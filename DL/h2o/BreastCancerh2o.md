# Deep learning using h2o
### load packages and start h2o
nthreads =-1 will utilize all your cpu cores
```markdown
library('mlbench')
library('h2o')
h2o.init(nthreads = -1)
```
### load data 
_the dataset two classes levels benign,malignant to predict the breast cancer_
```markdown
> data("BreastCancer")
> str(BreastCancer)
'data.frame':	699 obs. of  11 variables:
 $ Id             : chr  "1000025" "1002945" "1015425" "1016277" ...
 $ Cl.thickness   : Ord.factor w/ 10 levels "1"<"2"<"3"<"4"<..: 5 5 3 6 4 8 1 2 2 4 ...
 $ Cell.size      : Ord.factor w/ 10 levels "1"<"2"<"3"<"4"<..: 1 4 1 8 1 10 1 1 1 2 ...
 $ Cell.shape     : Ord.factor w/ 10 levels "1"<"2"<"3"<"4"<..: 1 4 1 8 1 10 1 2 1 1 ...
 $ Marg.adhesion  : Ord.factor w/ 10 levels "1"<"2"<"3"<"4"<..: 1 5 1 1 3 8 1 1 1 1 ...
 $ Epith.c.size   : Ord.factor w/ 10 levels "1"<"2"<"3"<"4"<..: 2 7 2 3 2 7 2 2 2 2 ...
 $ Bare.nuclei    : Factor w/ 10 levels "1","2","3","4",..: 1 10 2 4 1 10 10 1 1 1 ...
 $ Bl.cromatin    : Factor w/ 10 levels "1","2","3","4",..: 3 3 3 3 3 9 3 3 1 2 ...
 $ Normal.nucleoli: Factor w/ 10 levels "1","2","3","4",..: 1 2 1 7 1 7 1 1 1 1 ...
 $ Mitoses        : Factor w/ 9 levels "1","2","3","4",..: 1 1 1 1 1 1 1 1 5 1 ...
 $ Class          : Factor w/ 2 levels "benign","malignant": 1 1 1 1 1 2 1 1 1 1 ...
```
### preprocess the data
_remove the id column its of no use and convert all values to numeric by apply spply of mlbench and make class as factor_
```markdown
data<-BreastCancer[,-1]
data[,(1:ncol(data))]<-sapply(data[,(1:ncol(data))],as.numeric)
data[,'Class']<-as.factor(data[,'Class'])
```
### split the dataset into train test and validation set 60%,20%,20%
```markdown
splitsample<-sample(1:3,size = nrow(data),prob = c(0.6,0.2,0.2),replace = TRUE)
train_h2o<-as.h2o(data[splitsample==1,])
val_h2o<-as.h2o(data[splitsample==2,])
test_h2o<-as.h2o(data[splitsample==3,])
```
### build model
* x = columns no of input 
* y= columns no of output
* activation = activation function ex tan,sigmoid,relu 
#### regularization parameters
* for input input_dropout_ratio = 0.2 -- 20%
* for the hidden layers hidden_dropout_ratios = c(0.3,0.3) -- 30%
* hidden - it will take a vector of no of hidden layer in sequence
* epochs -- no of times the process of train should iterate
```markdown
>model<-h2o.deeplearning(x=1:9,
                        y=10,
                        training_frame = train_h2o,
                        activation = "TanhWithDropout",
                        #input dropout
                        input_dropout_ratio = 0.2,
                        balance_classes = TRUE,
                        hidden = c(10,10),
                        #hidden dropout
                        hidden_dropout_ratios = c(0.3,0.3),
                        epochs = 10,
                        seed = 0)
                        > #model prediction measures                     
```
### predictions
```markdown
> h2o.confusionMatrix(model)
Confusion Matrix (vertical: actual; across: predicted)  for max f1 @ threshold = 0.138356237602112:
         1   2    Error     Rate
1      261  12 0.043956  =12/273
2        7 270 0.025271   =7/277
Totals 268 282 0.034545  =19/550
```
