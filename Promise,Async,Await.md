---


---

<h2 id="🔹-1️⃣-what-is-a-promise">🔹 1️⃣ <strong>What is a Promise?</strong></h2>
<p>A <strong>Promise</strong> is an object that represents the eventual completion (or failure) of an <strong>asynchronous operation</strong>.</p>
<p>✅ <strong>States of a Promise</strong></p>

<table>
<thead>
<tr>
<th>State</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Pending</strong></td>
<td>Initial state, neither fulfilled nor rejected.</td>
</tr>
<tr>
<td><strong>Fulfilled</strong></td>
<td>The operation completed successfully.</td>
</tr>
<tr>
<td><strong>Rejected</strong></td>
<td>The operation failed.</td>
</tr>
</tbody>
</table><p>✅ <strong>Basic Promise Syntax</strong></p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> myPromise <span class="token operator">=</span> <span class="token keyword">new</span>  <span class="token class-name">Promise</span><span class="token punctuation">(</span><span class="token punctuation">(</span>resolve<span class="token punctuation">,</span> reject<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> <span class="token punctuation">{</span> <span class="token keyword">let</span> success <span class="token operator">=</span> <span class="token boolean">true</span><span class="token punctuation">;</span> <span class="token comment">// Simulate success or failure  setTimeout(() =&gt; { if (success) { resolve("✅ Promise Resolved!"); // Success } else { reject("❌ Promise Rejected!"); // Failure }</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span> <span class="token number">2000</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

myPromise
  <span class="token punctuation">.</span><span class="token function">then</span><span class="token punctuation">(</span><span class="token punctuation">(</span>message<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>message<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token comment">// Handle success </span>
  <span class="token punctuation">.</span><span class="token keyword">catch</span><span class="token punctuation">(</span><span class="token punctuation">(</span>error<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>error<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token comment">// Handle failure</span>
  <span class="token punctuation">.</span><span class="token keyword">finally</span><span class="token punctuation">(</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">=&gt;</span>  console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"🎉 Operation Complete!"</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<hr>
<h2 id="🔹-2️⃣-chaining-promises">🔹 2️⃣ <strong>Chaining Promises</strong></h2>
<p>✅ <strong>When one promise depends on another</strong></p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">function</span>  <span class="token function">stepOne</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token keyword">return</span>  <span class="token keyword">new</span>  <span class="token class-name">Promise</span><span class="token punctuation">(</span><span class="token punctuation">(</span>resolve<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> <span class="token punctuation">{</span> <span class="token function">setTimeout</span><span class="token punctuation">(</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">=&gt;</span>  <span class="token function">resolve</span><span class="token punctuation">(</span><span class="token string">"Step 1 Done!"</span><span class="token punctuation">)</span><span class="token punctuation">,</span> <span class="token number">1000</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span> <span class="token keyword">function</span>  <span class="token function">stepTwo</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token keyword">return</span>  <span class="token keyword">new</span>  <span class="token class-name">Promise</span><span class="token punctuation">(</span><span class="token punctuation">(</span>resolve<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> <span class="token punctuation">{</span> <span class="token function">setTimeout</span><span class="token punctuation">(</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">=&gt;</span>  <span class="token function">resolve</span><span class="token punctuation">(</span><span class="token string">"Step 2 Done!"</span><span class="token punctuation">)</span><span class="token punctuation">,</span> <span class="token number">1000</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span> <span class="token comment">// Chaining  stepOne()</span>
  <span class="token punctuation">.</span><span class="token function">then</span><span class="token punctuation">(</span><span class="token punctuation">(</span>result<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> <span class="token punctuation">{</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>result<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token keyword">return</span>  <span class="token function">stepTwo</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span><span class="token punctuation">)</span>
  <span class="token punctuation">.</span><span class="token function">then</span><span class="token punctuation">(</span><span class="token punctuation">(</span>result<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>result<span class="token punctuation">)</span><span class="token punctuation">)</span>
  <span class="token punctuation">.</span><span class="token keyword">catch</span><span class="token punctuation">(</span><span class="token punctuation">(</span>error<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>error<span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<hr>
<h2 id="🔹-3️⃣-promise-methods">🔹 3️⃣ <strong>Promise Methods</strong></h2>

<table>
<thead>
<tr>
<th>Method</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>Promise.all([p1, p2])</code></td>
<td>Runs all promises in parallel and waits for <strong>all</strong> to resolve. If any fail, it rejects.</td>
</tr>
<tr>
<td><code>Promise.race([p1, p2])</code></td>
<td>Returns <strong>first resolved or rejected</strong> promise.</td>
</tr>
<tr>
<td><code>Promise.allSettled([p1, p2])</code></td>
<td>Returns <strong>all results</strong> (fulfilled or rejected).</td>
</tr>
<tr>
<td><code>Promise.any([p1, p2])</code></td>
<td>Returns <strong>first successfully resolved</strong> promise.</td>
</tr>
</tbody>
</table><p>✅ <strong>Example: <code>Promise.all()</code></strong></p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> p1 <span class="token operator">=</span> <span class="token keyword">new</span>  <span class="token class-name">Promise</span><span class="token punctuation">(</span><span class="token punctuation">(</span>resolve<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> <span class="token function">setTimeout</span><span class="token punctuation">(</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">=&gt;</span>  <span class="token function">resolve</span><span class="token punctuation">(</span><span class="token string">"First Done"</span><span class="token punctuation">)</span><span class="token punctuation">,</span> <span class="token number">2000</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">const</span> p2 <span class="token operator">=</span> <span class="token keyword">new</span>  <span class="token class-name">Promise</span><span class="token punctuation">(</span><span class="token punctuation">(</span>resolve<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> <span class="token function">setTimeout</span><span class="token punctuation">(</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">=&gt;</span>  <span class="token function">resolve</span><span class="token punctuation">(</span><span class="token string">"Second Done"</span><span class="token punctuation">)</span><span class="token punctuation">,</span> <span class="token number">3000</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span> 
Promise<span class="token punctuation">.</span><span class="token function">all</span><span class="token punctuation">(</span><span class="token punctuation">[</span>p1<span class="token punctuation">,</span> p2<span class="token punctuation">]</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">then</span><span class="token punctuation">(</span><span class="token punctuation">(</span>results<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>results<span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span> 

<span class="token comment">// ["First Done", "Second Done"]</span>
</code></pre>
<hr>
<h2 id="🔹-4️⃣-async--await-es8">🔹 4️⃣ <strong>Async &amp; Await (ES8)</strong></h2>
<p>✅ <strong><code>async</code> makes a function return a Promise.</strong><br>
✅ <strong><code>await</code> pauses execution until a Promise resolves.</strong></p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">async</span>  <span class="token keyword">function</span>  <span class="token function">fetchData</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token keyword">return</span>  <span class="token string">"Data Loaded"</span><span class="token punctuation">;</span> <span class="token comment">// Automatically wraps in a Promise } fetchData().then(console.log); // Output: "Data Loaded"</span>
</code></pre>
<hr>
<h2 id="🔹-5️⃣-using-await-with-promises">🔹 5️⃣ <strong>Using <code>await</code> with Promises</strong></h2>
<p>✅ <strong>Example: Fetching data with <code>await</code></strong></p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">function</span>  <span class="token function">getUserData</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token keyword">return</span>  <span class="token keyword">new</span>  <span class="token class-name">Promise</span><span class="token punctuation">(</span><span class="token punctuation">(</span>resolve<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> <span class="token punctuation">{</span> <span class="token function">setTimeout</span><span class="token punctuation">(</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">=&gt;</span>  <span class="token function">resolve</span><span class="token punctuation">(</span><span class="token string">"User Data Fetched"</span><span class="token punctuation">)</span><span class="token punctuation">,</span> <span class="token number">2000</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span> <span class="token keyword">async</span>  <span class="token keyword">function</span>  <span class="token function">loadUser</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Fetching user..."</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token keyword">const</span> user <span class="token operator">=</span> <span class="token keyword">await</span>  <span class="token function">getUserData</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Waits for the promise  console.log(user);</span>
<span class="token punctuation">}</span> <span class="token function">loadUser</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<p>✅ <strong>Handling Errors with <code>try...catch</code></strong></p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">async</span>  <span class="token keyword">function</span>  <span class="token function">fetchData</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token keyword">try</span> <span class="token punctuation">{</span> <span class="token keyword">let</span> response <span class="token operator">=</span> <span class="token keyword">await</span>  <span class="token function">fetch</span><span class="token punctuation">(</span><span class="token string">"https://api.example.com/data"</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token keyword">let</span> data <span class="token operator">=</span> <span class="token keyword">await</span> response<span class="token punctuation">.</span><span class="token function">json</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>data<span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span> <span class="token keyword">catch</span> <span class="token punctuation">(</span><span class="token class-name">error</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Error:"</span><span class="token punctuation">,</span> error<span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span> <span class="token function">fetchData</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<hr>
<h2 id="🔹-6️⃣-combining-asyncawait-with-promise.all">🔹 6️⃣ <strong>Combining <code>async/await</code> with <code>Promise.all()</code></strong></h2>
<p>✅ <strong>Running multiple asynchronous functions in parallel</strong></p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">async</span>  <span class="token keyword">function</span>  <span class="token function">fetchData</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token keyword">const</span> p1 <span class="token operator">=</span> <span class="token keyword">new</span>  <span class="token class-name">Promise</span><span class="token punctuation">(</span><span class="token punctuation">(</span>resolve<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> <span class="token function">setTimeout</span><span class="token punctuation">(</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">=&gt;</span>  <span class="token function">resolve</span><span class="token punctuation">(</span><span class="token string">"Data 1"</span><span class="token punctuation">)</span><span class="token punctuation">,</span> <span class="token number">2000</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token keyword">const</span> p2 <span class="token operator">=</span> <span class="token keyword">new</span>  <span class="token class-name">Promise</span><span class="token punctuation">(</span><span class="token punctuation">(</span>resolve<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> <span class="token function">setTimeout</span><span class="token punctuation">(</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">=&gt;</span>  <span class="token function">resolve</span><span class="token punctuation">(</span><span class="token string">"Data 2"</span><span class="token punctuation">)</span><span class="token punctuation">,</span> <span class="token number">3000</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token keyword">const</span> results <span class="token operator">=</span> <span class="token keyword">await</span>  Promise<span class="token punctuation">.</span><span class="token function">all</span><span class="token punctuation">(</span><span class="token punctuation">[</span>p1<span class="token punctuation">,</span> p2<span class="token punctuation">]</span><span class="token punctuation">)</span><span class="token punctuation">;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>results<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// ["Data 1", "Data 2"] } fetchData();</span>
</code></pre>
<hr>
<h2 id="🔥-summary-table">🔥 <strong>Summary Table</strong></h2>

<table>
<thead>
<tr>
<th>Feature</th>
<th>Description</th>
<th>Example</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Promise</strong></td>
<td>Represents async operation</td>
<td><code>new Promise((resolve, reject) =&gt; {...})</code></td>
</tr>
<tr>
<td><strong>.then()</strong></td>
<td>Handles resolved promise</td>
<td><code>promise.then((result) =&gt; console.log(result))</code></td>
</tr>
<tr>
<td><strong>.catch()</strong></td>
<td>Handles rejected promise</td>
<td><code>promise.catch((error) =&gt; console.log(error))</code></td>
</tr>
<tr>
<td><strong>async function</strong></td>
<td>Declares an async function</td>
<td><code>async function getData() {...}</code></td>
</tr>
<tr>
<td><strong>await</strong></td>
<td>Waits for promise to resolve</td>
<td><code>const data = await fetchData()</code></td>
</tr>
<tr>
<td><strong>Promise.all()</strong></td>
<td>Waits for all promises</td>
<td><code>Promise.all([p1, p2])</code></td>
</tr>
<tr>
<td><strong>Promise.race()</strong></td>
<td>Returns first resolved/rejected</td>
<td><code>Promise.race([p1, p2])</code></td>
</tr>
<tr>
<td><strong>try…catch</strong></td>
<td>Handles async errors</td>
<td><code>try { await fetch() } catch (err) {}</code></td>
</tr>
</tbody>
</table><hr>
<h2 id="🏆-key-takeaways">🏆 <strong>Key Takeaways</strong></h2>
<p>✅ <strong>Promises</strong> help manage asynchronous code with <code>.then()</code>, <code>.catch()</code>, <code>.finally()</code>.<br>
✅ <strong>Chaining Promises</strong> allows sequential execution.<br>
✅ <strong>Async/Await</strong> makes async code look <strong>synchronous &amp; readable</strong>.<br>
✅ <strong>Error handling</strong> with <code>try...catch</code> improves reliability.<br>
✅ <code>Promise.all()</code> runs <strong>multiple async tasks in parallel</strong>.</p>

