This folder contains solution to the 2nd machine learnign assignment, UCF Spring 2019.


## Models used:



### Architecture 1 :   - model1()


- We use 2 blocks of convolutional layers, each containing 2 convolutional layers each,hence a total of **4 convolutional layers** . 
- We use 32 filters in the first block followed by 64 filters in the second block.
- We use Relu activation
- The convolutional blocks are followed by dense layers , the first containing 512 neurons.
- The last fully connected layer is a softmax layer.
- We use dropout (probability 0.25 ) after the convolution blocks 
- We use dropout of 0.5 after 1st fully connected layer.



### Architecture 2 :   - model2() increased number of layers


- We use 3 blocks of convolutional layers, each containing 2 convolutional layers each,hence a total of **6 convolutional layers** . 
- We use 64 filters in the first block followed by 128 filters in the second block.
- We use 128 filters in the 3rd block.
- We use Relu activation
- The convolutional blocks are followed by dense layers , the first containing 512 neurons.
- The last fully connected layer is a softmax layer.
- We use dropout (probability 0.25 ) after the convolution blocks 
- We use dropout of 0.5 after 1st fully connected layer.



### Architecture 2 :   - model3() without dropout


- We use 2 blocks of convolutional layers, each containing 2 convolutional layers each,hence a total of **4 convolutional layers** . 
- We use 32 filters in the first block followed by 64 filters in the second block.
- We use Relu activation
- The convolutional blocks are followed by dense layers , the first containing 512 neurons.
- The last fully connected layer is a softmax layer.
- No dropout after the convolution blocks 
- No dropout after 1st fully connected layer



### Architecture 4 :   - model4() increased number of filters with dropout


- We use 2 blocks of convolutional layers, each containing 2 convolutional layers each,hence a total of **4 convolutional layers** . 
- We use 64 filters in the first block followed by 128 filters in the second block.
- We use Relu activation
- The convolutional blocks are followed by dense layers , the first containing 512 neurons.
- The last fully connected layer is a softmax layer.
- We use dropout (probability 0.25 ) after the convolution blocks 
- We use dropout of 0.5 after 1st fully connected layer.




We also experimented with different **optimizers** mainly 

1) RMSprop
2) SGD
3) Adam
4) Adagrad

We also tweaked the learning rate ranging from
*1e-1 to 1e-6*

0.01, 0.001, 0.0001, 0.00001, 0.0000001

















