# Modulation Recognition Using Neural Networks

# Contributers
Mohamed Elsayed Abdelrehim
Mohamed Ibrahim El-Metwally

## The Dataset

link: http://opendata.deepsig.io/datasets/2016.10/RML2016.10b.tar.bz2

The size of the data set was nearly 3 GB. Due to memory limitations we only tested our model with the raw time series dataset, its integration, and its first derivative.  

## Fully Connected Architecture
In the fully connected architecture, we used two hidden layers and one output layer. The first hidden layer has 400 components, the second hidden layer has 512 components, and the output layer has 10 components. Each of the hidden layers is connected to a ReLu activation unit. We used a dropout layer after each hidden layer with .2 probability to reduce overfitting. There was no intuition behind our choice of the number of components or the number of hidden layers. It was just trial and error.

## Results

### The Raw Time Series Dataset
The Fully Connected architecture with the raw time series dataset gave us a 49% overall test accuracy. The data with snr value of 0 gave us 68.8% test accuracy and the highest test accuracy (71.3%) was from the data with snr value 4.  


### The Integration Dataset 
The Fully Connected architecture with the integration dataset gave us a 51.23% overall test accuracy. The data with snr value of zero gave us 69.1% test accuracy and the highest test accuracy (73.1%) was from the data with snr value 14.  

### The Differentiation Dataset 
The Fully Connected architecture with the differentiation dataset gave us low test accuracy results. The test accuracy was 42.88%. The data with snr value of 0 gave us 10.1% test accuracy, and the highest test accuracy (52.8%) came from the data with snr value 12.
 

## Convolutional Neural Network Architecture
In CNN architecture, we didn’t need to design our own architecture we just implemented the one given in the problem statement. The only parameter we could tuned was the learning rate. We found that a learning rate of 0.001 gave us the best results. We used a dropout layer after each linear layer present with .25 probability to reduce overfitting. 

## Results


### The Raw Time Series Dataset
The CNN architecture with the raw time series dataset gave us a 53.07% overall test accuracy. The data with snr value of 0 gave us 73.1% test accuracy and the highest test accuracy (76.4%) was from the data with snr value 14.
  
### The Integration Dataset 
The CNN architecture with the integration dataset gave us a 50.017% overall test accuracy. The data with snr value of zero gave us 66.5% test accuracy and the highest test accuracy (73%) was from the data with snr value 10.  
The Differentiation Dataset 
The CNN architecture with the differentiation dataset gave us the lowest test accuracy results. The test accuracy was 10.029%. The data with snr value of 0 gave us 10% test accuracy, and the highest test accuracy (10.2%) came from the data with snr values -14, -4, and 4.
 

