# GTZAN Music Genre Tagger

A neural network-based music genre tagger on GTZAN dataset by Yuhao Zhang (yz3044), Peng Guo (pg2539), and Jesse Liu (ll3313).

## Prerequisites
  - [GTZAN Music Genre Dataset](http://marsyasweb.appspot.com/download/data_sets/).
  - [Theano](http://deeplearning.net/software/theano/index.html). Version 0.9.0 is used here but it should work with some similar versions.
  - [Keras 1.2.2](https://github.com/fchollet/keras/tree/1.2.2/keras) (*NOT THE MOST RECENT VERSION*)
    - set `image_dim_ordering : th` in `~/keras/keras.json`
    - set `backend : theano`, too.
  - [Kapre OLD VERSION for OLD KERAS](https://github.com/keunwoochoi/kapre/tree/a3bde3e38f62fc5458231198ea2528b752fbb373), an audio preprocessor library for Keras.
  
In short,
  
```
$ pip install theano==0.9
$ pip install keras==1.2.2
$ git clone https://github.com/keunwoochoi/kapre.git
$ cd kapre
$ git checkout a3bde3e
$ python setup.py install
```

## Usage

### Mode 1/2: Train the Entire Model

1. Run `Convert GTZAN to npy.ipynb` to convert audio files in GTZAN to numpy arrays. **Remember to change `PATH_DATASET` to path to the dataset on your own computer.**
2. Run `CNN5+Softmax.ipynb` to train and evaluate the model.


### Mode 2/2: Use pre-extracted feature and train fully-connected layers.

1. Run `Train Two-layer Classifiers with Pre-extracted Features.ipynb`. This iPython notebook contains different structures for fully-connected layer part as well as scripts to test their performances.


## Structure
![diagram](https://github.com/gooliath12/GTZAN_music_genre_tagger/blob/master/model.png "diagram")
