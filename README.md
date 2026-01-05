# NetGuard

## Description
NetGuard is a machine-learning based project designed to assist security analysts in identifying malicious network traffic. This project applies preprocessing learning techniques to network flow data, with a focus on the challenge of detecting rare attack types in imbalanced datasets. 

## Dataset
This project uses the CIC-IDS2017 dataset provided by the Canadian Institute for Cybersecurity. This dataset represents traffic seen throughout the week including benign and malicious activity. Due to the size of the dataset, it is not included and must be downloaded separately. 

## Notebook
The Jupyter Notebook included in this project is the full ML pipeline including preprocessing, model training and evaluation. For ease of use, all the user has to do is replace the name of the dataset on the second block with your set of choice and run all cells. 

Download the dataset here: https://www.unb.ca/cic/datasets/ids-2017.html

## How to Run
Download the dataset above and ensure all the files are in the same directory. Run all cells making sure to have the desired dataset loaded as there are multiple available. Required libraries at the top of the notebook may need installation. 

## Results
The model was extremely accurate in most cases. This project should not be used to do an analyst's job for them, rather to help an analyst notice trends that are common with different attack types. The evaluation in this project includes precision, recall, F1 score, and confusion matrices. Most notably, rare attack types such as XSS or SQL Injection have a low recall due to the dataset being so imbalanced towards benign traffic. To help solve this, I implemented oversampling, a technique that increases the number of rare cases. 

The Tuesday working hour dataset often confused XSS attacks and Brute Force attacks. These two could have been confused because they both can produce bursts of the same requests. Since the model only uses CSV files, it may miss sequential patterns inherent to some attacks. 

## Future Improvements
This project uses a Random Forest Classifier, which is susceptible to overfitting and not a great fit for imbalanced datasets. Although the oversampling with RandomOverSampler reduces the effect of some of these problems, I would like to switch to a gradient model such as LightGBM or XGBoost. These models have built-in class weighting which could prove useful for this project.
