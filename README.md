# 2020LACrimes_DB
SQL Database and queries

This is a database created using MYSQL for a subset of Los Angeles Crime Data from 2019-2020.

## SAMPLE QUERIES

Below is a set of questions that can be answered from the data and the SQL queries used to answer them.

### Where Crimes are Being Reported

1.  Which cross street has had the most reported crime incidences? And what percentage of total reported crimes did it have?
    `mysql> select cross_st,count(cross_st) as num_reports,count(cross_st)*100/(select count(1) from reports) as percent from reports group by cross_st order by num_reports desc limit 1;`
2.	What are the top 5 areas with the most crimes in 2019?
3.	What 5 premise types have the most crimes?
4.	The *areas_2018* table has total counts of confirmed violent and property crimes by area in 2018. Using the *areas_2018* table as an estimate, what percent of violent crimes reported in 2019 might be actual occurrences of crime?

### Demographic Questions

5.	How many crimes have been reported by each descent?
6.	What crime categories have more female victims than male victims?
7.	Looking at the arrest status for the crime reports, what crimes have been committed by juveniles?

### Additional Questions

8.	What is the average number of days between when a crime occurs and when it is reported?
9.	Give a breakdown of the number of reported crimes for each arrest status.
10.	We want to know the monthly trend of when robberies occur. For each month, what is the number of crimes that occurred in the ‘Robbery’ category?


## ENTITY RELATIONSHIP DIARGRAM (ERD)

![ERD](images/erd.png)


## DATABASE CREATION DECISION OUTLINE

This section provides an outline why I made certain decisions regarding the structure of the database and the tables within it.


