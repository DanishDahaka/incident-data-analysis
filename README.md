# Analyzing incidents in the offshore wind industry

Short Summary: A comparison of supervised Machine Learning classifiers' performance on unstructured text and structured nurmerical data.

## Short Table of Contents
1. Why
2. How
3. What
    1. Classification problem
    2. Data splits
    3. Results

## Why
Installing, operating, and maintaining Offshore Wind Farms is a field particularly prone to occupational incidents due to the hazardous work environment. Offshore Wind Farm operators thus strive to mitigate future risks by minimizing the number of incidents.

## How
Thanks to the [Cross-industry standard process for data mining (CRISP-DM)](https://en.wikipedia.org/wiki/Cross-industry_standard_process_for_data_mining):
![](https://github.com/DanishDahaka/incident-analysis-ml/blob/main/images/crisp_dm.png)

## What
Training and testing of various Machine Learning algorithms on incident data (numerical, text) to classify the physical location where an incident occured.

### Classification problem
The available data sets were first explored from a business perspective. 
The business perspective first yielded that we may focus on incident severity. 
However, our Machine Learning classifiers did show accuracies close to random choice.

Hence, we re-iterated three times in total and finally settled on classifying the location, where an incident could have happened.

For multiple locations we created a supervised multi-class classification problem with four targets:
![](https://github.com/DanishDahaka/incident-analysis-ml/blob/main/images/methodology_area_cm.png)

### Data splits

Four different Machine Learning estimators were trained on the data and three different train/test split variations were compared:
![](https://github.com/DanishDahaka/incident-analysis-ml/blob/main/images/methodology_train_test_80.png)

![](https://github.com/DanishDahaka/incident-analysis-ml/blob/main/images/methodology_train_test_70_90.png)

### Results

An overview of the results for all different model and dataset variations is shown here:
![](https://github.com/DanishDahaka/incident-analysis-ml/blob/main/images/results_summary_graph.png)

As a key takeaway, an accuracy boost of up to **10 %** was gained through feeding the additional text data into the Machine Learning models.
Different train/test-splits did only slightly change the Machine Learning model accuracy.

Some files (e.g. accessing, joining and exploring the dataset / Latent Dirichlet Allocation / Word metrics / Keras comparison accuracies) are not part of this repository.
If interested, feel free to ask about more info from these parts.
