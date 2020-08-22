<h1> Redis </h1>
<p> Redis is an open source (BSD licensed), in-memory data structure , used as a database, cache and message . 
It supports data structures such as strings, hashes, lists, sets, sorted sets with range queries, bitmaps, hyperloglogs,
geospatial indexes with radius queries and streams. </p>

![redis_icon](https://user-images.githubusercontent.com/62602944/90469566-fbf96600-e13a-11ea-917c-72e2122b28e3.png)

<h1> Installing On Linux </h1>
<p> First of all you go to your Terminal . Create a new File. For create new file type: </p><pre><code>mkdir (file_name)</code></pre>

![a](https://user-images.githubusercontent.com/62602944/90470119-7676b580-e13c-11ea-9d2b-8c4f37aa56aa.png)

<p> Now go to the file directory. </p> <pre><code>cd (file_name)</code></pre>

![b](https://user-images.githubusercontent.com/62602944/90470443-5e536600-e13d-11ea-9f7b-6fad78aff548.png)

<p> Now download Redis.For this type this command: </p> <pre><code>wget http://download.redis.io/releases/redis-6.0.6.tar.gz</code></pre>

![2](https://user-images.githubusercontent.com/62602944/90470710-f6514f80-e13d-11ea-92db-3ac8b3b7993c.png)

<p> Downloaded Redis file.But this file was zip. For Unzip Redis file type this command: </p> <pre><code> tar xzf redis-6.0.6.tar.gz</code></pre>

![3](https://user-images.githubusercontent.com/62602944/90470881-711a6a80-e13e-11ea-9869-69416df5d5f7.png)

<P> For install Redis type this command: </p> <pre><code>make</code> </pre>

![4](https://user-images.githubusercontent.com/62602944/90471237-7af09d80-e13f-11ea-830e-80e2ed609c7a.png)

<p> Now you open a new terminal. Go to the file directory.The binaries that are now compiled are available in the src directory. Run Redis with: </p><pre><code>src/redis-server</code></pre>

![Screenshot from 2020-08-17 23-23-00](https://user-images.githubusercontent.com/62602944/90471973-41b92d00-e141-11ea-9d00-ffb3863e57db.png)

<p> Connect to the redis-server type this command:</p> <pre><code>src/redis-cli</code></pre>

![5](https://user-images.githubusercontent.com/62602944/90472192-ca37cd80-e141-11ea-8c6e-a394bcc7be42.png)



<h1> Data Type </h1>
<h2> Strings </h2>
<p>Strings are the most basic kind of Redis value. Redis Strings are binary safe, this means that a Redis string can contain any kind of data, for instance a JPEG image or a serialized Ruby object.</p>
<p> A String value can be at max 512 Megabytes in length.</p>
<h3> String Commands</h3>
<p> For set value</p> 
<pre><code>set (key) (value)</code></pre>

![a1](https://user-images.githubusercontent.com/62602944/90949280-fb2d4080-e468-11ea-80c4-fe18966c7396.png)

<p>For get value</p>
<pre><code>get (key)</code></pre>

![1](https://user-images.githubusercontent.com/62602944/90949283-03857b80-e469-11ea-9bdc-418423ea8925.png)

<p>See all keys </p>
<pre><code>keys *</code></pre>

![2](https://user-images.githubusercontent.com/62602944/90949315-2b74df00-e469-11ea-8594-272ed0141d7c.png)

<p>For delete key</p>
<pre><code>del (key)</code></pre>

![3](https://user-images.githubusercontent.com/62602944/90949318-2e6fcf80-e469-11ea-88a4-21ccb0e8747e.png)

<p> Flush all the keys</p> 
<pre><code> flushall</code></pre>

![4](https://user-images.githubusercontent.com/62602944/90949321-33cd1a00-e469-11ea-861a-e17c45fe36be.png)

<p> Define time. After this time(second) the key will be delete.</p>
<pre><code>setex (key) (second) (value)</code></pre>

<p> See how many time to delete the key </p>
<pre> <code>ttl (key)</code></pre>

![5](https://user-images.githubusercontent.com/62602944/90949327-39c2fb00-e469-11ea-9a37-dbaebe72788c.png)

<p> If you have same key It did not set.If you have not same key It set this value</p>
<pre><code>setnx (key) (value)</code></pre>

![6](https://user-images.githubusercontent.com/62602944/90949329-3d568200-e469-11ea-97f8-41b7148ca563.png)

<p> See key values length</p>
<pre><code>strlen (key)</code></pre>

![7](https://user-images.githubusercontent.com/62602944/90949332-41829f80-e469-11ea-9f3b-66e38247ffb3.png)

<p> Define time. After this time(millisecond) the key will be delete.</p>
<pre><code>psetex (key) (time) (value)</code></pre>
  
![8](https://user-images.githubusercontent.com/62602944/90949333-45162680-e469-11ea-9b35-b8720c30e1a9.png)

<p> Set multiple keys</p>
<pre><code>mset (key) (value) (key) (value).....</code></pre>

![9](https://user-images.githubusercontent.com/62602944/90949335-49dada80-e469-11ea-8fe6-bcc1f8339f4a.png)

<p> Auto increment</p>
<pre><code>incr (key)</code></pre>

<p> Auto decrement </p> 
<pre><code> decr (key)</code></pre>

<p> Increment by number</p>
<pre><code>imcrby (key) (number)</code></pre>

<p> Decrement by number</p>
<pre><code>decrby (key) (number)</code></pre>

![10](https://user-images.githubusercontent.com/62602944/90949337-4d6e6180-e469-11ea-9aa5-6b61557daad5.png)

<p>Add with previous value</p>
<pre><code>append (key) ("value")</code></pre>

![11](https://user-images.githubusercontent.com/62602944/90949339-5101e880-e469-11ea-972d-060298c9535c.png)












<h2>Lists</h2>
<p>Redis Lists are simply lists of strings, sorted by insertion order. It is possible to add elements to a Redis List pushing new elements on the head (on the left) or on the tail (on the right) of the list.</p>
<p>The LPUSH command inserts a new element on the head, while RPUSH inserts a new element on the tail. A new list is created when one of this operations is performed against an empty key. Similarly the key is removed from the key space if a list operation will empty the list. These are very handy semantics since all the list commands will behave exactly like they were called with an empty list if called with a non-existing key as argument.</p>
<h3>Lists command</h3>
<p>Set value top</p><pre><code>lpush (key) (value) (value)....</code></pre>

![22](https://user-images.githubusercontent.com/62602944/90949379-7bec3c80-e469-11ea-99fe-35d8caa17693.png)

<p>Show all data</p><pre><code>lrange (key) 0 -1</code></pre>

![23](https://user-images.githubusercontent.com/62602944/90949381-7ee72d00-e469-11ea-81b1-2e9a03721756.png)

<p>Delete from the left side</p><pre><code>lpop (key)</code></pre>
<p>Note:Delete data from top side</p>

![24](https://user-images.githubusercontent.com/62602944/90949384-81e21d80-e469-11ea-8ce7-ac731f0ee7a4.png)

<p>Set value bottom</p><pre><code>rpush (key) (value) (value)....</code></pre>
<p>Delete from the right side</p><pre><code>rpop (key)</code></pre>
<p>Note:Delete data from bottom side</p>

![25](https://user-images.githubusercontent.com/62602944/90949387-86a6d180-e469-11ea-99c0-cbf302a18144.png)

<p>Show the length of list</p><pre><code>llen (key)</code></pre>

![26](https://user-images.githubusercontent.com/62602944/90949388-89a1c200-e469-11ea-8a77-3b35c507fb58.png)

<p>See left value serial number</p><pre><code>lindex (key) (index)</code></pre>

![27](https://user-images.githubusercontent.com/62602944/90949391-8c041c00-e469-11ea-930f-c307e08fa9c7.png)

<p>Add value in the fixed position</p><pre><code>linsert (key) (BEFORE|AFTER) (pivot) (value)</code></pre>

![28](https://user-images.githubusercontent.com/62602944/90949394-90303980-e469-11ea-90f1-2327d939602c.png)







<h2>Sets</h2>
<p>Redis Sets are an unordered collection of Strings. It is possible to add, remove, and test for existence of members in O(1) (constant time regardless of the number of elements contained inside the Set).</p>
<p>Redis Sets have the desirable property of not allowing repeated members. Adding the same element multiple times will result in a set having a single copy of this element. Practically speaking this means that adding a member does not require a check if exists then add operation.</p>
<h3>Sets commands</h3>
<p>Set value</p><pre><code>sadd (key) (member)</code></pre>

![29](https://user-images.githubusercontent.com/62602944/90949399-96261a80-e469-11ea-8f1c-a52b36077fef.png)

<p>Show values</p><pre><code>smembers</code></pre>

![30](https://user-images.githubusercontent.com/62602944/90949449-dbe2e300-e469-11ea-8901-2479074112a0.png)

<p>Length of set</p><pre><code>scard (key)</code></pre>

![31](https://user-images.githubusercontent.com/62602944/90949408-9c1bfb80-e469-11ea-847c-e68de6f72df9.png)

<p>Different between key</p><pre><code>sdiff (key) (key)</code></pre>

![32](https://user-images.githubusercontent.com/62602944/90949411-9e7e5580-e469-11ea-9cf6-d50d1122e033.png)

<p>Diffrent between key store in the destination </p><pre><code>sdiffstore (destination) (key) (key)</code></pre>

![33](https://user-images.githubusercontent.com/62602944/90949412-a2aa7300-e469-11ea-9f3e-b78d01c3da0f.png)

<p>Like as union set</p><pre><code>sunion (key) (key)</code></pre>

![34](https://user-images.githubusercontent.com/62602944/90949414-a5a56380-e469-11ea-8f50-8cc0a73f2d03.png)

<p>Union value store in the first destination</p><pre><code>sunionstre</code></pre>

![35](https://user-images.githubusercontent.com/62602944/90949418-adfd9e80-e469-11ea-8c19-4394569f1485.png)

<p>Delete fixed member</p><pre><code>srem (key) (member)</code></pre>

![36](https://user-images.githubusercontent.com/62602944/90949422-b229bc00-e469-11ea-9e6e-3db5155d99a8.png)

<p>Like an inter set</p><pre><code>sinter (key) (key)</code></pre>

![37](https://user-images.githubusercontent.com/62602944/90949423-b6ee7000-e469-11ea-911c-27ae478bb3e4.png)

<p>Inter value store in the first destination</P><pre><code>sinerstore (destination) (key) (key)</code></pre>

![38](https://user-images.githubusercontent.com/62602944/90949425-b9e96080-e469-11ea-9bf3-30d52317e175.png)


<h2> Hashes </h2>
<p>Redis Hashes are maps between string fields and string values, so they are the perfect data type to represent objects</p>
<h3> Hashes command</h3>
<p>Set multiple key</p><pre><code>hmset (key) (field) (value) (field) (value)....</code></pre>

![12](https://user-images.githubusercontent.com/62602944/90949342-53fcd900-e469-11ea-8b74-fb1eca09d847.png)

<p>Get field value</p><pre><code>hget (key) (field)</code></pre>

![13](https://user-images.githubusercontent.com/62602944/90949347-57906000-e469-11ea-9551-6df6c480f2b0.png)

<p>Get all data with field </p><pre><code>hgetall (key)</code></pre>

![14](https://user-images.githubusercontent.com/62602944/90949349-5bbc7d80-e469-11ea-89a8-b6136736bb57.png)

<p>Search field name</p><pre><code>hexists (key) (field)</code></pre>

![15](https://user-images.githubusercontent.com/62602944/90949354-5f500480-e469-11ea-88ed-bb125d7dc9ab.png)

<p>Delete fixd field value</p><pre><code>hdel (key) (field)</code></pre>

![16](https://user-images.githubusercontent.com/62602944/90949359-62e38b80-e469-11ea-8179-d2c30c0ad87e.png)

<p>If the field exists don't set field value. If the field exists set the field value.</p>
<p>Show all fields</p><pre><code>hkeys (key)</code></pre>

![17](https://user-images.githubusercontent.com/62602944/90949363-65de7c00-e469-11ea-8c31-39d400ddefc6.png)

<p>Increage by number</p> <pre><code>incrby (key) (field) (number)</code></pre>


![18](https://user-images.githubusercontent.com/62602944/90949364-69720300-e469-11ea-8aec-b2d805babb5d.png)

<p>Show all field values</p><pre><code>hvals (key)</code></pre>

![19](https://user-images.githubusercontent.com/62602944/90949365-6bd45d00-e469-11ea-8eed-24c1b6f0a409.png)

<p>Show how many field</p><pre><code>hlen (key)</code></pre>

![20](https://user-images.githubusercontent.com/62602944/90949368-6ecf4d80-e469-11ea-9f72-efb2c2873153.png)

<p>See multiple field value</p><pre><code>hmget (key) (field) (field)....</code></pre>

![21](https://user-images.githubusercontent.com/62602944/90949371-74c52e80-e469-11ea-92fe-9fad124b256b.png)



<h2>Sorted sets</h2>
<p>Redis Sorted Sets are, similarly to Redis Sets, non repeating collections of Strings. The difference is that every member of a Sorted Set is associated with score, that is used in order to take the sorted set ordered, from the smallest to the greatest score. While members are unique, scores may be repeated.</p>
<h3>Shorted sets command</h3>
<p>Add score value</p><pre><code>zadd (key) (score) (value) (score)....</code></pre>

![39](https://user-images.githubusercontent.com/62602944/90949429-bd7ce780-e469-11ea-87de-7e09d3f8a8f7.png)

<p>See all score value</p><pre><code>zrange (key) 0 -1</code></pre>

![40](https://user-images.githubusercontent.com/62602944/90949431-c077d800-e469-11ea-9b01-3f5baa29aa4f.png)

<p>See value rank</p><pre><code>zrank (key) (value)</code></pre>

![41](https://user-images.githubusercontent.com/62602944/90949435-c53c8c00-e469-11ea-9309-f128f093d06e.png)
