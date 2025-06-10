# Electrical Meter Data Analysis

This project was developed during a **1-month internship at Radius Synergies**. It processes electrical meter data to detect anomalies such as power outages, voltage fluctuations, surge currents, and power factor inconsistencies. The script also cleans and visualizes the data.

📈 **Analyzed 260,452 entries of electrical grid data with 7.9 seconds average runtime**  
📄 [Internship Report]([https://www.canva.com/design/DAGH_sKZJQs/k-7aoyrqc8QYSULhxln8gA/view?utm_content=DAGH_sKZJQs&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=ha469c26268])

## Features

✅ Reads and processes electrical meter data from a CSV file  
✅ Detects **power outages**  
✅ Identifies **over-voltage, under-voltage, and high surge currents**  
✅ Flags **abnormal power consumption** and **frequency deviations**  
✅ Checks **power factor efficiency** and ensures consistency  
✅ Handles **negative and null values** using interpolation  
✅ Generates **various graphs** for data visualization  

## How It Works  

The script will:  
- Analyze the dataset and print warnings if any anomalies are found.  
- Clean and save the processed data as `Meter_Data.csv`.  
- Generate graphical representations of voltage, current, power consumption, and power factor.  

## Code Overview  

### Data Preprocessing  
- Reads `electrical_meter_data.csv`  
- Identifies numeric columns for analysis  

### Anomaly Detection Functions  

#### 1. Power Outage Detection  
- Checks if all voltage and current values are `0`  

#### 2. Abnormal Value Detection  
- Detects over-voltage (`>250V`), under-voltage (`<209V`), and surge currents (`>16A`)  
- Flags unusually high power consumption  

#### 3. Power Factor Efficiency  
- Identifies poor/bad power factor (`<0.95`)  
- Validates power factor calculations for consistency  

#### 4. Handling Negative and Null Values  
- Converts errors to NaN and interpolates missing values  

## Data Visualization  

The processed data (`Meter_Data.csv`) is used to plot:  
- **Voltage Over Time** (Phases R, Y, B)  
- **Current Over Time**  
- **Instantaneous Power Over Time**  
- **Real & Apparent Power Over Time**  
- **Power Factor Trend**  

## Output Messages  

- `INFO:` messages indicate successful execution  
- `WARNING:` messages flag anomalies in the dataset  

## Future Improvements  

- Implement **machine learning** for predictive anomaly detection  
- Add **real-time streaming data analysis**  

## Author  

👤 **Prarthna Puhan**  
Developed during an internship at **Radius Synergies International Pvt Ltd, Sector-63, Noida, Uttar Pradesh**.
