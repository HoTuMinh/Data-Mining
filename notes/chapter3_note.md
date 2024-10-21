# CHAPTER 3. DATA PREPROCESSING

### Overview 

- **Data preprocessing** helps to improve the quality and efficiency of data for analysis.
- It involves cleaning, integrating, reducing, and transforming the data.

#### Why Preprocess Data?
- Data needs to be of high quality for accurate analysis. Quality includes:
  - **Accuracy**: Correctness of data.
  - **Completeness**: Data should be whole, without missing parts.
  - **Consistency**: Data should be the same across different datasets.
  - **Timeliness**: Data should be updated and available on time.
  - **Believability**: Data must be trusted.
  - **Interpretability**: Data should be easy to understand.

#### Common Data Problems
- Real-world data is often:
  - **Incomplete**: Missing values or incomplete attributes.
  - **Inaccurate**: Contains errors or noise.
  - **Inconsistent**: Mismatched data between different databases.

#### Major Tasks in Data Preprocessing
  
  - **Data Cleaning**: Fixing errors, removing duplicates, and filling in missing data.
  - **Data Integration**: Merging data from multiple sources.
  - **Data Reduction**: Reducing the data size while keeping its essential features (e.g., removing irrelevant attributes or applying dimensionality reduction).
  - **Data Transformation**: Converting data into a format suitable for analysis (e.g., normalizing or aggregating data).

### Data Cleaning 

_Real-world data often contains errors, missing values, and inconsistencies. **Data cleaning** is the process of fixing these issues, allowing the data to be useful in analysis.
_

#### Missing Values

_What are missing values?_
  - **Missing values** occur when certain fields in your data (like customer income) are not filled in.
  - It's common in datasets, and there are different ways to handle this problem.

#### Methods for handling missing values:
1. **Ignore the tuple (row)**
   - Skip rows that have missing values.
   - Works when the amount of missing data is small.
   - May not work if a large portion of the dataset has missing information.

2. **Fill in missing values manually**
   - Manually input the missing values.
   - Time-consuming and inefficient for large datasets.
   - Works well for small datasets or critical missing values.

3. **Use a global constant**
   - Replace missing values with a constant like "Unknown" or a specific number.
   - Example: For missing income, you could use "-999" or "N/A".
   - This doesn’t provide meaningful information but flags the missing data clearly.

4. **Use the mean/median of the attribute**
   - For numerical data, replace missing values with the mean or median of that column.
   - Example: If some income data is missing, calculate the average income and fill in the gaps.
   - Works well when data is evenly distributed.

5. **Use the most probable value (Prediction)**
   - Predict the missing value using models like regression or decision trees.
   - Takes into account other information in the dataset to make an informed guess.
   - Requires more advanced techniques but is more accurate.

#### Noisy Data

_What is noisy data?_
  - **Noisy data** contains errors or random variations.
  - It can lead to incorrect conclusions or poor model performance.

#### Methods for handling noisy data:
1. **Binning**
   - Group data into "bins" or ranges and replace each data point with the average or boundary value of its bin.
   - Types of binning:
     - **Equal-frequency bins**: Divide data into bins with an equal number of data points.
     - **Smoothing by bin means**: Replace data points with the average value of the bin.
     - **Smoothing by bin boundaries**: Replace data points with the nearest boundary value of the bin.
   - Example: For prices [4, 8, 15, 21, 24, 25, 28, 34], you can divide them into bins and replace the values with bin averages or boundaries.

2. **Regression**
   - Use regression models to smooth data by fitting it to a function.
   - **Linear regression**: Finds the best-fitting line to describe the data.
   - **Multiple linear regression**: Uses more than one variable to smooth or predict missing data.

3. **Outlier analysis**
   - Detects and removes outliers, which are data points that are far from the rest of the data.
   - Example: A price of $200 when most prices are between $10 and $50 is an outlier and might be removed or flagged.

#### Data Cleaning as a Process

_What is the process of data cleaning?_
  - It involves **discrepancy detection** and **data transformation**.
  - Data may have errors due to:
    - Poorly designed data entry forms.
    - Human errors during data entry.
    - Deliberate errors or outdated information.

#### Steps in the data cleaning process:
1. **Discrepancy Detection**
   - Look for errors or inconsistencies in the data.
   - Example: Two different formats for dates, like "2010/12/25" and "25/12/2010", which need to be standardized.

2. **Field Overloading**
   - When a single field is used for more than one purpose, leading to confusion.
   - Example: A field meant for "age" might also store an unrelated "flag" (yes/no), causing errors.

3. **Unique and Consecutive Rules**
   - Unique rules ensure that each value is distinct (e.g., customer IDs).
   - Consecutive rules ensure that values fall within a specific range (e.g., ages between 0 and 100).

#### Tools for Discrepancy Detection and Transformation:
  - **Data scrubbing tools**: Automatically detect and fix errors like misspellings or wrong formats.
  - **Data auditing tools**: Analyze the data to find issues and provide suggestions for corrections.

#### Handling Discrepancies:
  - Once discrepancies are found, the data needs to be **transformed** (corrected).
  - This may involve:
    - Replacing wrong values with correct ones.
    - Transforming data to a consistent format (e.g., converting all dates to "YYYY-MM-DD").

#### Modern Approaches to Data Cleaning

- Interactive tools for data cleaning:
  - **Interactive tools** allow users to see changes step by step and fix errors in real-time.
  - Example: If a transformation introduces an error, the user can immediately correct it before proceeding.

- Automated error detection:
  - Automated tools check the latest data and fix common errors, making the process faster and more reliable.

### Data Integration 

### Data Reduction 

### Data Transformation and Data Discretization 

### Summary 

### Exercises

### Questions 

### Linkie
