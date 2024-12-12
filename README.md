# Employee Benefits Impact Analysis

## Executive Summary

**Objective:**
The objective of this project was to analyse the impact of employee benefits on job satisfaction and retention, with a focus on identifying the most valued benefits that contribute to a positive employee experience. In today’s competitive job market, companies are increasingly recognizing the importance of offering comprehensive benefits packages to attract and retain top talent. This project aimed to provide actionable insights that can guide companies in optimizing their benefits offerings.

### Problem Statement:
The central problem addressed in this project is the challenge of understanding which employee benefits are most valued by employees and how these benefits influence their job satisfaction and decision to remain with the company. The hypothesis was that high-quality benefits, such as health insurance, flexible working arrangements, and pension plans, have a substantial positive impact on employee satisfaction and retention.

### Key Findings:
- **Impact of Benefits:**
  - The analysis shows that benefits like work-from-home flexibility and sick pay are highly valued by employees, as reflected by the higher frequency and positive sentiments associated with these themes.
  - The distribution of benefits shows a strong preference for flexibility-related benefits, with the least focus on areas like retirement benefits and leave policies.

- **Deeper into Others:**
  - After refining the themes within the “Other” category, it shows that miscellaneous themes remain the most frequent whereas the presence of company policies and discounts make up a smaller portion.

- **Overall Sentiment Distribution:**
  - Majority of the feedback on benefits was positive, which is a strong indicator of general satisfaction with the company’s benefit package. However, there is a significant portion of neutral and negative sentiment that needs attention.
  - The presence of neutral suggests that some benefits do not significantly impact employee satisfaction, possibly because they are seen as standard or expected. While for negative, it highlights where the company may need to focus improvements.

### Methodology:
To address these objectives, a comprehensive analysis was performed using sentiment classification, and various machine learning models, including Random Forest, SVM, and Gradient Boosting. The analysis was divided into two parts:

#### Part 1:
- Building and training a deep learning model from scratch.
- Utilizing transfer learning with pre-trained models.
- Comparing the performance of both models on an image classification task, focusing on the impact of different employee benefits.

#### Part 2:
- Applying sentiment analysis to financial datasets using deep learning models.
- Training models on Twitter sentiment data and comparing performance against financial sentiment data.

### Problems Encountered:
- One of the main challenges faced during the project was dealing with incomplete or inconsistent data. Missing values in the dataset required data cleaning and preprocessing.
- The sentiment data was imbalanced, with more positive reviews compared to negative ones. This imbalance made it difficult to predict sentiment classification in some cases. To address this, the dataset was transformed into a binary classification problem, focusing on ‘Positive’ vs ‘Others’ sentiments. Categorical features were one-hot encoded.

### Conclusion:
- **Modelling:** SMOTE was applied using Random Forest, SVM, and Gradient Boosting, with Random Forest demonstrating the best balance between precision and recall for both classes, making it the most reliable among the models tested with the highest accuracy of 73.98% compared to 69% and 67%.
- **Feature Importance:** `benefits.highlights.val.commentCount` and `benefits.comments.val.rating` were identified as the top two most important features. This means that these variables had the largest impact on the model's ability to correctly classify employee sentiment (i.e., whether it's positive or not).
- **Cross-validation:** The cross-validation scores ranged from 0.774 to 0.776, with an average of 0.775. This consistency indicates that the model performs reliably across different subsets of the data.

### Does it support the hypothesis?
- Yes, the analyses conducted—ranging from feature importance to correlation and model validation—conclusively demonstrate that the quality of employee benefits is a significant factor in determining whether employees express positive sentiment.

### Recommendations:
- Companies should prioritize improving benefits such as work-from-home options as they are most strongly associated with higher employee satisfaction and retention.
- To maintain evolving employee needs, companies should also assess and update their benefit offerings.
- Utilize the Random Forest model for ongoing analysis and predictions of the future benefits on employee sentiment, given its proven effectiveness.
