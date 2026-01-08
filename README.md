# Exoplanet Transit Detection using Machine Learning
This project is my first hands-on exploration into astronomy and machine learning.  
The goal was to understand how astronomers use data from space telescopes and whether a simple machine learning model can learn to identify exoplanet transit signals from stellar light curves.
Rather than focusing on discovering new planets, this project focuses on building and understanding the full data-to-model pipeline using real observational data.

## About the Problem
Exoplanets are planets that orbit stars outside our solar system.  
One common detection method is the **transit method**, where a planet passing in front of its host star causes a small dip in the observed brightness.
These brightness measurements form what are called **light curves**.  
Manually analyzing thousands of such curves is difficult, which makes this an interesting problem for machine learning.

## Dataset
- Each row represents a star
- Each column represents brightness (flux) values over time
- Labels indicate whether a star hosts a planet or not
- The dataset is highly imbalanced, which reflects real astronomical observations
The data also contains noise and missing values, which makes preprocessing an important step.

## Approach
The workflow followed in this project:
1. Load and explore real astronomical time-series data
2. Visualize stellar light curves
3. Normalize flux values for consistency
4. Handle missing values using statistical imputation
5. Train a baseline Logistic Regression model
6. Evaluate results using a confusion matrix

The focus was on understanding each step rather than optimizing performance.

## Results
The trained model was able to correctly identify a known exoplanet transit in the test dataset.  
While overall accuracy is high, recall for the planet class is limited due to class imbalance and the simplicity of the model.
This is expected for a baseline approach and highlights the challenges of exoplanet detection.

## What I Learned
- Working with real scientific data is very different from clean tutorial datasets
- Handling missing values and noise is critical
- Accuracy alone is not a reliable metric for imbalanced problems
- Even simple models can learn meaningful patterns from real data

## Future Improvements

- Use class-balanced or cost-sensitive models
- Try ensemble methods or deep learning approaches
- Extract domain-specific features such as transit depth and duration


## Tools Used
Python, NumPy, Pandas, Matplotlib, Scikit-learn
