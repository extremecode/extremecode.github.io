# Dataset Operations

## set your working dir
setwd('C:/Users/../Rworkingdir/')
getwd()
```markdown
[1] "C:/Users/../Rworkingdir/"
```
emp <- read.csv('empnew.csv',sep = ',')
emp
```markdown
     id gender      bdate educ    jobcat salary salbegin jobtime prevexp minority
1     1   Male 03-02-1952   15   Manager  57000    27000      98     144       No
2     2   Male 23-05-1958   16  Clerical  40200    18750      98      36       No
3     3 Female 26-07-1929   12  Clerical  21450    12000      98     381       No
4     4 Female 15-04-1947    8  Clerical  21900    13200      98     190       No
5     5   Male 09-02-1955   15  Clerical  45000    21000      98     138       No
6     6   Male 22-08-1958   15  Clerical  32100    13500      98      67       No
7     7   Male 26-04-1956   15  Clerical  36000    18750      98     114       No
8     8 Female 06-05-1966   12  Clerical  21900     9750      98      NA       No
9     9 Female 23-01-1946   15  Clerical  27900    12750      98     115       No
10   10 Female 13-02-1946   12  Clerical  24000    13500      98     244       No
11   11 Female 07-02-1950   16  Clerical  30300    16500      98     143       No
12   12   Male 11-01-1966    8  Clerical  28350    12000      98      26      Yes
13   13   Male 17-07-1960   15  Clerical  27750    14250      98      34      Yes
14   14 Female 26-02-1949   15  Clerical  35100    16800      98     137      Yes
15   15   Male 29-08-1962   12  Clerical  27300    13500      97      66       No
16   16   Male 17-11-1964   12  Clerical  40800    15000      97      24       No
17   17   Male 18-07-1962   15  Clerical  46000    14250      97      48       No
18   18   Male 20-03-1956   16   Manager 103750    27510      97      70       No
19   19   Male 19-08-1962   12  Clerical  42300    14250      97     103       No
20   20 Female 23-01-1940   12  Clerical  26250    11550      97      48       No
21   21 Female 19-02-1963   16  Clerical  38850    15000      97      17       No
22   22   Male 24-09-1940   12  Clerical  21750    12750      97     315      Yes
23   23 Female 15-03-1965   15  Clerical  24000    11100      97      75      Yes
24   24 Female 27-03-1933   12  Clerical  16950     9000      97     124      Yes
25   25 Female 01-07-1942   15  Clerical  21150     9000      97     171      Yes
26   26   Male 08-11-1966   15  Clerical  31050    12600      96      14       No
27   27   Male 19-03-1954   19   Manager  60375    27480      96      96       No
28   28   Male 11-04-1963   15  Clerical  32550    14250      96      43       No
29   29   Male 28-01-1944   19   Manager 135000    79980      96     199       No
30   30   Male 17-09-1961   15  Clerical  31200    14250      96      54       No
31   31   Male 24-02-1964   12  Clerical  36150    14250      96      83       No
32   32   Male 28-01-1954   19   Manager 110625    45000      96     120       No
33   33   Male 18-03-1961   15  Clerical  42000    15000      96      68       No
34   34   Male 02-02-1949   19   Manager  92000    39990      96     175       No
35   35   Male 22-08-1961   17   Manager  81250    30000      96      18       No
36   36 Female 07-08-1963    8  Clerical  31350    11250      96      52       No
37   37   Male 09-10-1954   12  Clerical  29100    13500      96     113      Yes
38   38   Male 27-04-1962   15  Clerical  31350    15000      96      49      Yes
39   39   Male 22-06-1960   16  Clerical  36000    15000      96      46      Yes
40   40 Female 28-08-1933   15  Clerical  19200     9000      96      23      Yes
41   41 Female 18-03-1961   12  Clerical  23550    11550      96      52      Yes
42   42   Male 23-09-1960   15  Clerical  35100    16500      95      90       No
43   43   Male 18-01-1964   12  Clerical  23250    14250      95      46       No
44   44   Male 15-06-1963    8  Clerical  29250    14250      95      50       No
45   45   Male 02-08-1938   12 Custodial  30750    13500      95     307       No
46   46 Female 18-11-1940   15  Clerical  22350    12750      95     165       No
47   47 Female 28-04-1938   12  Clerical  30000    16500      95     228       No
48   48   Male 07-06-1947   12 Custodial  30750    14100      94     240       No
49   49   Male 16-09-1958   15  Clerical  34800    16500      94      93       No
50   50   Male 09-02-1960   16   Manager  60000    23730      94      59       No
51   51   Male 08-07-1962   12  Clerical  35550    15000      94      48       No
52   52   Male 12-11-1963   15  Clerical  45150    15000      94      40       No
53   53   Male 21-04-1954   18   Manager  73750    26250      94      56       No
54   54   Male 04-06-1931   12  Clerical  25050    13500      94     444       No
55   55   Male 25-06-1960   12  Clerical  27000    15000      94     120       No
56   56   Male 16-04-1962   15  Clerical  26850    13500      94       5       No
57   57   Male 15-04-1963   15  Clerical  33900    15750      94      78       No
58   58 Female 14-11-1964   15  Clerical  26400    13500      94       3       No
59   59   Male 07-05-1961   15  Clerical  28050    14250      94      36      Yes
60   60   Male 16-02-1959   12  Clerical  30900    15000      94     102      Yes
61   61   Male 28-04-1964    8  Clerical  22500     9750      94      36      Yes
62   62   Male 18-07-1962   16   Manager  48000    21750      93      22       No
63   63   Male 20-08-1961   17   Manager  55000    26250      93      32       No
64   64   Male 28-09-1963   16   Manager  53125    21000      93      48       No
65   65   Male 28-03-1964    8  Clerical  21900    14550      93      41       No
66   66   Male 16-02-1962   19   Manager  78125    30000      93       7       No
67   67   Male 28-05-1964   16   Manager  46000    21240      93      35       No
68   68   Male 05-05-1963   16   Manager  45250    21480      93      36       No
69   69   Male 23-06-1960   16   Manager  56550    25000      93      34       No
70   70   Male 08-02-1962   15  Clerical  41100    20250      93      27       No
71   71   Male 26-08-1948   17   Manager  82500    34980      93     207       No
72   72 Female 07-01-1964   16  Clerical  54000    18000      93      11       No
73   73 Female 09-02-1968   12  Clerical  26400    10500      93      NA       No
74   74 Female 28-04-1933   15  Clerical  33900    19500      93     192       No
75   75 Female 12-08-1965   15  Clerical  24150    11550      93      NA       No
76   76 Female 03-09-1967   15  Clerical  29250    11550      93      11       No
77   77 Female 09-09-1968   12  Clerical  27600    11400      93       6       No
78   78 Female 20-08-1968   12  Clerical  22950    10500      93      10       No
79   79 Female 23-01-1962   16  Clerical  34800    14550      93       8       No
80   80 Female 25-05-1961   16  Clerical  51000    18000      93      22       No
81   81 Female 12-03-1968   12  Clerical  24300    10950      93       5       No
82   82 Female 28-08-1947   12  Clerical  24750    14250      93     193      Yes
83   83 Female 12-10-1967   12  Clerical  22950    11250      93      NA      Yes
84   84 Female 12-03-1967    8  Clerical  25050    10950      93       8      Yes
85   85   Male 09-04-1962   15  Clerical  25950    17100      92      42       No
86   86   Male 25-08-1961   15  Clerical  31650    15750      92      64       No
87   87   Male 20-10-1959   12  Clerical  24150    14100      92     130       No
88   88   Male 10-02-1962   19   Manager  72500    28740      92      10       No
89   89   Male 24-06-1961   19   Manager  68750    27480      92       8       No
90   90 Female 27-02-1938    8  Clerical  16200     9750      92      NA       No
91   91 Female 04-11-1967   12  Clerical  20100    11250      92      24       No
92   92 Female 25-06-1968    8  Clerical  24000    10950      92       6       No
93   93 Female 05-03-1968   12  Clerical  25950    10950      92      NA       No
94   94 Female 04-08-1950   12  Clerical  24600    10050      92      44       No
95   95 Female 08-08-1968   12  Clerical  28500    10500      92       6       No
96   96   Male 02-10-1933    8 Custodial  30750    15000      92     432      Yes
97   97   Male 18-01-1953   17  Clerical  40200    19500      92     168      Yes
98   98   Male 17-05-1956    8 Custodial  30000    15000      92     144      Yes
99   99 Female 07-07-1968   12  Clerical  22050    10950      92       5      Yes
100 100   Male 25-10-1963   18   Manager  78250    27480      91      47       No
 [ reached 'max' / getOption("max.print") -- omitted 374 rows ]
 ```
 ### to check data dimension
