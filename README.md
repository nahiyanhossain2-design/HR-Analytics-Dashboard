# HR Analytics Dashboard 📊

## Project Overview
This project focuses on analyzing HR data to uncover insights regarding employee attrition and performance.

## Data Source
- **Source:** [Mock HR Data]
  
## Technical Documentation
### 1. Power Query (ETL Process)
During the data transformation phase, I performed the following:
- Cleaned null values in the 'Termination Date' column.
- Changed data types for date consistency.

### 2. Data Modeling
I implemented a **Star Schema** to optimize performance.
- **Fact Table:** `FactPerformanceRating`
- **Dimension Tables:** `DimEmployee`, `DimDate`, `DimEducationLevel`, 'DimRatingLevel', 'DimSatisfiedLevel'

![Data Model](./data_model.png)

### 3. DAX Measures (Samples)
To provide deep insights, I wrote several custom DAX measures:

**Attrition Rate:**
```dax
% Attrition Rate = DIVIDE([InactiveEmployees], [TotalEmployees])

**Job Satisfaction:**
```dax
JobSatisfaction = MAX(FactPerformanceRating[JobSatisfaction])
