# Exercise
Understand the basic concept of Machine Learning ( Source: https://github.com/TienLungSun/2020-PyTorch-Colab)

**1.2.1. Learn from sparse data-Exercise Natan - Try to adding more neural network layers and check the loss result behavior.
Action: Adding NN Layers
MyNet = nn.Sequential(
    nn.Linear(1, 50),
    nn.ReLU(),
    nn.Linear(50, 25),
    nn.ReLU(),
    nn.Linear(25, 15),
    nn.ReLU(),
    nn.Linear(15, 10),
    nn.ReLU(),
    nn.Linear(10, 1),
)
 Result: Loss on training was better than before.
 ![image](https://user-images.githubusercontent.com/55201272/110065501-d748a100-7da1-11eb-9a3a-1d6c026ad5c2.png)
 
 **1.2.2. Overfitting-Exercise Natan - Understand the concept of overfitting and try to solve this issue.
 
 Action: Adding NN (no impact than before), Lock random state number, Add L1 regularization.
 
Training loss:
 ![image](https://user-images.githubusercontent.com/55201272/110065683-4c1bdb00-7da2-11eb-9ee6-175ff5004179.png)

Testing Loss:
![image](https://user-images.githubusercontent.com/55201272/110065702-59d16080-7da2-11eb-8954-759d3e4a5aa6.png)

The problem is the Y variable is always changing and the Y result always different for every new trying. 
(lock the random seed)
y = 3*x + random.uniform(0, 1)*100

![image](https://user-images.githubusercontent.com/55201272/110066786-dcf3b600-7da4-11eb-82ae-fc6382e136b7.png)


Add L1 regularization on training mode: (Ref Formula L1: https://stackoverflow.com/questions/42704283/adding-l1-l2-regularization-in-pytorch)

![image](https://user-images.githubusercontent.com/55201272/110066972-3c51c600-7da5-11eb-9aec-b37353db5da4.png)


Result:

Training Loss:

![image](https://user-images.githubusercontent.com/55201272/110067604-a9b22680-7da6-11eb-93cf-71bc93778487.png)


Testing Loss:

![image](https://user-images.githubusercontent.com/55201272/110067619-af0f7100-7da6-11eb-84e1-8ddbc5dfe01d.png)

**1.2.3. Regularization

 Best L1:
 
 ![image](https://user-images.githubusercontent.com/55201272/110074948-9a39da00-7db4-11eb-87bc-478c9e4230bf.png)

 
 Training:
 ![image](https://user-images.githubusercontent.com/55201272/110074893-85f5dd00-7db4-11eb-9191-acb2626ee109.png)

 Testing:
 ![image](https://user-images.githubusercontent.com/55201272/110074933-9312cc00-7db4-11eb-98af-8c60ce577ec9.png)

 



