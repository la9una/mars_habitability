## Mars 2020 MEDA Data Processing Script

This script is designed to process environmental data from the Mars 2020 Perseverance Rover's MEDA (Mars Environmental Dynamics Analyzer) instrument package. The script processes various physical variables, such as **Air Temperature (ATS)**, **Radiation and Dust Sensor (RDS)**, **Pressure Sensor (PS)**, **Relative Humidity Sensor (RHS)**, and **Thermal Infrared Sensor (TIRS)**. It organizes these data points by Martian sols and calculates average values for each Martian season.

### Script Functionality

1. **Load Time and Season Data**:
   - The script loads a CSV file (`mars2020_time_table_sorted_by_season_and_sol.csv`) containing time data for the Mars 2020 mission, with information on Martian sols and associated Martian seasons. This file helps to organize each sol's data according to its season.
2. **Process Physical Variables**:
   - The script contains predefined folders for each physical variable (ATS, RDS, PS, RHS, and TIRS). Each folder holds CSV files where each file represents data collected from a specific sol.
   - Users can select a specific variable from an interactive menu. The script then reads all the CSV files for the chosen variable, processes them, and calculates average values for each sol.
3. **Calculate Seasonal Averages**:
   - After calculating the average values for each sol, the script merges this data with the seasonal information from the time data file.
   - It then computes the average of the chosen variable for each Martian season (Spring, Summer, Autumn, Winter).
4. **Save and Download Results**:
   - The seasonal averages are saved in a new CSV file (e.g., `average_ATS_per_season.csv`), which provides the seasonal breakdown of average values for the chosen variable.
   - If the script is run in Google Colab, the resulting CSV file is automatically downloaded to the user’s local machine. In a local environment, the file is saved in the current directory.

### Usage

The script is adapted to run in both Jupyter Notebook and Google Colab environments. It leverages `ipywidgets` for interactive menus, allowing users to easily select a variable for analysis.

### Requirements

- **Python 3.x**
- **Pandas** for data manipulation.
- **Ipywidgets** for creating interactive menus (`pip install ipywidgets`).
- **Google Colab**: If running on Google Colab, the script uses the `files` module to enable automatic file downloads.

### Example Use Case

1. Run the script in a Jupyter Notebook or Google Colab environment.
2. Select a variable from the interactive dropdown menu.
3. The script processes the selected variable's data, calculates seasonal averages, displays the result in the notebook, and saves the output to a CSV file.
4. In Google Colab, the CSV file is automatically downloaded after processing.

This script provides a streamlined way to analyze and organize environmental data from the Mars 2020 MEDA package by season, allowing researchers to easily interpret seasonal trends in temperature, radiation, humidity, pressure, and thermal infrared measurements on Mars.