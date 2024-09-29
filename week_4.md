# Exercises 3
### Question 1
SELECT country.name as "country name", airport.name as "airport name"
    -> FROM airport, country
    -> WHERE country.name = "Iceland"
    -> AND airport.iso_country = country.iso_country;

![Screenshot 2024-09-09 153747](https://github.com/user-attachments/assets/a9f4adc4-d34f-41ac-8f71-4ba37340e1ad)

### Question 2
SELECT airport.name as "airport name"
    -> FROM airport, country
    -> WHERE airport.iso_country = country.iso_country
    -> AND country.name = "France"
    -> AND airport.type = "large_airport";
![Screenshot 2024-09-29 075508](https://github.com/user-attachments/assets/b2a7d7ed-0fd8-400f-855b-9a0eb1748529)

### Question 3
SELECT country.name as country_name, airport.name as airport_name
    -> FROM airport, country
    -> WHERE airport.iso_country = country.iso_country
    -> AND country.continent = "AN";
![Screenshot 2024-09-29 075655](https://github.com/user-attachments/assets/677b757c-548c-4549-8f5a-edcd1306c50b)

### Question 4
SELECT elevation_ft FROM airport, game
    -> WHERE location = ident
    -> AND screen_name = "Heini";
![Screenshot 2024-09-29 075846](https://github.com/user-attachments/assets/d97a126b-a71d-40e3-b643-55599e04630c)

### Question 5
 SELECT elevation_ft*0.3048 as elevation_m
    -> FROM airport, game
    -> WHERE location = ident
    -> AND screen_name = "Heini";
![Screenshot 2024-09-29 080026](https://github.com/user-attachments/assets/63a73eb5-bc27-444e-bdaa-c434c21ecd64)

### Question 6
SELECT name FROM airport, game
    -> WHERE location = ident
    -> AND screen_name = "Ilkka";
![Screenshot 2024-09-29 073121](https://github.com/user-attachments/assets/3d3089e4-50c2-43cf-9b82-4cad11a4e6a0)

### Question 7
SELECT country.name FROM airport, game, country
    -> WHERE location = ident
    -> AND airport.iso_country = country.iso_country
    -> AND screen_name = "Ilkka";
![Screenshot 2024-09-29 074015](https://github.com/user-attachments/assets/a021a8a1-06b3-4243-8184-0094e03e48dc)

### Question 8
SELECT country.name FROM airport, game, country
    -> WHERE location = ident
    -> AND airport.iso_country = country.iso_country
    -> AND screen_name = "Ilkka";
![Screenshot 2024-09-29 082611](https://github.com/user-attachments/assets/eebfadc8-76f7-4d14-872e-5e9235f7b6b2)

### Question 9
SELECT airport.name
    -> FROM airport, game, goal, goal_reached
    -> WHERE ident = location
    -> AND game.id = game_id
    -> AND goal.id = goal_id
    -> AND screen_name = "Ilkka"
    -> AND goal.name = "CLOUDS";
![Screenshot 2024-09-29 082914](https://github.com/user-attachments/assets/7888b3cb-969e-4bdf-a2c7-4eb89266e89b)

### Question 10
SELECT country.name
    -> FROM country, airport,game,goal,goal_reached
    -> WHERE airport.iso_country = country.iso_country
    -> AND ident = location
    -> AND game.id = game_id
    -> AND goal.id = goal_id
    -> AND screen_name = "Ilkka"
    -> AND goal.name = "CLOUDS";
![Screenshot 2024-09-29 083211](https://github.com/user-attachments/assets/96a0d4d5-6dae-4df6-b61a-d010dafcc950)
