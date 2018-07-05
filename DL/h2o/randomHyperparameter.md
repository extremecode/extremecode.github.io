# Deep learning using h2o
## Hyperparameter Training
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
### hyper parameter tuning
_try almost known combination of hyperparmeters and tuned it accordingly_
```markdown
hyper_params<-list(
  activation=c("Rectifier","Tanh","Maxout"
                ,"RectifierWithDropout",
                "TanhWithDropout","MaxoutWithDropout"),
  hidden=list(c(20,20),c(50,50),c(30,30,30),c(25,25,25,25)),
  input_dropout_ratio=c(0,0.5),
  l1=seq(0,1e-4,1e-6),
  l2=seq(0,1e-4,1e-6)
)
```
### setting the search criteria
_ max_runtime_secs= time in seconds max which a model train,
  max_models=100 no of models to train,seed= same situation,stopping_rounds= iterations,
  stopping_tolerance= max of % of train in no  ex = 1% e-2 two iteration_
search_criteria<-list(
  strategy="RandomDiscrete",max_runtime_secs=360,
  max_models=100,seed=1234567,stopping_rounds=5,
  stopping_tolerance=1e-2
)
dl_random_grid<-h2o.grid(
  algorithm = "deeplearning",
  grid_id = "dl_grid_random",
  training_frame=train_h2o,
  validation_frame=val_h2o,
  x=1:9,
  y=10,
  epochs=1,
  stopping_metric="logloss",
  stopping_tolerance=1e-2,
  stopping_rounds=2,
  hyper_params = hyper_params,
  search_criteria = search_criteria
)
### get the best grid on the basis of logloss
```markdown
grid<-h2o.getGrid("dl_grid_random",sort_by="logloss",
               decreasing=FALSE)
grid@summary_table[1,]
```
### best model
```markdown
best_model<-h2o.getModel(grid@model_ids[[1]])
best_model
```
