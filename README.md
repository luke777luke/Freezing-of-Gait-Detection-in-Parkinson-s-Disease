# Freezing-of-Gait-Detection-in-Parkinson-s-Disease
Detection and classification of "Freezing of Gait" events in the neurodegenerative disease

ReadMe 
 
Group Information: 
Group 1 
Sihe Zheng, szheng12@depaul.edu   
YunTzu Yu, yyu54@depaul.edu   
Saruul Enkhtur, senkhtur@depaul.edu   
Lukasz Grzybek, lgrzybek@depaul.edu   
Course: DSC 672 DATA SCIENCE CAPSTONE   
University: DePaul University, College of Computing and Digital Media   
 
Project Description:  
In this project, we explore the effectiveness of recurrent neural network (RNN) architectures, including LSTM, GRU, and SimpleRNN, for FOG event classification using accelerometer data from the tdcsfog and defog datasets. Through comprehensive evaluation and hyperparameter tuning, we identified the GRU model as the top performer, demonstrating superior accuracy, precision, and recall compared to LSTM and SimpleRNN. 
 
Environment Details： 
OS: Google Colab (Runtime type Python3) 
Memory (RAM): High-RAM 
Disk Space: Sufficient space for dataset storage 
CPU/GPU: 4T GPU 
Environment Configurations: Ensure that the required packages are installed using the provided `requirements.txt` file. 
 
Instructions: 
 
1.	Environment Setup:   
●	Install the necessary packages on Jupyter notebook/Google Colab using the `requirements.txt` file. 
●	Set up the environment on Google Colab with Runtime type Python3, Hardware accelerator of 4T GPU with High-RAM. 
 
2.	Data Files: 
●	Download the original dataset from the Parkinson's Freezing of Gait Prediction Competition on Kaggle: [Dataset Link](https://www.kaggle.com/competitions/tlvmc-parkinsons-freezing-gait-prediction/data) 
●	Dataset Downloaded to Google Drive: [Google Drive Link](https://drive.google.com/drive/folders/1ts7cHB2C_sHSlUspTIgiuHK4SgPt5N6t?usp=sharing) 
○	Downloaded File Names: 
■	‘train/’ Folder containing the data series in the training set within three subfolders: ‘tdcsfog/’, ‘defog/’, and ‘notype/’. 
■	‘Test/’ Folder: Only the `Time`, `AccV`, `AccML`, and `AccAP` fields are provided for the test series. 
■	‘unlabeled/’ Folder containing the unannotated data series from the daily dataset. 
■	‘tdcsfog_metadata.csv’: Identifies each series in the `tdcsfog` dataset by a unique Subject, Visit, Test, Medication condition. 
■	‘defog_metadata.csv’: Identifies each series in the `defog` dataset by a unique Subject, Visit, Medication condition. 
■	‘daily_metadata.csv’: Each series in the daily dataset is identified by the Subject id. This file also contains the time of day the recording began. 
■	‘subjects.csv’: Metadata for each Subject in the study, including their Age and Sex as well as: 
■	‘events.csv’: Metadata for each FoG event in all data series. The event times agree with the labels in the data series. 
■	‘tasks.csv’: Task metadata for series in the defog dataset. 
3.	Code Files:   
●	EDA_Event_and_Subjects_for_Data Preparing.ipynb/html:  
○	Exploratory Data Analysis (EDA) on both the Event dataset and Subject dataset was downloaded in Google Drive. Perform data cleaning and preparation. 
●	EDA_LSTM_on_tdcsfog.ipynb / html: 
○	 EDA on `full_tdcsfog.csv` and basic LSTM model training and evaluation. 
●	EDA_LSTM_on_defog.ipynb / html:  
○	EDA on `full_defog.csv` and basic LSTM model training and evaluation. 
●	Models_defog.ipynb / html: 
○	EDA on `full_defog.csv`, model training (LSTM, GRU, SimpleRNN), evaluation, and hyperparameter tuning using KerasTuner. 
●	defog_simplernn.ipynb / html 
○	SimpleRNN model training and evaluation on `full_defog.csv`. 
●	tdcfog_simplernn_updated.ipynb / html:  
○	SimpleRNN model training and evaluation on `full_tdcsfog.csv`. 
●	Models_tdcsfog.ipynb / html:  
○	EDA on `full_tdcsfog.csv`, model training (LSTM, GRU, SimpleRNN), evaluation, and hyperparameter tuning using KerasTuner. 
 
