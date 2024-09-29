# Exercise 6: Aggregate Queries
### Question 1
SELECT max(elevation_ft) FROM airport;
![Screenshot 2024-09-29 092924](https://github.com/user-attachments/assets/9290cacc-72f3-4860-b81e-aee57d5d5bfe)

### Question 2
SELECT continent, count(*)
    -> FROM country
    -> GROUP BY continent;
![Screenshot 2024-09-29 093344](https://github.com/user-attachments/assets/ad459362-ee09-4ffa-8b05-08a3938d9a32)

### Question 3
SELECT screen_name, count(*)
    -> FROM game, goal_reached
    -> WHERE id = game_id
    -> GROUP BY screen_name;
![Screenshot 2024-09-29 093651](https://github.com/user-attachments/assets/3b8d7718-dc74-4bab-82ee-9321e8d0205e)

### Question 4
SELECT screen_name
    -> FROM game
    -> WHERE co2_consumed IN(
    -> SELECT min(co2_consumed) FROM game);
![Screenshot 2024-09-29 094033](https://github.com/user-attachments/assets/b16f02e4-92a1-40c5-8810-9fafdd70ef01)

### Question 5
SELECT country.name, count(*)
    -> FROM airport, country
    -> WHERE airport.iso_country = country.iso_country
    -> GROUP BY country.iso_country
    -> ORDER BY count(*) DESC limit 50;
![Screenshot 2024-09-29 094332](https://github.com/user-attachments/assets/f9801cc1-aee1-4e25-9cae-30a527a5abfb)

### Question 6
SELECT country.name
    -> FROM airport, country
    -> WHERE airport.iso_country = country.iso_country
    -> GROUP BY country.iso_country
    -> HAVING count(*)>1000;
  ![Screenshot 2024-09-29 101051](https://github.com/user-attachments/assets/ddb94831-003e-407c-a19e-ccc38c72279d)

### Question 7
SELECT name
    -> FROM airport
    -> WHERE elevation_ft IN (
    -> SELECT max(elevation_ft)
    -> FROM airport);
![Screenshot 2024-09-29 103419](https://github.com/user-attachments/assets/0b50faaf-3526-4cd0-875f-1eaa81e75542)

### Question 8
SELECT name
    -> FROM country
    -> WHERE iso_country IN (
    -> SELECT iso_country
    -> FROM airport
    -> WHERE elevation_ft IN (
    -> SELECT max(elevation_ft)
    -> FROM airport));
![Screenshot 2024-09-29 103739](https://github.com/user-attachments/assets/7dda39a2-6b9f-4685-a933-c7f01b8d2e84)

### Question 9
SELECT count(*)
    -> FROM game, goal_reached
    -> WHERE id = game_id and screen_name = "Vesa"
    -> GROUP BY screen_name;
![Screenshot 2024-09-29 104307](https://github.com/user-attachments/assets/43be87c3-938b-4a49-9ec4-4c239e9df3f5)

### Question 10
SELECT name
    -> FROM airport
    -> WHERE latitude_deg IN (
    -> SELECT min(latitude_deg)
    -> FROM airport);
![Screenshot 2024-09-29 104434](https://github.com/user-attachments/assets/db36b136-da9a-48e6-a32d-c48421738032)

# Exercise 6: Update Queries
### Question 1
UPDATE game
    -> SET location = (
    -> SELECT ident
    -> FROM airport
    -> WHERE name = "Nottingham Airport"),
    -> co2_consumed = co2_consumed + 500
    -> WHERE screen_name = "Vesa";
![Screenshot 2024-09-29 105051](https://github.com/user-attachments/assets/9c60d75f-4865-4bed-9f97-be8c16dc0ad7)

### Question 2
b. We have to delete data first from goal_reached table.
### Question 3
DELETE FROM goal_reached;
### Question 4
DELETE FROM goal_reached;
