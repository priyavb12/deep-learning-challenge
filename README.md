# deep-learning-challenge
challenge 21

#Overview of the analysis: Explain the purpose of this analysis.

#Results: Using bulleted lists and images to support your answers, address the following questions:

#Data Preprocessing

1. What variable(s) are the target(s) for your model?

Answer: The target is the Is-Successful column

2. What variable(s) are the features for your model?

Answer: Features list of this model are the following: name, application type affliation classification use_case organization income special consideration status and ask amount

3. What variable(s) should be removed from the input data because they are neither targets nor features?

Answer: EIN (Employee identification)

#Compiling, Training, and Evaluating the Model

1. How many neurons, layers, and activation functions did you select for your neural network model, and why?

Answer: For this model 3 hidden layers each with many neurons because the compute seems to increase the accuracy above 75% this expensive and costly. The first activation is relu and the other layer are sigmoid it might boost accuracy using the functions.

2. Were you able to achieve the target model performance?

Yes

3. What steps did you take in your attempts to increase model performance?

Required to convert the NAME into datapoints which has the biggest impact on improving efficiency but costly and it requires adding third layer using sigmoid activation function

#Summary: Summarize the overall results of the deep learning model.

overall the accuracy above 75% we are able to correctly classify each in the test 75% of the time.
And an applicant has a 80% chance of being successful if the follow this:

Name of applicants appears more than 5 tmes
type of applications following T3 T4 T5 T6 T7 T8 T10 T19 application of following classification 

#Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation

RandomForest model

Compiling, Training, and Evaluating the Model

The final model had three layers. The first layer had 100 neurons or nodes, the second layer had 30 neurons, and the third layer had 10 neurons. The model used two different activation functions - rectified linear units (relu) and sigmoid. See the image below for details of the model construction.

model definition and summary

The model exceeded the target performance of 75%. The model reached 79% accuracy - see the image below.
model evaluation

I took the following steps to increase the model's performance:

Including the NAME column. There were a significant number of organization names that were repeated in the data. I thought there could be a connection betwen the organization and its success.
Two columns, SPECIAL_CONSIDERATIONS and STATUS were removed because they were both almost all one value.

I added a third layer to increase the model's complexity.

I changed the activation functions on the second and third layers as well as the output layer.

Summary

The tuned neural network was able to predict outcomes with 79% accuracy. This is a marked increase when compared to the original neural network which predicted outcomes with 73% accuracy. This was achieved by adding the organization NAME to the feature variables, removing SPECIAL_CONSIDERATIONS and STATUS from the feature variables, increasing the model's complexity by adding a third hidden layer, and changing some of the layers' activation functions.

As an alternative to the nn model, a random forest classifier could be used. I attempted this and was able to get 78% accuracy. This is a much better score than the 75% threshold I was shooting for. However, the neural network won out with 79% accuracy. With further tuning, it may be possible to improve on one or both of these models and get an even better predictive classifier.
