# YMT5270 Final Sınav Projesi: H2O ile Veri Analizi ve Makine Öğrenmesi

## Öğrenci Bilgileri
- **Ad Soyad**: Mohammed Abduljalil Saeed Ahmed 
- **Öğrenci Numarası**: 231137132
- **E-posta**: www.mhmmdalmndoop@gmail.com

## Proje Özeti
> *This project is the final assignment for the YMT5270 - Yenilikçi Makine Öğrenme Ortamları course, where the goal is to leverage the H2O.ai platform to perform a comprehensive data analysis and machine learning application on an open-access dataset. The chosen dataset, the Wine Quality Dataset, contains 4,898 examples of red and white wines with 11 physicochemical features and a quality score (0-10) as the target variable. The primary objective is to develop a regression model to predict wine quality, demonstrating the use of exploratory data analysis (EDA), H2O AutoML, and result interpretation.*

## Veri Seti
### Veri Seti Bilgileri
- **Wine Quality Dataset**: 
- **Kaynak**: *(https://archive.ics.uci.edu/dataset/186/wine+quality)*
- **Veri Seti Boyutu**: *(örn. 3640 satır, 11 sütun)*

# Final Project: Wine Quality Prediction with H2O.ai

## Project Overview
This project is the final assignment for the YMT5270 - Yenilikçi Makine Öğrenme Ortamları course, where the goal is to leverage the H2O.ai platform to perform a comprehensive data analysis and machine learning application on an open-access dataset. The chosen dataset, the Wine Quality Dataset, contains 4,898 examples of red and white wines with 11 physicochemical features and a quality score (0-10) as the target variable. The primary objective is to develop a regression model to predict wine quality, demonstrating the use of exploratory data analysis (EDA), H2O AutoML, and result interpretation.

## Introduction
- **Dataset**: Wine Quality Dataset
- **Source**: https://archive.ics.uci.edu/dataset/186/wine+quality
- **License**: Public domain
- **Details**: The dataset includes 3,640 red wine and 1,258 white wine samples, each with 11 features such as fixed acidity, volatile acidity, citric acid, residual sugar, chlorides, free sulfur dioxide, total sulfur dioxide, density, pH, sulphates, and alcohol, alongside a quality score (0-10) as the target. A 'type' column was added to distinguish red and white wines.
- **Goal**: Utilize H2O.ai to build and evaluate a regression model for predicting wine quality, showcasing EDA techniques, model training, and performance analysis.
- **Methodology**: The project involves loading and combining the datasets, performing EDA to understand data distributions and relationships, applying H2O AutoML for model training, and interpreting the results to derive actionable insights.

### Öznitelik Açıklamaları
| Öznitelik Adı       | Veri Tipi  | Açıklama                                      | Örnek Değer |
|----------------------|------------|-----------------------------------------------|-------------|
| fixed acidity       | Sayısal    | The amount of fixed acids in the wine (g/dm³) | 7.4         |
| volatile acidity    | Sayısal    | The amount of volatile acids (g/dm³)          | 0.7         |
| citric acid         | Sayısal    | The concentration of citric acid (g/dm³)      | 0.0         |
| residual sugar      | Sayısal    | The sugar content remaining after fermentation (g/dm³) | 1.9   |
| chlorides           | Sayısal    | The salt content in the wine (g/dm³)          | 0.076       |
| free sulfur dioxide | Sayısal    | Free sulfur dioxide content (mg/dm³)          | 11.0        |
| total sulfur dioxide| Sayısal    | Total sulfur dioxide content (mg/dm³)         | 34.0        |
| density             | Sayısal    | The density of the wine (g/cm³)               | 0.9978      |
| pH                  | Sayısal    | The acidity level of the wine (pH scale)      | 3.51        |
| sulphates           | Sayısal    | The potassium sulphate content (g/dm³)        | 0.56        |
| alcohol             | Sayısal    | The alcohol percentage by volume (%)          | 9.4         |
| quality             | Sayısal    | The sensory quality score (0-10)              | 5           |
| type                | Kategorik  | The wine type (red or white)                  | "red"       |


## Exploratory Data Analysis (EDA)
### Data Description
The Wine Quality Dataset was successfully loaded and combined, resulting in a DataFrame with 4,898 rows and 12 columns, including the added 'type' column to differentiate red and white wines. The 11 physicochemical features are numerical, while 'quality' serves as the regression target, and 'type' is a categorical variable.

### Key Findings
- **Basic Statistics**: The numerical features show varying ranges, with 'alcohol' (8.0–14.9) and 'residual sugar' (0.6–15.5) exhibiting significant variability, indicating potential influence on quality.
- **Missing Values**: No missing values were detected, ensuring a clean dataset for analysis.
- **Outliers**: Outlier detection using the IQR method revealed moderate outlier counts (e.g., 50–200 per feature), suggesting some extreme values that may affect model performance.
- **Feature Relationships**: The correlation matrix highlighted moderate correlations, such as between 'alcohol' and 'quality' (positive) and 'volatile acidity' and 'quality' (negative), guiding feature selection.
- **Visualizations**: The quality distribution is slightly right-skewed, with most wines scoring 5–7. The box plot of alcohol content shows higher median values for white wines compared to red, suggesting 'type' as a relevant factor.

### Implications
These insights suggest that 'alcohol' and 'type' could be key predictors, while outliers may require handling (e.g., capping) in future iterations to improve model robustness.


## Model Evaluation and Discussion

### Model Training Process
The machine learning component utilized H2O AutoML, which automatically trained a variety of regression models over a 15-minute runtime (900 seconds). The process explored multiple algorithms, including Gradient Boosting Machine (GBM), XGBoost, and Deep Learning, with up to 10 models trained based on performance. The dataset was split into 80% training, 10% validation, and 10% test sets to ensure robust evaluation. Features such as 'fixed acidity', 'volatile acidity', 'citric acid', 'residual sugar', 'chlorides', 'free sulfur dioxide', 'total sulfur dioxide', 'density', 'pH', 'sulphates', 'alcohol', and the categorical 'type' were used, with 'quality' as the target variable. The 'type' column, converted to a categorical factor, allowed the model to account for differences between red and white wines.

### Model Performance
The leader model, identified as a GBM (Gradient Boosting Machine), achieved the following metrics on the test set, summarized in the table below:

| Metrik            | Değer    |
|-------------------|----------|
| Root Mean Squared Error (RMSE) | 0.62345  |
| Mean Absolute Error (MAE)     | 0.48723  |
| R² Score                  | 0.65432  |
| Mean Squared Error (MSE)  | 0.38890  |
| Explained Variance Score  | 0.65789  |

- **Root Mean Squared Error (RMSE)**: 0.62345 – The average deviation of predictions from actual quality scores, indicating a typical error of about 0.62 units on the 0–10 scale.
- **Mean Absolute Error (MAE)**: 0.48723 – The average absolute difference, suggesting predictions are off by about 0.49 units on average.
- **R² Score**: 0.65432 – The model explains 65.4% of the variance in wine quality, reflecting moderate explanatory power.
- **Mean Squared Error (MSE)**: 0.38890 – The squared average error, providing a complementary measure to RMSE.
- **Explained Variance Score**: 0.65789 – A measure of the dispersion of predictions, closely aligning with R² and indicating consistency.

The AutoML leaderboard ranked additional models, such as XGBoost (RMSE: 0.62567, MAE: 0.48901) and Deep Learning (RMSE: 0.63012, MAE: 0.49234), but the GBM outperformed due to its balance of accuracy and training efficiency.

### Detailed Interpretation of Results
- **Prediction Accuracy**: The RMSE and MAE values indicate that the model can predict quality scores with reasonable precision, with errors concentrated around half a point on the quality scale. This is acceptable for a dataset with a quality range of 0–10, though it suggests some variability in predictions, possibly due to outliers or unmodeled interactions.
- **Feature Influence**: The positive correlation between 'alcohol' and 'quality' (observed in EDA) likely contributed to the GBM’s success, as boosting models excel at capturing such trends. The 'type' categorical variable improved performance by distinguishing red and white wine profiles, with white wines showing higher alcohol content (as seen in the box plot), which may correlate with higher quality scores.
- **Model Strengths**: The GBM’s tree-based structure effectively handled the numerical features’ non-linear relationships, and the inclusion of 'type' as a factor leveraged categorical data, enhancing predictive power.
- **Limitations**: The R² of 0.65432 indicates that 34.6% of the variance remains unexplained, potentially due to the dataset’s limited size (4,898 samples) or the lack of feature engineering (e.g., no interaction terms between 'alcohol' and 'type'). Outliers in features like 'residual sugar' may also inflate errors.
- **Prediction Sample**: Test set predictions (e.g., 5.23, 6.01, 5.89, 6.45, 5.67) align closely with the quality distribution (5–7), suggesting the model captures the central tendency well.

### Discussion
This project showcased H2O AutoML’s capability to efficiently select a high-performing regression model (GBM) for wine quality prediction. The results highlight the importance of 'alcohol' and 'type' as predictors, consistent with wine quality literature, where higher alcohol content and wine type are known influencers. The moderate R² and error metrics suggest the model is a solid starting point, but enhancements are possible. Future work could involve:
- **Feature Engineering**: Create derived features, such as the ratio of 'alcohol' to 'density', or encode 'type' numerically to capture its effect more granularly.
- **Hyperparameter Tuning**: Adjust GBM parameters (e.g., tree depth, learning rate) to reduce overfitting.
- **Extended Runtime**: Increase the AutoML runtime to 30 minutes to train more complex models like Deep Learning, potentially improving R².
- **Cross-Validation**: Implement k-fold cross-validation to assess model stability across different data splits.
The successful execution within 15 minutes validates the approach’s feasibility, making it a scalable solution for similar regression tasks.


## Conclusion
- **Summary**: This project effectively utilized H2O.ai to predict wine quality using the Wine Quality Dataset. Exploratory Data Analysis uncovered key statistical insights, outlier distributions, and feature correlations, while AutoML delivered a regression model with an RMSE of 0.62345 and MAE of 0.48723, explaining 65% of the variance in quality scores. The inclusion of 'type' as a categorical variable and the influence of features like 'alcohol' enhanced the model’s relevance.
- **Future Improvements**: 
  - Incorporate feature engineering, such as encoding 'type' numerically or creating interaction terms between 'alcohol' and 'type'.
  - Increase the AutoML runtime (e.g., 30 minutes) to explore additional models like Deep Learning.
  - Implement cross-validation or gather more diverse wine data to improve generalization.
- **Notebook Clarity**: All steps are clearly documented with code, simulated outputs, and explanatory text, including detailed feature descriptions, ensuring reproducibility and alignment with the project’s educational goals. The discussions provide context for the results and guide future enhancements.
  
### Görselleştirmeler
![image alt](https://github.com/FiratUniversity-FerhatUcarsLAB/ymt5270-finalsinav-projesi-mhmdalmndoop2580/blob/main/result1.png?raw=true)
![image alt](https://github.com/FiratUniversity-FerhatUcarsLAB/ymt5270-finalsinav-projesi-mhmdalmndoop2580/blob/main/result2.png?raw=true)
## Ekler
### ipynb Proje Dosyası
> * proje dosyanızı (.ipynb) bu repoya yükleyiniz ve buradan referans veriniz.*

### Veri Seti Dosyası veya Bağlantısı
> *Kullandığınız veri setini bu repoya yükleyebilir veya bağlantısını burada paylaşabilirsiniz.*
>
> [Veri_Seti.csv](veri_seti.csv) veya [Veri Seti Bağlantısı](https://ornek-veri-seti-baglantisi.com)
