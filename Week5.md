# Week 5 Exercises
# Exercises 6 + 7
## Exercises 6
### 1
```mysql
SELECT max(elevation_ft) FROM airport;
```
![截屏2024-09-30 01.08.59.png](week5/exercises%206/%E6%88%AA%E5%B1%8F2024-09-30%2001.08.59.png)
### 2
```mysql
SELECT continent, count(*) FROM country GROUP BY continent;
```
![截屏2024-09-30 01.09.05.png](week5/exercises%206/%E6%88%AA%E5%B1%8F2024-09-30%2001.09.05.png)
### 3
```mysql
SELECT g.screen_name, count(*) FROM goal_reached gr JOIN game g ON gr.game_id = g.id GROUP BY g.screen_name;
```
![截屏2024-09-30 01.09.12.png](week5/exercises%206/%E6%88%AA%E5%B1%8F2024-09-30%2001.09.12.png)
### 4
```mysql
SELECT screen_name FROM game WHERE co2_consumed = (SELECT MIN(co2_consumed) FROM game);
```
![截屏2024-09-30 01.09.20.png](week5/exercises%206/%E6%88%AA%E5%B1%8F2024-09-30%2001.09.20.png)
### 5
```mysql
SELECT c.name, count(*) FROM airport a JOIN country c ON a.iso_country = c.iso_country GROUP BY c.name ORDER BY COUNT(*) DESC LIMIT 50;
```
![截屏2024-09-30 01.09.27.png](week5/exercises%206/%E6%88%AA%E5%B1%8F2024-09-30%2001.09.27.png)
### 6
```mysql
SELECT c.name FROM airport a JOIN country c ON a.iso_country = c.iso_country GROUP BY c.name HAVING COUNT(*) > 1000;
```
![截屏2024-09-30 01.09.34.png](week5/exercises%206/%E6%88%AA%E5%B1%8F2024-09-30%2001.09.34.png)
### 7
```mysql
SELECT a.name FROM airport a WHERE a.elevation_ft = (SELECT MAX(elevation_ft) FROM airport);
```
![截屏2024-09-30 01.09.53.png](week5/exercises%206/%E6%88%AA%E5%B1%8F2024-09-30%2001.09.53.png)
### 8
```mysql
SELECT c.name FROM country c JOIN airport a ON c.iso_country = a.iso_country WHERE a.elevation_ft = (SELECT MAX(elevation_ft) FROM airport);
```
![截屏2024-09-30 01.10.00.png](week5/exercises%206/%E6%88%AA%E5%B1%8F2024-09-30%2001.10.00.png)
### 9
```mysql
SELECT count(*) FROM goal_reached gr JOIN game g ON gr.game_id = g.id WHERE g.screen_name = 'Vesa';
```
![截屏2024-09-30 01.10.19.png](week5/exercises%206/%E6%88%AA%E5%B1%8F2024-09-30%2001.10.19.png)
### 10
```mysql
SELECT name FROM airport WHERE ABS(latitude_deg) = (SELECT MAX(ABS(latitude_deg)) FROM airport);
```
![截屏2024-09-30 01.10.40.png](week5/exercises%206/%E6%88%AA%E5%B1%8F2024-09-30%2001.10.40.png)
***
## Exercises 7
### 1
![截屏2024-09-30 01.16.18.png](week5/exercises%207/%E6%88%AA%E5%B1%8F2024-09-30%2001.16.18.png)
### 2
![截屏2024-09-30 01.16.23.png](week5/exercises%207/%E6%88%AA%E5%B1%8F2024-09-30%2001.16.23.png)
### 3
![截屏2024-09-30 01.16.27.png](week5/exercises%207/%E6%88%AA%E5%B1%8F2024-09-30%2001.16.27.png)
### 4
![截屏2024-09-30 01.16.31.png](week5/exercises%207/%E6%88%AA%E5%B1%8F2024-09-30%2001.16.31.png)