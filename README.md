COVID-19 Infection ETL Project

By Sandeep Prasad

Project Proposal

Leveraging the comprehensive COVID-19 data compiled by John Hopkins University , this project aims to explore 

the early trends and impacts of the pandemic, specifically focusing on the relationship between confirmed cases, deaths, and recoveries during March 2020. The core objective is to extract this valuable CSV data, perform necessary transformations, and migrate it to a PostgreSQL database for efficient analysis and querying.

Project Description

The dataset utilized for this project was sourced from data.humdata.org, which aggregates information meticulously compiled by the John Hopkins University Center for Systems Science and Engineering (JHU CSSE). This compilation draws from various authoritative sources, including the World Health Organization and the European Centre for Disease Prevention and Control. To narrow the project's scope due to the continuously updating nature of the data, the focus was specifically placed on March 2020, allowing for a detailed evaluation of confirmed cases, deaths, and recoveries during that crucial period.


Finding Data

All data for this project was obtained from the following source: 

https://data.humdata.org/dataset/novel-coronavirus-2019-ncov-cases. This resource serves as a central repository for the data compiled by the John Hopkins University Center for Systems Science and Engineering (JHU CSSE), incorporating data from diverse organizations such as the World Health Organization (WHO), the Hong Kong Department of Health, and the European Centre for Disease Prevention and Control. Given the ongoing updates to this dataset, the analysis was specifically confined to the month of March 2020.

Data Cleanup and Analysis

TRANSFORMATION STEPS
The transformation phase involved a series of steps to ensure the data was clean, readily presentable, and optimized for subsequent querying. Key actions included:

Developing a Python cleaning function to precisely select and isolate data pertaining to March 2020 across all datasets.

Utilizing the 

pd.melt function in Pandas to treat all date-related entries within the datasets as distinct values, facilitating easier manipulation.

Implementing a method to calculate the daily increase for each table, with the resulting float values being converted to integers for consistency.

LOADING STEPS
To facilitate data storage and retrieval, the following loading procedures were performed:

An initial connection was established to a local PostgreSQL server on the desktop.

A schema was defined specifically for creating the necessary tables, and its successful implementation was confirmed using 

engine.table_names().

The processed Pandas DataFrames were then pushed to the local PostgreSQL server, making the data available for direct retrieval and querying within a Jupyter Notebook environment.

Analysis / SQL Queries
The analysis phase aims to derive specific insights from the cleaned and loaded data through targeted SQL queries. The primary areas of exploration include:

Identifying the top 5 countries with both the highest and lowest confirmed COVID-19 cases.

Determining the top 5 countries with the most and fewest reported deaths.

Pinpointing the top 5 countries with the highest and lowest numbers of recovered cases.

Identifying the specific date in March that recorded the highest numbers of confirmed cases, deaths, and recoveries.
