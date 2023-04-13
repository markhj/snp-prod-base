[
  id: php-configure-cacert
  tags:
    - php.ini
  locations:
]: #

# Configure cURL cacert

Download ``cacert.pem`` from: https://curl.se/docs/caextract.html.

Put it somewhere on your machine.

Open ``php.ini``, locate the line with ``curl.cainfo``, and change its value to the path of the ``cacert.pem`` file.

````bash
curl.cainfo = /path/to/cacert.pem
````

Remember to remove the prefixed ``;`` if present.

> ℹ️ Running instances of PHP/Apache may need to be restarted. CLI mode should function immediately.
