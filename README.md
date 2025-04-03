![Static Badge](https://img.shields.io/badge/Version-2.1-blue)

# SLS Data Processing Script

## Overview
This script is designed to process raw SLS `.txt` files at TNO EMSA, combine them into an Excel file with multiple sheets, and generate adjustable scatter plots saved in a separate Excel file. It automates the workflow for handling and visualizing SLS data.

## Features
1. **Combine Raw Data**: Reads `.txt` files from a specified folder, processes the data, and combines it into a single Excel file with each file's data in a separate sheet.
2. **Generate Plots**: Creates scatter plots with straight lines for each sheet and saves them in a new Excel file with adjustable charts.
3. **Customizable Output**: Allows users to specify folder names and output file names.

## Prerequisites
- Python 3.x
- Required Python libraries:
  - `pandas`
  - `matplotlib`
  - `openpyxl`
  - `xlsxwriter`
  - `os`
  - `io`

Install the required libraries using:
```bash
pip install pandas matplotlib openpyxl xlsxwriter
```
or using requirements.txt file from the script files:
```bash
pip install -r requirements.txt
```
Note: Use "!pip install" in Visual Studio Code.

## Usage

### Step 1: Prepare the Raw Data
1. Place the script in the main folder containing a subfolder with the raw `.txt` files.
2. Update the `raw_directory` variable in the script with the name of the subfolder containing the raw data.
3. Specify the output file name for the combined data in the `combined_sheets_filename` variable.

### Step 2: Loading Libraries
Run the first cell of the script to import needed libraries.

### Step 3: Combine Raw Data
Run the second cell to process the `.txt` files and generate an Excel file with combined data:
The combined Excel file will be saved in the main folder.

### Step 4: Generate Plots
Run the last cell. The script will automatically create scatter plots for each sheet in the combined Excel file and save them in a new Excel file in an `Output` folder.

## Output
1. **Combined Data File**: An Excel file (`combined sheets.xlsx`) containing all processed `.txt` files as separate sheets.
2. **Plots File**: An Excel file (`output.xlsx`) with scatter plots for each sheet, saved in the `Output` folder.

## Notes
- Ensure the raw `.txt` files follow the expected format as described in the script comments.
- Sheet names in Excel are truncated to 31 characters to avoid naming conflicts.
- The x-axis of the plots is logarithmic, and two y-axes are used for different data series.
- The raw files include meta data and is selectively and manually included in the output.

## Author
- **Name**: Zaf Khalil
- **Date**: 28-June-2024

## License
This script is provided as-is without any warranty. Use it at your own risk.
