# BD-kennedy-salvador
los salvé
VINO SU SALVADOR👀
SELECT film_actor.actor_id, film.title
FROM film
INNER JOIN film_actor
ON film_actor.film_id=film.film_id;


#1
SELECT customer.first_name, payment.amount
FROM payment
INNER JOIN customer
ON customer.customer_id = payment.customer_id
#2
SELECT title, actor.actor_id
FROM actor
INNER JOIN film_actor ON film_actor.actor_id= actor.actor_id
INNER JOIN film ON film_actor.film_id= film.film_id
#3
SELECT actor.last_name, film.title
FROM actor
INNER JOIN film_actor ON film_actor.actor_id= actor.actor_id
INNER JOIN film ON film_actor.film_id= film.film_id
ORDER BY last_name;
#4
SELECT customer.first_name, payment.amount
FROM customer
INNER JOIN payment
ON payment.customer_id= customer.customer_id
ORDER BY amount desc
LIMIT 5;
#5
SELECT actor.first_name, film.length, film.title
FROM actor
INNER JOIN film_actor ON film_actor.actor_id= actor.actor_id
INNER JOIN film ON film_actor.film_id= film.film_id
WHERE film.length > 119;
#6
SELECT DISTINCT customer.first_name, payment.amount, customer.last_name
FROM payment
INNER JOIN customer ON customer.customer_id= payment.customer_id
ORDER BY customer.last_name ASC, payment.amount ASC;
#7
SELECT actor.first_name, film.length, film.title
FROM actor
INNER JOIN film_actor ON film_actor.actor_id= actor.actor_id
INNER JOIN film ON film_actor.film_id= film.film_id
WHERE film.title LIKE 'A%';

#8
SELECT actor.first_name, film.length, film.title
FROM actor
INNER JOIN film_actor ON film_actor.actor_id= actor.actor_id
INNER JOIN film ON film_actor.film_id= film.film_id
WHERE film.length > 179;
#9
SELECT customer.first_name, customer.last_name, payment.amount
FROM customer
INNER JOIN payment ON payment.customer_id= customer.customer_id
WHERE amount > 6.99
ORDER BY payment.amount ASC;
#10
SELECT actor.first_name, actor.last_name, film.title, film.length
FROM actor
INNER JOIN film_actor ON film_actor.actor_id= actor.actor_id
INNER JOIN film ON film_actor.film_id= film.film_id
ORDER BY film.length;
#11
