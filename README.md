## Exploratory Analysis

### **Steps Taken and Findings**
*1. Identify data types*
  - Columns 1, 4, 5, 6 and 7 are floats while Columns 2 and 3 and integers
  
*2. Size of Dataset*
  - Dataset is very small with only 818 examples and 7 variables
  
*3. Check for missing values*

  - There are no missing values in Columns 1, 2, 3 and 4
  
  - 1.47% of Column 5 is missing
  
  - 74.8% of Columns 6 and 7 is missing
  
*4. Column Analysis*
  - There are 230 unique values in Column 1, 3 in Column 2, 12 in Column 3, 36 in Column 4 and 46 in Column 5. There are only 4 unique values for Columns 6 and 7       with the majority of their values missing.
  - I observe that there are many unique values in Column 1, this could be a representation of some sort of identification like USER ID, SHOP ID, etc. 
  - Column 2 looks to be categorical in the form of discrete numerical values since its range is in [0, 1, 2]. 
  - Column 3 seems to be an ordinal variable since it has range [0,1,...,11]
  - I evaluate Columns 4 and 5 to be numerical variables.
  
*4. Get statistical summary for each numerical variable*
  - I only get the statistical summary for Columns 4 and 5.
  
    ![Describe plot](/images/plot1.png)
  - Mean and standard deviation for both Columns 4 and 5 are roughly the same.
  - The distribution of values for Column 5 seem to be on the larger values in the same range, as compared to Column 4. This can be shown from the 50 and 75      percentile.
    
*5. Derive correlation matrix between categorical and numerical variable*
  ![Corr plot](/images/plot1.png)
  - From this correlation matrix plot, we see a correlation value of:
    -0.547 between col2 and col4
    -0.596 between col2 and col5
    -0.667 between col4 and col5
  - I am going to start exploring the relationship between col2 and col4, col2 and col5 and col4 and col5

*6. Further explore data pattern behind each correlation*
  ![Count plot](/images/plot1.png)
  - From the pivot table above, I note that there 12 unique col1 values where col1= -1, 206 for 0 and 12 for 1. Interestingly, we see that for col2 = -1, there are 12 unique col1 values for 600 rows which means that each of those 12 col1 values have been repeated in the dataset. It states otherwise for col2 = 0 and col2 = 1 where there are 218 unique col1 values for 218 col2 values

**Column 2 vs Column 4**

  -  I observe that range and distribution of col4 values for each value of col2 is different. This could explain the -0.56 correlation value between col2 and col4.
  - The range of values that col4 takes on is different for each of the 3 values in col2.

    - If value of col2 is 1: col4 values take on [0,1]

    - If value of col2 is 0: col4 values take on [0,1,2]

    - If value of col2 is -1: col4 values take on [0,...,43] (This resembles a bimodal distribution)



## Conclusion
