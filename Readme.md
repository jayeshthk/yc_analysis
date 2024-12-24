# Company Acquisition and Performance Analysis

This Jupyter Notebook analyzes company data to identify trends in acquisitions and overall performance across different industries. It leverages several Python libraries for data manipulation, visualization, and statistical analysis.

## Data

The analysis relies on two CSV files:

- `companies.csv`: Contains information about individual companies, including status (e.g., acquired, operating), descriptions, and potentially an identifier linking to industry data.
- `industries.csv`: Contains information about different industries.

**Important Note:** The code assumes a method for merging these datasets, which is marked as pseudo-code and needs to be adapted to the actual column names and relationship in your files. Currently, the code merges based on the 'id' column, which may need adjustment.

## Analysis

1. **Acquisition Rates by Industry:**

   - Calculates the acquisition rate for each industry.
   - Visualizes the acquisition rates using a bar plot, allowing for easy comparison of industries' susceptibility to acquisitions.

2. **AI Company Acquisition Rates:**

   - Identifies companies with mentions of "AI" in their descriptions.
   - Compares acquisition rates between AI and non-AI companies across different industries.
   - Uses bar plots for clear visualization of these comparisons.
   - Includes additional bar plots showing raw counts of AI vs. Non-AI companies by industry for context.

3. **Success and Failure Rates:**

   - Defines "success" and "failure" based on company status.
   - Calculates success and failure rates for each industry.
   - Visualizes these rates using bar plots with superimposed success and failure rates for easy comparison.
   - Shows raw counts of successful vs failed companies by industry in an additional bar plot.
   - Includes radar charts for comparing success/failure rates across the top 6 industries (by company count) for enhanced visualization.

4. **Industry Growth Over Time:**
   - Extracts the year information from the 'batch' column (assuming a specific format).
   - Calculates and visualizes the growth (number of new companies) in each industry over the years using a line chart. The industries are sorted by total count for clarity.

## Libraries Used

- `pandas`: Data manipulation and analysis.
- `numpy`: Numerical computing.
- `matplotlib` and `seaborn`: Data visualization.
- `plotly`: Interactive visualizations (though not extensively used in the current code).
- `scipy`: Scientific computing.
- `scikit-learn`: Machine learning (used in the acquisition rate prediction part).

## Setup

1. **Install Libraries:** Run the pip install commands in the notebook to ensure all necessary libraries are installed.
2. **Data Files:** Place the `companies.csv` and `industries.csv` files in a subdirectory named `data` within the notebook directory or adjust the file paths in the code.

## Running the Notebook

Execute the code cells sequentially in the Jupyter Notebook. The analysis results (visualizations and calculated statistics) will be displayed directly within the notebook.

## Future Improvements

- **Robust Data Linking:** Implement a robust method for linking the `companies` and `industries` datasets using the most reliable identifiers.
- **Explore Additional Features:** Investigate other features in the datasets that may contribute to acquisition or success prediction and include them in the analysis.
- **Advanced Modeling:** Develop machine learning models (e.g., regression, classification) to predict acquisition likelihood or company success.
- **Interactive Visualizations:** Integrate more interactive Plotly visualizations for a dynamic exploration of the data.
