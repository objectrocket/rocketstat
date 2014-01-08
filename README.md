<h2>Overview</h2>
Rocketstat is essentially a copy of the <a href=https://github.com/kgorman/mongostat>original</a> python 'mongostat' utility written by Kenny Gorman in 2010, however it's designed to utilize the <a href=http://www.objectrocket.com>ObjectRocket</a> public API as a data source.  The functionality should roughly mirror the 10gen utility called 'mongostat' where it makes sense.  Some stats don't translate to the ObjectRocket cloud service and thus are omitted.  A guideline of the values reported can be found in the <a href=http://docs.mongodb.org/manual/reference/mongostat/>10gen docs</a>.

Requires: <a href=http://www.python.org/>python 2.7.x</a>

<h2>Usage</h2>
<p>
	In order to use rocketstat you will need an ObjectRocket API Key.  You will need to signup for a <a href=http://www.objectrocket.com>Objectrocket account</a>, create an instance, then select the API tab under your instance.  Copy/Paste the API key to the command line below.
<p>
	Rocketstat reports aggregate stats across your entire instance.  That means that your data is summated across all the shards.  You are seeing total overall statistics about your MongoDB instance on ObjectRocket.
<pre>
usage: rocketstat [-h] -a API_KEY [-H HOSTNAME]

ObjectRocket stat utility. See www.objectrocket.com for an account.

optional arguments:
  -h, --help            show this help message and exit
  -a API_KEY, --api_key API_KEY
                        ObjectRocket API key.
  -H HOSTNAME, --hostname HOSTNAME
                        hostname to connect to.

$>python rocketstat --api_key=your_api_key
  instance                  time     query    insert    update    delete     aconn     lock%    queued    active    idxacc    idxhit   idxmiss      idx%
test	     31-07-2012.09:35:20     35684        96     74488         0       372       0.0         0         2         0         0         0       0.0
test         31-07-2012.09:35:30         1         0         3         0       372       0.0         0         2         0         0         0       0.0
</pre>

<h2>License</h2>
Copyright 2012 ObjectRocket Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

<a href=http://www.apache.org/licenses/LICENSE-2.0>http://www.apache.org/licenses/LICENSE-2.0</a>

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.