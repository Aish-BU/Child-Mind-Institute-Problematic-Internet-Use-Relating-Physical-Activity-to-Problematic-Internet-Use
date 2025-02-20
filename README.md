# Child-Mind-Institute-Problematic-Internet-Use-Relating-Physical-Activity-to-Problematic-Internet-Use
Problematic Internet Use (PIU) has become a growing concern, particularly among children and young people, as digital technology continues to integrate into daily life. The Severity Impairment Index (SII) is a standardized measure used to quantify the level of PIU, offering insights into its impact on behavior, mental health, and physical well-being. This study aims to develop a predictive model for SII using a rich dataset encompassing demographic, physical, and behavioral attributes, as well as results from the Parent-Child Internet Addiction Test (PCIAT).

The dataset includes 3,960 records with 81 features, providing a diverse range of indicators such as age, BMI, internet usage habits, and psychological scores. However, the presence of over 100,000 missing values and an imbalanced class distribution presents significant challenges for model development. Additionally, the test dataset lacks PCIAT features, which are highly correlated with the target variable, further complicating the prediction process.

This study explores various machine learning approaches, including classification and regression, to predict SII levels. Feature selection, imputation techniques, and hyperparameter tuning are employed to create robust models capable of handling the challenges posed by missing data and class imbalance. The findings aim to shed light on the factors contributing to PIU and provide a framework for identifying at-risk individuals, ultimately contributing to the broader understanding of digital behavior management in young populations.

## Key Points

- The main aim of the competition is to use our training data to predict sii or Severity Impairment Index, which is a standard measure of Problematic Internet Use (PIU).
- The training data comprises 3,960 records of children and young people with 81 columns (not including the ID column).
- Of particular importance in the data are results of the Parent-Child Internet Addiction Test (PCIAT).
- The target is actually derived from the field PCIAT-PCIAT_Total (scored out of 100).
- We can therefore choose to predict the PCIAT Total and convert this to sii (making this a regression problem) or stick with sii (making this a classification problem).
- The test data is really just formatted sample data. The actual test data of about 3,800 instances is hidden.
- In the sample data none of the 22 PCIAT fields are available (in addition to the target feature). Hence the sample data format has 58 columns compared to 81 in the train data.
- In 1,224 records in the train data the sii target and all the PCIAT columns are missing - presumably because not available.
- Overall there are > 100,000 missing values in the train data.
- Only 2,736 records have a target, the rest are missing.
- 996 of the young people also have sensor data from a worn device which measures gross motor activity.
