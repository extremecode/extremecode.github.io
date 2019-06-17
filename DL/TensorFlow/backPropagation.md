# backpropagation

## import libraries
```markdown
import numpy as np
import matplotlib.pyplot as plt
from builtins import range
```

## define forward function
```markdown
def forward(X,W1,b1,W2,b2):
    Z = 1/( 1 + np.exp(-X.dot(W1)-b1))
    expA = np.exp(Z.dot(W2)+b2)
    Y = expA/expA.sum(axis=1,keepdims = True)
    return Y,Z
    
def classification_rate(Y,P):
    n_total = 0
    n_correct = 0
    for i in range(len(Y)):
        n_total +=1
        if(Y[i] == P[i]):
            n_correct +=1
    return float(n_correct) / n_total    
```

## define gaussian clouds as our input
```markdown
Nclass = 500

D = 2
M = 3
K = 3

X1 = np.random.randn(Nclass,2) + np.array([0,-2])
X2 = np.random.randn(Nclass,2) + np.array([2,2])
X3 = np.random.randn(Nclass,2) + np.array([-2,2])

X = np.vstack([X1,X2,X3])
Y = np.array([0]*Nclass + [1]*Nclass + [2]*Nclass)

N = len(Y)
T = np.zeros((N,K))

for i in range(N):
    T[i,Y[i]] = 1
    
plt.scatter(X[:,0],X[:,1],c = Y,alpha=0.5,s = 100)
plt.show()

```

## backpropagation equation
```markdown
def cost(T,Y):
    tot = T*np.log(Y)
    return tot.sum()

def derivative_W2(T,Y,Z):
    N,D = T.shape
    M = Z.shape[1]
    
#     ret1 = np.zeros((M,K))
#     for n in range(N):
#         for m in range(M):
#             for k in range(K):
#                 ret1[m,k] += (T[n,k] - Y[n,k])*Z[n,m]
                
#     ret2 = np.zeros((M,K))
#     for n in range(N):
#         for k in range(K):
#             ret2[:,k] += (T[n,k] - Y[n,k])*Z[n,:]            
#     assert(np.abs(ret1-ret2).sum()<10e-10)  
    
#     ret3 = np.zeros((M,K))
#     for n in range(N):
#         ret3 += np.outer(Z[n],T[n] - Y[n])            
#     assert(np.abs(ret3-ret2).sum()<10e-10) 
    
#     ret4 = np.zeros((M,K))
#     ret4 = Z.T.dot(T-Y)           
#     assert(np.abs(ret4-ret3).sum()<10e-10) 
    
    return Z.T.dot(T-Y)

def derivative_b2(T,Y):
    return (T-Y).sum(axis = 0)

def derivative_W1(X,T,Y,Z,W2):
#     N,D = X.shape
#     M,k = W2.shape
    
#     ret = np.zeros((D,M))
    
#     for n in range(N):
#         for k in range(K):
#             for m in range(M):
#                 for d in range(D):
#                     ret[d,m] += (T[n,k] - Y[n,k])*W2[m,k]*Z[n,m]*(1-Z[n,m])*X[n,d]
                    
#     ret1 = np.zeros((D,M))
    
#     dZ = (T-Y).dot(W2.T)*Z*(1-Z)
#     ret1 = X.T.dot(dZ)
#     assert(np.abs(ret-ret1).sum()<10e-10) 
    
    dZ = (T-Y).dot(W2.T)*Z*(1-Z)
    return X.T.dot(dZ)
                    
def derivative_b1(T,Y,W2,Z):
    return ((T-Y).dot(W2.T)*Z*(1-Z)).sum(axis =0)
        
```


## train model and predict

```markdown
W1 = np.random.randn(D,M)
b1 = np.random.randn(M)
W2 = np.random.randn(M,K)
b2 = np.random.randn(K)


learning_rate = 10e-7
costs = []

for epoch in range(100000):
    output , hidden = forward(X,W1,b1,W2,b2)
    if epoch%100 == 0:
        c = cost(T,output)
        P = np.argmax(output,axis=1)
        print("cost is ",c," and classification rate at epoch",epoch,"is",classification_rate(Y,P))
        costs.append(c)
        
        
    W2 +=learning_rate*derivative_W2(T,output,hidden)
    b2 +=learning_rate*derivative_b2(T,output)
    W1 +=learning_rate*derivative_W1(X,T,output,hidden,W2)
    b1 +=learning_rate*derivative_b1(T,output,W2,hidden)

plt.plot(costs)
plt.show()
```
