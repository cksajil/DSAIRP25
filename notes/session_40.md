# Encoding, Scaling, Normalization, Corrleation

# Data Scaling (for numerical columns)
- Min-Max Scaling
x_scaled = x-min(x)/(max(x)-min(x))

- Standard Scaling
x_scaled = (x-mean(x))/stdev(x)

# Encoding (for categorical columns)
- One-hot Encoding
- Label Encoding

# Data Preprocessing Pipeline
- Dropping duplicate rows
- Finding and handling duplicate columns
- Inspecting column data type
- Splitting numerical and categorical variables
- Checking and Filling missing values
    - Filling Numerical
        - Inspcting with EDA
    - Filling Categorical
- Handling Class imbalance
- Outlier detection and removal
- Scaling numerical columns
- Encoding categorical columns
- Pickle Scalers and Encoders
- Separating features and labels
- Train-test split

# Feature Engineering
- Feature engineering is often done by domain experts/researchers in that specific field.
- This is often resulted from many decades of research findings.
- When you are working on any specific domain, you will have to discuss with domain experts.
- Read Scientific Literature
- Deep learning: Automaticall learn correct featurization with lots of data

## Domain Specific Transformations
- Audio
    - FFT (non-speech)
    - STFT (non-speech)
    - MFCC (for speech)

## Generic Feature Engineering Methods
- Feature Selection based on correlation to target column
    - Data Preprocessing
    - Compute correlation w.r.t. Target column
    - Take absolute value of correlation
    - Sort in descending order and find most relevant features 
- Log transformation for tailed distributed numerical columns

- Feature Binning
- Indicator Variable
- Use orthogonal features
- Polynomial Transformation
