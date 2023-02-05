Repo consists of 3 notebooks:

1 - CNN_TransferLearning_Muffin_Chihuahua.ipynb - I am using transfer learning from Inceptionv3 (https://keras.io/api/applications/inceptionv3/). The data has been downloaded from Kaggle, and standard means such as ImageDataGenerator with warious augmentation functions has been provided. The training is done on top of layer 'mixed7' , even I intended to run 100 epoches, using Callback the accuray 98.5% has been reached after one epoch. 

2 - LSTM_Covid_prediction.ipynb - Long Short-Term NN has been used to predict covid cases. I was not using moving average but only standard time series. The data has been cleaned (only Kosice area has been used) and scalled with MinMax scaler. Small LSTM NN has been build with short training. Mean Average Error is 272.1906 cases, so quite high and the training to be repetated with more Epoches. 

 3 - NLP_text_generator-Sladkovic_Marina_.ipynb - short GAN of NLP has been build to predict Sladkovic's poetry based on his poem Marina - intentionally chosen as this is the longest poem in Slovak language to have better dataset. Data has been cleanded, tokenized and padded. Using LSTM small DNN has been built.
