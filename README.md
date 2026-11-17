
# AI-Based Susoicious Review Detection and Customer Trust Analytics Using NLP and Machine Learning

## Abstract
This project aims to develop an AI-powered system that detects fake online reviews and provides customer trust analytics for e-commerce platforms. Using Natural Language Processing (NLP) and Machine Learning, the system classifies reviews as genuine or fake and generates customer trust insights.
## Problem Statement 
Online shopping platforms contain fake and misleading reviews that affect customer purchasing decisions. This project aims to identify fake reviews and measure customer trust using AI and machine learning .
## Objectives 
- Detect fake reviews using NLP and Machine Learning .
- Perform sentiment analysis.
- Generate a customer trust score.
- Build an interactive prediction dashboard.
## Dataset
Amazon Customer Reviews Dataset
## Technologies Used 
- Python
- Pandas
- NumPy
- Scikit-learn
- NLTK
- Streamlit
- matplotlib
- Github
## Project Workflow
- Data collection
- Data Understanding
- Data cleaning
- Exploratory Data Analysis (EDA)
- Feature engineering
- Weak supervision for suspicious review labelling
- NLP text preprocessing
- TF-IDF feature extraction
- Combine text and numerical features
- Train-Test Split
- Machine learning model training
  - Logistic Regression
  - Linear SVM
- Model Evaluation
  - Accuracy
  - Precision
  - Recall
  - F1 Score
  - Confusion Matrix
- Suspicious review prediction
- Customer trust score calculation
- Suspicious review and reviewer analysis
- Result
- Business insights
- Conclusion
## Data Preprocessing
The dataset was preprocessed to improve data quality and prepare it for analysis and Machine Learning.

The preprocessing steps include:

- Checking missing values
- Handling missing values
- Removing duplicate records
- Converting date columns into appropriate datetime format
- Cleaning review text
- Removing unnecessary characters
- Converting text to lowercase
- Creating cleaned review text
- Preparing numerical features for Machine Learning
## Exploratory Data Analysis (EDA)
Exploratory Data Analysis was performed to understand patterns and relationships in the review dataset.

The analysis includes:

- Rating distribution
- Review length distribution
- Review word count
- Review count analysis
- Country-wise review analysis
- Duplicate review analysis
- Suspicious review distribution
- Relationship between ratings and suspicious reviews
  
Various visualizations such as bar charts, histograms, count plots, and heatmaps were used to understand the dataset.
## Feature Engineering
Several features were created from the available review data.

- Text Features
  - Review Length
  - Review Word Count
  - Review Title Length
  - Title Word Count
- Behavioral Features
  - Review Count
  - Duplicate Review
  - Exclamation Count
  - Experience-Review Gap
- Other Features
 - Rating
 - Suspicious Score

These features help the Machine Learning models identify patterns associated with potentially suspicious reviews.
## Suspicious Review Labelling
The original dataset does not contain verified fake-review labels.

Therefore, a Suspicious Score was created using multiple review characteristics. Based on this score, reviews were categorized into:

- 0 → Genuine / Not Suspicious
- 1 → Suspicious
This approach is known as weak supervision.

The labels should be interpreted as potentially suspicious, rather than confirmed fake reviews.
##  NLP and TF-IDF
Natural Language Processing was used to analyze the textual content of reviews.

The review text was cleaned and transformed into numerical representations using TF-IDF (Term Frequency-Inverse Document Frequency).

TF-IDF helps identify words and phrases that are important within the review dataset.

The project uses:

- Unigrams
- Bigrams
- TF-IDF Vectorization

The TF-IDF features were combined with numerical and behavioral features before training the Machine Learning models.
## Machine Learning Models
Two Machine Learning algorithms were implemented:

Logistic Regression

Logistic Regression was used as one of the classification models to predict whether a review is potentially suspicious or not.

Linear SVM

Linear Support Vector Machine was also used for classification and comparison with Logistic Regression.

