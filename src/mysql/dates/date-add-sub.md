[
  id: mysql-date-add-sub-interval
  tags:
  locations:
]: #

# Add/subtract interval

Add or subtract seconds, minutes, days, weeks, months and more to a date value.

````mysql
DATE_ADD(NOW(), INTERVAL 4 HOUR)
````

This will add 4 hours to the current time. You can put column name or another value where ``NOW()`` is.

> :information_source: ``HOUR`` (and others like ``WEEK``, ``DAY``, ``SECOND``, etc.) must be written as singular.

# Documentation
https://dev.mysql.com/doc/refman/8.0/en/date-and-time-functions.html