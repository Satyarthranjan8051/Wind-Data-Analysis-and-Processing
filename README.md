# Wind Data Processing Project

This project processes meteorological wind data by converting units, resampling data, and identifying high wind speed instances. The final output provides a summary of maximum wind speeds at specific intervals.

## Steps Performed

1. **Data Loading and Conversion**
   - Loaded wind data from a CSV file.
   - Converted wind speed values from knots (kt) to kilometers per hour (km/h).
   - Rounded converted values to two decimal places.

2. **Data Cleaning and Preparation**
   - Selected relevant columns: `DATE`, `TIME(UTC)`, `WIND_MAX/GUST_10m(km/hr)`, `WIND_SPEED_10m(km/hr)`.
   - Merged `DATE` and `TIME(UTC)` into a single `TIME` column.
   - Set `TIME` as the DataFrame index.
   - Removed redundant `DATE` and `TIME(UTC)` columns.

3. **Resampling and Analysis**
   - Resampled data at 3-hour intervals to find maximum wind speeds.
   - Created a binary `max_speed` column to flag instances where wind speed exceeded 50 km/h.
   - Extracted and formatted `Month` and `Time` information for easier analysis.

4. **Data Aggregation**
   - Grouped data by `Month` and `Time` to sum high wind speed occurrences.

5. **Final Output**
   - Generated a summary DataFrame showing the number of high wind speed events for each month and time interval.
   - Saved the processed data to a new CSV file (`Final_p_Met_data_1.csv`).

## Dependencies
- Python libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `datetime`

## File Structure
- `Met_data_1.csv`: Original dataset
- `updated_Met_data_1.csv`: Intermediate processed dataset
- `Final_p_Met_data_1.csv`: Final output dataset

## Usage
1. Ensure all dependencies are installed.
2. Run the provided Python script to process the data.
3. Review the output CSV file for summarized wind speed information.

## Author
Satyarth Ranjan
