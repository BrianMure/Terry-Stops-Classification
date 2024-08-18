Terry Stops Prediction Project
Overview
The Terry Stops problem aims to predict the outcome of police stops based on reasonable suspicion using a classification model. The model considers various factors, including the presence of weapons, time of day, and possibly the gender and race of both the officer and the subject. However, due to the sensitive nature of race and gender data, ethical concerns arise, emphasizing the importance of avoiding bias and discrimination. The goal is to improve the efficiency and fairness of law enforcement actions while ensuring that any potential biases are carefully monitored and addressed.

1. Business Understanding
1.1 Problem Statement
Terry Stops present an opportunity to enhance the efficiency and fairness of law enforcement by developing a predictive model to assist officers in determining the likelihood of an arrest during a stop. The model's goal is to help reduce the number of false arrests and incidents of police misconduct. However, it is critical to approach this problem with caution and transparency, considering the ethical implications of using gender and race data. The ultimate objective is to provide a tool that aids in improving policing while avoiding biases and discrimination.

1.2 Aim
The aim of this project is to build a classifier that predicts the outcome of a Terry Stop (whether an arrest was made or not) based on reasonable suspicion. Factors such as the presence of weapons, time of day, and other relevant information will be considered. The model addresses a binary classification problem, aiming to improve the efficiency and fairness of law enforcement actions.

1.3 Objectives
Develop a predictive model for Terry Stops that accurately predicts the outcome of the stop (arrest made or not).
Incorporate key factors such as the presence of weapons and the time of the call into the model.
Ensure the model is ethically sound, avoiding any biases or discrimination related to gender and race.
2. Data Understanding
2.1 Dataset Description
The dataset used in this project is provided by the City of Seattle and managed by the Seattle Police Department. It contains 54,873 rows and 23 columns, with each row representing a unique Terry Stop record. The dataset includes information about both the subject of the stop and the officer conducting the stop, such as perceived age group, race, gender, officer's gender, race, and year of birth. It also includes details about the stop resolution, any weapons found, and the date and time of the stop. The data is updated daily and licensed under the public domain.

3. Modeling
3.1 Target Variable Definition
The target variable for the model is Stop Resolution, which indicates whether an arrest was made during the stop. The features used for prediction include various factors relevant to the stop.

3.2 Train/Test Split
The dataset is split into training and testing sets to evaluate model performance. The split is done with an 80/20 ratio.

python
Copy code
X_train, X_test, y_train, y_test = train_test_split(X, y, random_state=42, test_size=0.2)
3.3 Baseline Model
A logistic regression model is initially implemented as the baseline classifier.

python
Copy code
clf = LogisticRegression()
clf.fit(X_train, y_train)
Note: A convergence warning may occur, suggesting the need to increase the number of iterations or scale the data.

3.4 Decision Tree Model
A Decision Tree model is also developed, as it may offer improved accuracy in classification tasks.

4. Model Evaluation
The performance of the models is evaluated, with both achieving accuracy scores of over 80%. The models provide insights into the factors influencing the outcome of Terry Stops, particularly the likelihood of an arrest.

5. Conclusion
The models developed in this project successfully predict the outcome of Terry Stops with a significant emphasis on whether an arrest was made. These results can be instrumental in improving law enforcement decision-making processes.

6. Recommendations
Training: Train officers on the appropriate times to make arrests during Terry Stops, as this is a key predictor of outcomes.
Data Collection: Capture more detailed information, such as the officer's precinct, to enhance the model's predictive power.
Bias Mitigation: Address any biases in the data related to race, gender, or location to ensure that the model provides fair and unbiased predictions.
