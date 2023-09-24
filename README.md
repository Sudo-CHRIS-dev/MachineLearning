# Machine Learning

# Machine learning for the purpose of Predicting Insurance claims
- Author: Christian Bam
### Business problem:
- Predict the possibilties of insurance clients submitting a claim.
### Data: The data comtains the below information about patients
- Source: www.kaggle.com
 0   ID                   
 1   AGE                  
 2   GENDER               
 3   RACE                 
 4   DRIVING_EXPERIENCE   
 5   EDUCATION           
 6   INCOME           
 7   CREDIT_SCORE       
 8   VEHICLE_OWNERSHIP  
 9   VEHICLE_YEAR  
 10  MARRIED  
 11  CHILDREN
 12  POSTAL_CODE 
 13  ANNUAL_MILEAGE 
 14  VEHICLE_TYPE  
 15  SPEEDING_VIOLATIONS 
 16  DUIS              
 17  PAST_ACCIDENTS  
 18  OUTCOME


## Methods
* Cleaning and Visualization
   - Delete unnecessary columns.
   - Deleted duplicate rows.
   - Identified and corrected inconsistencies in data for categorical values (i.e. Cat, cat, cats).
   - Identified outliers.
   - Identified and addressed missing values.
   - Produced univariate visuals for the target and all features.
     
* Exploratory Data Analysis
   - Produced univariate visuals for the target and all features.

* Explanatory Data Analysis
  - Show Correlation between target and features
  - Use univariate visualization to show the distribution of values/categories
  - Use multivariate visualization plotting each feature vs the target

![image](https://github.com/Desh86/Project2/assets/138576166/1c53619a-54a6-4c29-a186-6f2ca4b607ca)
This graph indicates the correlation between having heart disease and smoking.
Its clear that people which have never smoked as a less chance of having heart disease.

Surprisingly people who used to smoke and stopped have heart disease as compared to people who are active smokers.

We also have a number of people on our dataset which we do not have a smoking status data for.

![image](https://github.com/Desh86/Project2/assets/138576166/eb8e4b8f-a1f4-4af9-ad99-da3eaf777385)
The heat map indicates that the onlyfeature  correlation is a patients age, all the other features have a very small to almost no correlation.


* Modeling
  - Decision Tree Classifier 
  - Random Forest Classifier 
  - Baggings Classifier 

* Use GridSearchCV to Hypertune the Three models

* Best tuned model results using Accuracy Metrics:
      Decision Tree Classifier - 0.94% with hypertuning
      Randon Forest Classifier - 0.94% without hypertuning
      Bagging Classifier - 0.937% with hypertuning

* Apply with and without PCA to determine the best model.
  Random Forest and Baggings provided the best results accuracy metrics


* Final production model to be used and recommendations:

  - The PCA models poduced a higher accuracy result as compared to the hypertune models.

  -Two of the 3 PCA models produced high accuracy and were almost identical in results. These PCA models were the Random Forest and Baggings Classifier Models.

  -However even though the Baggings Classifier produced a higher speed vs the Random Forest, the Random Forest Model produced a precsion of 100% as compared to 0.99% of the Baggings Classifier.

  -Since this model will be predicting the possiblities of having a stroke we require the best results therefore I would recommend the PCA Random Forest Classifier Model.
