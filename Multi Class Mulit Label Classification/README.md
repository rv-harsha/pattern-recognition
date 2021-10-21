The dataset is obtained from - https://archive.ics.uci.edu/ml/datasets/Anuran+Calls+%28MFCCs%29. It is Anuran Calls (MFCCs) Data Set with each instance consisting of three labels: Families, Genus, and Species. Each of the labels has multiple classes.

Now, the first step was to train a classifier for each label. For this, a SVM was trained using Gaussian Kernel and one vs all classifier. The weight of the SVM penalty and the width of the Gaussian Kernel was determined using 10 fold cross-validation. Next, trained a L1-penalized SVM and also remedied class imbalance using SMOTE.

The results for One Vs All Classifier has an Exact Match ratio of 0.96 for label Family, 0.962 for label Genus and 0.97 for Species. The Hamming loss for the above are 0.03, 0.037 and 0.028 respectively. From the comparitive analysis performed, we see that the One vs All Classifier performed the best based on the Exact Match Ratio and Hamming Loss values for the Anuran Calls dataset.

Also executed K-means clustering along with Monte-Carlo simulation (50 times) on the dataset and obtained a Mean of 0.22 and Standard Deviation of 0.003 for Hamming Distances.
