This folder contains solutions to our second Machine Learning assignment. 

###### Maliha Arif
###### UCF ID : 4506817


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

> 1) RMSprop
> 2) SGD
> 3) Adam
> 4) Adagrad

We also tweaked the learning rate ranging from
*1e-1 to 1e-6*

0.01, 0.001, 0.0001, 0.00001, 0.0000001



Through multiple experiments, we observed that Adam optimizer with a learning rate of 1e-3 was working best and which we used to train all the 4 models.

[Model 1](https://github.com/MalihaUCF/Machine-Learning-Course-Assignments-Spring-2019/blob/master/Assignment%202/Model1.ipynb)

[Model 2](https://github.com/MalihaUCF/Machine-Learning-Course-Assignments-Spring-2019/blob/master/Assignment%202/Model2.ipynb)

[Model 3](https://github.com/MalihaUCF/Machine-Learning-Course-Assignments-Spring-2019/blob/master/Assignment%202/Model3.ipynb)

[Model 4](https://github.com/MalihaUCF/Machine-Learning-Course-Assignments-Spring-2019/blob/master/Assignment%202/Model4.ipynb)



We performed the above experiments for 30 epochs and then picked model 1 which gave the higest accuracy till then. We then used that model and trained it for 200 epochs

The **link** to this notebook is [Best_Model](https://github.com/MalihaUCF/Machine-Learning-Course-Assignments-Spring-2019/blob/master/Assignment%202/More_120_epochs_CNN_5.ipynb)


For the above models, we were employing simple hold out validation. For K-fold validation, we chose this best model and then applied k -fold validation. 




### K-fold Validation

- We trained our models using our defined k-fold function as follows :


> k_fold_dataset():


- Create a starting index and ending index 
- The start index is multiplied with iteration number so that the start of the validation split is different each time
- the step size is 10000 as that is the number of images we want in the validation fold for each iteration
- We do not shuffle the list after the first iteration as the whole idea of k fold is prevent bias
- To create the training set, we append the remaining images in a list, the images before the validation block and after the validation block.


We perform k-fold with k=5 and split create the validation set as shown below and explained above in the function description.


<img width="833" alt="Screen Shot 2019-04-03 at 1 54 24 PM" src="https://user-images.githubusercontent.com/42460909/55501272-0f746180-5618-11e9-8caf-5f207be1f061.png">

  




### K-fold link

[k-fold-model](https://github.com/MalihaUCF/Machine-Learning-Course-Assignments-Spring-2019/blob/master/Assignment%202/Final_k_fold_Model1.ipynb)





## Conclusion

We observe that using k-fold does increase the average test accuracy but since our best model doesnt overfit, we get similar accuracy using hold validation too.













