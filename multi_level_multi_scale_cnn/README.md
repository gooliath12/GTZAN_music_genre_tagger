# Part 2 -- Multi-level Multi-scale CNN

This is the second part of our project, in which we trained a set of 4 CNN models as "local feature extractors" on GTZAN dataset, and we trained a neural network-based classifier for predicting the genre of music based on extracted features.

## Prerequisites
  - [GTZAN Music Genre Dataset](http://marsyasweb.appspot.com/download/data_sets/).
  - [Theano](http://deeplearning.net/software/theano/index.html).
  - [Keras 1.2.2](https://github.com/fchollet/keras/tree/1.2.2/keras) (*NOT THE MOST RECENT VERSION*)
    - set `image_dim_ordering : th` in `~/keras/keras.json`
    - set `backend : theano`, too.
  
In short,
  
```
$ pip install theano
$ pip install keras==1.2.2
```

## Usage


1. Run `Data Preprocessing.ipynb` to convert audio files in GTZAN to spectrograms and split them into training and testing data. **Remember to change `PATH_DATASET` to path to the dataset on your own computer.**
2. Run `Train Local Feature Extractors.ipynb` to train 4 CNN models.
3. Run `Feature Extraction & FC Training.ipynb` to extract features using pre-trained 4 CNN models and train classifier for genre tagging.

**Detailed guidance and instructions are provided in each jupyter notebook for using our code and reproducing our results.**


