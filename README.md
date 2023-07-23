# Car price prediction

Through a database (26 features, 205 records) containing vehicles physical and mechanical characteristics, it was able to develop a prediction model for car price.
    
![alt text](https://github.com/ricardofariaromero/car_price_prediction/blob/main/images/car.png)


## Variables

For this study the following variables has been analyzed:

    - CarName: brand & model.
    - fueltype: whether is gas or diesel.
    - aspiration: standard or turbo.
    - doornumber: how many doors does de vehicle has.
    - carbody: convertible, sedan, wagon, etc.
    - drivewheel: traction of the vehicle.
    - enginelocation: whether the engine is in the front or rear position of the vehicle.
    - wheelbase: size of the wheelbase.
    - carlenght: how long is the car.
    - carwidth: how wide is the car.
    - carheight: how high is the car.
    - curbweight: weight og the car.
    - enginetype: type of engine (ohc, ohcv, etc.).
    - cylindernumber: number of cylinders of engine.
    - enginesize: size of engine.
    - fuelsystem: what kind of system uses for the fuel.
    - boreratio: determines engine power.
    - stroke: movement of the piston.
    - compressionratio: the ratio between the volume of the cylinder with the piston in the bottom position.
    - horsepower: power of the engine.
    - peakrpm: peak revolutions per minute for the engine.
    - citympg: how far can you drive in the highway per gallon of fuel.
    - highwaympg: how far can you drive in the highway per gallon of fuel.
    - price: the target variable.
    
## Exploratory analysis

Through the EDA, it was determined the importance of each variable and certain transformations were applied. For instance, some variables like "doornumber" were expressed as strings, later replaced by integers to facilitate hot encoding. Others, had few representation of certaing categories replacing them by the "other" category. Due to the amount of labels for "CarName", it was only considered the brand, and not the model.

The following variables were considered for the model:

    - brand
    - fueltype
    - aspiration
    - carbody
    - drivewheel
    - wheelbase
    - carlenght
    - carwidth
    - curbweight
    - enginetype
    - cylindernumber
    - enginesize
    - fuelsystem
    - compressionratio
    - horsepower
    - citympg
    - highwaympg
    - price


## Python Libraries and algorithm

The following libraries were used during this project:

    - Pandas
    - Seaborn
    - Matplotlib
    - Scikit-learn (LinearRegression & RandomForestRegressor)

## Analysis and results

In the following graph we can se the impact of variables on price: First, the numerical features:

    
![alt text](https://github.com/ricardofariaromero/car_price_prediction/blob/main/images/numerical.png)

And the categorical:

![alt text](https://github.com/ricardofariaromero/car_price_prediction/blob/main/images/categorical.png)


Regarding the model, it was finally implemented a "Random Forest Regressor" with the application of hyperparameters ('bootstrap': True, 'max_depth': 30, 'max_features': 'sqrt', 'min_samples_leaf': 1, 'min_samples_split': 5, 'n_estimators': 50), obtaining the following metrics:

    - Mean Squared Error: 1682724.62
    - Root Mean Squared Error: 1297.20
    - Mean Absolute Error: 888.20
    - R2: 0.9735

![alt text](https://github.com/ricardofariaromero/car_price_prediction/blob/main/images/Output.png)

## Credits

All code and development performed by [Ricardo Faría](https://www.linkedin.com/in/ricardo-e-faria-romero/?locale=en_US) 
