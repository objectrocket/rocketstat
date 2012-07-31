Rocketstat is essentially a copy of the <a href=https://github.com/kgorman/mongostat>original</a> 'mongostat' utility written by Kenny Gorman in 2010, however it's designed to utilize the <a href=http://www.objectrocket.com>ObjectRocket</a> public API as a data source.  The functionality should roughly mirror the 10gen utility called 'mongostat' where it makes sense.  Some stats don't translate to the ObjectRocket cloud service and thus are omitted.  A guideline of the values reported can be found in the <a href=http://docs.mongodb.org/manual/reference/mongostat/>10gen docs</a>.

Requires: python, pymongo

<pre>
Usage: rocketstat [options]

Options:
  -h, --help           show this help message and exit
  --hostname=HOSTNAME  hostname to connect to
  --port=PORT          port to connect to
  --api_key=API_KEY    ObjectRocket API key.  See www.objectrocket.com for an account


$>python rocketstat --api_key=foo
</pre>