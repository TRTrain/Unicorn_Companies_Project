# Unicorn Companies SQL Project 🦄:office:

## Objective 📍
Find out how many companies reached a valuation of over $1 billion across different industries between 2019 and 2021

## Reference 📄
Premium DataCamp Project :
[Analyzing Unicorn Companies](https://app.datacamp.com/learn/projects/1531)

## Database 🗃
PostgreSQL <a href="https://www.postgresql.org/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/postgresql-colored.svg" width="36" height="36" alt="PostgreSQL" /></a>
                    
## Strategy and Solution 🔎
There are several ways to produce this output, with one approach involving the use of three queries, of which two are common table expressions (CTEs)

<p> In the first common table expression (CTE) called top_industries, you need to find the top three industries in 2019, 2020, and 2021 based on a count of unicorns created.
You can filter the year using WHERE EXTRACT(___ FROM ___) in (‘___’, ‘___’, ‘___’).

![Screenshot (226)](https://github.com/TrainingForFuture/Unicorn_Companies_Project/assets/134767020/df3052cc-578e-44de-a1cd-b99170035011)

<p> In the second CTE, called yearly_rankings, you need to calculate the number of unicorns and the average valuation, grouped by year and industry.
This query involves using COUNT(), EXTRACT(___ FROM ___), and AVG().

![Screenshot (227)](https://github.com/TrainingForFuture/Unicorn_Companies_Project/assets/134767020/cfa516e9-6b2d-4d71-a57f-76335af936cd)

<p> In the final query you should select the industry, year, num_unicorns, and the average of average_valuation divided by one billion, rounding to two decimal places and aliasing as average_valuation_billions; filtering the results for 2019, 2020, and 2021, and where the industry is in top_industries. Remember to sort the results by industry, then by year in descending order.
<p> You’ll need to use ROUND(AVG(___), 2) to calculate average_valuation_billions.
<p> The WHERE clause takes two filters - the three desired years, along with top-performing industries from the top_industries CTE.
  
![Screenshot (228)](https://github.com/TrainingForFuture/Unicorn_Companies_Project/assets/134767020/6b8b4f4a-7aac-4ab5-993a-752b07ffe328)

  
![Screenshot (229)](https://github.com/TrainingForFuture/Unicorn_Companies_Project/assets/134767020/7bf9016f-73dc-4025-a4cd-78e019788f2c)
