# README.md
ICA 4
Question 1. Which teacher had the highest average math score?
''sql''
SELECT teacher, avg(sat_math) as avg_math_score
from datasets.sat_scores 
group by teacher 
order by avg_math_score desc 
''
