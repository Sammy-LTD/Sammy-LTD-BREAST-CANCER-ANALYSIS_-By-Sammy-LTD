# Sammy-LTD-BREAST-CANCER-ANALYSIS_-By-Sammy-LTD
A model that predicts cancer status using the K-Nearest Neighbors (KNN) algorithm in a classification task.
## Step 1: Collecting Data
I used the Wisconsin Breast Cancer Diagnostic dataset, available from the UCI Machine Learning Repository at http://archive.ics.uci.edu/ml. This dataset was contributed by researchers from the University of Wisconsin and contains measurements derived from digitized images of fine-needle aspirates of breast masses.
The breast cancer dataset contains 569 cancer biopsy samples, each with 32 attributes. One attribute is an ID number, another is the diagnosis (labeled "M" for malignant or "B" for benign), and 30 are numerical lab measurements.
## Step 2: Exploring and preparing the data
In step 2, I will explore the data to uncover potential relationships by applying the K-Nearest Neighbors (K-NN) algorithm. I will start by importing the CSV file named wisc_bc_data.csv and loading the Wisconsin Breast Cancer Diagnostic dataset into a data frame called “wbcd”
Using the str(wbcd) command, I can confirm that the data is structured with 569 examples and 32 features, just as I expected. 
## Step 3 Training a model on the data
I’m ready to classify unknown records using the k-NN algorithm, which doesn’t build a model during training but stores the input data. To classify test instances, I’ll use the k-NN implementation from the R "class" package. If it’s not installed, I can install it with install.packages("class") and load it with library(class) when needed.
## Step 4: Evaluating model performance 
Now I need to check how accurate my model is by comparing the predicted results (stored in wbcd_test_pred) with the actual labels (stored in wbcd_test_labels). I can do this using the CrossTable() function from the gmodels package.
## Step 5: Improving Model Performance 
Instead of using normalization, I decided to try z-score standardization because it keeps extreme values, which might help detect malignant tumors better.
I used the scale() function in R to standardize the data:
This changed all features except the diagnosis column. I checked the summary and confirmed that the mean was near 0, which means the transformation worked.
