# Exercises 3
### Question 1
SELECT country.name as "country name", airport.name as "airport name"
    -> FROM airport, country
    -> WHERE country.name = "Iceland"
    -> AND airport.iso_country = country.iso_country;

![Screenshot 2024-09-09 153747](https://github.com/user-attachments/assets/a9f4adc4-d34f-41ac-8f71-4ba37340e1ad)
