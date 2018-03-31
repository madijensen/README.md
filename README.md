# README.md
ICA 4

Question 1. Which teacher had the highest average math score?

sql

SELECT teacher, avg(sat_math) as avg_math_score
from datasets.sat_scores 
group by teacher 
order by avg_math_score desc 

Question 2. Which School had the best average writing score?

sql 

SELECT school, avg(sat_writing) as avg_writing_score
from datasets.sat_scores 
group by school  
order by avg_writing_score desc 

Question 3. What was the breakdown of average total score between the three schools?

sql

SELECT school, avg(sat_writing+sat_verbal+sat_math) as avg_total_score
from datasets.sat_scores 
group by school  
order by avg_total_score desc 

Question 4. What were the top five total SAT scores?

sql

SELECT student_id, (sat_writing+sat_verbal+sat_math) as total_score
from datasets.sat_scores 
order by total_score desc 
limit 5


Question 5. Is there a relationship between total hours studied and total SAT score?

sql

SELECT hrs_studied, (sat_writing+sat_verbal+sat_math) as total_score
from datasets.sat_scores 
order by hrs_studied ASC


