Ocean Basalts
==============================

# Basalt's Chemistry Analylis to Determined Tectonic Setting using Machine Learning Algorithms
<center><img width="584" alt="Screenshot 2023-05-11 at 12 48 47 AM" src="https://github.com/CCNY-Earthchem-Projects/OceanBasaltML/assets/59939691/120b7c97-3245-4172-ad67-c2e9190e7b54"></center>

This is a porject being conducted by Jenifer Vivar, the Geology department of the city college of New York, the computer science department of the City College of New York, as part of the thesis project for my graduate studies.

The project uses data obtained from the EartChem website. The data is mantained by different colleges and is sponsored by the Natural Science Foundation. The data can be found here: https//www.earthchem.org/data-access/


The first part of the project consited of using Logistic Regression and Random Forest algorithms to explore what each model determined to be the most "important" features for classification. The techniques used to reduce bias on the feature selection were recursive feature elimination RFE and a permutation algorithm.


![perm_rfe_models](https://github.com/CCNY-Earthchem-Projects/OceanBasaltML/assets/59939691/28fa7ad8-5aca-452a-b038-0864b7e6957c)


The second part of the project focused on determining a way to detect mislabeled data. This was approached by determining outliers in the data. There are many algorithms that can be use for this purpose, and they all have their strength and weakneses. The idea here was to `diversify` an ensemble method by combining their approaches via majority voting. The ensemble works as follows: First all algorithms determined what they believe to be outliers, then voting is done and the features with the major votes are selected, then dummy_y values are created assigning one to suspected outliers and 0 to all other values, finally, the dummy y values are passed to a function that will determined if is probable that the sample is an outlier.

<img width="897" alt="Screenshot 2023-05-11 at 1 29 06 AM" src="https://github.com/CCNY-Earthchem-Projects/OceanBasaltML/assets/59939691/099aabe6-edb0-4205-b11a-18a62723b41d">
