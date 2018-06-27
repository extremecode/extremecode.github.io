# Deepl Learning usin h2o

### set path include library and start h2o cluster
```markdown
setwd('set your scripts directory')
library('h2o')
h2o.init()
```
### load data and divide ito train valid test
```markdown
digits.data<-read.csv("train.csv")
train<-digits.data[1:5000,]
valid<-digits.data[5000:10000,]
test<-digits.data[10001:15000,]
```

```markdown

```

```markdown

```
