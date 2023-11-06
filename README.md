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

<p align="center" style="margin: 20px 0;">
    <img src="https://latex.codecogs.com/png.latex?\dpi{300}&space;\bg_white&space;\small&space;\text{GreenwashingTendency}&space;=&space;\frac{w_1&space;(SV&space;-&space;\min(SV))}{\max(SV)&space;-&space;\min(SV)}&space;&plus;&space;\frac{w_2&space;(SDGA&space;-&space;\min(SDGA))}{\max(SDGA)&space;-&space;\min(SDGA)}&space;-&space;\frac{w_3&space;(ESGS&space;-&space;\min(ESGS))}{\max(ESGS)&space;-&space;\min(ESGS)}&space;&plus;&space;w_4&space;CS" alt="GreenwashingTendency" style="width: 600px; height: 50px;">
</p>

* SV: Sentiment Value
* SDGA: SDG Alignment
* ESGS: ESG Score        
* CS: Company Size            

Here, w₁, w₂, w₃, and w₄ are the weight factors for the respective components. min() and max() represent the minimum and maximum values of the respective metrics in the dataset.


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
