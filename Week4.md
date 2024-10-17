# Week 4 Exercises
# Exercises 4 + 5
## Exercises 4
### 1
```mysql
SELECT a.iso_country AS "country name", a.name AS "airport name" FROM airport a WHERE a.iso_country = 'FI' AND a.scheduled_service = 'yes';
```
![截屏2024-09-30 01.31.39.png](week4/exercises%204/%E6%88%AA%E5%B1%8F2024-09-30%2001.31.39.png)
### 2
```mysql
SELECT g.screen_name, a.name FROM game g JOIN airport a ON g.location = a.ident;
```
![截屏2024-09-30 00.37.00.png](week4/exercises%204/%E6%88%AA%E5%B1%8F2024-09-30%2000.37.00.png)
### 3
```mysql
SELECT g.screen_name, a.iso_country AS name FROM game g JOIN airport a ON g.location = a.ident;
```
![截屏2024-09-30 01.31.50.png](week4/exercises%204/%E6%88%AA%E5%B1%8F2024-09-30%2001.31.50.png)
### 4
```mysql
SELECT a.name, g.screen_name FROM airport a LEFT JOIN game g ON a.ident = g.location WHERE a.name LIKE '%Hels%';
```
![截屏2024-09-30 00.37.15.png](week4/exercises%204/%E6%88%AA%E5%B1%8F2024-09-30%2000.37.15.png)
### 5
```mysql
SELECT g.name, p.screen_name FROM goal g LEFT JOIN goal_reached gr ON g.id = gr.goal_id LEFT JOIN game p ON gr.game_id = p.id;
```
![截屏2024-09-30 00.37.23.png](week4/exercises%204/%E6%88%AA%E5%B1%8F2024-09-30%2000.37.23.png)
## Exercises 5
### 1
```mysql
SELECT c.name FROM country c JOIN airport a ON c.iso_country = a.iso_country WHERE a.name LIKE 'Satsuma%';
```
![截屏2024-09-30 00.49.10.png](week4/exercises%205/%E6%88%AA%E5%B1%8F2024-09-30%2000.49.10.png)
### 2
```mysql
SELECT a.name FROM airport a WHERE a.iso_country = 'MC';
```
![截屏2024-09-30 00.49.21.png](week4/exercises%205/%E6%88%AA%E5%B1%8F2024-09-30%2000.49.21.png)
### 3
```mysql
SELECT g.screen_name FROM goal_reached gr ON g.id = gr.game_id JOIN goal go ON gr.goal_id = go.id WHERE go.name = 'CLOUDS';
```
![截屏2024-09-30 00.49.29.png](week4/exercises%205/%E6%88%AA%E5%B1%8F2024-09-30%2000.49.29.png)
### 4
```mysql
SELECT c.name FROM country c WHERE c.iso_country NOT IN (SELECT a.iso_country FROM airport a);
```
![截屏2024-09-30 00.49.44.png](week4/exercises%205/%E6%88%AA%E5%B1%8F2024-09-30%2000.49.44.png)
### 5
```mysql
SELECT g.name FROM goal g WHERE g.id IN (SELECT gr.goal_id FROM goal_reached gr JOIN game gm ON gr.game_id = gm.id WHERE gm.screen_name = 'Heini');
```
![截屏2024-09-30 00.49.52.png](week4/exercises%205/%E6%88%AA%E5%B1%8F2024-09-30%2000.49.52.png)