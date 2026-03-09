# Analyse_of_income_tax_around_the_globe
Data Visualisation for Economics — Assignment 3
Overview

This repository contains the data, R code, and final report for a comprehensive analysis of global income tax rates. The project focuses on scraping real-world data from Wikipedia, cleaning it using custom R functions, and performing exploratory data analysis (EDA) through advanced visualizations. It also includes a secondary analysis of French labor market data (INSEE) to explore the relationship between age, gender, and unemployment.
Repository Structure

The project is organized into the following directories:

    code/: Contains the primary analysis script.

        ASSIGNMENT 3.Rmd: The R Markdown file containing the full pipeline from scraping to final visualization.

    data/: Includes both raw and processed datasets.

        tax_data_clean.csv: The dataset generated after automated cleaning.

        tax_data_clean_new.csv: A refined dataset incorporating manual data implementations.

        DD_EEC_ANNUEL_2024_data.csv: Raw unemployment data from INSEE (2024).

    assignment/: Contains the final documentation.

        ASSIGNMENT-3.pdf: The complete rendered report with interpretations and figures.

Data Sources

The analysis relies on two main sources:

    Wikipedia: The "List of countries by tax rates" table was scraped to obtain Corporate Tax, Top Marginal Income Tax, and VAT rates for over 230 jurisdictions.

    INSEE: Annual French employment data (2024) used to analyze unemployment disparities across different demographic groups.

Key Methodology

    Data Scraping: Utilizing the rvest library to extract HTML tables.

    Custom Cleaning: A robust clean_rate function was developed to handle non-numeric characters, citations, and percentage ranges within the scraped data.

    Data Imputation: To handle missing values, the project demonstrates a strategy of replacing missing top marginal income tax rates with corporate tax rates for specific comparative visualizations.

    Geospatial Mapping: Mapping countries to continents and generating world heatmaps using countrycode and ggplot2.

Requirements

To run the analysis, you will need R and the following libraries installed:

    rvest & magrittr (Scraping)

    tidyverse (Data manipulation and ggplot2)

    countrycode (Geospatial classification)

    stringr & dplyr (Data cleaning)

Usage

    Ensure the raw INSEE data (DD_EEC_ANNUEL_2024_data.csv) is present in the working directory.

    Open code/ASSIGNMENT 3.Rmd in RStudio.

    Knit the document to PDF to execute the scraping and generate the full report.
