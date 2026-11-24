# Laptop Price Analysis

**2323 CIS — Introduction to Data Science**  
**King Khalid University — Group 3**

## Research question
How do listed laptop prices differ across brands and RAM categories?

## Dataset and currency
The analysis uses [MainakRepositor / Datasets / laptop_price.csv](https://github.com/MainakRepositor/Datasets/blob/master/laptop_price.csv), accessed on 24 November 2026. The CSV has **1,303 records and 13 original columns**. The original `Price_euros` field is kept unchanged.

Prices are also shown in Saudi riyals using **1 EUR = 4.1256 SAR**, based on [X-Rates historical rates (23 November 2026)](https://www.x-rates.com/historical/?amount=1&date=2026-11-23&from=EUR). The currency conversion is `Price_SAR = round(Price_euros × 4.1256, 2)`. This is a currency conversion for analysis, **not** a claim about present-day Saudi retail prices. The source data's collection period is not specified.

## Method
The notebook loads the CSV and checks data types, missing entries, duplicate rows, and price validity. It creates numeric RAM and weight fields using regular expressions, converts prices to SAR, groups laptops by brand and RAM capacity, and produces three charts with interpretations.

## Findings
- Listed prices range from approximately **SAR 718 to SAR 25,162**.
- The **median** price is about **SAR 4,031**; the **mean** is about **SAR 4,636**.
- **998 of 1,303** laptops (76.6%) are below the original €1,500 cutoff (about **SAR 6,188**).
- Among brands with 20+ devices, the median for **MSI** is about **SAR 6,597** (54 laptops), compared with **SAR 2,306** for **Acer** (103 laptops).
- The median is about **SAR 2,055** for 4 GB RAM and **SAR 7,799** for 16 GB RAM. The Pearson correlation between RAM and price is about **0.743**.

The results show associations in this dataset, not causal effects.

## Project files

```text
notebooks/Laptop_Price_Analysis.ipynb
data/README.md
outputs/figures/01_price_distribution.png
outputs/figures/02_brand_median_prices.png
outputs/figures/03_ram_median_prices.png
presentation/Group3_Laptop_Price_Analysis.pptx
presentation/Group3_Laptop_Price_Analysis.pdf
requirements.txt
```

## Running the analysis
Open `notebooks/Laptop_Price_Analysis.ipynb` in Google Colab or Jupyter Notebook and run all the cells. The notebook downloads the dataset when no local CSV exists. It saves a cleaned CSV and three chart images. Packages for local use are listed in `requirements.txt`.

## Group 3
| Student | ID |
|---|---|
| Lena Ali Alsweed | 448815928 |
| Lamees Mansor | 448815902 |
| GHADAY Saeed | 448815777 |
| Lara Saleh | 448816083 |
| Samar saeed | 448815879 |

## References
- King Khalid University, *2323 CIS Introduction to Data Science Laboratory Manual*, LAB 14–15, pp. 31–33.
- MainakRepositor, `laptop_price.csv` dataset, accessed 24 November 2026.
- X-Rates, [SAR historical reference](https://www.x-rates.com/historical/?amount=1&date=2026-11-23&from=EUR), 23 November 2026.
