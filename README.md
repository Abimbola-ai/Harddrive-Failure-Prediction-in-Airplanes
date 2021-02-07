# Harddrive-Failure-Prediction-in-Airplanes
This project predicts the failure of a hard-drives installed on an airplane. This was a school machine learning summative assessment.

The following steps were carried out:

* Data importation and cleaning: Some non-ascii characters were replaced with sigle space in the columns. The dataset consist of 50 attributes and 75130 observations. First set of data were dropped based on domain knowledge. Mean-filling and mode filling was also carried out on some of the attributes. Some 15959 observations were further dropped from 3 attributes End-to-End error / IOEDC, Reported Uncorrectable Errors and Command Timeout.

* Data visualizations: Some visualizations were plotted based on the how each of the attributes contribute to the failure/no failure. Not enough failed device is available as the dataset has only 0.02% of failed device.

* Feature Engineering: Dropped off all constant columns and grouped the dataset based on serial number of the harddrive. Selected the device's first day of operation and appended it to the device's last day of operation. This makes the data more balanced as the number of failed device is 49 % and not-failed devices to 50 %.

* Model Fitting: Data was scaled with the MinMaxScaler as the result got better than with using standard scaler. Train and test split was 80/20. The models used were logistic Regression, Decision Tree Classifier, Random Forest, Gradient Boosting and Support Vector Machine.

* Produce Recommendations: The chosen model (Random Forest) was ran on new data, with failure prediction set at 80% probability of failure.