**Problem Statement**

  Online judges provide a platform where many users solve problems everyday to improve their programming skills. The users can be beginners or experts in competitive programming. Some users might be good at solving specific category of problems(e.g. Greedy, Graph algorithms, Dynamic Programming etc.) while others may be beginners in the same. There can be patterns to everything, and the goal of the machine learning would be to identify these patterns and model user’s behaviour from these patterns. The goal of this challenge is to predict range of attempts a user will make to solve a given problem given user and problem details. Finding these patterns can help the programming committee, as it will help them to suggest relevant problems to solve and provide hints automatically on which users can get stuck.  
  
  **Evaluation Metric**
  
The metric used for evaluating the performance of the model is the F1 score between the predicted and the actual value with average parameter set to ‘weighted’.



**Data**


There are 3 training data files and 1 file for testing:

 

*train_submissions.csv*:

This contains 1,55,295 submissions which are selected randomly from 2,21,850 submissions. Contains 3 columns (‘user_id’, ‘problem_id’, ‘attempts_range’). The variable ‘attempts_range’ denoted the range no. in which attempts the user made to get the solution accepted lies.

*user_data.csv*:

This is the file containing data of users. It contains the following features :-

- user_id - unique ID assigned to each user
- submission_count - total number of user submissions
- problem_solved - total number of accepted user submissions
- contribution - user contribution to the judge
- country - location of user
- follower_count - amount of users who have this user in followers
- last_online_time_seconds - time when user was last seen online
- max_rating - maximum rating of user
- rating - rating of user
- rank - can be one of ‘beginner’ ,’intermediate’ , ‘advanced’, ‘expert’
- registration_time_seconds - time when user was registered

*problem_data.csv*: 

This is the file containing data of the problems. It contains the following features :-

problem_id - unique ID assigned to each problem
level_id - the difficulty level of the problem between ‘A’ to ‘N’
points - amount of points for the problem
tags - problem tag(s) like greedy, graphs, DFS etc.

*test_submissions.csv*:

This contains the remaining 66,555 submissions from total 2,21,850 submissions. Contains 1 column (ID). The ‘attempts_range’ column is to be predicted.
 