Both models were trained using the combined TF-IDF + numerical/behavioral features.
## Model Evaluation
The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix
  
The performance of Logistic Regression and Linear SVM was compared to determine which model performs better on the dataset.
## Model Comparison

| Model | Accuracy | Precision | Recall | F1-Score |
|---|---|---|---|---|
| Logistic Regression | 94.56% | 76.04% | 90.25% | 82.54% | 
| Linear SVM | 92.03% | 70.32% | 76.36% | 73.22% |
## Suspicious Review Prediction
A prediction function was developed to classify new reviews.

The system accepts information such as:

- Review text
- Rating
- Review count
  
It then processes the review, generates TF-IDF features, combines them with numerical features, and predicts whether the review is:

- Genuine Review
- Suspicious Review
  
The system also provides a suspicious probability for the prediction.
## Customer Trust Analytics
A Customer Trust Analytics component was developed using the model predictions and review characteristics.

The Trust Score combines:

- Genuine Probability
- Rating Score
- Review Quality Score
  
The resulting score is converted into a scale of 0–100.

Reviews are categorized as:

- High Trust: 75–100
- Medium Trust: 50–74
- Low Trust: Below 50
  
This provides an additional way to analyze the reliability of customer reviews.
## Customer Trust Analysis
Customer trust was analyzed using different aspects of the review dataset.

The analysis includes:

- Customer Trust Distribution
- Average Trust Score by Rating
- Country-wise Trust Analysis
- Suspicious Reviews by Rating
- Suspicious Review Percentage
  
These analyses help identify patterns in customer trust and review quality.
## Reviewer Analysis
Reviewer-level analysis was performed to identify unusual reviewer behavior.

The analysis considers:

- Total number of reviews
- Average rating
- Average suspicious probability
- Average trust score
  
This can help identify reviewers whose reviews may require additional investigation.
## Result 
The project successfully implemented a Machine Learning-based system for detecting potentially suspicious reviews and analyzing customer trust.

The model evaluation produced the following results:

- Logistic Regression achieved 94.56% accuracy.
- Linear SVM achieved 92.03% accuracy.
- Logistic Regression performed better than Linear SVM across the evaluated metrics.
- The system successfully predicts potentially suspicious reviews.
- Customer Trust Analytics categorizes reviews into High Trust, Medium Trust, and Low Trust.

Overall, Logistic Regression was selected as the better-performing model among the two models tested.

Note: The results are based on weakly supervised labels and do not confirm that a review is genuinely fake.
## Business Insights
The project can provide useful insights for businesses and customers:

- Identify potentially suspicious reviews.
- Monitor unusual review patterns.
- Identify reviewers requiring further investigation.
- Understand the relationship between ratings and suspicious reviews.
- Analyze customer trust across different groups.
- Help businesses improve review-quality monitoring.
- Help customers make more informed decisions.
## Limitations 
- The dataset does not contain verified fake-review labels.
- The suspicious labels are generated using weak supervision.
- Therefore, the model cannot confirm that a review is definitely fake.
- Model performance depends on the quality of the generated labels.
- A verified labelled dataset would provide more reliable evaluation.
## Conclusion
This project developed an NLP and Machine Learning-based system for identifying potentially suspicious reviews and analyzing customer trust.

Review data was cleaned and explored through EDA, followed by feature engineering using textual and behavioral characteristics. TF-IDF was used to transform review text into numerical features, which were combined with numerical features for Machine Learning.

Logistic Regression and Linear SVM were implemented and evaluated using Accuracy, Precision, Recall, F1-Score, and Confusion Matrix.

A Customer Trust Score was also developed to categorize reviews into High Trust, Medium Trust, and Low Trust. The system can help identify potentially suspicious reviews, analyze reviewer behavior, and provide useful customer-trust insights.

Since the original dataset does not contain verified fake-review labels, the detected suspicious reviews should be considered potentially suspicious rather than confirmed fake reviews.




