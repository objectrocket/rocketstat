Rocketstat is essentially a copy of the origional 'mongostat' utility written by Kenny Gorman, however it's designed to utilize the ObjectRocket public API as a data source.  The functionality should roughly mirror the 10gen utility called 'mongostat'

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