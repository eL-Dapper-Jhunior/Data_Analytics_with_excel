# Data Cleaning, Analysis, and Visualization Using Excel

This project demonstrates how to clean, analyze, and visualize data using Microsoft Excel. Through this project, I learned the following skills:

1. **Data Cleaning**:
   - Formatting columns and rows.
   - Checking for missing values.
   - Checking for duplicates.
   - Checking for and removing white spaces.

2. **Basic Excel Functions**:
   - Examples of commonly used functions like `SUM`, `AVERAGE`, `COUNT`, `IF`, `TRIM`, `CONCATENATE`, and more.

3. **Advanced Excel Functions**:
   - Conditional formatting.
   - Nested IFs.
   - RIGHT and LEFT functions.
   - VLOOKUP.
   - INDEX and MATCH.

4. **Data Analysis**:
   - Creating pivot tables.
   - Visualizing data using charts.

5. **Dashboards**:
   - Creating interactive dashboards.

---

## Table of Contents
1. [Data Cleaning](#data-cleaning)
   - [Formatting Columns and Rows](#formatting-columns-and-rows)
   - [Checking for Missing Values](#checking-for-missing-values)
   - [Checking for Duplicates](#checking-for-duplicates)
   - [Checking for White Spaces](#checking-for-white-spaces)
2. [Basic Excel Functions](#basic-excel-functions)
   - [SUM](#sum)
   - [AVERAGE](#average)
   - [COUNT](#count)
   - [IF](#if)
   - [TRIM](#trim)
   - [CONCATENATE](#concatenate)
3. [Advanced Excel Functions](#advanced-excel-functions)
   - [Conditional Formatting](#conditional-formatting)
   - [Nested IFs](#nested-ifs)
   - [RIGHT and LEFT Functions](#right-and-left-functions)
   - [VLOOKUP](#vlookup)
   - [INDEX and MATCH](#index-and-match)
4. [Data Analysis](#data-analysis)
   - [Pivot Tables](#pivot-tables)
   - [Visualizations](#visualizations)
5. [Dashboards](#dashboards)
6. [Conclusion](#conclusion)

---

## Data Cleaning

### Formatting Columns and Rows
Formatting ensures that the data is visually consistent and easy to read. Here’s how I formatted columns and rows:
- **Adjusting Column Width**: Double-clicked the right edge of the column header to auto-fit the content.
- **Formatting Numbers**: Selected the cells and used the **Number Format** options (e.g., Currency, Percentage, Date).
- **Applying Borders**: Added borders to cells using the **Borders** tool under the **Home** tab.
- **Changing Font and Alignment**: Adjusted font size, style, and alignment for better readability.

---

### Checking for Missing Values
Missing values can skew analysis, so it’s important to identify and handle them. Here’s how I checked for missing values:
1. **Using Conditional Formatting**:
   - Selected the dataset.
   - Went to **Home > Conditional Formatting > Highlight Cell Rules > Blanks**.
   - All blank cells were highlighted, making them easy to identify.

2. **Using the `IF` Function**:
   - Created a new column to flag missing values:
     ```excel
     =IF(ISBLANK(A2), "Missing", "OK")
     ```

3. **Filling Missing Values**:
   - Replaced missing values with "N/A" or the average of the column:
     ```excel
     =IF(ISBLANK(A2), "N/A", A2)
     ```

---

### Checking for Duplicates
Duplicates can lead to inaccurate analysis. Here’s how I checked for and removed duplicates:
1. **Using the `Remove Duplicates` Tool**:
   - Selected the dataset.
   - Went to **Data > Remove Duplicates**.
   - Chose the columns to check for duplicates and clicked **OK**.

2. **Using the `COUNTIF` Function**:
   - Created a new column to identify duplicates:
     ```excel
     =COUNTIF(A:A, A2)
     ```
   - Filtered the dataset to show rows where the count was greater than 1.

---

### Checking for White Spaces
Extra white spaces can cause issues in data analysis. Here’s how I checked for and removed them:
1. **Using the `TRIM` Function**:
   - Created a new column to remove leading, trailing, and extra spaces:
     ```excel
     =TRIM(A2)
     ```

2. **Using Find and Replace**:
   - Pressed `Ctrl + H` to open the **Find and Replace** dialog.
   - Typed a single space in the **Find** field and left the **Replace** field empty.
   - Clicked **Replace All** to remove all spaces.

---

## Basic Excel Functions

### SUM
The `SUM` function adds up a range of numbers. Here’s how I used it:
```excel
=SUM(A2:A100)  // Adds all values in cells A2 to A100

### AVERAGE
The `AVERAGE` function calculates the average of a range of numbers. Here’s how I used it:

=AVERAGE(B2:B100)  // Calculates the average of values in cells B2 to B100


### COUNT
The `COUNT` function counts the number of cells with numeric values. Here’s how I used it:

=COUNT(C2:C100)  // Counts the number of numeric values in cells C2 to C100


### IF
The `IF` function performs a logical test and returns one value if true and another if false. Here’s how I used it:

=IF(D2 > 50, "High", "Low")  // Returns "High" if the value in D2 is greater than 50, otherwise "Low"


### TRIM
The `TRIM` function removes extra spaces from text. Here’s how I used it:

=TRIM(E2)  // Removes leading, trailing, and extra spaces from the text in E2


### ONCATENATE
The `CONCATENATE` function combines text from multiple cells. Here’s how I used it:

=CONCATENATE(F2, " ", G2)  // Combines the text in F2 and G2 with a space in between


## Advanced Excel Functions
Conditional Formatting
Conditional formatting helps visualize data by applying formatting rules. Here’s how I used it:

Highlighting Values Above a Threshold:

Selected the data range.

Went to Home > Conditional Formatting > Highlight Cell Rules > Greater Than.

Entered the threshold value (e.g., 100) and chose a formatting style.

Color Scales:

Applied a color scale to show data distribution:

Selected the data range.

Went to Home > Conditional Formatting > Color Scales.

Nested IFs
Nested IFs allow for multiple conditions. Here’s how I used them:


=IF(A2 > 90, "A", IF(A2 > 80, "B", IF(A2 > 70, "C", "D")))  // Assigns grades based on scores


RIGHT and LEFT Functions
The RIGHT and LEFT functions extract substrings from text. Here’s how I used them:

=LEFT(A2, 5)  // Extracts the first 5 characters from the text in A2
=RIGHT(A2, 3)  // Extracts the last 3 characters from the text in A2


VLOOKUP
The VLOOKUP function searches for a value in a table and returns a corresponding value. Here’s how I used it:

=VLOOKUP(A2, PriceTable, 2, FALSE)  // Finds the price of a product based on its ID

INDEX and MATCH
The INDEX and MATCH functions are a more flexible alternative to VLOOKUP. Here’s how I used them:

(PriceColumn, MATCH(A2, IDColumn, 0))  // Finds the price of a product based on its ID


# Data Analysis
## Pivot Tables
Pivot tables summarize and analyze large datasets. Here’s how I created one:

Selected the dataset.

Went to Insert > Pivot Table.

Chose the rows, columns, and values to summarize (e.g., total sales by region).

Visualizations
Visualizations help present data insights. Here’s how I created charts:

Bar Chart:

Selected the data.

Went to Insert > Bar Chart.

Line Chart:

Selected the data.

Went to Insert > Line Chart.

Pie Chart:

Selected the data.

Went to Insert > Pie Chart.

Dashboards
Dashboards provide an interactive way to visualize data. Here’s how I created one:

Inserted Charts and Pivot Tables:

Added charts and pivot tables to a new sheet.

Added Slicers:

Selected a pivot table.

Went to Insert > Slicer to add interactive filters.

Formatted the Dashboard:

Arranged charts and tables for a clean layout.

Added titles and labels for clarity.

### Conclusion
Through this project, I learned how to clean, analyze, and visualize data using Excel. These skills are essential for working with data and making informed decisions.