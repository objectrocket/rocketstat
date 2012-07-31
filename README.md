<h2>Overview</h2>
Rocketstat is essentially a copy of the <a href=https://github.com/kgorman/mongostat>original</a> python 'mongostat' utility written by Kenny Gorman in 2010, however it's designed to utilize the <a href=http://www.objectrocket.com>ObjectRocket</a> public API as a data source.  The functionality should roughly mirror the 10gen utility called 'mongostat' where it makes sense.  Some stats don't translate to the ObjectRocket cloud service and thus are omitted.  A guideline of the values reported can be found in the <a href=http://docs.mongodb.org/manual/reference/mongostat/>10gen docs</a>.

Requires: <a href=http://www.python.org/>python</a>, <a href=http://api.mongodb.org/python/current/>pymongo</a>

<h2>Usage</h2>
<p>
	In order to use rocketstat you will need an ObjectRocket API Key.  You will need to signup for a <a href=http://www.objectrocket.com>Objectrocket account</a>, create an instance, then select the API tab under your instance.  Copy/Paste the API key to the command line below.
<p>
	Rocketstat reports aggregate stats across your entire instance.  That means that your data is summated across all the shards.  You are seeing total overall statistics about your MongoDB instance on ObjectRocket.
<pre>
Usage: rocketstat [options]

Options:
  -h, --help           show this help message and exit
  --hostname=HOSTNAME  hostname to connect to
  --port=PORT          port to connect to
  --api_key=API_KEY    ObjectRocket API key.  See www.objectrocket.com for an account


$>python rocketstat --api_key=<your api key>
</pre>

<h2>License</h2>
Copyright (c) 2012 ObjectRocket Inc.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.