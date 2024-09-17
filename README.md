# SQL-Project-
SELECT * FROM employee
ORDER BY levels DESC
LIMIT 1

SELECT COUNT(invoice_id) as invoices, billing_country FROM invoice
GROUP BY billing_country
ORDER BY invoices DESC

SELECT total FROM invoice
ORDER BY total DESC
LIMIT 3

SELECT billing_city, SUM(total) AS invoice_total FROM invoice
GROUP BY billing_city
ORDER BY invoice_total DESC
LIMIT 1

SELECT customer.customer_id, customer.first_name, customer.last_name, SUM(invoice.total) AS total FROM customer
JOIN invoice ON customer.customer_id = invoice.customer_id
GROUP BY 1
ORDER BY 4 DESC
LIMIT 1
