# Ingesting And Building LinkedIn Data Marts (ETL)

## Project Overview

This project focuses on the extraction, transformation, and loading (ETL) of LinkedIn profile data into a data mart, followed by the visualization of the processed data using Tableau. The project aims to streamline LinkedIn profile data management by creating a structured SQL database from JSON data extracted via API. The final product is a comprehensive and interactive Tableau dashboard that enables users to explore and analyze LinkedIn profile data effectively.

## Table of Contents

- [Project Overview](#project-overview)
- [Architecture](#architecture)
- [Technologies Used](#technologies-used)
- [Dataset](#dataset)
- [ETL Pipeline](#etl-pipeline)
  - [Extraction](#extraction)
  - [Transformation](#transformation)
  - [Loading](#loading)
- [Database Schema](#database-schema)
- [Tableau Visualizations](#tableau-visualizations)
- [Final Dashboard](#final-dashboard)
- [Setup and Execution](#setup-and-execution)
- [Future Work](#future-work)
- [Contributors](#contributors)

## Architecture

The project is divided into three main stages:

1. **ETL Pipeline**: 
   - **Extraction**: Extract LinkedIn profile data and pictures in JSON format via API.
   - **Transformation**: Normalize the extracted data, applying over 10 transformations to parse the JSON into structured SQL tables.
   - **Loading**: Store the processed data into an SQL database.
   
2. **Data Mart**:
   - The SQL database is used as a data mart for LinkedIn profile information.

3. **Visualization**:
   - The SQL database is imported into Tableau to create over 10 visualizations, culminating in a comprehensive dashboard with interactive search filters.

## Technologies Used

- **Pentaho ETL**: For data extraction, transformation, and loading processes.
- **SQL**: For data storage and normalization.
- **Tableau**: For data visualization and dashboard creation.
- **JSON**: For data extraction via API.

## Dataset

The dataset consists of LinkedIn profile data, including user details, job experiences, education, skills, and profile pictures, all in JSON format.

## ETL Pipeline

### Extraction

- **Source**: LinkedIn API
- **Data Format**: JSON
- **Process**: Extracted LinkedIn profile data and pictures using the LinkedIn API.

### Transformation

- **Normalization**: Parsed and transformed the JSON data into normalized SQL tables.
- **Transformations**: Applied over 10 transformations to ensure data integrity, remove redundancies, and prepare the data for loading into SQL.
- **Tools**: Used Pentaho ETL for managing the transformation processes.

### Loading

- **Destination**: SQL Database
- **Process**: Loaded the transformed data into the SQL database, ensuring it is structured for efficient querying and analysis.

## Database Schema

The database schema is designed to handle normalized data efficiently. Below is a simplified schema overview:

- **Users**: Stores general profile information.
- **Experiences**: Stores job experiences linked to users.
- **Education**: Stores educational background linked to users.
- **Skills**: Stores skills associated with users.
- **Profile_Pictures**: Stores links to user profile pictures.

The detailed schema can be explored in the attached SQL file (`dump_group_11.sql`).

## Tableau Visualizations

After the ETL process, the SQL database was imported into Tableau, where the following visualizations were created:

1. **Profile Summary**: Overview of LinkedIn profiles.
2. **Job Experience Analysis**: Visual breakdown of job experiences.
3. **Education Analysis**: Insights into the educational background.
4. **Skills Distribution**: Analysis of skills across profiles.
5. **Profile Picture Distribution**: Distribution of profile pictures.

(Include a brief description for each visualization you created.)

## Final Dashboard

The final Tableau dashboard combines all the visualizations into an interactive user interface. Key features include:

- **Interactive Search Filter**: Allows users to search profiles based on various criteria such as job title, skills, education, etc.
- **Drill-Down Capabilities**: Users can click on elements to see more detailed information.
- **Dynamic Updates**: The dashboard updates automatically based on the filter criteria.

## Setup and Execution

### Prerequisites

- **Pentaho ETL**
- **SQL Database (e.g., MySQL, PostgreSQL)**
- **Tableau Desktop**
- **LinkedIn API Access**

### Steps to Run the Project

1. **Clone the Repository**: 
   ```bash
   git clone https://github.com/kumareshpv/LinkedIn-Data-Mart
   ```

2. **Set Up the SQL Database**:
- Import the provided SQL dump `(dump_group_11.sql)` into your SQL server.

3. **Run the ETL Process**:
- Configure and run the ETL pipeline using Pentaho to extract, transform, and load data into the SQL database.

4. **Import Data into Tableau**:
- Connect Tableau to the SQL database and import the data.
- Open the Tableau workbook and explore the visualizations.

5. **Explore the Dashboard**:
- Use the interactive filters to explore LinkedIn profiles in the dashboard.

### Future Work

- Automating ETL Processes: Implementing automation to update the SQL database with the latest LinkedIn data.
- Expanding Data Sources: Integrating additional data sources for a more comprehensive analysis.
- Enhanced Visualizations: Developing more advanced visualizations and adding predictive analytics.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.


### Contributors

Kumaresh PV - [LinkedIn](https://www.linkedin.com/in/kumaresh-pv)
