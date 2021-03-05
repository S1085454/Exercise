# Exercise
Understand the basic concept of Machine Learning ( Source: https://github.com/TienLungSun/2020-PyTorch-Colab)
1. 2.1. Learn from sparse data-Exercise Natan - Try to adding more neural network layers and check the loss result behavior.
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
 
 1. 2.2. Overfitting-Exercise Natan - Understand the concept of overfitting and try to solve this issue.
 Action: Adding NN (no impact than before), Lock random state number, Add L1 regularization.
 
Training loss:
 ![image](https://user-images.githubusercontent.com/55201272/110065683-4c1bdb00-7da2-11eb-9ee6-175ff5004179.png)

Testing Loss:
![image](https://user-images.githubusercontent.com/55201272/110065702-59d16080-7da2-11eb-8954-759d3e4a5aa6.png)

The concept is the Y variable is always changing because the formula include random uniform: (lock the random seed)
y = 3*x + random.uniform(0, 1)*100

Add L1 regularization

Result:

Training Loss:

![image](https://user-images.githubusercontent.com/55201272/110066309-ba14d200-7da3-11eb-86ce-826c24ff8e09.png)

Testing Loss:

![image](https://user-images.githubusercontent.com/55201272/110066332-c436d080-7da3-11eb-86a0-196a19771d8c.png)



