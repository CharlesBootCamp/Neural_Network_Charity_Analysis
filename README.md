# Neural_Network_Charity_Analysis

## Overview of the Analysis 
The charitable organization Alphabet Soup wants us to look at a list of over 34k businesses to examine the funding that these organizations received from Alphabet Soup over the years. Most likely this is used to determine how well the money is spent by these businesses and to examine whether or not money should still be given to these organizations.

## Results 

### Data Preprocessing 

- Variable that was considered as the target for my model: The IS_SUCCESSFUL column
- Variables that were considered features for my model: Every column except for the IS_SUCCESSFUL
- Variable that were neither targets or features for the dataset: I dropped the EIN and the NAME columns, since they're only there for extra identification purposes, I also removed the USE_CASE, since the use isn't as important as the amount of funding being transferred.

### Compiling, Training and Evaluating the Model

The number of neurons, layers, and activation functions I selected for my neural network model:
- For this case, I decided to have 2 hidden layers. The first ones having 80 neurons and the second having 30, while there is also an output layer. The first and second hidden layer have the "relu" activation function and the activation function for the output layer is "sigmoid."


Was the model able to achieve the target model performance?
- The model was not able to reach the target 75%. Only having a meager 39%.

![image](https://github.com/CharlesBootCamp/Neural_Network_Charity_Analysis/blob/main/Resources/Deliverable%202.png)

The following attempts are used with increased criteria to try to make sure that it can reach at least 75%.

- Attempt 1: Removed additional feature, in this case, the 'USE_CASE' column. This case has a 70% accuracy, which is closer, but still not enough.

![image](https://github.com/CharlesBootCamp/Neural_Network_Charity_Analysis/blob/main/Resources/Deliverable%203.1.png)

-  Attempt 2: Added additional neurons to hidden layers and additional hidden layers are added. This case drops down to a 47% accuracy, moving further from the target.

![image](https://github.com/CharlesBootCamp/Neural_Network_Charity_Analysis/blob/main/Resources/Deliverable%203.2.png)

- Attempt 3: Changing activation function of output layer from "sigmoid" to "tanh." This case drops down to a 45% accuracy, moving even farther from the target.

![image](https://github.com/CharlesBootCamp/Neural_Network_Charity_Analysis/blob/main/Resources/Deliverable%203.3.png)

## Summary 

Ultimately, the 75% goal was unobtainable, but it got much closer when the USE_CASE column was removed, making it seem that potentially removing more columns, such as the ORGANIZATION and AFFILIATION columns. The Alphabet Soup organization will need to do a little more examination before anything potentially useful is able to be obtained.
