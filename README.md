# Module_17
UC Berkeley AI and ML - Module 17 Assignment 17.1

The following files are important to this assignment:
1. prompt_III_Nesper.ipynb
2. bank-additional.csv
3. bank-additional-full.csv
4. Assign 17-1 Results.csv

Inside the Notebooks file prompt_III Nesper.ipynb , there is a sub-directory /content/ included in the file name for each datafile, for example for the bank-additional.csv file the name specified in the pd.read_csv statement is /content/bank-additional.csv. This may need to be modified if the file is relocated to a different directory. The best way to ensure that all cells are properly executed is to Run All cells. Some cells can be executed individually, but not all cells.

I created a number of Text Cells inside the Notebook and prefaced my added comments with "DN comments" to distinguish them from the instructions. In the comments that I added I have responded to questions posed in the instructions and to clarify my approach.

As I worked through this assignment I accumulated results in a file so I could compare multiple iterations. The file is plotted as a table_plot towards the bottom of the Notebook. The table was created at a point in time and does not get updated dynamically with each execution of the Notebook.

All test scores exceeded the DummyClassifier Baseline. Further I looked for cases that had high test scores where the Test Score exceeded the Train Score and found this trend: Logistic Regression consistently had Test Scores that increased over Train Scores and SVC intermittently had Test Scores that exceeded Train Scores, or were very close.

With respect to Average Fit Time, decisiontreeclassifier consistently had the smallest amount of time. The optimum max_depth 5 was consistently selected. The highest Average Fit Time was SVC. In one test using the 100% dataset the multiple comparison between lowest and highest Average Fit Time was ~378x.

I timed-out on 4 iterations when processing the SVC model when using the 100% dataset. When I ran with the 10% dataset I ran to conclusion and the C=1 hyperparameter (regularization) was chosen in best_params. I then re-ran SVC using the 100% dataset and ran to conclusion but I kept values for C less than or equal to 1.0. The learning was to be aware of the compute required to execute the models and also highlighted the potentially significant difference in compute across the models.

Based on my testing of the models I would recommend Logistic Regression as the best performer with respect to performance and compute efficiency. Additional testing should be done with SVC using variations of hyperparameters. The main consideration with SVC is the amount of compute required relative to the other models.
