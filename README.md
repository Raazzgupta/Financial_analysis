# Financial Market Sentiment Analysis

This repository contains a Python-based project to analyze financial market sentiments using machine learning techniques. The project processes financial news data, transforms it into numerical representations, and uses a Random Forest classifier to predict market sentiment labels.

## Dataset
The dataset contains financial market news headlines and their corresponding sentiment labels:
- **News columns**: A series of 25 news headlines per row.
- **Label**: A binary column (0 or 1) indicating negative or positive sentiment.

The dataset is loaded directly from a URL:
```python
https://raw.githubusercontent.com/YBIFoundation/Dataset/main/Financial%20Market%20News.csv
```

## Workflow

### 1. Data Loading and Exploration
- Load the dataset using `pandas`.
- Explore the dataset structure and handle missing values.

### 2. Preprocessing
- Concatenate 25 news columns into a single text feature for each row.
- Convert text data into numerical representations using Bag-of-Words (BoW) with `CountVectorizer`.

### 3. Model Training and Evaluation
- Split the dataset into training and testing sets using `train_test_split`.
- Train a Random Forest Classifier on the training data.
- Evaluate the model using accuracy, precision, recall, F1-score, and a confusion matrix.

### 4. Results
The initial implementation shows issues in model performance, with precision and F1-scores being undefined for certain labels. Adjustments in preprocessing and model tuning are recommended to improve performance.

## Prerequisites
Install the required Python libraries:
```bash
pip install pandas numpy scikit-learn
```

## Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/financial-market-sentiment.git
   ```
2. Navigate to the project directory:
   ```bash
   cd financial-market-sentiment
   ```
3. Run the Jupyter Notebook or Python script to analyze the data:
   ```bash
   jupyter notebook Financial_Market_Sentiment_Analysis.ipynb
   ```

## File Structure
- `Financial_Market_Sentiment_Analysis.ipynb`: Main analysis notebook.
- `README.md`: Project overview and instructions.

## Issues and Recommendations
- Ensure the `news` feature is correctly concatenated during preprocessing.
- Tune hyperparameters of the Random Forest Classifier.
- Consider using other feature extraction methods like TF-IDF or pretrained embeddings (e.g., Word2Vec, BERT).

## License
This project is licensed under the MIT License. Feel free to use, modify, and distribute this project as per the license terms.

## Contribution
Contributions are welcome! To contribute:
1. Fork the repository.
2. Create a new branch for your feature/bug fix.
3. Submit a pull request.

---

Feel free to reach out with questions or suggestions. Happy coding!
