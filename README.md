# Bachelorarbeit: Data-driven Analysis of Greenwashing in Sustainability Reports

## Overview
This repository contains the code and documentation for my bachelor's thesis titled "Tracking Greenwashing: A Data-driven Analysis of Sustainability Reports from DAX 40 Companies using NLP" The thesis aims to explore and identify potential greenwashing tendencies in sustainability reports using Natural Language Processing (NLP) techniques.

## Table of Contents
- [Introduction](#introduction)
- [Methodology](#methodology)
- [Folder Structure](#folder-structure)
- [Setup](#setup)
- [Usage](#usage)
- [Results](#results)
- [Conclusion](#conclusion)
- [References](#references)

## Introduction
The thesis focuses on analyzing sustainability reports from DAX 40 companies to uncover discrepancies between the stated sustainability practices and actual corporate behavior. Employing NLP, the project aims to provide a comprehensive understanding of the language used in these reports and identify potential instances of greenwashing.

## Methodology
The methodology involves data extraction, pre-processing, sentiment analysis, SDG alignment assessment using embeddings, and incorporating ESG scores. The final Greenwashing Tendency Score is calculated as: 

 **Greenwashing Tendency Formula:**

![Greenwashing Tendency Formula](https://latex.codecogs.com/svg.latex?\color{red}{\begin{aligned}&space;\text{GreenwashingTendency}&space;=&space;\frac{w_1&space;(SV&space;-&space;\min(SV))}{\max(SV)&space;-&space;\min(SV)}&space;\\&space;&plus;&space;\frac{w_2&space;(SDGA&space;-&space;\min(SDGA))}{\max(SDGA)&space;-&space;\min(SDGA)}&space;\\&space;-&space;\frac{w_3&space;(ESGS&space;-&space;\min(ESGS))}{\max(ESGS)&space;-&space;\min(ESGS)}&space;\\&space;&plus;&space;w_4&space;\times&space;CS&space;\\&space;&plus;&space;w_5&space;\times&space;\text{AbsDiff}(SV,&space;ESGS)&space;\\&space;&plus;&space;w_6&space;\times&space;\text{AbsDiff}(SDGA,&space;ESGS)&space;\end{aligned}})


 Where:
 * `SV`: Sentiment Value
 * `SDGA`: SDG Alignment
 * `ESGS`: ESG Score
 * `w1`, `w2`, `w3`, `w4`, `w5`, and `w6`: Weight factors for the respective components
 * `min()`, `max()`, and `AbsDiff()`: Represent the minimum, maximum values, and absolute difference function of the respective metrics in the dataset.


The individual components of the equation (Sentiment value, SDG-Alignment, ESG-Score & Company Size) could have different effects on the greenwashing tendency. Therefore, it could be useful to apply weight factors that reflect the relative importance of each component.

Normalizing values is crucial for ensuring a consistent scale and comparability of results. Employing min-max normalization, each value is standardized within the range of 0 to 1, enhancing the coherence of your analysis.

Larger companies may possess more resources for marketing and PR, potentially leading to a higher inclination for greenwashing. One way to address this would be to introduce an additional factor into the equation that accounts for the company's size.




## Folder Structure
- `data/`: Contains the raw and processed data.
- `code/`: Holds the Python scripts for data processing, analysis, and visualization.
- `results/`: Stores the results and visualizations generated during the analysis.

## Setup
1. Clone the repository.
2. Install the required dependencies using `pip install -r requirements.txt`.
3. Follow the instructions in the `code/README.md` for step-by-step execution.

## Usage
Detailed instructions for running the analysis and reproducing the results can be found in the `code/README.md` file.

## Results
The findings and visualizations obtained during the analysis will be presented in the final thesis document.

## Conclusion
This research aims to contribute valuable insights into the effectiveness of sustainability reporting and the prevalence of greenwashing practices among DAX 40 companies.

## References
A comprehensive list of references and cited works will be provided in the final thesis document.
