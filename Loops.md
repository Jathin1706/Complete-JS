---


---

<h4 id="️⃣-what-are-loops">1️⃣ <strong>What are Loops?</strong></h4>
<ul>
<li>Loops <strong>repeat a block of code</strong> as long as a condition is <code>true</code>.</li>
<li>JavaScript provides several types of loops:
<ul>
<li><strong>for</strong></li>
<li><strong>while</strong></li>
<li><strong>do…while</strong></li>
<li><strong>for…in</strong></li>
<li><strong>for…of</strong></li>
</ul>
</li>
</ul>
<hr>
<h3 id="🔹-1.-for-loop">🔹 <strong>1. <code>for</code> Loop</strong></h3>
<p>✅ Best for when the number of iterations is known.<br>
✅ Syntax:</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">for</span> <span class="token punctuation">(</span>initialization<span class="token punctuation">;</span> condition<span class="token punctuation">;</span> update<span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token comment">// Code to execute }</span>
</code></pre>
<p>✅ Example: Print numbers from 1 to 5</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">for</span> <span class="token punctuation">(</span><span class="token keyword">let</span> i <span class="token operator">=</span> <span class="token number">1</span><span class="token punctuation">;</span> i <span class="token operator">&lt;=</span> <span class="token number">5</span><span class="token punctuation">;</span> i<span class="token operator">++</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>i<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
<hr>
<h3 id="🔹-2.-while-loop">🔹 <strong>2. <code>while</code> Loop</strong></h3>
<p>✅ Best when the number of iterations is <strong>unknown</strong> and based on a condition.<br>
✅ Syntax:</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">while</span> <span class="token punctuation">(</span>condition<span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token comment">// Code to execute }</span>
<span class="token template-string"><span class="token string">``</span></span> 

✅ Example<span class="token punctuation">:</span> Print numbers <span class="token keyword">from</span> <span class="token number">1</span> to <span class="token number">5</span>

js

<span class="token template-string"><span class="token string">``</span></span>`js
<span class="token keyword">let</span> i <span class="token operator">=</span> <span class="token number">1</span><span class="token punctuation">;</span> <span class="token keyword">while</span> <span class="token punctuation">(</span>i <span class="token operator">&lt;=</span> <span class="token number">5</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>i<span class="token punctuation">)</span><span class="token punctuation">;</span>
    i<span class="token operator">++</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
<hr>
<h3 id="🔹-3.-do...while-loop">🔹 <strong>3. <code>do...while</code> Loop</strong></h3>
<p>✅ <strong>Runs at least once</strong> before checking the condition.<br>
✅ Syntax:</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">do</span> <span class="token punctuation">{</span> <span class="token comment">// Code to execute } while (condition);</span>
</code></pre>
<p>✅ Example: Print numbers from 1 to 5</p>
<p>js</p>
<p>CopyEdit</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">let</span> i <span class="token operator">=</span> <span class="token number">1</span><span class="token punctuation">;</span> <span class="token keyword">do</span> <span class="token punctuation">{</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>i<span class="token punctuation">)</span><span class="token punctuation">;</span>
    i<span class="token operator">++</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span> <span class="token keyword">while</span> <span class="token punctuation">(</span>i <span class="token operator">&lt;=</span> <span class="token number">5</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<hr>
<h3 id="🔹-4.-for...in-loop-for-objects">🔹 <strong>4. <code>for...in</code> Loop</strong> (For Objects)</h3>
<p>✅ Iterates over <strong>object properties</strong> (keys).<br>
✅ Syntax:</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">for</span> <span class="token punctuation">(</span><span class="token keyword">let</span> key <span class="token keyword">in</span> object<span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token comment">// Code to execute }</span>
</code></pre>
<p>✅ Example: Loop through an object</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">let</span> person <span class="token operator">=</span> <span class="token punctuation">{</span> name<span class="token punctuation">:</span> <span class="token string">"Alice"</span><span class="token punctuation">,</span> age<span class="token punctuation">:</span> <span class="token number">25</span><span class="token punctuation">,</span> city<span class="token punctuation">:</span> <span class="token string">"New York"</span> <span class="token punctuation">}</span><span class="token punctuation">;</span> <span class="token keyword">for</span> <span class="token punctuation">(</span><span class="token keyword">let</span> key <span class="token keyword">in</span> person<span class="token punctuation">)</span> <span class="token punctuation">{</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>key <span class="token operator">+</span> <span class="token string">": "</span> <span class="token operator">+</span> person<span class="token punctuation">[</span>key<span class="token punctuation">]</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
<p>🔹 <strong>Output:</strong></p>
<p><code>name: Alice age: 25 city: New York</code></p>
<hr>
<h3 id="🔹-5.-for...of-loop-for-arrays--strings">🔹 <strong>5. <code>for...of</code> Loop</strong> (For Arrays &amp; Strings)</h3>
<p>✅ Iterates over <strong>iterable objects</strong> like arrays &amp; strings.<br>
✅ Syntax:</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">for</span> <span class="token punctuation">(</span><span class="token keyword">let</span> value <span class="token keyword">of</span> iterable<span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token comment">// Code to execute }</span>
</code></pre>
<p>✅ Example: Loop through an array</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">let</span> colors <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token string">"Red"</span><span class="token punctuation">,</span> <span class="token string">"Green"</span><span class="token punctuation">,</span> <span class="token string">"Blue"</span><span class="token punctuation">]</span><span class="token punctuation">;</span> <span class="token keyword">for</span> <span class="token punctuation">(</span><span class="token keyword">let</span> color <span class="token keyword">of</span> colors<span class="token punctuation">)</span> <span class="token punctuation">{</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>color<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
<p>🔹 <strong>Output:</strong></p>
<p><code>Red Green Blue</code></p>
<hr>
<h3 id="🔥-key-differences-between-loops">🔥 <strong>Key Differences Between Loops</strong></h3>

<table>
<thead>
<tr>
<th>Loop Type</th>
<th>Best Used For</th>
<th>Runs At Least Once?</th>
<th>Example Use Case</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>for</code></td>
<td>Known number of iterations</td>
<td>❌ No</td>
<td>Iterating a fixed number of times</td>
</tr>
<tr>
<td><code>while</code></td>
<td>Unknown number of iterations</td>
<td>❌ No</td>
<td>Running until a condition is met</td>
</tr>
<tr>
<td><code>do...while</code></td>
<td>Ensuring at least one execution</td>
<td>✅ Yes</td>
<td>Asking user for input at least once</td>
</tr>
<tr>
<td><code>for...in</code></td>
<td>Iterating over object properties</td>
<td>❌ No</td>
<td>Accessing object keys &amp; values</td>
</tr>
<tr>
<td><code>for...of</code></td>
<td>Iterating over arrays &amp; strings</td>
<td>❌ No</td>
<td>Looping through elements of an array</td>
</tr>
</tbody>
</table><hr>
<h3 id="🏆-which-one-to-use">🏆 <strong>Which One to Use?</strong></h3>
<p>✅ <strong>Use <code>for</code></strong> when the iteration count is known.<br>
✅ <strong>Use <code>while</code></strong> when looping until a condition is met.<br>
✅ <strong>Use <code>do...while</code></strong> when the block must run at least once.<br>
✅ <strong>Use <code>for...in</code></strong> for objects.<br>
✅ <strong>Use <code>for...of</code></strong> for arrays, strings, or iterables.</p>

