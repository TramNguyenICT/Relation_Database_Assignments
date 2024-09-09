# Week 3
### Question 1
SELECT * FROM goal;
![Screenshot 2024-09-09 143921](https://github.com/user-attachments/assets/7270b1a4-3b27-4bac-87e4-b22fed43b025)

### Question 2
SELECT name, type FROM airport WHERE iso_country = "FI";
![Screenshot 2024-09-09 145115](https://github.com/user-attachments/assets/91ea4d16-3d73-4f51-9612-2cdc051483cc)

### Question 3
SELECT name FROM airport WHERE iso_country = "FI" ORDER BY name ASC;
![Screenshot 2024-09-09 150042](https://github.com/user-attachments/assets/e37ce505-3331-41fb-8e45-9a18460de5b2)

### Question 4
SELECT name, type FROM airport WHERE iso_country = "FI" ORDER BY type ASC, name ASC;
![Screenshot 2024-09-09 150226](https://github.com/user-attachments/assets/04c09ec4-2185-458f-955b-fbeeb67378f6)

### Question 5
SELECT name FROM country WHERE name LIKE "F%";
![Screenshot 2024-09-09 151218](https://github.com/user-attachments/assets/b607f5d2-20bd-4d00-b959-f48fd69a7d99)

### Question 6
SELECT name FROM country WHERE name LIKE "%F%";
![Screenshot 2024-09-09 151315](https://github.com/user-attachments/assets/277a99c6-9062-4215-aa7a-bb2c04ce6d7f)

### Question 7
SELECT location FROM game WHERE screen_name = "Vesa";
![Screenshot 2024-09-09 151404](https://github.com/user-attachments/assets/282fd70a-b1aa-42d1-bd5f-9358908d822e)

### Question 8
SELECT co2_consumed FROM game WHERE screen_name = "Ilkka";
![Screenshot 2024-09-09 151505](https://github.com/user-attachments/assets/4bee8993-e431-4492-b08c-baac3134abaa)

### Question 9
SELECT DISTINCT co2_budget FROM game;

![Screenshot 2024-09-09 151614](https://github.com/user-attachments/assets/cb6ae272-45f2-4724-ab7d-9148749d3ae6)

### Question 10
SELECT screen_name, co2_budget, co2_consumed, (co2_budget - co2_consumed) as co2_left FROM game WHERE screen_name = "Ilkka";
![Screenshot 2024-09-09 151703](https://github.com/user-attachments/assets/d7f20d6e-6c4d-4a89-9788-db39a3f43cd3)

@TramNguyenICT
Comment
