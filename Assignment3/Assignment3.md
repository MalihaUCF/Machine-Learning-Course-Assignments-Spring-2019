## Assignment 3

This readme contains descriptions and solution (links) to our 3rd Machine learning assignment.

###### Maliha Arif
###### PID:4506817

---


**Pre-trained convnet Used: VGG-19**

**Dataset Used: Cats and dogs**



The goal of this homework was to learn to leverage pretrained convnets and to use some visualization techniques. We 
experiment with different classifiers placing on top of VGG-19 network ,and tried to maximize the validation accuracy.The solution here shows one of such classifiers as instructed in the assignment.


### Problem 1

Do feature extraction with data augmentation.

We experimented with 5 classifiers which we placed on top of the base VGG-19 network. We made sure the conv_base was frozen and only the classifier was trainable.

Following were the classifiers, involving 1 or 2 dense layers , with and without dropout.

#### Classifier 1

- 1 dense layer with 256 filters
- dropout (0.3)
- dense layer with sigmoid activation and 1 neuron


#### Classifier 2

- 2 dense layer with 4096 filters
- dropout (0.5) after each layer
- dense layer with sigmoid activation and 1 neuron
- dropout again (0.5)


#### Classifier 3

- 2 dense layer with 512 filters
- dropout (0.3) after each layer
- dense layer with sigmoid activation and 1 neuron


#### Classifier 4

- 1 dense layer with 256 filters
- no dropout
- dense layer with sigmoid activation and 1 neuron


We used model 3 with batch_size=30 and RMSprop optimizer with 2e-5 learing rate which gave us **89.4 % ~ 90 %** validation accuracy after 100 epochs.


[Problem 1 solution](https://github.com/MalihaUCF/Machine-Learning-Course-Assignments-Spring-2019/blob/master/Assignment3/Problem1_HW3_v2.ipynb)



### Problem 2

Do fine-tuning with data augmentation. 


In this part of the assignment , we were allowed to train the last conv layers of VGG-19 model, hence we fine tuned the model we used in problem 1.

We observed a significant increase in our validation score. We were able to get **95% validation** accuracy and no overfitting.


[Problem 2 solution](https://github.com/MalihaUCF/Machine-Learning-Course-Assignments-Spring-2019/blob/master/Assignment3/Problem2_HW3_functionalAPI.ipynb)


### Problem 3


Visualize heatmaps of class activation for the the model obtained in Problem 2.


[Heat_map](https://github.com/MalihaUCF/Machine-Learning-Course-Assignments-Spring-2019/blob/master/Assignment3/Problem3_Visualize_Class_Activations.ipynb)



### Problem 4

Build an activation model that takes as input an image and produces as output the activation of the last conv layer of the model obtained in Problem 2. Using this activation model obtain the corresponding activations for the validation images. Apply t-SNE visualization to these activations to see how well the convnet separates cats from dogs.



[Activations_and_ t-SNE visualization](https://github.com/MalihaUCF/Machine-Learning-Course-Assignments-Spring-2019/blob/master/Assignment3/Problem4.ipynb)




