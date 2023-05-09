## Predicting Sales Probability Using Logistic Regression

*This is a simple demonstration of using Python and DS libraries inside Power BI to create a simple machine learning model and matplotlib visuals.*

### Task: Create a sales predictor for fictional company Smithy GmbH

#### Overview

The dataset consists of a records from completed projects with columns project name, amount, start and end date, its difference, and a binary indicator of sales success. 

<a href="https://nixonline.github.io/ds-portfolio/images/smithy_1.jpg" target="_blank">
  <img src="images/smithy_1.jpg?raw=true" class="img-zoom"/>
</a>

* Pearson correlation shows weak relationship between project value and sales status. This is because the dataset is filtered to show only projects with less than 25k value.
* The interquartile regions of the boxplot shows a clear distinction between winning and losing projects.
* Width of boxplot shows variance.
* Lose datapoints ouside the left whisker indicates outliers.

#### Model

Logistic regression is appropriate since the task is binary - to predict wether sales is or not closed based on the current project life. The logicstic regression formula can be interpreted as: what is the probability that a random project Y is closed, given the current X project life.

The dataset is divided for learning and validation with a ratio of 85/15.

<a href="https://nixonline.github.io/ds-portfolio/images/smithy_2.jpg" target="_blank">
  <img src="images/smithy_2.jpg?raw=true" class="img-zoom"/>
</a>

* The model performed with 85% accuracy during training while 66% for testing.
* Predicted and probability column is added to the dataset for comparison with the actual.
* The model will return binary value - 1 if probability is above .5. It is possible to retrieve the probability as shown as red line in the scatter plot.

#### Prediction

A new dataset of ongoing projects is loaded on this page. The inquiry column is subtracted to the current date at the time of screenshot, to get project life and evaluate in the predictor model. 

<a href="https://nixonline.github.io/ds-portfolio/images/smithy_3.jpg" target="_blank">
  <img src="images/smithy_3.jpg?raw=true" class="img-zoom"/>
</a>
