[
  id: mysql-create-user-with-privileges
  tags:
  locations:
]: #

# Create user (with privileges)

Create a new user with access to ``<database>``. Set to ``*`` for full access (not recommended).

````mysql
GRANT ALL PRIVILEGES ON <database>.* TO 'username'@'localhost' IDENTIFIED BY 'password';
````
