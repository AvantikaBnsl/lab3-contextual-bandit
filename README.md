Main code notebook is lab3_results_U20230063 for the RL lab3 submission. 

Topics covered -
1) User Classification:
A classifier is trained using train_users.csv to predict the user context (User1, User2, or User3) from user features. The classifier with best results is RandomForest.

2) Contextual Bandit Learning
Separate bandit agents are trained for each user context. Each agent learns expected rewards for four news categories:

Entertainment
Education
Tech
Crime

3) Three exploration strategies were implemented and evaluated:

ε-Greedy
Upper Confidence Bound (UCB)
Softmax

4) Recommendation Engine
A user is first classified into a context. The corresponding bandit agent selects a news category. An article is randomly sampled from news_articles.csv within that category and predicted for news category label. 


- Observations:

UCB performs best with rewards converging to 8.
ε-Greedy performs well with moderate exploration (ε ≈ 0.05–0.1).
Softmax is not that efficient with the texted hyperparameters. 