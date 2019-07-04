# R walkthrough
## setting the current working directory
setwd("C:\\Users\\...")

## to list the variables defined
ls()

## to define diffrent data types

### create an numeric 
num1 <- 40
class(num1)
```markdown
[1] "numeric"
```

### Create an integer

int1<- 40L
class(int1)
```markdown
[1] "integer"
```

Note-- Operations remain the same only the storage type changes

a=num1+10
class(a)
```markdown
[1] "numeric"
```
int1=int1 +10
class(a)
```markdown
[1] "numeric"
```
int1<-40L
b=int1+10L
class(b)
```markdown
[1] "integer"
```


###  We can do type conversions as shown above
class(num1)
```markdown
[1] "numeric"
```
int2<-as.integer(num1)
```markdown
[1] "integer"
```

### Override data types post creation
num2<-as.numeric(int2)
class(num2)
```markdown
[1] "numeric"
```
is.numeric(num2)
```markdown
[1] TRUE
```
is.integer(num2)
```markdown
[1] FALSE
```
#### do type conversion on a list
 a<-c("5","4")
 class(a)
```markdown
[1] "character"
```
 b<-as.integer(a)
 is.integer(b)
 ```markdown
[1] TRUE
```
 class(b)
 ```markdown
[1] "integer
```
 num1<-40
 is.numeric(num1)
 ```markdown
[1] TRUE
```
 class(num1)
 ```markdown
[1] "numeric"
```
 as.character(num1)
```markdown
[1] "40"
```
 as.logical(num1)
 ```markdown
[1] TRUE
```
 as.integer(num1)
 ```markdown
[1] 40
```
 as.factor(num1)
 ```markdown
[1] 40
Levels: 40
```

#### for a character variable
 char1<-'Hello'
 char1
 ```markdown
 [1] "Hello"
 ```
 is.character(char1)
 ```markdown
[1] TRUE
```
 class(char1)
 ```markdown
[1] "character"
```
 as.factor(char1)
 ```markdown
[1] Hello
Levels: Hello
```
 as.logical(char1)
 ```markdown
[1] NA
```
 as.numeric(char1)
 ```markdown
[1] NA
```
 as.integer(char1)
 ```markdown
[1] NA
```


## vectors
v1 <- c(12,14,15,20,25) -- Numerical
v1  -- numerical vector
 ```markdown
[1] 12 14 15 20 25
 ```
v2 <- c("ram","sam","irfan","uma","zora" ) 
 v2
```markdown
[1] "ram"   "sam"   "irfan" "uma"   "zora" 
```
 v3<-c("M","M","F","M")
 v3
```markdown
[1] "M" "M" "F" "F"
```
v4 <- c(TRUE,TRUE,FALSE,TRUE,TRUE)  #logical
 v4
```markdown
[1]  TRUE  TRUE FALSE  TRUE  TRUE
```
v5 <-c(12000,14000,0,20000,25000) 
 v5
```markdown
[1] 12000 14000     0 20000 25000
```
 income
```markdown
[1] 12000 14000 15000 20000 25000
```
 cust<-data.frame(id,v1,v2,v3,v4)
 cust 
```markdown
  id v1    v2 v3    v4
1  1 12   ram  M  TRUE
2  2 14   sam  M  TRUE
3  3 15 irfan  F FALSE
4  4 20   uma  F  TRUE
5  5 25  zora  M  TRUE
```
 newincome
```markdown
[1] 12 20 30 40 60
```
 mode(cust)
```markdown
[1] "list"
```
 class(cust)
```markdown
[1] "data.frame"
```
 dim(cust)
```markdown
[1] 5 5
```
 str(cust)
```markdown
'data.frame':   5 obs. of  5 variables:
 $ id: num  1 2 3 4 5
 $ v1: num  12 14 15 20 25
 $ v2: Factor w/ 5 levels "irfan","ram",..: 2 3 1 4 5
 $ v3: Factor w/ 2 levels "F","M": 2 2 1 1 2
 $ v4: logi  TRUE TRUE FALSE TRUE TRUE
 ```


cust<-data.frame(id,v1,v2,v3,v4,stringsAsFactors = FALSE)
str(cust)
```markdown
'data.frame':	5 obs. of  5 variables:
 $ id: num  1 2 3 4 5
 $ v1: num  12 14 15 20 25
 $ v2: chr  "ram" "sam" "irfan" "uma" ...
 $ v3: chr  "M" "M" "F" "F" ...
 $ v4: logi  TRUE TRUE FALSE TRUE TRUE
 ```
cust$v3<-as.factor(v3)
v3
```markdown
[1] "M" "M" "F" "F" "M"
```
cust$v3<-as.factor(v3)
 str(v3)
 ```markdown
 chr [1:5] "M" "M" "F" "F" "M"
 ```
 str(cust)
 ```markdown
'data.frame':	5 obs. of  5 variables:
 $ id: num  1 2 3 4 5
 $ v1: num  12 14 15 20 25
 $ v2: chr  "ram" "sam" "irfan" "uma" ...
 $ v3: Factor w/ 2 levels "F","M": 2 2 1 1 2
 $ v4: logi  TRUE TRUE FALSE TRUE TRUE
 ```

