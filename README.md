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
  <li>Were you able to achieve the target model performance?</li>
  <ul><li></li></ul>
  <li>What steps did you take in your attempts to increase model performance?</li>
  <ul><li></li></ul>
</ul>
