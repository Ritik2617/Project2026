# Project2026
“My project is on Predicting Brand Deal Closure for Instagram Influencers using Machine Learning.
The goal was to understand what factors help brands successfully close deals with influencers, and to build a model that can predict whether a deal will close or not.”
“Brands spend a lot of money on influencer marketing, but many negotiations fail due to poor fit, slow response, or too many negotiations.
I wanted to analyze influencer-brand interactions and build a model that predicts whether a deal will close.”
“I used a dataset with 300 influencer-brand negotiation records.
It contains features like:

Followers

Engagement rate

Brand fit score

Past collaboration success

Response time

Negotiation rounds

Whether influencer asked for payment or free product

Final deal outcome (deal_closed: 0 or 1)”
“First, I performed EDA to understand patterns. I found that:

Higher brand fit score increases chances of deal closure

Higher past success rate increases chances of deal

More negotiation rounds reduce success

Slower brand response time reduces success.”

Model Performance and Insights
The RandomForestClassifier, incorporating one-hot encoded categorical features, achieved an accuracy of 60% on the test set. This is an improvement compared to the Logistic Regression model (50% accuracy) and is slightly better than the best KNN model (53.3% accuracy).
Key Insights from Feature Importance:
Based on the feature importance plot, the top influencing factors for deal closure, as identified by the RandomForestClassifier, are:
1.	past_collab_success_rate: This remains a critical predictor, indicating that an influencer's past success in collaborations is highly valued.
2.	brand_response_time_hours: A shorter response time from the brand correlates with a higher likelihood of deal closure.
3.	brand_fit_score: A strong alignment between the influencer and the brand's values continues to be a significant positive factor.
4.	followers and engagement_rate_%: While important, their relative importance is lower than the top three, suggesting that quality and fit might be prioritized over sheer reach for deal closure.
5.	negotiation_rounds: More negotiation rounds tend to negatively impact deal closure, consistent with previous observations.
The inclusion of one-hot encoded categorical features (niche, preferred_communication, content_format) has contributed to a modest improvement in model performance, indicating their relevance in predicting deal outcomes. Specific niches like 'Gaming' and content formats like 'Story' also show some influence on deal closure.
________________________________________
Final Task
Subtask:
Summarize the findings from the new model, compare its performance to previous models, and discuss key insights gained from the feature importance analysis.
________________________________________
Summary:
Q&A
The new model, a RandomForestClassifier incorporating one-hot encoded categorical features, achieved an accuracy of 60% on the test set. This represents an improvement compared to the previously developed Logistic Regression model, which had an accuracy of 50%, and is slightly better than the best KNN model, which attained 53.3% accuracy.
Key insights from the feature importance analysis indicate that past_collab_success_rate, brand_response_time_hours, and brand_fit_score are the most critical predictors for deal closure. While followers and engagement_rate_% are important, their influence is secondary to these top three factors. negotiation_rounds tend to negatively impact deal closure. The newly incorporated one-hot encoded categorical features, such as 'niche', 'preferred_communication', and 'content_format', have contributed to this modest improvement in performance, confirming their relevance in predicting deal outcomes.
Data Analysis Key Findings
•	One-hot encoding successfully transformed the original DataFrame (shape (300, 19)) into an encoded DataFrame (shape (300, 31)), adding new feature columns for 'niche', 'preferred_communication', and 'content_format'.
•	The RandomForestClassifier model, trained on the prepared data, achieved an accuracy of 60% on the test set.
•	This performance marks an improvement over previous models, specifically the Logistic Regression model (50% accuracy) and the best KNN model (53.3% accuracy).
•	Feature importance analysis revealed that past_collab_success_rate, brand_response_time_hours, and brand_fit_score are the top three most influential factors in predicting deal closure.
•	Other significant predictors include followers and engagement_rate_%, though with lower relative importance than the top three, and negotiation_rounds, which likely indicates a negative impact on deal closure.
•	The inclusion of one-hot encoded categorical features (e.g., 'Gaming' niche, 'Story' content format) also showed some contribution to deal closure prediction, suggesting their value in the model.
Insights or Next Steps
•	The improved model performance (60% accuracy) demonstrates the value of incorporating relevant categorical features through one-hot encoding, leading to a more robust prediction of deal closures.
•	Future efforts could focus on further hyperparameter tuning of the RandomForestClassifier or exploring other ensemble models to potentially achieve even higher predictive accuracy.

