---


---

<h2 id="🔹-1️⃣-what-are-higher-order-functions">🔹 1️⃣ <strong>What are Higher-Order Functions?</strong></h2>
<p>✅ A <strong>Higher-Order Function (HOF)</strong> is a function that:</p>
<ul>
<li><strong>Takes another function</strong> as an argument <strong>(callback function)</strong>.</li>
<li><strong>Returns a function</strong> as a result.</li>
</ul>
<p>✅ <strong>Why use HOFs?</strong></p>
<ul>
<li>Make code <strong>more readable &amp; reusable</strong>.</li>
<li>Enable <strong>functional programming</strong> concepts.</li>
<li>Reduce repetition and <strong>improve abstraction</strong>.</li>
</ul>
<hr>
<h2 id="🔹-2️⃣-what-is-a-callback-function">🔹 2️⃣ <strong>What is a Callback Function?</strong></h2>
<p>✅ A <strong>callback function</strong> is a function passed as an argument to another function and executed later.</p>
<p>✅ <strong>Example of a function using a callback</strong></p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">function</span>  <span class="token function">greet</span><span class="token punctuation">(</span>name<span class="token punctuation">,</span> callback<span class="token punctuation">)</span> <span class="token punctuation">{</span> 
console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Hello, "</span> <span class="token operator">+</span> name<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token function">callback</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
 <span class="token keyword">function</span>  <span class="token function">sayBye</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Goodbye!"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span> 
<span class="token function">greet</span><span class="token punctuation">(</span><span class="token string">"Alice"</span><span class="token punctuation">,</span> sayBye<span class="token punctuation">)</span><span class="token punctuation">;</span>
 <span class="token comment">// Output:</span>
   <span class="token comment">// Hello, Alice </span>
   <span class="token comment">// Goodbye!</span>
</code></pre>
<hr>
<h2 id="🔹-3️⃣-common-higher-order-functions-in-javascript">🔹 3️⃣ <strong>Common Higher-Order Functions in JavaScript</strong></h2>
<p>md</p>

<table>
<thead>
<tr>
<th>HOF Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>forEach</strong></td>
<td>Loops through an array and applies a function to each element.</td>
</tr>
<tr>
<td><strong>map</strong></td>
<td>Creates a new array by transforming each element in the original array.</td>
</tr>
<tr>
<td><strong>filter</strong></td>
<td>Creates a new array with only elements that match a condition.</td>
</tr>
<tr>
<td><strong>reduce</strong></td>
<td>Reduces an array to a single value by applying a function.</td>
</tr>
<tr>
<td><strong>find</strong></td>
<td>Returns the first element that matches a condition.</td>
</tr>
<tr>
<td><strong>sort</strong></td>
<td>Sorts an array based on a comparison function.</td>
</tr>
</tbody>
</table><hr>
<h2 id="🔹-4️⃣-examples-of-higher-order-functions">🔹 4️⃣ <strong>Examples of Higher-Order Functions</strong></h2>
<h3 id="✅-foreach-–-iterates-over-an-array">✅ <strong>forEach()</strong> – Iterates Over an Array</h3>
<ul>
<li>Calls a function <strong>for each</strong> element in an array.</li>
</ul>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> numbers <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token number">1</span><span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">,</span> <span class="token number">3</span><span class="token punctuation">,</span> <span class="token number">4</span><span class="token punctuation">]</span><span class="token punctuation">;</span>

numbers<span class="token punctuation">.</span><span class="token function">forEach</span><span class="token punctuation">(</span>num <span class="token operator">=&gt;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>num <span class="token operator">*</span> <span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span> 
<span class="token comment">// Output: 2, 4, 6, 8</span>
</code></pre>
<hr>
<h3 id="✅-map-–-creates-a-new-array">✅ <strong>map()</strong> – Creates a New Array</h3>
<ul>
<li>Returns a <strong>new array</strong> by transforming each element.</li>
</ul>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> numbers <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token number">1</span><span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">,</span> <span class="token number">3</span><span class="token punctuation">,</span> <span class="token number">4</span><span class="token punctuation">]</span><span class="token punctuation">;</span> 
<span class="token keyword">const</span> squared <span class="token operator">=</span> numbers<span class="token punctuation">.</span><span class="token function">map</span><span class="token punctuation">(</span>num <span class="token operator">=&gt;</span> num <span class="token operator">*</span> num<span class="token punctuation">)</span><span class="token punctuation">;</span>
console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>squared<span class="token punctuation">)</span><span class="token punctuation">;</span> 
<span class="token comment">// [1, 4, 9, 16]</span>
</code></pre>
<hr>
<h3 id="✅-filter-–-filters-an-array">✅ <strong>filter()</strong> – Filters an Array</h3>
<ul>
<li>Returns a <strong>new array</strong> with elements that satisfy a condition.</li>
</ul>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> numbers <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token number">10</span><span class="token punctuation">,</span> <span class="token number">20</span><span class="token punctuation">,</span> <span class="token number">30</span><span class="token punctuation">,</span> <span class="token number">40</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
 <span class="token keyword">const</span> filtered <span class="token operator">=</span> numbers<span class="token punctuation">.</span><span class="token function">filter</span><span class="token punctuation">(</span>num <span class="token operator">=&gt;</span> num <span class="token operator">&gt;</span> <span class="token number">20</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
 console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>filtered<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// [30, 40]</span>
</code></pre>
<hr>
<h3 id="✅-reduce-–-reduces-an-array-to-a-single-value">✅ <strong>reduce()</strong> – Reduces an Array to a Single Value</h3>
<ul>
<li>Accumulates values into a <strong>single result</strong>.</li>
</ul>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> numbers <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token number">1</span><span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">,</span> <span class="token number">3</span><span class="token punctuation">,</span> <span class="token number">4</span><span class="token punctuation">]</span><span class="token punctuation">;</span> <span class="token keyword">const</span> sum <span class="token operator">=</span> numbers<span class="token punctuation">.</span><span class="token function">reduce</span><span class="token punctuation">(</span><span class="token punctuation">(</span>acc<span class="token punctuation">,</span> num<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> acc <span class="token operator">+</span> num<span class="token punctuation">,</span> <span class="token number">0</span><span class="token punctuation">)</span><span class="token punctuation">;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>sum<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// 10</span>
</code></pre>
<hr>
<h3 id="✅-find-–-finds-the-first-matching-element">✅ <strong>find()</strong> – Finds the First Matching Element</h3>
<ul>
<li>Returns the <strong>first</strong> element that matches the condition.</li>
</ul>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js">
<span class="token keyword">const</span> users <span class="token operator">=</span> <span class="token punctuation">[</span>
    <span class="token punctuation">{</span> name<span class="token punctuation">:</span> <span class="token string">"Alice"</span><span class="token punctuation">,</span> age<span class="token punctuation">:</span> <span class="token number">25</span> <span class="token punctuation">}</span><span class="token punctuation">,</span>
    <span class="token punctuation">{</span> name<span class="token punctuation">:</span> <span class="token string">"Bob"</span><span class="token punctuation">,</span> age<span class="token punctuation">:</span> <span class="token number">30</span> <span class="token punctuation">}</span><span class="token punctuation">,</span>
<span class="token punctuation">]</span><span class="token punctuation">;</span> <span class="token keyword">const</span> user <span class="token operator">=</span> users<span class="token punctuation">.</span><span class="token function">find</span><span class="token punctuation">(</span>user <span class="token operator">=&gt;</span> user<span class="token punctuation">.</span>age <span class="token operator">&gt;</span> <span class="token number">26</span><span class="token punctuation">)</span><span class="token punctuation">;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>user<span class="token punctuation">)</span><span class="token punctuation">;</span> 

<span class="token comment">// { name: "Bob", age: 30 }</span>
</code></pre>
<hr>
<h3 id="✅-sort-–-sorts-an-array">✅ <strong>sort()</strong> – Sorts an Array</h3>
<ul>
<li>Sorts elements based on a comparison function.</li>
</ul>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> numbers <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token number">5</span><span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">,</span> <span class="token number">8</span><span class="token punctuation">,</span> <span class="token number">1</span><span class="token punctuation">]</span><span class="token punctuation">;</span>

