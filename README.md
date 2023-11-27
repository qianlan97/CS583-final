# CS583-final

## Data split (data_split.ipynb)
The original data are downloaded and extraced from the Kaggle zip file. [Link to the data](https://www.kaggle.com/c/dogs-vs-cats)
```
original_data/
├── train/
│   ├── cat.X.jpg
│   └── dog.X.jpg
├── test1/
│   └── X.jpg
└── sampleSubmission.csv
```
Here we're only using the train dataset since it has labels. We select 10000 cats and 10000 dog images for training and 2500 each for testing (Using 1000/250 when developing) and put them into `processed_data` for `torchvision.datasets.ImageFolder` structure.
```
processed_data/
├── train/
│   ├── cat/
│   │   └── cat.X.jpg
│   └── dog/
│       └── dog.X.jpg
└── test/
    ├── cat/
    │   └── cat.X.jpg
    └── dog/
        └── dog.X.jpg
``` 
Note: `X` are numbers from 0, and both image folders are added into `.gitignore`.

To change the amount of images we want use in the training/testing, modify the `data_split.ipynb` file at the following lines:
```
copy_images(0, 100, 'cat', source_dir, train_dir)
copy_images(100, 125, 'cat', source_dir, test_dir)
copy_images(0, 100, 'dog', source_dir, train_dir)
copy_images(100, 125, 'dog', source_dir, test_dir)
```

## Run
Simply execuate the four jupyter notebook files.

## Predicting result

- VGG19
```
Accuracy on test set: 97.4680%

Classification Report:
              precision    recall  f1-score   support

           0       0.99      0.97      0.98      4650
           1       0.95      0.98      0.97      2775

    accuracy                           0.97      7425
   macro avg       0.97      0.98      0.97      7425
weighted avg       0.98      0.97      0.97      7425
```

- VGG19 Pre-Trained
```
Accuracy on test set: 99.3131%

Classification Report:
              precision    recall  f1-score   support

           0       1.00      0.99      0.99      4650
           1       0.99      0.99      0.99      2775

    accuracy                           0.99      7425
   macro avg       0.99      0.99      0.99      7425
weighted avg       0.99      0.99      0.99      7425
```
- Resnet18
```
Accuracy on test set: 97.3064%

Classification Report:
              precision    recall  f1-score   support

           0       0.97      0.98      0.98      4650
           1       0.97      0.95      0.96      2775

    accuracy                           0.97      7425
   macro avg       0.97      0.97      0.97      7425
weighted avg       0.97      0.97      0.97      7425
```
- ResNet18 Pre-Trained
```
Accuracy on test set: 99.2054%

Classification Report:
              precision    recall  f1-score   support

           0       1.00      0.99      0.99      4650
           1       0.99      0.99      0.99      2775

    accuracy                           0.99      7425
   macro avg       0.99      0.99      0.99      7425
weighted avg       0.99      0.99      0.99      7425

```

## Runtime
The training takes up to 5 hours runinng on dual 2080Ti GPUs with 50 epochs on 20000 images.