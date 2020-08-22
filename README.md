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
<p> For set value</p> <code>set (key) (value)</code>

![a1](https://user-images.githubusercontent.com/62602944/90949280-fb2d4080-e468-11ea-80c4-fe18966c7396.png)

<p>For get value</p><code>get (key)</code>

![1](https://user-images.githubusercontent.com/62602944/90949283-03857b80-e469-11ea-9bdc-418423ea8925.png)

<p>See all keys </p><code>keys *</code>

![2](https://user-images.githubusercontent.com/62602944/90949315-2b74df00-e469-11ea-8594-272ed0141d7c.png)

<p>For delete key</p><code>del (key)</code>

![3](https://user-images.githubusercontent.com/62602944/90949318-2e6fcf80-e469-11ea-88a4-21ccb0e8747e.png)

<p> Flush all the keys</p> <code> flushall</code>

![4](https://user-images.githubusercontent.com/62602944/90949321-33cd1a00-e469-11ea-861a-e17c45fe36be.png)

<p> Define time. After this time(second) the key will be delete.</p><code>setex (key) (second) (value)</code>
<p> See how many time to delete the key </p> <code>ttl (key)</code>

![5](https://user-images.githubusercontent.com/62602944/90949327-39c2fb00-e469-11ea-9a37-dbaebe72788c.png)

<p> If you have same key It did not set.If you have not same key It set this value</p><code>setnx (key) (value)</code>

![6](https://user-images.githubusercontent.com/62602944/90949329-3d568200-e469-11ea-97f8-41b7148ca563.png)

<p> See key values length</p><code>strlen (key)</code>

![7](https://user-images.githubusercontent.com/62602944/90949332-41829f80-e469-11ea-9f3b-66e38247ffb3.png)

<p> Define time. After this time(millisecond) the key will be delete.<p><code>psetex (key) (time) (value)</code>
  
![8](https://user-images.githubusercontent.com/62602944/90949333-45162680-e469-11ea-9b35-b8720c30e1a9.png)

<p> Set multiple keys</p><code>mset (key) (value) (key) (value).....</code>

![9](https://user-images.githubusercontent.com/62602944/90949335-49dada80-e469-11ea-8fe6-bcc1f8339f4a.png)

<p> Auto increment</p><code>incr (key)</code>
<p> Auto decrement </p> <code> decr (key)</code>
<p> Increment by number</p><code>imcrby (key) (number)</code>
<p> Decrement by number</p><code>decrby (key) (number)</code>

![10](https://user-images.githubusercontent.com/62602944/90949337-4d6e6180-e469-11ea-9aa5-6b61557daad5.png)

<p>Add with previous value</p><code>append (key) ("value")</code>

![11](https://user-images.githubusercontent.com/62602944/90949339-5101e880-e469-11ea-972d-060298c9535c.png)

<h2> Hashes </h2>
<p>Redis Hashes are maps between string fields and string values, so they are the perfect data type to represent objects</p>

