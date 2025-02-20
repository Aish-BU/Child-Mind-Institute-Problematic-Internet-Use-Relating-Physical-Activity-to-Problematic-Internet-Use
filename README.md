# Child-Mind-Institute-Problematic-Internet-Use-Relating-Physical-Activity-to-Problematic-Internet-Use
Problematic Internet Use (PIU) has become a growing concern, particularly among children and young people, as digital technology continues to integrate into daily life. The Severity Impairment Index (SII) is a standardized measure used to quantify the level of PIU, offering insights into its impact on behavior, mental health, and physical well-being. This study aims to develop a predictive model for SII using a rich dataset encompassing demographic, physical, and behavioral attributes, as well as results from the Parent-Child Internet Addiction Test (PCIAT).

The dataset includes 3,960 records with 81 features, providing a diverse range of indicators such as age, BMI, internet usage habits, and psychological scores. However, the presence of over 100,000 missing values and an imbalanced class distribution presents significant challenges for model development. Additionally, the test dataset lacks PCIAT features, which are highly correlated with the target variable, further complicating the prediction process.

This study explores various machine learning approaches, including classification and regression, to predict SII levels. Feature selection, imputation techniques, and hyperparameter tuning are employed to create robust models capable of handling the challenges posed by missing data and class imbalance. The findings aim to shed light on the factors contributing to PIU and provide a framework for identifying at-risk individuals, ultimately contributing to the broader understanding of digital behavior management in young populations.

## Dataset Description
The Healthy Brain Network (HBN) dataset is a clinical sample of about five-thousand 5-22 year-olds who have undergone both clinical and research screenings. The objective of the HBN study is to find biological markers that will improve the diagnosis and treatment of mental health and learning disorders from an objective biological perspective. Two elements of this study are being used for this competition: physical activity data (wrist-worn accelerometer data, fitness assessments and questionnaires) and internet usage behavior data. The goal of this competition is to predict from this data a participant's Severity Impairment Index (sii), a standard measure of problematic internet use.

In this public version, some sample data is given in the correct format to help author solutions. The full test set comprises about 3800 instances.

The target sii is missing for a portion of the participants in the training set. You may wish to apply non-supervised learning techniques to this data. The sii value is present for all instances in the test set.

## HBN Instruments
The tabular data in train.csv and test.csv comprises measurements from a variety of instruments. The fields within each instrument are described in data_dictionary.csv. These instruments are:

Demographics - Information about age and sex of participants.
Internet Use - Number of hours of using computer/internet per day.
Children's Global Assessment Scale - Numeric scale used by mental health clinicians to rate the general functioning of youths under the age of 18.
Physical Measures - Collection of blood pressure, heart rate, height, weight and waist, and hip measurements.
FitnessGram Vitals and Treadmill - Measurements of cardiovascular fitness assessed using the NHANES treadmill protocol.
FitnessGram Child - Health related physical fitness assessment measuring five different parameters including aerobic capacity, muscular strength, muscular endurance, flexibility, and body composition.
Bio-electric Impedance Analysis - Measure of key body composition elements, including BMI, fat, muscle, and water content.
Physical Activity Questionnaire - Information about children's participation in vigorous activities over the last 7 days.
Sleep Disturbance Scale - Scale to categorize sleep disorders in children.
Actigraphy - Objective measure of ecological physical activity through a research-grade biotracker.
Parent-Child Internet Addiction Test - 20-item scale that measures characteristics and behaviors associated with compulsive use of the Internet including compulsivity, escapism, and dependency.
Note in particular the field PCIAT-PCIAT_Total. The target sii for this competition is derived from this field as described in the data dictionary: 0 for None, 1 for Mild, 2 for Moderate, and 3 for Severe. Additionally, each participant has been assigned a unique identifier id.

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
