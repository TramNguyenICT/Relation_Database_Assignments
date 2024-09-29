# Exercises 4
### Question 1
SELECT country.name as "country name", airport.name as "airport name"
    -> FROM country
    -> INNER JOIN airport ON airport.iso_country = country.iso_country
    -> WHERE country.name = "Finland"
    -> AND scheduled_service = "yes";
![Screenshot 2024-09-29 084219](https://github.com/user-attachments/assets/a7ce4736-dd91-4ad4-bb3d-7c5766dc506c)

### Question 2
SELECT screen_name, airport.name
    -> FROM game
    -> INNER JOIN airport ON location = ident;
![Screenshot 2024-09-29 084442](https://github.com/user-attachments/assets/39f362ac-b6af-492b-8f95-4deeb96be2cd)

### Question 3
SELECT screen_name, country.name
    -> FROM game
    -> INNER JOIN airport ON location = ident
    -> INNER JOIN country ON airport.iso_country = country.iso_country;
![Screenshot 2024-09-29 084830](https://github.com/user-attachments/assets/2d0e133a-5072-4c8a-8612-3f637f8fbe9f)


### Question 4
SELECT airport.name, screen_name
    -> FROM airport
    -> LEFT JOIN game ON ident = location
    -> WHERE name like "%Hels%";
![Screenshot 2024-09-29 085112](https://github.com/user-attachments/assets/04068570-d1b0-4bba-a79c-828c0bad61e8)

### Question 5
SELECT name, screen_name
    -> FROM goal
    -> LEFT JOIN goal_reached ON goal.id = goal_id
    -> LEFT JOIN game on game.id = game_id;
 ![Screenshot 2024-09-29 085241](https://github.com/user-attachments/assets/060124b2-6634-4d32-826e-6cee544bcff2)

# Exercises 5
### Question 1
SELECT name
    -> FROM country
    -> WHERE iso_country IN(
    -> SELECT iso_country
    -> FROM airport
    -> WHERE name like "Satsuma%");
![Screenshot 2024-09-29 090929](https://github.com/user-attachments/assets/3f2a1e0c-9f28-4b53-9b06-c911b305b30c)

### Question 2
SELECT name
    -> FROM airport
    -> WHERE iso_country IN(
    -> SELECT iso_country
    -> FROM country
    -> WHERE name = "Monaco");
![Screenshot 2024-09-29 091426](https://github.com/user-attachments/assets/0b586344-b97b-46dc-b506-15cd117b22fd)

### Question 3
SELECT screen_name
    -> FROM game
    -> WHERE id IN(
    -> SELECT game_id
    -> FROM goal_reached
    -> WHERE goal_id IN(
    -> SELECT id
    -> FROM goal
    -> WHERE name = "CLOUDS"));
![Screenshot 2024-09-29 091842](https://github.com/user-attachments/assets/16d0445e-71bf-489a-8238-36b5fa0127e1)

### Question 4
SELECT name
    -> FROM country
    -> WHERE iso_country NOT IN(
    -> SELECT iso_country
    -> FROM airport);
![Screenshot 2024-09-29 092309](https://github.com/user-attachments/assets/01145d4b-8353-4866-b2f9-e509ee74e0a6)

### Question 5
SELECT name
    -> FROM goal
    -> WHERE id NOT IN(
    -> SELECT goal_id
    -> FROM goal_reached
    -> WHERE game_id IN(
    -> SELECT id
    -> FROM game
    -> WHERE screen_name = "Heini"));
![Screenshot 2024-09-29 092640](https://github.com/user-attachments/assets/35e9a4ea-e8e0-4408-9b55-eafe2986587d)

