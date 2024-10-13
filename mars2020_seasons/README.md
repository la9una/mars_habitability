# Mars Seasons Script

The purpose of this script is to **process and analyze data from the Mars2020 mission** by adding Martian seasons based on **solar longitude (L_s)**, a fundamental measure in Martian astronomy. Additionally, the script generates a **representative sample of data for each season**, facilitating accurate and reliable environmental analyses in line with **best statistical practices**.

## Core Procedures

### 1. Generate column "Season"

A new column named "Season" is generated using solar longitude (L_s) to determine the corresponding season:

- Spring: 0° ≤ L_s < 90°
- Summer: 90° ≤ L_s < 180°
- Autumn: 180° ≤ L_s < 270°
- Winter: 270° ≤ L_s < 360°

### 2. **Representative Sampling by Season**

The script performs **stratified random sampling** by season using the following criteria:

- Selects **30 samples** or **10% of the available data** for each season, whichever is greater.
- If a season has fewer than 30 records, it selects **all available data**.
- The sampling is **random and without replacement** to ensure diversity and minimize bias.

### 3. **Data Export**

- A `generated_mars2020_time_table_with_seasons.csv` file is generated, containing the data with seasons added.
- A `generated_mars2020_time_table_sample.csv` file is generated, containing a representative sample of the data.


## Usage
This script is designed to run in **[Jupyter Notebook](https://jupyter.org/install)**, an interactive environment for writing and executing code along with explanatory text. It supports various programming languages, with Python being the most common. This script can be executed both **locally using Jupyter Notebook** and **online through [Google Colab](https://colab.google/)** and was tested on Ubuntu 24.04 LTS

1. **Clone the Repository**: 
```bash
git clone https://github.com/la9una/mars_habitability.git
```

2. **Make the Script Executable**:

 ```bash
 cd mars_habitability/mars2020_seasons
 ```

3. **Run the Script**:

Open with [Jupyter Notebook](https://jupyter.org) or [Visual Studio Code](https://code.visualstudio.com/) locally, or with [Google Colab](https://colab.google/) online.

## References

- Perseverance (Mars 2020) Analyst's Notebook. (n.d.). Mission Timeline. Retrieved from [https://an.rsl.wustl.edu/m20/AN/missTimes.aspx](https://an.rsl.wustl.edu/)

© 2024 Raúl Jesús López - This work is licensed under a Creative Commons Attribution 4.0 International License. [Link to the license](https://creativecommons.org/licenses/by/4.0/)
