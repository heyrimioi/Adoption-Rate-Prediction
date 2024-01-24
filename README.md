This project was carried out as a project of the UCA DSAI course "Machine Learning Algorithms" class.

## Project Overview : Adoption Rate Prediction
The dataset presents pet's characteristics and includes tabular, text and image data. It's come from: https://www.petfinder.my.

Data fields:
* index - Unique hash ID of pet profile
* Type - Dog or Cat
* Age - Age of pet when listed, in months
* Gender - Gender of pet (Male, Female, Mixed, if profile represents group of pets)
* Color1 - Color 1 of pet
* Color2 - Color 2 of pet 
* Color3 - Color 3 of pet 
* MaturitySize - Size at maturity (Small, Medium, Large, Extra Large, Not Specified)
* FurLength - Fur length (Short, Medium, Long, Not Specified)
* Vaccinated - Pet has been vaccinated (Yes, No, Not Sure)
* Dewormed - Pet has been dewormed (Yes, No, Not Sure)
* Sterilized - Pet has been spayed / neutered (Yes, No, Not Sure)
* Health - Health Condition (Healthy, Minor Injury, Serious Injury, Not Specified)
* Fee - Adoption fee (0 = Free)
* Breed - breed of pet (see on the dataset)
* Description - Profile write-up for this pet. The primary language used is English, with some in Malay or Chinese.
* Image - a pointer to an image

The aim is to predict AdoptionSpeed. The value is determined by how quickly, if at all, a pet is adopted. The values are determined in the following way: 

* 0 - Pet was adopted on the same day as it was listed. 
* 1 - Pet was adopted between 1 and 7 days (1st week) after being listed. 
* 2 - Pet was adopted between 8 and 30 days (1st month) after being listed. 
* 3 - Pet was adopted between 31 and 90 days (2nd & 3rd month) after being listed. 
* 4 - No adoption after 100 days of being listed. (There are no pets in this dataset that waited between 90 and 100 days).

Metric
* Submissions are scored based on the quadratic weighted kappa, which measures the agreement between two ratings. This metrics exist on sklean: sklearn.metrics.cohen_kappa_score with weights="quadratic".

Supposed task(mandatory): 
* Build a sklearn or imblearn pipeline that includes all the necessary preprocessing regardless of the data type (tabular, text or image) and uses a predictor.
* use cross validation to determine the best preprocessing and the best predictor and its best hyper-parameters.
