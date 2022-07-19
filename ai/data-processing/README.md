# Data Processing
[code](https://github.com/hchoi256/ai-boot-camp/blob/main/ai/data-processing/data-preprocessing.ipynb)

![image](https://user-images.githubusercontent.com/39285147/177332275-18157d62-4234-43c0-b72b-e550f6bdf1bd.png)
- **Standarization**
  - range: [-sd, +sd]
  - Always operates
- **Normalization**
  - range: [0, 1]
  - optimal for normal distribution
 
## Implementation
-	Importing the librarires
-	Importing the dataset
-	Encoding categorical data
-	Splitting the dataset into the Training set and Test set
-	Feature Scaling

## Libraries
- *from sklearn.impute import SimpleImputer*
- *from sklearn.compose import ColumnTransformer*
- *from sklearn.preprocessing import OneHotEncoder*
- *from sklearn.preprocessing import LabelEncoder*
- *from sklearn.model_selection import train_test_split*
- *from sklearn.preprocessing import StandardScaler*
