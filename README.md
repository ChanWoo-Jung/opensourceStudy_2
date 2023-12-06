# opensourceStudy_2

Project #2-1 Data analysis with pandas
Project Requirements 
▪ Please implement the Python source code corresponding to the below requirements
1) Print the top 10 players in hits (안타, H), batting average (타율, avg), homerun (홈런, HR), and onbase percentage (출루율, OBP) for each year from 2015 to 2018.
2) Print the player with the highest war (승리 기여도) by position (cp) in 2018. (15 points)
▪ Position info. - 포수, 1루수, 2루수, 3루수, 유격수, 좌익수, 중견수, 우익수
3) Among R (득점), H (안타), HR (홈런), RBI (타점), SB (도루), war (승리 기여도), avg (타율), OBP 
(출루율), and SLG (장타율), which has the highest correlation with salary (연봉)? 
▪ Implement code to calculate correlations and print the answer to the above question.


Project #2-2 Data analysis with sklearn
▪ Project Goal
  ▪ Train various ML models to predict the salary of the batter in the specific year
  ▪ This is a regression task and we will use three kinds of ML models
    ▪ Decision Tree Regressor
    ▪ Random Forest Regressor
    ▪ Support Vector Machine Regressor
  ▪ We will use only numerical features

Project2에 대한 함수 설명
▪ Function descriptions
  ▪ sort_dataset
    ▪ Return sorted version of the given dataframe by year(해당 시즌) column in ascending order
  ▪ split_dataset
    ▪ Return X_train, X_test, Y_train, Y_test dataframes
    ▪ We use the salary column for the label
 
    ▪ Split the index range of [:1718] for the given dataframe as the train dataset
    ▪ Split the index range of [1718:] for the given dataframe as the test dataset

  ▪ extract_numerical_cols
    ▪ Return a dataframe that extracts only numerical features from the input dataframe
    ▪ Numerical columns: 'age', 'G', 'PA', 'AB', 'R', 'H', '2B', '3B', 'HR', 
      'RBI', 'SB', 'CS', 'BB', 'HBP', 'SO', 'GDP', 'fly', 'war’
      
  ▪ train_predict_decision_tree
    ▪ Train decision tree regressor model using given X_train and Y_train
    ▪ Return prediction result of X_test by using the trained model

  ▪ train_predict_random_forest
    ▪ Train random forest regressor model using given X_train and Y_train
    ▪ Return prediction result of X_test by using the trained model
    
  ▪ train_predict_svm
    ▪ Train the pipeline consists of a standard scaler and SVM model using given X_train and 
      Y_train
    ▪ Return prediction result of X_test by using the trained model

  ▪ calculate_RMSE
    ▪ Calculate and return RMSE using given labels and predictions
