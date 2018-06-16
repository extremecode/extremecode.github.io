# Basic
### IQR
*	Q3-Q1 for even set – no middle value
*	Step 1: Put the numbers in order.
1, 2, 5, 6, 7, 9, 12, 15, 18, 19, 27.
*	Step 2: Find the median.
1, 2, 5, 6, 7, 9, 12, 15, 18, 19, 27.
*	Step 3: Place parentheses around the numbers above and below the median. 
Not necessary statistically, but it makes Q1 and Q3 easier to spot.
(1, 2, 5, 6, 7), 9, (12, 15, 18, 19, 27).
*	Step 4: Find Q1 and Q3
Think of Q1 as a median in the lower half of the data and think of Q3 as a median for the upper half of data.
(1, 2, 5, 6, 7),  9, ( 12, 15, 18, 19, 27). Q1 = 5 and Q3 = 18.
*	Step 5: Subtract Q1 from Q3 to find the interquartile range.
18 – 5 = 13.
```markdown
> a<-c(1,2,5,6,7,9,12,15,18,19,27)
> IQR(a)
[1] 13
```
