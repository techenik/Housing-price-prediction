
## Problem Statement
- Housing price prediction

## Problem Description
- Ask a home buyer to describe their dream house, and they probably won't begin with the height of the basement ceiling or the proximity to a north-south railroad. House price negotiations often have a lot of influencing factors and not just the number of bedrooms or the position of the kitchen.
- Take the given dataset with 79 explanatory variables describing (almost) every aspect of residential homes in Ames, Iowa. In this hackathon, predict the final price of each home.  
- The application should be modelled using Spark, and the same can be streamed to the Kafka server. Apply containerisation principles as a better software engineering practice.  
- The model can be deployed in a Kubernetes environment if you consider scalability and self-healing ability are important. The choice of Kubernetes can be your own infrastructure or on any of the popular cloud environments such as Google Kubernetes Engine (GKE) for example. 

## Pre-requisites
- Install `docker`
- Install `docker-compose`

## Running Instructions
- Create a fork of the repo using the `fork` button.
- Clone your fork using `https://github.com/technik/Housing-price-prediction`
- Build the images using `docker-compose build`
- Spin up the containers using `docker-compose up`

## About the Data Set
- We used the data set from `https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data`
- Description of feilds in the dataset
	- MSSubClass: The building class
	- MSZoning: The general zoning classification
	- LotFrontage: Linear feet of street connected to property
	- LotArea: Lot size in square feet
	- Street: Type of road access
	- Alley: Type of alley access
	- LotShape: General shape of property
	- LandContour: Flatness of the property
	- Utilities: Type of utilities available
	- LotConfig: Lot configuration
	- LandSlope: Slope of property
	- Neighborhood: Physical locations within Ames city limits
	- Condition1: Proximity to main road or railroad
	- Condition2: Proximity to main road or railroad (if a second is present)
	- BldgType: Type of dwelling
	- HouseStyle: Style of dwelling
	- OverallQual: Overall material and finish quality
	- OverallCond: Overall condition rating
	- YearBuilt: Original construction date
	- YearRemodAdd: Remodel date
	- RoofStyle: Type of roof
	- RoofMatl: Roof material
	- Exterior1st: Exterior covering on house
	- Exterior2nd: Exterior covering on house (if more than one material)
	- MasVnrType: Masonry veneer type
	- MasVnrArea: Masonry veneer area in square feet
	- ExterQual: Exterior material quality
	- ExterCond: Present condition of the material on the exterior
	- Foundation: Type of foundation
	- BsmtQual: Height of the basement
	- BsmtCond: General condition of the basement
	- BsmtExposure: Walkout or garden level basement walls
	- BsmtFinType1: Quality of basement finished area
	- BsmtFinSF1: Type 1 finished square feet
	- BsmtFinType2: Quality of second finished area (if present)
	- BsmtFinSF2: Type 2 finished square feet
	- BsmtUnfSF: Unfinished square feet of basement area
	- TotalBsmtSF: Total square feet of basement area
	- Heating: Type of heating
	- HeatingQC: Heating quality and condition
	- CentralAir: Central air conditioning
	- Electrical: Electrical system
	- 1stFlrSF: First Floor square feet
	- 2ndFlrSF: Second floor square feet
	- LowQualFinSF: Low quality finished square feet (all floors)
	- GrLivArea: Above grade (ground) living area square feet
	- BsmtFullBath: Basement full bathrooms
	- BsmtHalfBath: Basement half bathrooms
	- FullBath: Full bathrooms above grade
	- HalfBath: Half baths above grade
	- Bedroom: Number of bedrooms above basement level
	- Kitchen: Number of kitchens
	- KitchenQual: Kitchen quality
	- TotRmsAbvGrd: Total rooms above grade (does not include bathrooms)
	- Functional: Home functionality rating
	- Fireplaces: Number of fireplaces
	- FireplaceQu: Fireplace quality
	- GarageType: Garage location
	- GarageYrBlt: Year garage was built
	- GarageFinish: Interior finish of the garage
	- GarageCars: Size of garage in car capacity
	- GarageArea: Size of garage in square feet
	- GarageQual: Garage quality
	- GarageCond: Garage condition
	- PavedDrive: Paved driveway
	- WoodDeckSF: Wood deck area in square feet
	- OpenPorchSF: Open porch area in square feet
	- EnclosedPorch: Enclosed porch area in square feet
	- 3SsnPorch: Three season porch area in square feet
	- ScreenPorch: Screen porch area in square feet
	- PoolArea: Pool area in square feet
	- PoolQC: Pool quality
	- Fence: Fence quality
	- MiscFeature: Miscellaneous feature not covered in other categories
	- MiscVal: $Value of miscellaneous feature
	- MoSold: Month Sold
	- YrSold: Year Sold
	- SaleType: Type of sale
	- SaleCondition: Condition of sale
	- SalePrice: Selling Price of the House
- We used "Random Forest Regressor" to train and predict the the selling price of the house after taking in the different parameters into consideration.

## Files Description
- "Trainr" folder is training the model on the given dataset
- "Trainr/models/prices_nb.pkl" is the model which is trained on the dataset and used for predicting the selling price
- "Trainr/data/train.csv" is the training dataset on which the model is trained
- "explainability(AI).ipynb" have the explainability of the different model on the given dataset
- "Kafka-Consumer" folder have the configurations of the Kafka consumer.
- "kafka-producer" folder have the configurations of the Kafka producer.