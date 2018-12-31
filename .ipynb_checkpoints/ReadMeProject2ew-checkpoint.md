##Readme Project 2 (Eric Wong)

## Kaggle Submission:
[Kaggle Link for Eric Wong](https://www.kaggle.com/ezewong)

## Presentation Slides:
[Google Slides Link for Eric Wong](https://docs.google.com/presentation/d/1HxMZ0x4TTM5UfCKSuFXpAwH2b8rcN5_TbKvRPWQhIWc/edit?usp=sharing)

## Executive Summary:
#####The goal of this analysis was to determine if housing sale prices could be modeled given a dataset from Iowa Ames. We worked to have the Machine Learning use a Linear Regression to express the relationship of several key factors that are predictive of pricing.(aka. Features). 

##  Metrics/Evaluation of model:
##### We evaluated the model using RMSE. The rationale as due to the Kaggle evaluation method uses to test our model. In addition, a lower RMSE score will indicate our model has a better fit. I've also scored based on R2 score to see how the models will fit to itself to get a general understanding.

## Regularization:
##### Intially tried a ridge regression under the assumption there was a high level of multicolinarity and multiple imposing factors. However, when trying an Elsatic Net CV analysis the model suggested a Lasso regression would provide a better fit for the model. Once trying it, the lasso optimized the R2 score better with cross validation. 

## Findings:
##### The most correlative features to the Sale Price with positive impact was overall quality, living area quality, gararage area, amount of cars can be parked, total basment sqaure feet, 1st floor square feet, and year built. These findings would indicate that the common precepts of quality and living space have the largest positive impacts on price. Garage size and parkable spaces may be indicative of overall house size and quality.

#####Whereas having average exerior quality, average kitchen quality, and average basement quality all had negative effects. Having no fireplace was also negatively correlated to price. The question as to why an average quality has a larger impact than the expected poor, likely is explained by the sample size. External Quality of average comprises 61% of sample set, good 34% and poor quality was only 1% of sample size.

## Limitations/Risks/Assumptions:
##### A major limitation of the predictive model built is the assumption is the distribution of sample sizes for each catergory. We have low sample sizes for features such as the External Quality mentoined above. There are also many catergorial values that likely would be difficult to intepret quantively in a linear regression model. Lastly, some key features such as total sq ft the house which may be more representive of a sale price correlation. Veneer quality of the kitchen and some other factors may be adding noise, although look indicative of correlation. 
##### Another issue with the current analysis may have been using some projected values of NA and setting them to 0. While those fields could be quantified, (ie. Having no 2nd floor, and seting it to quanitifable 0 ) could have been a large 1 floor house. A solution to this would again, be getting the total square footage or another measure.

## Feature selection:
#### Features were selected on the basis of their correlation to the "sale price". If their correlation was above .20 they were deemed correlative enough to keep as a variable and included in our Linear Regression model. Some variables were created from dummy variables.
#### Features with a 20% + correlation rate with housing sale price:
1. '1st_flr_sf', 
2.  '2nd_flr_sf', 
3.  'bsmt_exposure_Gd', 
4.  'bsmt_exposure_No', 
5.  'bsmt_full_bath', 
6.  'bsmt_qual_Gd', 
7.  'bsmt_qual_TA',
8.   'bsmtfin_sf_1', 
9.   'bsmtfin_type_1_GLQ',
10. 'central_air_Y', 
11.    'electrical_SBrkr', 
12.    'exter_qual_Gd',
13.     'exter_qual_TA', 
14.     'exterior_1st_VinylSd',
15.      'exterior_2nd_VinylSd', 
16.      'fireplace_qu_Gd', 
17.      'fireplace_qu_Nofp', 
18.      'fireplaces', 
19.      'foundation_CBlock',
20.       'foundation_PConc', 
21.       'full_bath',
22.        'garage_area',
23.         'garage_cars',
24.        'garage_cond_Nog',
25.        'garage_cond_TA', 
26.        'garage_finish_Nog', 
27.        'garage_finish_Unf', 
28.        'garage_qual_Nog', 
29.        'garage_qual_TA',
30.         'garage_type_Attchd', 
31.         'garage_type_BuiltIn',
32.          'garage_type_Detchd', 
33.          'garage_type_Nog', 
34.          'gr_liv_area',
35.           'half_bath', 
36.           'heating_qc_TA',
37.            'house_style_2Story',
38.             'kitchen_qual_Gd',
39.              'kitchen_qual_TA',
40.               'land_contour_HLS', 
41.               'lot_area', 
42.               'lot_shape_Reg', 
43.               'mas_vnr_area', 
44.               'mas_vnr_type_BrkFace',
45.                'mas_vnr_type_None', 
46.                'mas_vnr_type_Stone', 
47.                'ms_zoning_RL',
48.                 'ms_zoning_RM',
49.                  'neighborhood_NoRidge',
50.                   'neighborhood_NridgHt', 
51.                   'neighborhood_OldTown',
52.                    'neighborhood_StoneBr', 
53.                    'open_porch_sf', 
54.                    'overall_qual', 
55.                    'paved_drive_Y', 
56.                    'pid', 
57.                    'roof_style_Gable',
58.                    'roof_style_Hip',
59.                     'sale_type_New', 
60.                     'sale_type_WD ', 
61.                     'total_bsmt_sf',
62.                      'totrms_abvgrd', 
63.                      'wood_deck_sf', 
64.                      'year_built',
65.                       'year_remod/add'

