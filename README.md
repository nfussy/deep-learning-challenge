# deep-learning-challenge
The report on the Neural Network can be found in this README.md file. The initial training code for the Neural Network model can be found in the 'Starter_Code.ipynb' file with a printout of the network available in the h5 file, 'AlphabetSoupCharity.h5'.

The additional attempts at optimizing the Nerual Network to achieve an accuracy score of 75% can be found in the 'AlphabetSoupCharity_Optimization.ipynb' file with a printout of the network in the h5 file, 'AlphabetSoupCharity_Optimization.h5'.

# Overview
<ul>
  <li>Purpose of this analysis:</li>
  <ul>
    <li>In this assignment, I was attempting to create a predictive model that would help the company select applicants for funding.</li>
    <li>We were given a dataset of over 34,000 organizations that had receieved funding prior and the outcomes of said organization.</li>
    <li>Some of the provided Metadata:</li>
      <ul>
        <li>EIN and Name</li>
        <li>APPLICATION_TYPE</li>
        <li>AFFILIATION</li>
        <li>CLASSIFICATION</li>
        <li>USE_CASE</li>
        <li>ORGANIZATION</li>
        <li>STATUS</li>
        <li>INCOME_AMT</li>
        <li>SPECIAL_CONSIDERATIONS</li>
        <li>ASK_AMT</li>
        <li>IS_SUCCESSFUL</li>
      </ul>
  </ul>
</ul>

# Results
Data Preprocessing
<ul>
  <li>What variable(s) are the target(s) for your model?</li>
  <ul><li>The variable that was used as a target in my model was 'IS_SUCCESSFUL'.</li></ul>
  <li>What variable(s) are the features for your model?</li>
  <ul><li>I used all of the other variables besides EIN and Name when it came to the features used in my models.</li></ul>
  <li>What variable(s) should be removed from the input data because they are neither targets nor features?</li>
  <ul><li>Per the inital code, we wanted to remove both the EIN and Name from the dataset, as they were not features.</li></ul>
</ul>

Compiling, Training, and Evaluating the Model
<ul>
  <li>How many neurons, layers, and activation functions did you select for your neural network model, and why?</li>
    <ul>
      <li>Neurons:</li>
        <ul><li>80, 30, 1</li></ul>
      <li>Layers:</li>
        <ul><li>2 Dense Hidden Layers, 1 Dense Output Layer.</li></ul>
      <li>Activation Functions:</li>
        <ul><li>relu, sigmoid</li></ul>
    </ul>
  In the original neural network, there were three layers added: the first layer, a hidden layer, with 80 Neurons and an activation function of 'relu'; the second layer, another hidden layer, with 30 neurons and an activation function of 'relu'; and a third layer, the output layer, with 1 neuron and a sigmoid activation function.
  <li>Were you able to achieve the target model performance?</li>
  <ul><li>No. The best I was able to achieve was 72.99%.</li></ul>
  <li>What steps did you take in your attempts to increase model performance? (note, in all of these tests, the cutoff amounts for both of the original bins were set to 500)</li>
  <ul>
    <li>Attempt #1: Editing the number of nodes per hidden layer</li>
      <ul>
        <li>I edited the nodes to follow multiples of 7 when it came to the two hidden layers. This came out to 72.77% Accuracy.</li>
        ![image](https://github.com/user-attachments/assets/0f51f7d9-ae47-4a7c-b2f5-233e198c1cb5)
      </ul>
    <li>Attempt #2: Adding in an additional hidden layer</li>
      <ul>
        <li>In this version of the model, I added in an additional Sigmoid layer with 30 Neurons. This came out to 72.99% Accuracy.</li>
        ![image](https://github.com/user-attachments/assets/749790fa-6351-4056-9b96-391f836d3941)
      </ul>
    <li>Attempt #3: Using Keras-Tuner to determine the optimal hyperparameters</li>
      <ul>
        <li>In this version of the model, I used keras-tuner to find the most optimal hyperparameter values for the original model. This was run over 20 epochs. This came out to 72.69% Accuracy.</li>
        ![image](https://github.com/user-attachments/assets/bd448e30-db52-4803-9569-f89d6d06a943)
        ![image](https://github.com/user-attachments/assets/b1eb1a81-df94-43c8-b679-0736a2c84138)
      </ul>
    <li>Attempt #4: Evaluating the best keras-tuner model with 100 epochs</li>
      <ul>
        <li>This is the same model mentioned before run with 100 epochs. This came to 72.48% Accuracy.</li>
        ![image](https://github.com/user-attachments/assets/c8da4669-8d74-4a60-987a-35b44feae38e)
      </ul>
  </ul>
</ul>

# Summary
Unfortunately, I invested quite some time in coming up with additional ways the neural network could squeak out more performance, yet they seemed to perform worse than the more minor edits. This could partially be due to only opting for two hidden layers, or excluding the names column -- I managed to find others' attempts at this same problem and when they included company names in their features, it allowed for them to surpass the 75% Accuracy goal and even approach 80%. If I were to do this again, I would likely include the Names column and bin it in a similar way to the CLASSIFICATIONS or APPLICATION_TYPE columns. In addition to that, I would attempt to beef up the code for the keras tuner and have it look at adding in additional hidden layers, etc.
