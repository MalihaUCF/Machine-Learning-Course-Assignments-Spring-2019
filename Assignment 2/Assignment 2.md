This folder contains solution to the 2nd machine learnign assignment, UCF Spring 2019.


## Models used:



### Architecture 1 :

- We use 2 blocks of convolutional layers, each containing 2 convolutional layers each,hence a total of *4 convolutional layers* . 
- We use 32 filters in the first block followed by 64 filters in the second block.
- We use Relu activation
- The convolutional blocks are followed by dense layers , the first containing 512 neurons.
- The last fully connected layer is a softmax layer.
- We use dropout (probability 0.25 ) after the convolution blocks 
- We use dropout of 0.5 after 1st fully connected layer.






Architecture 2:
