<h1> Redis </h1>
<p> Redis is an open source (BSD licensed), in-memory data structure store, used as a database, cache and message broker. 
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


