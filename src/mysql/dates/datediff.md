[
  id: mysql-date-diff
  tags:
  locations:
]: #

# Difference in days

Gives the difference in days looking purely at the date, and not the time.

````bash
DATEDIFF(a, b)
````

If the oldest date is first the value is given as negative.

## Behavior

Timestamp is not taken into consideration (i.e. it's not about each 24 hour, it's about the date)
````mysql
SELECT DATEDIFF("2023-04-18 03:00", "2023-04-17 23:00")   # 1
````

# Documentation
https://dev.mysql.com/doc/refman/8.0/en/date-and-time-functions.html#function_datediff

