### Team member: You should know whether you will be working with another student or not.
Nan Chen & Shaocheng Shi

### Title & Problem Statement: You should have an idea of the specific problem that you are trying to solve for the project.
- We're trying to implement different CNN models(ResNet18 & VGG19) using pytorch to solve an image classification problem we found on Kaggle.
- We want to implement the models and see if our accuracy report are somewhat similar comparing to the original paper.
- Also we will be comparing the arruracy between the two models.
- Furthermore, we will compare the performance between our built-from-scratch model and the pretained model from pytorch to see how transfer-learning affect deep learning models.

### Data & Evaluation: You should have idea of what type of data will be used, is it publicly available, or will you need to scrap it. Additionally, you should know the evaluation criteria you will be using to measure the performance of your system.
- Our data will be publicly available from Kaggle. [Link to the data](https://www.kaggle.com/c/dogs-vs-cats)
- The training data contains 25000 images of dogs and cats with various sizes. I'm personaly thinking about reducing the training input size(at least for the begining part) since we only got a PC with 2 2080ti as computing resources, and I'm not sure how the training speed is gonna be.
- There's a test data provided, but since it's a kaggle competition, no test label are provided. Thus, we need to split the training data(with labels) into train and test part for computing accuracy.
- Labels are not explicitly provided. Instead, every image are named like `cat.11.jpg` so we need to write a program to seperate the labels.
- We will be comparing our performance both to the original paper, the pretrained model, and those competitors from Kaggle leaderboard. 