### to  edit the loaded dataset
fix(cust)

### similar like data frame character mode
news<-c("north","east","west","south")
news
```markdown
[1] "north" "east"  "west"  "south"
```
mode(news)
```markdown
[1] "character"
```
news<-as.factor(news)
str(news)
```markdown
 Factor w/ 4 levels "east","north",..: 2 1 4 3
```




### matrix operation and definations
matr1<-matrix(1:12,ncol=4)
matr1
```markdown
[,1] [,2] [,3] [,4]
[1,]    1    4    7   10
[2,]    2    5    8   11
[3,]    3    6    9   12
```
matr2<-matrix(1:12,nrow=4)
matr2
```markdown
[,1] [,2] [,3]
[1,]    1    5    9
[2,]    2    6   10
[3,]    3    7   11
[4,]    4    8   12
```
class(matr2)
```markdown
[1] "matrix"
```
str(matr2)
```markdown
int [1:4, 1:3] 1 2 3 4 5 6 7 8 9 10 ...
```
dim(matr2)
```markdown
[1] 4 3
```


matdf<-as.data.frame(matr1)
matdf
```markdown
  V1 V2 V3 V4
1  1  4  7 10
2  2  5  8 11
3  3  6  9 12
```
class(matdf)
```markdown
[1] "data.frame"
```
mat<-as.matrix(matr1)
class(mat)
```markdown
[1] "matrix"
```
edit(matdf)
```markdown
  V1 V2 V3 V4
1  1  4  7 10
2  2  5  8 11
3  3  6  9 12
```
id
```markdown
[1] 1 2 3 4 5
```
v1
```markdown
[1] 12 14 15 20 25
```

#### do a horizontal or row level matrix creation
idv1<-rbind(id,v1)
idv1
```markdown
    [,1] [,2] [,3] [,4] [,5]
id    1    2    3    4    5
v1   12   14   15   20   25
```
class(idv1)
```markdown
[1] "matrix"
```
#### do a horizontal or row level matrix creation
idv1cbind<-cbind(id,v1)
idv1cbind
```markdown
      id v1
[1,]  1 12
[2,]  2 14
[3,]  3 15
[4,]  4 20
[5,]  5 25
```
class(idv1cbind)
```markdown
[1] "matrix"
```
#### transpose a matrix
t(idv1)
```markdown
      id v1
[1,]  1 12
[2,]  2 14
[3,]  3 15
[4,]  4 20
[5,]  5 25
```



#### assign names to ro and columns to a matrix
matr1
```markdown
             [,1] [,2] [,3] [,4]
      [1,]    1    4    7   10
      [2,]    2    5    8   11
      [3,]    3    6    9   12
```      
row.names(matr1)<-c("emp1","emp2","emp3")
matr1
```markdown
            [,1] [,2] [,3] [,4]
      emp1    1    4    7   10
      emp2    2    5    8   11
      emp3    3    6    9   12
```
colnames(matr1)<-c("col1","col2","col3","col")
matr1
```markdown
            col1 col2 col3 col
      emp1    1    4    7  10
      emp2    2    5    8  11
      emp3    3    6    9  12
```


 #### matrix multiplication
matr1
```markdown
       col1 col2 col3 col4
emp1    1    4    7   10
emp2    2    5    8   11
emp3    3    6    9   12
```
matr2
```markdown
      [,1] [,2] [,3]
[1,]    1    5    9
[2,]    2    6   10
[3,]    3    7   11
[4,]    4    8   12
```
mulmat <- matr-1  *  1
mulmat <- matr1 %*% matr2
mulmat
```markdown
      [,1] [,2] [,3]
emp1   70  158  246
emp2   80  184  288
emp3   90  210  330
```
matr1
```markdown
      col1 col2 col3 col4
emp1    1    4    7   10
emp2    2    5    8   11
emp3    3    6    9   12
```
matr2
```markdown
      [,1] [,2] [,3]
[1,]    1    5    9
[2,]    2    6   10
[3,]    3    7   11
[4,]    4    8   12
```





objlist1<-list(1,"ram",100)
objlist1
```markdown
[[1]]
[1] 1

[[2]]
[1] "ram"

[[3]]
[1] 100
```

matr1[3]
```markdown
[1] 3
```
matr1
```markdown
      col1 col2 col3 col4
emp1    1    4    7   10
emp2    2    5    8   11
emp3    3    6    9   12
```
matr1[4]
```markdown
[1] 4
```
matr1
```markdown
      col1 col2 col3 col4
emp1    1    4    7   10
emp2    2    5    8   11
emp3    3    6    9   12
```
rowsum<-rowSums(matr1)
rowsum
```markdown
emp1 emp2 emp3 
22   26   30 
```
colsum<-colSums(matr1)
colsum
```markdown
col1 col2 col3 col4 
6   15   24   33 
```


