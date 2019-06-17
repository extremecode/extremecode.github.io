# backpropagation

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
