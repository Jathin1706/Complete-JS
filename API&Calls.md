---


---

<h2 id="🔹-1️⃣-what-is-an-api-call">🔹 <strong>1️⃣ What is an API Call?</strong></h2>
<p>An <strong>API call</strong> is a request sent to a server to retrieve or modify data. The server processes the request and responds with data.</p>
<p>✅ <strong>Common HTTP Methods in API Calls</strong></p>

<table>
<thead>
<tr>
<th>HTTP Method</th>
<th>Description</th>
<th>Example</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>GET</strong></td>
<td>Fetch data from the server</td>
<td>Fetch user details</td>
</tr>
<tr>
<td><strong>POST</strong></td>
<td>Send new data to the server</td>
<td>Create a new user</td>
</tr>
<tr>
<td><strong>PUT</strong></td>
<td>Update existing data</td>
<td>Update user info</td>
</tr>
<tr>
<td><strong>PATCH</strong></td>
<td>Partially update data</td>
<td>Modify a specific field</td>
</tr>
<tr>
<td><strong>DELETE</strong></td>
<td>Remove data from the server</td>
<td>Delete a user</td>
</tr>
</tbody>
</table><hr>
<h2 id="🔹-2️⃣-methods-to-make-api-calls-in-javascript">🔹 <strong>2️⃣ Methods to Make API Calls in JavaScript</strong></h2>
<h3 id="✅-1.-using-fetch-modern--recommended">✅ <strong>1. Using <code>fetch()</code> (Modern &amp; Recommended)</strong></h3>
<p>The <code>fetch()</code> API is a built-in JavaScript method for making network requests.</p>
<h4 id="📌-get-request-fetching-data">📌 <strong>GET Request (Fetching Data)</strong></h4>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token function">fetch</span><span class="token punctuation">(</span><span class="token string">"https://jsonplaceholder.typicode.com/users"</span><span class="token punctuation">)</span>

  <span class="token punctuation">.</span><span class="token function">then</span><span class="token punctuation">(</span>response <span class="token operator">=&gt;</span> response<span class="token punctuation">.</span><span class="token function">json</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token comment">// Convert response to JSON </span>
  <span class="token punctuation">.</span><span class="token function">then</span><span class="token punctuation">(</span>data <span class="token operator">=&gt;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>data<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token comment">// Handle data </span>
  <span class="token punctuation">.</span><span class="token keyword">catch</span><span class="token punctuation">(</span>error <span class="token operator">=&gt;</span> console<span class="token punctuation">.</span><span class="token function">error</span><span class="token punctuation">(</span><span class="token string">"Error:"</span><span class="token punctuation">,</span> error<span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Handle error</span>
</code></pre>
<h4 id="📌-post-request-sending-data">📌 <strong>POST Request (Sending Data)</strong></h4>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token function">fetch</span><span class="token punctuation">(</span><span class="token string">"https://jsonplaceholder.typicode.com/posts"</span><span class="token punctuation">,</span> <span class="token punctuation">{</span> method<span class="token punctuation">:</span> <span class="token string">"POST"</span><span class="token punctuation">,</span> headers<span class="token punctuation">:</span> <span class="token punctuation">{</span> <span class="token string">"Content-Type"</span><span class="token punctuation">:</span> <span class="token string">"application/json"</span> <span class="token punctuation">}</span><span class="token punctuation">,</span> body<span class="token punctuation">:</span> JSON<span class="token punctuation">.</span><span class="token function">stringify</span><span class="token punctuation">(</span><span class="token punctuation">{</span> title<span class="token punctuation">:</span> <span class="token string">"New Post"</span><span class="token punctuation">,</span> body<span class="token punctuation">:</span> <span class="token string">"Hello World!"</span> <span class="token punctuation">}</span><span class="token punctuation">)</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span>
  <span class="token punctuation">.</span><span class="token function">then</span><span class="token punctuation">(</span>response <span class="token operator">=&gt;</span> response<span class="token punctuation">.</span><span class="token function">json</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span>
  <span class="token punctuation">.</span><span class="token function">then</span><span class="token punctuation">(</span>data <span class="token operator">=&gt;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Created:"</span><span class="token punctuation">,</span> data<span class="token punctuation">)</span><span class="token punctuation">)</span>
  <span class="token punctuation">.</span><span class="token keyword">catch</span><span class="token punctuation">(</span>error <span class="token operator">=&gt;</span> console<span class="token punctuation">.</span><span class="token function">error</span><span class="token punctuation">(</span><span class="token string">"Error:"</span><span class="token punctuation">,</span> error<span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<hr>
<h3 id="✅-2.-using-asyncawait-with-fetch">✅ <strong>2. Using <code>async/await</code> with <code>fetch()</code></strong></h3>
<p>A cleaner way to write asynchronous API calls.</p>
<h4 id="📌-get-request-fetching-data-1">📌 <strong>GET Request (Fetching Data)</strong></h4>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">async</span>  <span class="token keyword">function</span>  <span class="token function">getUsers</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> 
<span class="token keyword">try</span> <span class="token punctuation">{</span> <span class="token keyword">let</span> response <span class="token operator">=</span> <span class="token keyword">await</span>  <span class="token function">fetch</span><span class="token punctuation">(</span><span class="token string">"https://jsonplaceholder.typicode.com/users"</span><span class="token punctuation">)</span><span class="token punctuation">;</span> 
<span class="token keyword">let</span> data <span class="token operator">=</span> <span class="token keyword">await</span> response<span class="token punctuation">.</span><span class="token function">json</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span> 
console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>data<span class="token punctuation">)</span><span class="token punctuation">;</span>

  <span class="token punctuation">}</span> 
 <span class="token keyword">catch</span> <span class="token punctuation">(</span><span class="token class-name">error</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  console<span class="token punctuation">.</span><span class="token function">error</span><span class="token punctuation">(</span><span class="token string">"Error:"</span><span class="token punctuation">,</span> error<span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span> <span class="token function">getUsers</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<h4 id="📌-post-request-sending-data-1">📌 <strong>POST Request (Sending Data)</strong></h4>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">async</span>  <span class="token keyword">function</span>  <span class="token function">createPost</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token keyword">try</span> <span class="token punctuation">{</span> <span class="token keyword">let</span> response <span class="token operator">=</span> <span class="token keyword">await</span>  <span class="token function">fetch</span><span class="token punctuation">(</span><span class="token string">"https://jsonplaceholder.typicode.com/posts"</span><span class="token punctuation">,</span> <span class="token punctuation">{</span> method<span class="token punctuation">:</span> <span class="token string">"POST"</span><span class="token punctuation">,</span> headers<span class="token punctuation">:</span> <span class="token punctuation">{</span> <span class="token string">"Content-Type"</span><span class="token punctuation">:</span> <span class="token string">"application/json"</span> <span class="token punctuation">}</span><span class="token punctuation">,</span> body<span class="token punctuation">:</span> JSON<span class="token punctuation">.</span><span class="token function">stringify</span><span class="token punctuation">(</span><span class="token punctuation">{</span> title<span class="token punctuation">:</span> <span class="token string">"Async Post"</span><span class="token punctuation">,</span> body<span class="token punctuation">:</span> <span class="token string">"Hello Async!"</span> <span class="token punctuation">}</span><span class="token punctuation">)</span>
    <span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token keyword">let</span> data <span class="token operator">=</span> <span class="token keyword">await</span> response<span class="token punctuation">.</span><span class="token function">json</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Created:"</span><span class="token punctuation">,</span> data<span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span> <span class="token keyword">catch</span> <span class="token punctuation">(</span><span class="token class-name">error</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> console<span class="token punctuation">.</span><span class="token function">error</span><span class="token punctuation">(</span><span class="token string">"Error:"</span><span class="token punctuation">,</span> error<span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span> <span class="token function">createPost</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<hr>
<h3 id="✅-3.-using-xmlhttprequest-older-method">✅ <strong>3. Using <code>XMLHttpRequest</code> (Older Method)</strong></h3>
<p>Used before <code>fetch()</code>, but still seen in legacy code.</p>
<h4 id="📌-get-request">📌 <strong>GET Request</strong></h4>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">let</span> xhr <span class="token operator">=</span> <span class="token keyword">new</span>  <span class="token class-name">XMLHttpRequest</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
xhr<span class="token punctuation">.</span><span class="token function">open</span><span class="token punctuation">(</span><span class="token string">"GET"</span><span class="token punctuation">,</span> <span class="token string">"https://jsonplaceholder.typicode.com/users"</span><span class="token punctuation">,</span> <span class="token boolean">true</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
xhr<span class="token punctuation">.</span><span class="token function-variable function">onload</span> <span class="token operator">=</span> <span class="token keyword">function</span> <span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token keyword">if</span> <span class="token punctuation">(</span>xhr<span class="token punctuation">.</span>status <span class="token operator">===</span> <span class="token number">200</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>JSON<span class="token punctuation">.</span><span class="token function">parse</span><span class="token punctuation">(</span>xhr<span class="token punctuation">.</span>responseText<span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span><span class="token punctuation">;</span>
xhr<span class="token punctuation">.</span><span class="token function">send</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<hr>
<h3 id="✅-4.-using-axios-third-party-library">✅ <strong>4. Using Axios (Third-Party Library)</strong></h3>
<p>Axios is a <strong>popular library</strong> for API calls that supports automatic JSON conversion and error handling.</p>
<p>📌 <strong>Install Axios:</strong></p>
<p>sh</p>
<p><code>npm install axios</code></p>
<h4 id="📌-get-request-1">📌 <strong>GET Request</strong></h4>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js">axios<span class="token punctuation">.</span><span class="token keyword">get</span><span class="token punctuation">(</span><span class="token string">"https://jsonplaceholder.typicode.com/users"</span><span class="token punctuation">)</span>
  <span class="token punctuation">.</span><span class="token function">then</span><span class="token punctuation">(</span>response <span class="token operator">=&gt;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>response<span class="token punctuation">.</span>data<span class="token punctuation">)</span><span class="token punctuation">)</span>
  <span class="token punctuation">.</span><span class="token keyword">catch</span><span class="token punctuation">(</span>error <span class="token operator">=&gt;</span> console<span class="token punctuation">.</span><span class="token function">error</span><span class="token punctuation">(</span><span class="token string">"Error:"</span><span class="token punctuation">,</span> error<span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<h4 id="📌-post-request">📌 <strong>POST Request</strong></h4>
<p>js</p>
<p>CopyEdit</p>
<p><code>axios.post("https://jsonplaceholder.typicode.com/posts", { title: "Axios Post", body: "Hello Axios!" }) .then(response =&gt; console.log("Created:", response.data)) .catch(error =&gt; console.error("Error:", error));</code></p>
<hr>
<h2 id="🔹-3️⃣-types-of-api-calls">🔹 <strong>3️⃣ Types of API Calls</strong></h2>
<p>APIs can be categorized based on their <strong>communication method</strong> and <strong>response format</strong>.</p>
<h3 id="✅-1.-rest-api-representational-state-transfer">✅ <strong>1. REST API (Representational State Transfer)</strong></h3>
<ul>
<li>Most common API type.</li>
<li>Uses <strong>HTTP methods</strong> (GET, POST, PUT, DELETE).</li>
<li>Returns <strong>JSON or XML</strong>.</li>
<li>Example: <code>https://api.example.com/users</code></li>
</ul>
<p>📌 <strong>Example REST API Response (JSON):</strong></p>
<p>json</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>  
<span class="token string">"id"</span><span class="token punctuation">:</span>  <span class="token number">1</span><span class="token punctuation">,</span> 
<span class="token string">"name"</span><span class="token punctuation">:</span>  <span class="token string">"John Doe"</span><span class="token punctuation">,</span>  
<span class="token string">"email"</span><span class="token punctuation">:</span>  <span class="token string">"john@example.com"</span>  
<span class="token punctuation">}</span>
</code></pre>
<hr>
<h3 id="✅-2.-soap-api-simple-object-access-protocol">✅ <strong>2. SOAP API (Simple Object Access Protocol)</strong></h3>
<ul>
<li>Uses <strong>XML</strong> for request &amp; response.</li>
<li>More <strong>secure</strong> but <strong>slower</strong> than REST.</li>
<li>Example: Used in <strong>banking and enterprise applications</strong>.</li>
</ul>
<p>📌 <strong>Example SOAP Request (XML Format):</strong></p>
<p>xml</p>
<pre class=" language-xml"><code class="prism  language-xml"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span><span class="token namespace">soapenv:</span>Envelope</span>  <span class="token attr-name"><span class="token namespace">xmlns:</span>soapenv</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>http://schemas.xmlsoap.org/soap/envelope/<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span> 
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span><span class="token namespace">soapenv:</span>Body</span><span class="token punctuation">&gt;</span></span> 
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>getUser</span><span class="token punctuation">&gt;</span></span> <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>id</span><span class="token punctuation">&gt;</span></span>1<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>id</span><span class="token punctuation">&gt;</span></span> <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>getUser</span><span class="token punctuation">&gt;</span></span> 
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span><span class="token namespace">soapenv:</span>Body</span><span class="token punctuation">&gt;</span></span> 
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span><span class="token namespace">soapenv:</span>Envelope</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<hr>
<h3 id="✅-3.-graphql-api">✅ <strong>3. GraphQL API</strong></h3>
<ul>
<li>Allows fetching <strong>only required data</strong> (flexible queries).</li>
<li>Uses a <strong>single endpoint</strong> for multiple queries.</li>
<li>Example: <code>https://api.example.com/graphql</code></li>
</ul>
<p>📌 <strong>Example GraphQL Query:</strong></p>
<p>graphql</p>
<p><code>{ user(id: 1) { name email } }</code></p>
<p>📌 <strong>GraphQL Response:</strong></p>
<p>json</p>
<p><code>{ "data": { "user": { "name": "John Doe", "email": "john@example.com" } } }</code></p>
<hr>
<h3 id="✅-4.-websockets-api">✅ <strong>4. WebSockets API</strong></h3>
<ul>
<li>Used for <strong>real-time communication</strong> (e.g., chat apps, stock prices).</li>
<li>Keeps a <strong>persistent connection</strong> between client and server.</li>
<li>Example: <code>wss://example.com/socket</code></li>
</ul>
<p>📌 <strong>Example WebSocket Client:</strong></p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">let</span> socket <span class="token operator">=</span> <span class="token keyword">new</span>  <span class="token class-name">WebSocket</span><span class="token punctuation">(</span><span class="token string">"wss://example.com/socket"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

socket<span class="token punctuation">.</span><span class="token function-variable function">onopen</span> <span class="token operator">=</span> <span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">=&gt;</span>  console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Connected!"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
socket<span class="token punctuation">.</span><span class="token function-variable function">onmessage</span> <span class="token operator">=</span> <span class="token punctuation">(</span>event<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Received:"</span><span class="token punctuation">,</span> event<span class="token punctuation">.</span>data<span class="token punctuation">)</span><span class="token punctuation">;</span>
socket<span class="token punctuation">.</span><span class="token function-variable function">onclose</span> <span class="token operator">=</span> <span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">=&gt;</span>  console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Disconnected!"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<hr>
<h2 id="🔹-4️⃣-comparison-table-rest-vs-soap-vs-graphql-vs-websocket">🔹 <strong>4️⃣ Comparison Table: REST vs SOAP vs GraphQL vs WebSocket</strong></h2>

<table>
<thead>
<tr>
<th>Feature</th>
<th>REST API</th>
<th>SOAP API</th>
<th>GraphQL API</th>
<th>WebSocket</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Data Format</strong></td>
<td>JSON, XML</td>
<td>XML</td>
<td>JSON</td>
<td>Binary, JSON</td>
</tr>
<tr>
<td><strong>Speed</strong></td>
<td>Fast</td>
<td>Slower</td>
<td>Faster</td>
<td>Real-time</td>
</tr>
<tr>
<td><strong>Security</strong></td>
<td>Moderate</td>
<td>High</td>
<td>Moderate</td>
<td>Moderate</td>
</tr>
<tr>
<td><strong>Use Case</strong></td>
<td>Web apps, APIs</td>
<td>Banking, Payments</td>
<td>Modern APIs</td>
<td>Chat, Live Updates</td>
</tr>
</tbody>
</table><hr>
<h2 id="🏆-key-takeaways">🏆 <strong>Key Takeaways</strong></h2>
<p>✅ <strong><code>fetch()</code></strong> is the modern way to make API calls.<br>
✅ <strong>Axios</strong> makes API calls easier with built-in JSON handling.<br>
✅ <strong>REST APIs</strong> are the most commonly used APIs.<br>
✅ <strong>GraphQL APIs</strong> allow fetching <strong>specific data only</strong>.<br>
✅ <strong>WebSockets</strong> enable <strong>real-time</strong> data transfer.</p>

