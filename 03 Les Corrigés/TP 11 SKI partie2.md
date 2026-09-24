Salika

```sql
SELECT 
    f.title,
    COUNT(r.rental_id) AS nombre_locations
FROM film AS f
JOIN inventory AS i 
    ON f.film_id = i.film_id
JOIN rental AS r 
    ON i.inventory_id = r.inventory_id
GROUP BY f.film_id, f.title
ORDER BY nombre_locations DESC
LIMIT 5;
```
```sql
SELECT
    c.customer_id,
    CONCAT(c.first_name, ' ', c.last_name) AS client,
    COUNT(r.rental_id) AS nb_locations
FROM customer c
JOIN rental r ON c.customer_id = r.customer_id
GROUP BY c.customer_id, c.first_name, c.last_name
ORDER BY nb_locations DESC
LIMIT 5;
```


