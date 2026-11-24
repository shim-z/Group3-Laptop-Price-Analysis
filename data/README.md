# Dataset information

**Original CSV:** https://github.com/MainakRepositor/Datasets/blob/master/laptop_price.csv  
**Source accessed:** 24 November 2026  
**Original columns:** 13  
**Records:** 1,303  
**Original currency:** EUR (`Price_euros`)  
**Converted currency:** SAR (`Price_SAR`)  
**Conversion:** `Price_SAR = round(Price_euros * 4.1256, 2)`  
**Exchange-rate reference:** X-Rates, 23 November 2026: https://www.x-rates.com/historical/?amount=1&date=2026-11-23&from=EUR

The original collection period is unspecified. Converting to SAR does not imply that the prices are current Saudi retail prices. The notebook downloads the original file and saves a cleaned copy without overwriting the original source.
