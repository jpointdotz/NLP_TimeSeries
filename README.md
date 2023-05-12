Repo consists of 7 notebooks:

1 - CNN_TransferLearning_Muffin_Chihuahua.ipynb - I am using transfer learning from Inceptionv3 (https://keras.io/api/applications/inceptionv3/). The data has been downloaded from Kaggle, and standard means such as ImageDataGenerator with warious augmentation functions have been provided. The training has not been done on top of the last layer, but by unfreezing of more layers on top of layer 'mixed7' , even I intended to run 100 epoches, using Callback the accuray 98.5% has been reached after one epoch. 

2 - LSTM_Covid_prediction.ipynb - Long Short-Term NN has been used to predict covid cases. I was not using moving average what is standard in such case, but only common time series. The data has been cleaned (only Kosice area has been used) and scalled with MinMax scaler. Small LSTM NN has been build with short training. Mean Average Error is 272.1906 cases, so quite high thus the training to be repetated with more Epoches. 

 3 - NLP_text_generator-Sladkovic_Marina_.ipynb - short GAN of NLP has been build to predict Sladkovic's poetry based on his poem Marina - intentionally chosen as this is the longest poem in Slovak language to have better dataset. Data has been cleaned, tokenized and padded. Using LSTM small NN has been built.

4 - EDA_CNN_Tumor_detection.ipynb - Tumor detection on data from Kaggle. First basic analysis of the dataset with some wranglings and adjustements. Then by means of OOP created a class to use only instances for various classifiers for transfer learning on top layer for ResNet40, Inception V3 and Mobilenet V1. The training performed on Google colab GPU and the best results obtained for Inception V3 on valid data with accuracy 96%. However, once using test data (never seen images from google) the model failed - model obviously overfitted. Some ideas from Kaggle collected about learning rate scheduling, focal loss instead loss function and balancing the dataset - to be used on next notebook. The next step is to use U-NET semantic detection for the same dataset.

5 - DNN_GridSeachCV_for_DNN_hyperparamaters.ipynb - I am using the standard dataset from Kaggle "California housing prices" for regression I have already used for other notebook. The data has been normalized as the distribution was quite skewed and some small adjustemnts done along. In this notebook I am using GridSearchCV for DNN Tensorflow model wrapped by KerasRegressor from SciKeras lib (there were similar wrapper from ScikitLearn which is not supported anymore). I decided to tune n. of hidden layers, n. of neurons in respective layer and learning rate of Adam optimizer. To shorten time, there were only 50 Epochs done and as results we got the best parameters of learning rate 0.001, 1 hidden layer wwith 128 neurons. 

6 - DNN_KerasTuner-Hyperband_for_DNN_hyperparameters.ipynb - The notebook as comparison to "DNN_GridSeachCV_for_DNN_hyperparamaters.ipynb" with using of Hyperband from KerasTuner to tune the very same parameters with the same def build_model() function to compare results on regression problem. In fact the same results as "the best" have been obtained - 0.001 learning rate of Adam, with 1 hidden layer and 128 neurons - results comparable to GridSearchCV, however based on several resources the KerasTuner is more robust and preferable to use instead of GridSearchCV due to better utilizing of resources for computation. 

7 - CNN_EDA_Animals_ClassWeights-TransferLearning.ipynb - The notebook with transfer learning on Animals dataset (>1GB), not having enough capacity to train ... training on Google Colab failed. The main point of the notebook was to compute weight of particular classes based on distribution within the dataset and include the Weight classes within model.fit() function. 

8 - Chatting_with_GPT - "Chatting" with GPT in notebook - prompt coding to analyse, translate, conlude ... part of Moby Dick book with generating of Pandas/Seaborn code by GPT. 

9 - OpenCV_Blur-Pixelation-Replacement-DNN-Caffee_model - using DNN Caffee pre-trained model to face detection and anonymize face with blur, pixelation and replacement options. 
