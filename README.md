safety_stock_project/
├── safety_stock.py
├── README.md
├── LICENSE
└── .gitignore

# safety_stock.py (o código principal)
# O conteúdo completo do seu código Python será salvo aqui.

# README.md
# Safety Stock Calculation

This project is a Python script that calculates Ideal Safety Stock based on consumption data, current stock, and transfer price, using a statistical approach to estimate demand variability and lead time.

## Features

- Reads Excel files with consumption, stock, and pricing data
- Calculates average monthly consumption and estimated standard deviation
- Automatically identifies lead time (PDT) column
- Calculates Ideal Safety Stock using a 95% service level
- Compares actual vs. ideal safety stock
- Generates Excel output with results, formatting, and comparison chart
- Simple graphical interface to select input/output files

## Requirements

- Python 3.x
- pandas
- openpyxl
- tkinter (usually included with Python)

## How to Use

1. Run the `safety_stock.py` script
2. Select the input Excel file
3. Choose where to save the result Excel file
4. Check the generated file containing the calculation and chart sheets

## Calculation Explanation

- Monthly average consumption = Total 24-month consumption / 24
- Estimated standard deviation = 20% of average monthly consumption
- Lead time converted from days to months
- Service level Z factor = 1.64 (for 95%)
- Safety Stock = Z × standard deviation × √(lead time in months)

---

## Author

[Your Name or GitHub Username]

---

## License

This project is licensed under the MIT License - see the LICENSE file for details.

# LICENSE (MIT License)

MIT License

Copyright (c) 2025 [Your Name or GitHub Username]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights 
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell 
copies of the Software, and to permit persons to whom the Software is 
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in 
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR 
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, 
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE 
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER 
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, 
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN 
THE SOFTWARE.

# .gitignore
__pycache__/
*.pyc
*.pyo
*.pyd
.env
*.env
*.sqlite3
.DS_Store
*.xls
*.xlsx
*.xlsm
.idea/
.vscode/
*.log
