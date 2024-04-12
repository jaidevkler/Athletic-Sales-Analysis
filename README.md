# Athletic Sales Analysis
Module 5 Challenge analyzes sales data to gain insights into which cities in the U.S. have sold the most athletic wear over two years. The analysis determines which retailers had the greatest total sales for athletic wear, and which retailers sold the most women's athletic footwear. Finally, the analysis determines which day and week had the highest sales for women's athletic footwear.

## Code Source
The code location is: [Click Here to view](https://github.com/jaidevkler/athletic_sales_analysis)

## Files
* athletic_sales_analysis_starter_code.ipynb [Click here to view](https://github.com/jaidevkler/athletic_sales_analysis/blob/main/athletic_sales_analysis_starter_code.ipynb)<br />
* README.md [Click here to view](https://github.com/jaidevkler/athletic_sales_analysis/blob/main/README.md)<br />
* athletic_sales_2020.csv [Click here to view](https://github.com/jaidevkler/athletic_sales_analysis/blob/main/Resources/athletic_sales_2020.csv)<br />
* athletic_sales_2021.csv [Click here to view](https://github.com/jaidevkler/athletic_sales_analysis/blob/main/Resources/athletic_sales_2021.csv)<br />

## How to run the program
Dowload the files and then use jupyter notebook or jupyter lab and open the athletic_sales_analysis_starter_code.ipynb file. Please make sure that that two csv files are saved in a folder named Resources.

## Program
### 1. Combine and Clean the Data
* Read the CSV files into DataFrames using pd.read_csv() function
* Display the DataFrames
* Use dtypes to check the data types of all the data in two DataFrames
* Combine the two DataFrames using the concat() fuction to join them
* Check if there is any null data in the new DataFrame
* Covert the invoice_date column to a datatime data type by using the to_datetime() function
* Check the data type of the DataFrame to confirm the changes

### 2. Determine which Region Sold the Most Products
* Using the groupby() and pivot_table() functions the program sets the index of the DataFrame to region, state and city and the column is set to units_sold. The total is calculated by using the sum function.
* The column is then renamed to Total_Products_Sold
* The DataFrame is then sorted by 'Total_Products_Sold in a descending order to show the results.

### 3. Determine which Region had the Most Sales
* Using the groupby() and pivot_table() functions the program sets the index of the DataFrame to region, state and city and the column is set to total_sales. The total is calculated by using the sum function.
* The column is then renamed to Total Sales
* The DataFrame is then sorted by Total Sales in a descending order to show the results.

### 4. Determine which Retailer had the Most Sales
* Using the groupby() and pivot_table() functions the program sets the index of the DataFrame to retailer, region, state and city and the column is set to total_sales. The total is calculated by using the sum function.
* The column is then renamed to Total Sales
* The DataFrame is then sorted by Total Sales in a descending order to show the results.

### 5. Determine which Retailer Sold the Most Women's Athletic Footwear
* A new DataFrame is created by filtering out the sales data for Women's Athletic Footwear
* Using the groupby() and pivot_table() functions the program sets the index of the DataFrame to retailer, region, state and city and the column is set to units_sold. The total is calculated by using the sum function.
* The column is then renamed to Womens_Footwear_Units_Sold.
* The DataFrame is then sorted by Womens_Footwear_Units_Sold in a descending order to show the results.

### 5. Determine the Day with the Most Women's Athletic Footwear Sales
* Using the pivot_table function the program sets the index to invoice_date and the column to total_sales. The total is calculated by using the sum function.
* The column is then renamed to Total Sales
* The DataFrame is then sorted by Total Sales in a descending order to show the results.
* The DataFrame is then resampled into daily bins using the resample() function with the 'D' argument. 
* The total is calculated using the sum function on the new DataFrame.
* The DataFrame is then sorted as per Total Sales om a descending order to show the results.

### 6. Determine the Week with the Most Women's Atheletic Footwear Sales
* The DataFrame is then resampled into weekly bins using the resample() function with the 'W' argument. 
* The total is calculated using the sum function on the new DataFrame.
* The DataFrame is then sorted as per Total Sales om a descending order to show the results.

## Conclusion
The assignment shows how different function (concat, groupby, pivot, resample) can be used to combine and sort data to analysis the data for better decision making.
