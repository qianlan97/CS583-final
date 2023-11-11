# CS583-final
我是把kaggle上面的dogs-vs-cats下载下来以后，只用了里面的train文件夹。我把train文件夹重新命名为dogs-vs-cats，再在这个文件夹里面创立train和test两个文件夹，再在train和test里面再分别创立dogs和cats两个文件夹。所以文件夹的顺序是dogs-vs-cats --> train, test. train --> dogs, cats. test --> dogs, cats. 然后我选取10000-12499编号的2500张dog/cat图片放入test里面的dogs/cats，选取0-9999编号的10000张dog/cat图片放入train里面的dogs/cats，这样就完成data的分类了。
在data_processing.ipynb里面，file的路径是../Downloads/..., 你把downloads改成dogs-vs-cats和data_processing共存的那个文件夹目录就可以run了。
