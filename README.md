# SQL exercises for job interviews
This repo contains SQL exercises to practice for job interviews

### 1. Highest Total Miles
You’re given a table of Uber rides that contains the mileage and the purpose for the business expense. You’re asked to find business purposes that generate the most miles driven for passengers that use Uber for their business transportation. Find the top 3 business purpose categories by total mileage.

Table: my_uber_drives

````sql
select sum(miles) as miles
	,purpose
from my_uber_drives
where category = "Business"
group by purpose
order by miles desc
limit 3
````
**Answer:**

The top 3 business purposes that generate most miles driven for passengers are:
Meeting
-Customer Visit
-Meal/Entertain  

***