dim(emp)
```markdown
[1] 474  10
```
### to check structure of the data 
str(emp)
```markdown
'data.frame':	474 obs. of  10 variables:
 $ id      : int  1 2 3 4 5 6 7 8 9 10 ...
 $ gender  : Factor w/ 2 levels "Female","Male": 2 2 1 1 2 2 2 1 1 1 ...
 $ bdate   : Factor w/ 462 levels "","01-02-1963",..: 29 366 410 227 116 358 408 73 361 189 ...
 $ educ    : int  15 16 12 8 15 15 15 12 15 12 ...
 $ jobcat  : Factor w/ 3 levels "Clerical","Custodial",..: 3 1 1 1 1 1 1 1 1 1 ...
 $ salary  : int  57000 40200 21450 21900 45000 32100 36000 21900 27900 24000 ...
 $ salbegin: int  27000 18750 12000 13200 21000 13500 18750 9750 12750 13500 ...
 $ jobtime : int  98 98 98 98 98 98 98 98 98 98 ...
 $ prevexp : int  144 36 381 190 138 67 114 NA 115 244 ...
 $ minority: Factor w/ 2 levels "No","Yes": 1 1 1 1 1 1 1 1 1 1 ...
 ```
 ### edit the dataset if needed
fix(emp)

### write the data to a file
write.csv(emp,file='emp.csv')
write.table(emp,file='location/emp.txt',sep="\t")
### to work with excel files
install.packages("readxl")
#### to load a package use library command
library(readxl)
Xldata<-read_excel("Path file.xlsx",sheet="sheetname")

### check the variable type
class(emp)
```markdown
[1] "data.frame"
```
### select observation and variables
emp10obs<-emp[1:10,]
emp5var<-emp[,1:5]
### select column or feature vectors specify columns as a vector
emp_cont<-emp[ ,c(4,6,7,8)]
emp_cat<-emp[,-c(4,6,7,8)]
### to see first 6 record 
head(emp_cat)
```markdown
  id gender      bdate   jobcat prevexp minority
1  1   Male 03-02-1952  Manager     144       No
2  2   Male 23-05-1958 Clerical      36       No
3  3 Female 26-07-1929 Clerical     381       No
4  4 Female 15-04-1947 Clerical     190       No
5  5   Male 09-02-1955 Clerical     138       No
6  6   Male 22-08-1958 Clerical      67       No
```
