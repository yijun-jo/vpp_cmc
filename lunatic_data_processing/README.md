# Lunatic data processing
This folder contains codes to process lunatic reports. Example data is provided in folder "example_data" or "params_raw" for testing the code. An "output" folder is also available for demonstration purpose. Below is a short description of each Jupyter notebooks. Please fefer to each Jupyter notebook for more detailed instructions. 

1. lunatic_clean_data_single.ipynb <br>
Processes a single lunatic report with both "Concentration (mg/mL)" and wavelength scanning results. The code takes in one excel report at a time and generates one "concentration.csv" and one "wavelength_scan.csv" in the end. 

2. lunatic_clean_data_folder.ipynb <br>
Processes lunatic reports in a folder. The code takes in all excel reports in a designated folder and generates one "concentration.csv" and one "wavelength_scan.csv" for each report based on defined keyword (i.e. pH) in the filename. The code assumes all lunatic reports contain both "Concentration (mg/mL)" and wavelength scanning results. For this notebook, use "example_data" folder to avoid naming errors since some files in "params_raw" do not have "pH" as keywords i their file names. 

3. lunatic_a260_a280_single.ipynb <br>
Processes lunatic report with wavelength scanning results. The code takes in one excel report at a time, extract data from A260 and A280 and generates one "a260_a280.csv" in the end. 

4. lunatic_params.ipynb <br>
Processes lunatic report with "Concentration (mg/mL)" results. The code takes in one lunatic report at a time and but can handle results from multiple plates. One params.txt file for each plate will be generated, and if the report contains results from multiple "plates", a plate number will be used as distinct prefix. The  params.txt files can then be read by TECAN Fluent instrument to mass adjust sample concentrations. 
