# Deep learning using h2o
# Hyperparameter Training
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
###
```markdown
```
###
```markdown
```
###
```markdown
```
###
```markdown
```
