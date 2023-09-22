# Job_Skills_Dataset


## Files
Original Dataset (job_skills.csv) : https://www.kaggle.com/datasets/niyamatalmass/google-job-skills  
Preprocessed Dataset (preprocessed_dataset/job_skills_processed_data.csv)  
Training Split (preprocessed_dataset/train.csv)  
Testing Split (preprocessed_dataset/test.csv)  

## Data Statistics
The statistics of preprocessed dataset are as follows.

Parameter | job_skills_processed_data.csv | train.csv | test.csv
--- | --- | --- | ---
No of Documents | 1091 | 930 | 161
Avg. Document Length (tokens)	| 93.93 | 94.06 | 93.18
Max Document Length (tokens) | 240 | 202 | 240
Min Document Length (tokens)	| 31 | 31 | 31
Avg. Expertise Length (tokens)	| 12.53 | 12.47 | 12.91
Max Expertise Length (tokens)	| 58 | 58 | 44
Min Expertise Length (tokens)	| 1 | 1 | 2
Avg. No of Expertise per Document	| 2.53 | 2.55 | 2.40
% of Absent Expertise per Document	| 100% | 100% | 100%




## Experimental Configuration

### Machine Configuration

AMD EPYC CPU (48 cores)  
Nvidia A100 80GB GPU  
1TB RAM  

### Hyperparameters for training bart-large
Hyperparameter | Value
--- | ---
Learning Rate | 2e-5
Batch Size | 64
Epochs | 15


## Results
(P=Precision, R=Recall, F1=F1 Score)
Model | Semantic Similarity (P, R, F1) | Equality (P, R, F1)
--- | --- | ---
TF-IDF | 0.460, 0.534, 0.495 | 0.000, 0.000, 0.000
PR | 0.532, 0.573, 0.552 | 0.000, 0.000, 0.000
BART | 0.829, 0.835, 0.832 | 0.025, 0.037, 0.030
