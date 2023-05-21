# Deep_Learning_Assignment_3
## Recurrent Neural network to build a transliteration system using Aksharantar Dataset
### ABout the Aksharantar Dataset:
  It contains the langugaes spoken in India. Every language file contains pair of words in latin and Devnagari. Further every language data file is also splited into train,test and validation data files.

Then this repository contains:
Files related to the questions asked in assignment 3 of deep learning.

Overview :
The purpose of this Assigment are :

1.Building a transliteration system using Recurrent Neural Networks.

2.Comparing different cells such as vanilla RNN, LSTM and GRU.


In the seq2seqwithoutAttention.ipynb file , a model is been created which accepts different cells/architecture depending on the user.

Code begins with some Data prepocessing then converting the words into one hot coded vector to feed as an input to the model.

Hyperparameter sweeping is been done to find the best set of hyperparamters which gives max_accuracy

Use the following function to perform hyperparameter sweeps in wandb:

The various hyperparameters used are :

hyperparameters = {
          "cell":   {"values":  ["RNN","GRU","LSTM"]},
          "embed_size": {"values":   [16,32,64,256]},
          "hidden_layer_size":  {"values":  [16,32,64,256]},
          "num_layers": {"values":   [1,2,3]},
          "dropout":    {"values":  [0.2,0.3,0.4]},
          "epochs": {"values":   [5,10,15,20]},
          "batch_size": {"values":  [32,64]},
          "optimizer":  {"values":    ["adam", "rmsprop", "nadam"]}
      }

