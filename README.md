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
Here we're only using the train dataset since it has labels. We select 100 cat and 100 dog images for training and 25 each for testing (This will be significantly larger when the model implementation is complete) and put them into `processed_data` for `torchvision.datasets.ImageFolder` structure.
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