Download Link: https://assignmentchef.com/product/solved-cs1675-homework4-k-nearest-neighbors
<br>
In this assignment, you will implement and experiment with KNN classification.

<u>Part I: K-nearest-neighbors</u>

Implement KNN. For each test instance, compute its distance to all training instances, pick the closest K training instances, pick the most common among their labels, and return it as the label for that test instance. Use the Matlab function <span style="font-family: courier new;">pdist2</span>.

<b>Inputs:</b>

<ul>

 <li>an NxD feature matrix <span style="font-family: courier new;">X_train</span> where N is the number of training instances and D is the feature dimension,</li>

 <li>an Nx1 label vector <span style="font-family: courier new;">y_train</span> for the training instances,</li>

 <li>an MxD feature matrix <span style="font-family: courier new;">X_test</span> where M is the number of test instances, and</li>

 <li>a scalar <span style="font-family: courier new;">K</span>.</li>

</ul>

<b>Outputs:</b>

<ul>

 <li>an Mx1 predicted label vector <span style="font-family: courier new;">y_test</span> for the test instances.</li>

</ul>

<u>Part II: Weighted KNN</u>

Implement a Gaussian-weighed KNN classifier using the equation given in class, in a function <span style="font-family: courier new;">weighted_knn.m</span>. This version uses all neighbors to make a prediction on the test set, but weighs them according to their distance to the test sample.

<b>Inputs:</b> The first three are as for <span style="font-family: courier new;">my_knn.m</span>. The fourth one is:

<ul>

 <li>a scalar <span style="font-family: courier new;">sigma</span> denoting the bandwidth of the Gaussian.</li>

</ul>

<b>Outputs:</b> same as above

<u>Part II: Testing KNN on the Pima Indians dataset</u>

You will use the <a href="https://people.cs.pitt.edu/~kovashka/cs1675_fa18/pima.data">Pima Indians Diabetes</a> dataset (originally from the UCI repository, but link is now disabled) to test your KNN implementation and experiment with different values of K. Write your code in a script <span style="font-family: courier new;">knn_classification.m</span>.

<ol>

 <li>[5 pts] Download the data file. The last value in each row contains the target label for that row, and the remaining values are the features. Split the data into 10 approximately equally-sized “folds”. Your results reported below should be an average of the results when you train on the first 9 folds and test on the remaining 1, then if you train on the folds numbered 1 through 8 and the 10th fold and testing on the 9th fold, etc. For simplicity, you can use folds of size 76 and drop the remaining 8 instances.</li>

 <li>[2 pts] Make sure to normalize the data X by subtracting the mean and dividing by the standard deviation over each dimension, computed using the training data only, as in HW3.</li>

 <li>[5 pts] Apply your KNN function and compute the accuracy over all folds, then average the results. To compute accuracy, check the ratio of test samples whose predicted labels are the same as the ground-truth labels, out of all test samples.</li>

 <li>[5 pts] Experiment with the following values: <span style="font-family: courier new;">K = 1:2:15</span>. Plot the results (with values of K on the x-axis and accuracy on the y-axis) and include the plot in a file <span style="font-family: courier new;">report.pdf/docx</span>.</li>

 <li>[3 pts] So far, we have been weighing neighbors equally. Now we want to experiment with weighing them according to their distance to the test sample of interest. Experiment with 3 different values of the bandwidth parameter <i>σ</i>, create a plot with <i>σ</i> on the x-axis and accuracy on the y-axis, and include the plot in the report file.</li>

</ol>

<b>Submission:</b> Please include the following files:

<ul>

 <li><span style="font-family: courier new;">my_knn.m</span></li>

 <li><span style="font-family: courier new;">weighted_knn.m</span></li>

 <li><span style="font-family: courier new;">knn_classification.m</span></li>

 <li><span style="font-family: courier new;">report.pdf/docx</span></li>

</ul>