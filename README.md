# README Description

This project involves analyzing and processing a dataset related to hate speech detection on social media platforms. The dataset contains comments and various attributes associated with each comment, such as sentiment, violence, hatespeech, and scores for different targeted categories (race, religion, origin, gender, sexuality, age, and disability). The main objective is to preprocess the text data and perform machine learning tasks to identify and categorize hate speech accurately.

## Dataset
The dataset used in this project is a CSV file containing the following columns:
- `comment_id`: Unique identifier for each comment.
- `platform`: Platform from which the comment was extracted.
- `sentiment`: Sentiment score of the comment.
- `violence`: Indicator of violent content.
- `hatespeech`: Indicator of hate speech content.
- `hate_speech_score`: Score representing the severity of hate speech.
- `text`: The actual comment text.
- `target_race`, `target_religion`, `target_origin`, `target_gender`, `target_sexuality`, `target_age`, `target_disability`: Binary indicators for whether the comment targets these categories.

## Steps Performed

1. **Data Loading and Preprocessing**:
   - Load the CSV file into a pandas DataFrame.
   - Select relevant columns for analysis.
   - Replace boolean values with binary indicators (1 for True, 0 for False).
   - Preprocess the text data to clean and standardize the comments (lowercasing, removing URLs, mentions, hashtags, punctuation, numbers, and extra whitespace).

2. **Grouping and Summarizing Data**:
   - Group the data by `comment_id` to aggregate scores for each comment.
   - Sum the binary indicators for targeted categories to get the overall targeting score for each category.

3. **Final Data Preparation**:
   - Merge the aggregated scores with the unique comments.
   - Apply text preprocessing to clean the comment text.

4. **Text Feature Extraction**:
   - Use TF-IDF vectorization to convert the cleaned comment text into numerical features suitable for machine learning models.

5. **Machine Learning Model Training**:
   - Train a machine learning model to identify and categorize hate speech based on the processed features and aggregated scores.
   - Evaluate the model's performance using accuracy and other relevant metrics.

## Results
The final processed dataset and the trained machine learning model provide insights into the prevalence and characteristics of hate speech on social media platforms. The analysis helps in understanding the patterns of hate speech and the effectiveness of automated detection methods.
