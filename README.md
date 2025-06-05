# Safety Stock Calculation

This project is a Python script that calculates the Ideal Safety Stock based on consumption data, current stock, and transfer price, using a statistical approach to estimate demand variability and lead time.

## Features

- Reads Excel files with consumption, current stock, and price data.
- Calculates average monthly consumption and estimated standard deviation.
- Automatically identifies the lead time (PDT) column.
- Calculates the Ideal Safety Stock using a 95% service level.
- Compares current safety stock with the ideal one.
- Generates an Excel file with results, formatting, and a comparison chart.
- Simple graphical interface for selecting input and output files.

## Requirements

- Python 3.x
- pandas
- openpyxl
- tkinter (included in most Python distributions)

## How to Use

1. Run the script `safety_stock.py`.
2. Select the Excel file with the input data.
3. Choose where to save the output Excel file.
4. Check the generated file containing calculation sheets and a comparison chart.

## Calculation Explanation

The Ideal Safety Stock calculation follows these steps:

- Average monthly consumption = Total consumption over 24 months / 24
- Estimated standard deviation = 20% of average monthly consumption
- Lead time converted from days to months
- Service level factor Z = 1.64 for 95%
- Safety Stock = Z × standard deviation × √(lead time in months)

---

## Author

Your Name or GitHub Username

---

## License

This project is licensed under the MIT License - see the LICENSE file for details.
