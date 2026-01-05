# NetGuard

## Description
NetGuard is a machine-learning based project designed to assist security analysts in identifying malicious network traffic. This project applies preprocessing learning technuques to network flow data, with a focus on the challenge of detecting rare attack types in imbalanced datasets. 

## Dataset
This project uses the CIC-IDS2017 dataset provided by the Candian Institute for Cybersecurity. This dataset represents traffic seen throughout the week including benign and malicious activity. Due to the size of the dataset, it is not included and must be downloaded seperately. 
## Notebook

The Jupyter Notebook included in this project is the full ML pipeline including preprocessing, model training and evaluation. For ease of use, all the user has to do is replace the name of the dataset on the second block with your set of choice and run all cells. 

Download the dataset here: https://www.unb.ca/cic/datasets/ids-2017.html

## How to Run
Download the data set above and ensure all the files are in the same directory. Run all cells making sure to have the desired dataset loaded as there are multiple available. Required libraries at the top of the notebook may need installation. 

## Results
Struggled with tuesday working hour dataset, confusing XSS for brute force and vice versa, not as bad BF to XSS tho 
## Future Improvements
