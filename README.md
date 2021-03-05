# Exercise
Understand the basic concept of Machine Learning
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

