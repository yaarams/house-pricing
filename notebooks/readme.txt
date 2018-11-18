data preperation:
1. outliers removal- 8 rows where GrLivArea>4000 or LotArea>100000.
2. drop columns that don't give additional information: 'HouseStyle','BldgType','GarageCars','Utilities'
3. fix 3 typo's in Exterior2nd
4. map OverallCond and OverallQual from 1-10 to: (Low, Average, High)
5. after making dummy variables drop these un necessary columns: 'SaleType_New', 'CentralAir_Y','LandSlope_Gtl' ,'BsmtFinType2_Unf',
            'Foundation_PConc','RoofStyle_Gable', 'PavedDrive_Y','Electrical_SBrkr'
6. drop yearbuilt (it gives no information because of YearRemodAdd)-to check again.
7. if YearRemodAdd>yearsold:fix that.
8. if GarageYrBlt<1950 change YearRemodAdd to the same value. 

replacing null values in train set (should be re examined!):
1. LotFrontage- replace with mean
2. MasVnrArea-replace with 0
3. GarageYrBlt-replace with mean


new variables:
1. a lot of dummy variables from categorical var's. some are significant
2. dummies for the intersection of MSZoning and MSSubClass. most are significant
3. average (above ground) room size. is significant
4. dummies for number of room (above ground). drop 8 rooms cause its unique. all are significant.
5. SaleDate to predict time trend. non linear time trend it apears.
6. n_transaction- number of transactions in the same month. significant
7. usa_sale_prices. not significant
8. Ames_sale_prices. usually not significant.
9. Ames Unemployment. significant
10. Addon_garage- garage that was built after the house- not significant
11. old house- since houses YearRemodAdd is always greater then 1950 i'm trying to predict if older houses suffer from price penalty. not significant.



data analisys:

1. garage in different neighberhoods have different affect on prices
2. difference between Exterior1st and Exterior2nd is not important and can be dropped.
3. 


to do:
1. group "cheap" and "expensive" Exterior1st and Exterior2nd materials.
2. check if diff in YearRemodAdd and yearbuilt help us explain the model.
