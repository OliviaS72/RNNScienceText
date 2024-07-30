# RNNScienceText
A **recurrent neural network** to classify text as relating to "Biology", "Chemistry", or "Physics".
This project uses a Kaggle dataset that can be found at this link: <br> 
[Physics, Chemistry, or Biology Kaggle Link](https://www.kaggle.com/datasets/vivmankar/physics-vs-chemistry-vs-biology/data) <br> 
The uploader/Kaggle user who provided this dataset is **VIVEK**. <br> 
**There are a total of 10,281 comments in this dataset, with each one relating to either the field of physics, chemistry or biology. The goal of classification is to accurately predict the field that the comments pertain to. The training data consists of 8,695 comments, and the testing data consists of 1,586 comments. Extra symbols, punctuation, and spaces will be removed as part of the cleaning process. Also, stop words will be removed and stemming will occur to simplify words down to their roots.**
**Here is a glimpse of some of the training data comments:** <br> 

<img src = /assets/img/TrainingDataScienceComments.png>

**After the embedding layer that uses GloVe embedding to create an embedding matrix of words where each word has a vector of 100 values assigned to it, a bidirectional LSTM layer with 64 nodes is added. One layer within this LSTM layer processes text in the forward direction, and the other processes text in the backward direction. Following the bidrectional layer are dropout layers with dropout rate of 0.2 and dense layers with 50 nodes and 'relu' activation.**

**The model is compiled with categorical crossentropy loss function and the 'Nadam' optimizer. I used a callback to monitor validation loss to prevent overfitting. If the validation loss increased over more than 2 consecutive epochs, the learning rate would be reduced.**

**Final model accuracy was 0.81. Plots of the accuracy, loss, precision, and recall do not show concerning patterns of overfitting. The training accuracy steadily increases, and validation accuracy does not experience any signfificant decrease. Precision and recall are both fairly high at about 0.82 for precision and 0.80 for recall, with a fair F1 score of 0.81 balancing the two measures.**

URL: https://www.kaggle.com/datasets/vivmankar/physics-vs-chemistry-vs-biology/data

