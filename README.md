# Ml-from-scratch
import numpy as np 
import matplotlib.pyplot as plt

x_train=np.array([1.0,2.0])
y=np.array([300.0,500.0])

print(x_train)
print(y)

print(x_train.shape)
print(y.shape)
print(x_train.shape[0])

i=0
x1=x_train[i]
y1=y[i]
print(f"(x^{(i)},y^{(i)}=x1,y1)")

plt.scatter(x_train,y)
plt.title("Housing Price")
plt.xlabel("Size(in sqft)")
plt.ylabel("Price in dollar")
print(plt.show())
w=200
b=100
def compute_first_model(x,w,b):
    m=x.shape[0]
    x1=np.zeros(m)
    for i in range(m):
        x1[i]=w*x[i]+b
    return x1

f_wb=compute_first_model(x_train,w,b)

plt.plot(x_train,f_wb,label="Prediction Value")
plt.scatter(x_train,y,label="Actual values")
plt.title("Housing price")
plt.xlabel("Size in sqft")
plt.ylabel("Price in 1000s")
plt.legend()
print(plt.show())

x_m=1.2
cost_1200sqft=w*x_m+b
print(cost_1200sqft)
 
