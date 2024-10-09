# Week 3 Exercises
# Exercises 2 + 3
## Exercises 2
### 1
```mysql
USE flight_game;
SELECT * FROM goal;
```
![截屏2024-09-29 22.02.37.png](week3/exercises2/%E6%88%AA%E5%B1%8F2024-09-29%2022.02.37.png)
### 2
```mysql
SELECT name, type FROM airport WHERE iso_country = 'FI';
```
![截屏2024-09-29 22.02.46.png](week3/exercises2/%E6%88%AA%E5%B1%8F2024-09-29%2022.02.46.png)
### 3
```mysql
SELECT name FROM airport WHERE iso_country = 'FI' ORDER BY name ASC;
```
![截屏2024-09-29 22.02.56.png](week3/exercises2/%E6%88%AA%E5%B1%8F2024-09-29%2022.02.56.png)
### 4
```mysql
SELECT name, type FROM airport WHERE iso_country = 'FI' ORDER BY type ASC, name ASC;
```
![截屏2024-09-29 22.03.04.png](week3/exercises2/%E6%88%AA%E5%B1%8F2024-09-29%2022.03.04.png)
### 5
```mysql
SELECT name FROM country WHERE name LIKE 'F%';
```
![截屏2024-09-29 22.03.15.png](week3/exercises2/%E6%88%AA%E5%B1%8F2024-09-29%2022.03.15.png)
### 6
```mysql
SELECT name FROM country WHERE name LIKE '%F%';
```
![截屏2024-09-29 22.03.23.png](week3/exercises2/%E6%88%AA%E5%B1%8F2024-09-29%2022.03.23.png)
### 7
```mysql
SELECT location FROM game WHERE screen_name = 'Vesa';
```
![截屏2024-09-29 22.03.30.png](week3/exercises2/%E6%88%AA%E5%B1%8F2024-09-29%2022.03.30.png)
### 8
```mysql
SELECT co2_consumed FROM game WHERE screen_name = 'Ilkka';
```
![截屏2024-09-29 22.03.44.png](week3/exercises2/%E6%88%AA%E5%B1%8F2024-09-29%2022.03.44.png)
### 9
```mysql
SELECT DISTINCT co2_budget FROM game;
```
![截屏2024-09-29 22.03.50.png](week3/exercises2/%E6%88%AA%E5%B1%8F2024-09-29%2022.03.50.png)
### 10
```mysql
SELECT screen_name, co2_budget, co2_consumed, (co2_budget - co2_consumed) AS co2_left 
FROM game WHERE screen_name = 'Ilkka';
```
![截屏2024-09-29 22.03.57.png](week3/exercises2/%E6%88%AA%E5%B1%8F2024-09-29%2022.03.57.png)
***
## Exercises 3
### 1
```mysql
SELECT c.name AS "country name", a.name AS "airport name" FROM country c JOIN airport a ON c.iso_country = a.iso_country WHERE c.name = 'Iceland';
```
![截屏2024-09-30 00.24.04.png](week3/exercises3/%E6%88%AA%E5%B1%8F2024-09-30%2000.24.04.png)
### 2
```mysql
SELECT name AS "airport name" FROM airport WHERE iso_country = 'Fr' AND type = 'large_airport';
```
![截屏2024-09-30 00.24.13.png](week3/exercises3/%E6%88%AA%E5%B1%8F2024-09-30%2000.24.13.png)
### 3
```mysql
SELECT country.name AS "country_name", airport.name AS "airport_name" FROM country JOIN airport ON country.iso_country = airport.iso_country WHERE country.continent = 'Europe';
```
![截屏2024-09-30 00.24.22.png](week3/exercises3/%E6%88%AA%E5%B1%8F2024-09-30%2000.24.22.png)
### 4
```mysql
SELECT a.elevation_ft FROM airport a JOIN game g ON a.ident = g.location WHERE g.screen_name = 'Heini';
```
![截屏2024-09-30 00.24.29.png](week3/exercises3/%E6%88%AA%E5%B1%8F2024-09-30%2000.24.29.png)
### 5
```mysql
SELECT a.elevation_ft * 0.3048 AS elevation_m FROM airport a JOIN game g ON a.ident = g.location WHERE g.screen_name = 'Heini';
```
![截屏2024-09-30 00.24.38.png](week3/exercises3/%E6%88%AA%E5%B1%8F2024-09-30%2000.24.38.png)
### 6
```mysql
SELECT a.name FROM airport a JOIN game g ON a.ident = g.location WHERE g.screen_name = 'Ilkka';
```
![截屏2024-09-30 00.24.48.png](week3/exercises3/%E6%88%AA%E5%B1%8F2024-09-30%2000.24.48.png)
### 7
```mysql
SELECT a.iso_country AS name FROM airport a JOIN game g ON a.ident = g.location WHERE gm.screen_name = 'Heini';
```
![截屏2024-09-30 01.24.54.png](week3/exercises3/%E6%88%AA%E5%B1%8F2024-09-30%2001.24.54.png)
### 8
```mysql
SELECT g.name FROM goal_reached gr JOIN game gm ON gr.game_id = gm.id JOIN goal g ON g.id = gr.goal_id WHERE gm.screen_name = 'Ilkka' AND g.name = 'CLOUDS';
```
![截屏2024-09-30 00.25.04.png](week3/exercises3/%E6%88%AA%E5%B1%8F2024-09-30%2000.25.04.png)
### 9
```mysql
SELECT a.name FROM goal_reached gr JOIN game gm ON gr.game_id = g.id JOIN goal g ON gr.goal_id = g.id WHERE gm.screen_name = 'Ilkka' AND g.name = 'CLOUDS';
```
![截屏2024-09-30 00.25.12.png](week3/exercises3/%E6%88%AA%E5%B1%8F2024-09-30%2000.25.12.png)
### 10
```mysql
SELECT a.iso_country AS name FROM goal_reached gr JOIN game g ON gr.game_id = g.id JOIN goal go ON gr.goal_id = go.id JOIN airport a ON g.location = a.ident WHERE g.screen_name = 'Ilkka' AND go.name = 'CLOUDS';
```
![截屏2024-09-30 01.25.02.png](week3/exercises3/%E6%88%AA%E5%B1%8F2024-09-30%2001.25.02.png)


