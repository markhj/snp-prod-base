[
  id: js-random-number-between-x-and-y
  tags:
  locations:
]: #

# Random number between X and Y


````js
function random(min, max) {
  return Math.floor(Math.random() * (max - min + 1)) + min;
}
````