numbers<span class="token punctuation">.</span><span class="token function">sort</span><span class="token punctuation">(</span><span class="token punctuation">(</span>a<span class="token punctuation">,</span> b<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> a <span class="token operator">-</span> b<span class="token punctuation">)</span><span class="token punctuation">;</span> 
<span class="token comment">// Ascending order  console.log(numbers);</span>
 <span class="token comment">// [1, 2, 5, 8]</span>
</code></pre>
<hr>
<h2 id="🔹-5️⃣-higher-order-function-returning-a-function">🔹 5️⃣ <strong>Higher-Order Function Returning a Function</strong></h2>
<p>✅ Functions can <strong>return another function</strong> to create <strong>customizable behaviors</strong>.</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">function</span>  <span class="token function">multiplyBy</span><span class="token punctuation">(</span>factor<span class="token punctuation">)</span> <span class="token punctuation">{</span> 
<span class="token keyword">return</span> 
<span class="token keyword">function</span> <span class="token punctuation">(</span>num<span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token keyword">return</span> num <span class="token operator">*</span> factor<span class="token punctuation">;</span>
    <span class="token punctuation">}</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span> <span class="token keyword">const</span> double <span class="token operator">=</span> <span class="token function">multiplyBy</span><span class="token punctuation">(</span><span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token function">double</span><span class="token punctuation">(</span><span class="token number">5</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span> 
<span class="token comment">// 10</span>
</code></pre>
<hr>
<h2 id="🔹-6️⃣-asynchronous-callbacks-settimeout--setinterval">🔹 6️⃣ <strong>Asynchronous Callbacks (setTimeout &amp; setInterval)</strong></h2>
<p>✅ <strong>setTimeout</strong> – Executes a function <strong>after a delay</strong>.</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token function">setTimeout</span><span class="token punctuation">(</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">=&gt;</span> <span class="token punctuation">{</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Executed after 2 seconds"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span><span class="token punctuation">,</span> <span class="token number">2000</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<p>✅ <strong>setInterval</strong> – Repeats a function <strong>at regular intervals</strong>.</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">let</span> count <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token keyword">const</span> interval <span class="token operator">=</span> <span class="token function">setInterval</span><span class="token punctuation">(</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">=&gt;</span> <span class="token punctuation">{</span>
    count<span class="token operator">++</span><span class="token punctuation">;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Count:"</span><span class="token punctuation">,</span> count<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token keyword">if</span> <span class="token punctuation">(</span>count <span class="token operator">===</span> <span class="token number">3</span><span class="token punctuation">)</span> <span class="token function">clearInterval</span><span class="token punctuation">(</span>interval<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Stops after 3 executions }, 1000);</span>
</code></pre>
<hr>
<h2 id="🔥-higher-order-functions-summary-table">🔥 <strong>Higher-Order Functions Summary Table</strong></h2>

<table>
<thead>
<tr>
<th>Function</th>
<th>Purpose</th>
<th>Example Usage</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>forEach</strong></td>
<td>Iterates over an array.</td>
<td><code>array.forEach(callback)</code></td>
</tr>
<tr>
<td><strong>map</strong></td>
<td>Creates a new transformed array.</td>
<td><code>array.map(callback)</code></td>
</tr>
<tr>
<td><strong>filter</strong></td>
<td>Returns a new array with filtered elements.</td>
<td><code>array.filter(callback)</code></td>
</tr>
<tr>
<td><strong>reduce</strong></td>
<td>Reduces an array to a single value.</td>
<td><code>array.reduce(callback, initialValue)</code></td>
</tr>
<tr>
<td><strong>find</strong></td>
<td>Finds the first matching element.</td>
<td><code>array.find(callback)</code></td>
</tr>
<tr>
<td><strong>sort</strong></td>
<td>Sorts an array based on a function.</td>
<td><code>array.sort(compareFunction)</code></td>
</tr>
</tbody>
</table><hr>
<h2 id="🏆-key-takeaways">🏆 <strong>Key Takeaways</strong></h2>
<p>✅ <strong>Higher-Order Functions</strong> improve <strong>code readability &amp; reusability</strong>.<br>
✅ <strong>Callback functions</strong> allow passing logic into other functions.<br>
✅ <strong>Array methods like <code>map</code>, <code>filter</code>, <code>reduce</code></strong> help write <strong>cleaner</strong> code.<br>
✅ <strong>Asynchronous callbacks</strong> (like <code>setTimeout</code>) enable <strong>non-blocking execution</strong>.</p>

