BIS_CBPR
---

- Retrieves policy rates from central banks using the BIS API.  
- If no country/ is specified, outputs data as a dictionary by country.
- Else, returns the current rate as a float.

 - Guide is available <a href="https://github.com/ndjoli-nathan/BIS_CBPR/blob/main/Guide.ipynb">here.</a>

---
 
Requirements: `requests` , `datetime`, `pandas`.

Install using: `pip install BIS-CBPR`

---
Example: 

```python
from MyPackages import BIS_CBPR

CentralBankPolicyRates("United States")
# >>> 0.04375  # As of 2025/02/01

CentralBankPolicyRates()
# >>> {'United States': {'Frequency': 'Daily',
#   'Country': 'United States',
#   'Country Code': 'US',
#   'Title': 'Central bank policy rates, United States',
#   'Unit': 'Per cent per year',
#   'Start Date': '1954-07-01',
#   'end_date': '2025-01-28',
#   'End Value': '4.375',
#   'End Value Status': 'Normal value',
#   'Last Updated': '2025-01-29T06:51:38.742Z'},
#  'United Kingdom': {'Frequency': 'Daily',
#   'Country': 'United Kingdom',
#   'Country Code': 'GB',
#   'Title': 'Central bank policy rates, United Kingdom',
#   'Unit': 'Per cent per year',
#   'Start Date': '1946-01-01',
#   'end_date': '2025-01-27',
#   'End Value': '4.75',
#   'End Value Status': 'Normal value',
#   'Last Updated': '2025-01-29T06:51:38.742Z'},
#  'Türkiye': {'Frequency': 'Daily',
#   'Country': 'Türkiye',
#   'Country Code': 'TR',
#   'Title': 'Central bank policy rates, Türkiye',
#   'Unit': 'Per cent per year',
#   ...}}
