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


# We can do type conversions
class(num1)
```markdown
[1] "numeric"
```
int2<-as.integer(num1)
```markdown
[1] "integer"
```
