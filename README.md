# Pump-it-Up-moracse_170199F
 Github - https://github.com/prahack/Pump-it-Up-moracse_170199F


## Handling missing values
### Droped some fetures;

* `scheme_name` - There are lot of null value percentage and dropped because of it.

* `construction_year` - Lots of invalied values (0s) in this feature column and dropped this feature.

* `num_private` - This feature is unknown and dropped this also.


### Filled some values

Handle some unusual 0 values with replacing mean or median. 

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
* Used `Sequntial Feature Selection` to select the best set of the features and use selected features for the model training process.

## Model 

I used `Catboost` model as the classification approach. I used 1000 iterations, 0.1 learning rate, depth 10 with `MultiClass` loss function.