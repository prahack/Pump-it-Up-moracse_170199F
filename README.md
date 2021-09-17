# Pump-it-Up-moracse_170199F
 Github - https://github.com/prahack/Pump-it-Up-moracse_170199F


## Handling missing values
### Dropped some features;

* `scheme_name` - There are a lot of null value percentages and dropped because of it.

* `construction_year` - Lots of invalid values (0s) in this feature column and dropped this feature.

* `num_private` - This feature is unknown and dropped this also.


### Filled some values

Handle some unusual 0 values by replacing mean or median. 

* `gps_height` - Group by `region` and `district_code`to fill the missing values(0s) using mean in this features.

* `population` - Group by `region` and `district_code`to fill the missing values(0s) using median in this features.

* `amount_tsh` - Group by `region` and `district_code`to fill the missing values(0s) using median in this features.

* `longitude` - Group by `region` and `district_code`to fill the missing values(0s) using mean in this features.

* `latitude` - Group by `region` and `district_code`to fill the missing values(0s) using mean in this features.


## Feature engineering

### Created features
* Created two features splitting the `date_recorded` feature.
### Feature selection
* Dropped some features looking at the visualizations.
* Used `Sequential Feature Selection` to select the best set of the features and use selected features for the model training process.

## Model training

* I used the `Catboost` model as the classification approach. I used 1000 iterations, 0.1 learning rate, depth 10 with the `MultiClass` loss function.

## Submissioin

![image (70)](https://user-images.githubusercontent.com/31022509/133833833-8522ab17-7721-4983-9f5c-150c1c7b2a37.png)
