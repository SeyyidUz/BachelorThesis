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

![Greenwashing Tendency Formula](https://latex.codecogs.com/svg.latex?\color{red}{GreenwashingTendency&space;=&space;\frac{w_{1}*&space;SV_{norm}*&space;SDGA_{norm}}{w_{2}*&space;ESGS_{norm}}})

 **with:**

![Formula](https://latex.codecogs.com/svg.latex?\color{red}{SV_{norm}&space;:=&space;\frac{SV&space;-&space;min(SV)}{max(SV)&space;-&space;min(SV)}})

![Formula](https://latex.codecogs.com/svg.latex?\color{red}{SDGA_{norm}&space;:=&space;\frac{SDGA&space;-&space;min(SDGA)}{max(SDGA)&space;-&space;min(SDGA)}})

![Formula](https://latex.codecogs.com/svg.latex?\color{red}{ESGS_{norm}&space;:=&space;\frac{ESGS&space;-&space;min(ESGS)}{max(ESGS)&space;-&space;min(ESGS)}})

**Where:**
 * SV : Sentiment Value
 * SDGA : SDG Alignment Value
 * ESGS : ESG Value
 * SV<sub>norm</sub> : Normalized Sentiment Value
 * SDGA<sub>norm</sub> : Normalized SDG-Alignment Value
 * ESGS<sub>norm</sub> : Normalized ESG Value
 * w<sub>1</sub> and w<sub>2</sub> : Weight factors for the respective components
 * min() and max() : Represent the minimum and maximum values of the respective metrics in the dataset


The individual components of the equation (Sentiment value, SDG-Alignment & ESG-Score) could have different effects on the greenwashing tendency. Therefore, it is useful to apply weight factors that reflect the relative importance of each component.

Normalizing values is crucial for ensuring a consistent scale and comparability of results. Employing min-max normalization, each value is standardized within the range of 0 to 1, enhancing the coherence of my analysis.

The Formula shows how much the company is 'exaggerating.' If the ESG score is very low (close to 0), but the Sentiment Value and SDG Alignment are high, this formula would indicate a particularly high level of greenwashing. It emphasizes the discrepancy between the proclaimed and actual performance of a company. Nevertheless, it is important to consider the sensitivity of this formula to extreme values and possibly take appropriate measures for smoothing or limitation.


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
