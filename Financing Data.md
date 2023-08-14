# Financing Data for New Investment

## Task Description
Data analyst for a company planning to venture into a new market involving financial services. The company is requesting insights on sources of financing companies tap into when entering the said industry. 

Decision makers will use insights from the report for their alternatives analysis as they explore probable sources of financing to start offering the new service. 

At the end of this task, the following questions will be answered:
- What type of funding would you recommend for the startup company?
- Why have you recommended this option?

The dataset can be found [here](https://drive.google.com/file/d/1QYA7J3sKzdyucj0h9bmtjzTQAv8wOrF8/view?usp=drive_link).

## Goals
### 1. Import the dataset to SQL and create an INVESTMENT table

#### Full SQL Query: [Goal 1 Queries.txt](https://github.com/ailaumalin/Data-Analysis-Projects/files/12290355/Goal.1.Queries.txt)

Using the table, write a query that meets the following conditions:
- Show all the columns in the table;
- Order the given result by the column in descending order.

Output: [Goal 1 Output.xlsx](https://github.com/ailaumalin/Data-Analysis-Projects/files/12290350/Goal.1.Output.xlsx)


### 2. Pull out data from companies that have received funding and operate within the FINANCIAL SERVICES sector.

#### Full SQL Query: [Goal 2 Queries.txt](https://github.com/ailaumalin/Data-Analysis-Projects/files/12290749/Goal.2.Queries.txt)

#### 2a - Using the table, write a statement that meets all of the following conditions:
- Show all the columns in the table;
- Filter the data to show the column containing the word market Financial Services;
- Further filter the data where the column is greater than funding_total_usd 0;
- Order the given result by the column name (in ascending order).

Output: [Goal 2a Output.xlsx](https://github.com/ailaumalin/Data-Analysis-Projects/files/12290580/Goal.2a.Output.xlsx)

#### 2b - Write a query that creates the table investment_subset containing the data shown from the SELECT query used in 2a. 
Output: [Goal 2b Output.xlsx](https://github.com/ailaumalin/Data-Analysis-Projects/files/12290700/Goal.2b.Output.xlsx)

#### 2c - Using the investment_subset table, write a query that achieves the following conditions:
- Show all the columns in the table;
- Order the given result by the column in descending order. 

Output: [Goal 2c Output.xlsx](https://github.com/ailaumalin/Data-Analysis-Projects/files/12290745/Goal.2c.Output.xlsx)

### 3. Explore the data using SQL Queries

#### Full SQL Query: [Goal 3 Queries.txt](https://github.com/ailaumalin/Data-Analysis-Projects/files/12291412/Goal.3.Queries.txt)


#### 3a - Using the table investment_subset, write a SELECT query that meets the following conditions:
- Show the columns founded_year and the COUNT() of funding_total_usd;
- Group the result by the column founded_year;
- Order the given result by the column founded_year (in ascending order).

Output: [Goal 3a Output.xlsx](https://github.com/ailaumalin/Data-Analysis-Projects/files/12291079/Goal.3a.Output.xlsx)

#### 3b - Using the investment_subset table, write a SELECT query that meets the following conditions:
- Show the column country_code;
- Show the column COUNT() of the column country_code with alias AS num_countries;
- Show the column AVG() of the column seed with alias AS avg_seed;
- Show the column AVG() of the column venture with alias AS avg_venture;
- Filter the data where the column founded_year is BETWEEN 2010 and 2014 and (inclusive);
- Group the data by the column country_code;
- Order the given result by the column num_countries in descending order.

Output: [Goal 3b Output.xlsx](https://github.com/ailaumalin/Data-Analysis-Projects/files/12291176/Goal.3b.Output.xlsx)

#### 3c - Using the investment_subset table, write a SELECT query that meets the following conditions:
- Show all the columns in the table;
- Filter the data where the column country_code is equal to 'USA';
- Further filter the data where the column founded_year is BETWEEN 2010 and 2014 (inclusive);
- Order the given result by the column funding_total_usd (in ascending order).

Output: [Goal 3c Output.xlsx](https://github.com/ailaumalin/Data-Analysis-Projects/files/12291410/Goal.3c.Output.xlsx)

The startup company decided to begin its business in the USA. Based on the funding received by the most recent companies, the startup is seeking to determine the most suitable type of funding to plan their business

### 4. Determine the most suitable type of funding to plan their business. 

#### Full SQL Query: [Goal 4 Queries.txt](https://github.com/ailaumalin/Data-Analysis-Projects/files/12291613/Goal.4.Queries.txt)

Using the investment_subset  table, write a SELECT query that meets the following conditions:
- Show the columns name, founded_year, funding_total_usd, seed, and venture
- Create a CASE statement
1. WHEN seed is equal to 0 and venture is greater than 0, then output the result as Venture Only
2. WHEN seed is greater than 0 and venture is equal 0, then output the result as Seed Only
3. ELSE output the result as Mixed ;
4. Give the resulting column an alias AS funding_type.
- Filter the data where the column country_code is equal to USA;
- Further filter the data where the column founded_year is between 2010 and 2014 (inclusive);
- Order the given result by the column funding_total_usd (in ascending order).

Output: [Goal 4 Output.xlsx](https://github.com/ailaumalin/Data-Analysis-Projects/files/12291669/Goal.4.Output.xlsx)

## Insights and Recommendations
The goal of this task is to answer the following questions:
- What type of funding would you recommend for the startup company?
- Why have you recommended this option?

In this file, you'll see the tables and charts for the output generated in Goal 4. Additional visualizations had also been added - [Visualization.xlsx](https://github.com/ailaumalin/Data-Analysis-Projects/files/12321341/Visualization.xlsx)

The visualizations can also be found [here](https://docs.google.com/document/d/1Fq-z5WTZqOEne2ao6eILmi6Q89voPS24Va7woXdicNA/edit).

Based on the visualized data after rigorous filtering, Seed funding is the most prominent type of funding in the US and what I would also recommend for a startup company. 

Based on [Investopedia](https://www.investopedia.com/terms/s/seedcapital.asp), seed funding is the foundation and the first stage in a series of four funding stages needed for a start-up to be an established company. Seed funding can be sourced from private investors, close family, friends, acquaintances, and the founders of the company. 

This funding is raised in the early stages of a business and often comes from personal sources which is why the sum is only moderate. This would also explain why the collective seed funding from US companies (on the 2nd chart) only amounts to 17 million USD while the venture is at 44 million – seed funding is not a large amount but moderate only. Eventually, the company may attract more financing and catch the attention of venture capitalists.

According to a [LinkedIn article](https://www.linkedin.com/pulse/importance-seed-capital-entrepreneurship-success-mario-haro-salazar/) by Mario Haro Salazar, seed capital is significant for entrepreneurs to turn their ideas into something concrete and actionable. Seed funding provides entrepreneurs resources to get ideas off the ground, develop services, products, or proposals, and create a strong foundation for their business. This will also help them assess market demand for their products/services before proceeding to large investments. 







