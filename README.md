```
__          __    __            _____  __            _____ ___  
 \ \        / /   / _|          |  __ \/_ |   ___    |  __ \__ \ 
  \ \  /\  / /_ _| |_ ___ _ __  | |  | || |  ( _ )   | |  | | ) |
   \ \/  \/ / _` |  _/ _ \ '__| | |  | || |  / _ \/\ | |  | |/ / 
    \  /\  / (_| | ||  __/ |    | |__| || | | (_>  < | |__| / /_ 
     \/  \/ \__,_|_| \___|_|    |_____/ |_|  \___/\/ |_____/____|
  _____        _                 _                               
 |  __ \      | |               | |                              
 | |  | | __ _| |_ __ _ ___  ___| |_ ___                         
 | |  | |/ _` | __/ _` / __|/ _ \ __/ __|                        
 | |__| | (_| | || (_| \__ \  __/ |_\__ \                        
 |_____/ \__,_|\__\__,_|___/\___|\__|___/      
```


# Introduction
This is the README of the Wafer D1 and Wafer D2 dataset. If you use these datasets, please consider citing the following paper:

Furnari G, Vattiato F, Allegra D, Milotta FLM, Orofino A, Rizzo R, De Palo RA, Stanco F. An Ensembled Anomaly Detector for Wafer Fault Detection. Sensors. 2021; 21(16):5465. https://doi.org/10.3390/s21165465

# Datasets info
Datasets concern semiconductors industry, both datasets contain timeseries made by a variable number of time samples.
Both datasets have 5 reference columns: MaterialID, StepID, duration_ms, target and is_test.
The samples are grouped by a MaterialID which repesents the production lot. The production process is divided into steps.
The number of steps is different between the two datasets. There are also mandatory and optional step.

# Reference columns
- MaterialID: represents the production lot
- StepID: represents the step of the production
- duration_ms: represents the time elapsed (normalized) from the first time sample (in mandatory step) which has duration_ms 0,
the last time sample (in mandatory step) has duration_ms equal to 1.
Time samples in optional step have duration_ms greater than 1 or lesser than 0.
- Target: is a boolean value that represent if the MaterialID is abnormal or not, 1 for abnormal MaterialID, 0 for normal MaterialID.
- is_test: is a boolean value that represent if the time sample has been used as training or test in our work. 1 means that the time
sample has been used as test, 0 means that the time sample has been used for the training phase.

## Wafer D1 StepID
Wafer D1 dataset has 7 steps, 5 are mandatory with IDs 2, 4, 5, 6 and 7 while 2 are optional with ID -1 and -2

## Wafer D1 MaterialID
Wafer D1 has 5105 MaterialID

## Wafer D2 StepID
Wafer D2 dataset has 2 mandatory steps and no optional steps.

## Wafer D2 MaterialID
Wafer D2 has 1157 MaterialID

# Features columns
Both dataset have features columns, the number of the features is different betwen the two dataset
All the features have been normalized with a z-scaler

## Wafer D1 Features columns
Wafer D1 has 15 features columns 

## Wafer D2 Features columns
Wafer D2 has 20 features columns 

# Datasets shape

## Wafer D1 shape
Wafer D1 counts 602108 rows and 20 columns

## Wafer D2 shape
Wafer D2 counts 126795 rows and 25 columns
