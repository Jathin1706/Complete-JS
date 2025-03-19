---


---

<h4 id="️⃣-what-are-operators">1️⃣ <strong>What are Operators?</strong></h4>
<ul>
<li>Operators are symbols used to perform operations on variables and values.</li>
<li>JavaScript has several types of operators:
<ul>
<li><strong>Arithmetic Operators</strong></li>
<li><strong>Assignment Operators</strong></li>
<li><strong>Comparison Operators</strong></li>
<li><strong>Logical Operators</strong></li>
<li><strong>Bitwise Operators</strong></li>
<li><strong>String Operators</strong></li>
<li><strong>Ternary Operator</strong></li>
<li><strong>Type Operators</strong></li>
</ul>
</li>
</ul>
<hr>
<h3 id="🔹-1.-arithmetic-operators">🔹 <strong>1. Arithmetic Operators</strong></h3>
<p>✅ Used for mathematical calculations.</p>
<p>md</p>

<table>
<thead>
<tr>
<th>Operator</th>
<th>Symbol</th>
<th>Example</th>
<th>Result</th>
</tr>
</thead>
<tbody>
<tr>
<td>Addition</td>
<td><code>+</code></td>
<td><code>5 + 3</code></td>
<td><code>8</code></td>
</tr>
<tr>
<td>Subtraction</td>
<td><code>-</code></td>
<td><code>5 - 3</code></td>
<td><code>2</code></td>
</tr>
<tr>
<td>Multiplication</td>
<td><code>*</code></td>
<td><code>5 * 3</code></td>
<td><code>15</code></td>
</tr>
<tr>
<td>Division</td>
<td><code>/</code></td>
<td><code>6 / 3</code></td>
<td><code>2</code></td>
</tr>
<tr>
<td>Modulus (Remainder)</td>
<td><code>%</code></td>
<td><code>5 % 3</code></td>
<td><code>2</code></td>
</tr>
<tr>
<td>Exponentiation</td>
<td><code>**</code></td>
<td><code>2 ** 3</code></td>
<td><code>8</code></td>
</tr>
<tr>
<td>Increment</td>
<td><code>++</code></td>
<td><code>let x = 5; x++</code></td>
<td><code>6</code></td>
</tr>
<tr>
<td>Decrement</td>
<td><code>--</code></td>
<td><code>let x = 5; x--</code></td>
<td><code>4</code></td>
</tr>
</tbody>
</table><p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">let</span> a <span class="token operator">=</span> <span class="token number">10</span><span class="token punctuation">;</span> <span class="token keyword">let</span> b <span class="token operator">=</span> <span class="token number">3</span><span class="token punctuation">;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>a <span class="token operator">+</span> b<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// 13  console.log(a % b); // 1</span>
</code></pre>
<hr>
<h3 id="🔹-2.-assignment-operators">🔹 <strong>2. Assignment Operators</strong></h3>
<p>✅ Used to assign values to variables.</p>
<p>md</p>

<table>
<thead>
<tr>
<th>Operator</th>
<th>Symbol</th>
<th>Example</th>
<th>Equivalent To</th>
</tr>
</thead>
<tbody>
<tr>
<td>Assign</td>
<td><code>=</code></td>
<td><code>x = 5</code></td>
<td><code>x = 5</code></td>
</tr>
<tr>
<td>Add &amp; Assign</td>
<td><code>+=</code></td>
<td><code>x += 3</code></td>
<td><code>x = x + 3</code></td>
</tr>
<tr>
<td>Subtract &amp; Assign</td>
<td><code>-=</code></td>
<td><code>x -= 2</code></td>
<td><code>x = x - 2</code></td>
</tr>
<tr>
<td>Multiply &amp; Assign</td>
<td><code>*=</code></td>
<td><code>x *= 2</code></td>
<td><code>x = x * 2</code></td>
</tr>
<tr>
<td>Divide &amp; Assign</td>
<td><code>/=</code></td>
<td><code>x /= 2</code></td>
<td><code>x = x / 2</code></td>
</tr>
<tr>
<td>Modulus &amp; Assign</td>
<td><code>%=</code></td>
<td><code>x %= 3</code></td>
<td><code>x = x % 3</code></td>
</tr>
<tr>
<td>Exponent &amp; Assign</td>
<td><code>**=</code></td>
<td><code>x **= 2</code></td>
<td><code>x = x ** 2</code></td>
</tr>
</tbody>
</table><p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">let</span> x <span class="token operator">=</span> <span class="token number">10</span><span class="token punctuation">;</span>
x <span class="token operator">+=</span> <span class="token number">5</span><span class="token punctuation">;</span> <span class="token comment">// x = x + 5 (x becomes 15)  console.log(x);</span>
</code></pre>
<hr>
<h3 id="🔹-3.-comparison-operators">🔹 <strong>3. Comparison Operators</strong></h3>
<p>✅ Used to compare values and return <code>true</code> or <code>false</code>.</p>
<p>md</p>

<table>
<thead>
<tr>
<th>Operator</th>
<th>Symbol</th>
<th>Example</th>
<th>Result</th>
</tr>
</thead>
<tbody>
<tr>
<td>Equal to</td>
<td><code>==</code></td>
<td><code>5 == "5"</code></td>
<td><code>true</code></td>
</tr>
<tr>
<td>Strict Equal</td>
<td><code>===</code></td>
<td><code>5 === "5"</code></td>
<td><code>false</code></td>
</tr>
<tr>
<td>Not Equal</td>
<td><code>!=</code></td>
<td><code>5 != 3</code></td>
<td><code>true</code></td>
</tr>
<tr>
<td>Strict Not Equal</td>
<td><code>!==</code></td>
<td><code>5 !== "5"</code></td>
<td><code>true</code></td>
</tr>
<tr>
<td>Greater Than</td>
<td><code>&gt;</code></td>
<td><code>5 &gt; 3</code></td>
<td><code>true</code></td>
</tr>
<tr>
<td>Less Than</td>
<td><code>&lt;</code></td>
<td><code>3 &lt; 5</code></td>
<td><code>true</code></td>
</tr>
<tr>
<td>Greater or Equal</td>
<td><code>&gt;=</code></td>
<td><code>5 &gt;= 5</code></td>
<td><code>true</code></td>
</tr>
<tr>
<td>Less or Equal</td>
<td><code>&lt;=</code></td>
<td><code>3 &lt;= 5</code></td>
<td><code>true</code></td>
</tr>
</tbody>
</table><p>js</p>
<pre class=" language-js"><code class="prism  language-js">console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token number">10</span> <span class="token operator">==</span> <span class="token string">"10"</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// true (loose equality)  console.log(10 === "10"); // false (strict equality)</span>
</code></pre>
<hr>
<h3 id="🔹-4.-logical-operators">🔹 <strong>4. Logical Operators</strong></h3>
<p>✅ Used for combining multiple conditions.</p>
<p>md</p>

<table>
<thead>
<tr>
<th>Operator</th>
<th>Symbol</th>
<th>Example</th>
<th>Result</th>
</tr>
</thead>
<tbody>
<tr>
<td>AND</td>
<td><code>&amp;&amp;</code></td>
<td><code>true &amp;&amp; false</code></td>
<td><code>false</code></td>
</tr>
<tr>
<td>OR</td>
<td><code>||</code></td>
<td><code>true || false</code></td>
<td><code>true</code></td>
</tr>
<tr>
<td>NOT</td>
<td><code>!</code></td>
<td><code>!true</code></td>
<td><code>false</code></td>
</tr>
</tbody>
</table><p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">let</span> isAdult <span class="token operator">=</span> <span class="token boolean">true</span><span class="token punctuation">;</span> <span class="token keyword">let</span> hasID <span class="token operator">=</span> <span class="token boolean">false</span><span class="token punctuation">;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>isAdult <span class="token operator">&amp;&amp;</span> hasID<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// false  console.log(isAdult || hasID); // true  console.log(!isAdult); // false</span>
</code></pre>
<hr>
<h3 id="🔹-5.-bitwise-operators">🔹 <strong>5. Bitwise Operators</strong></h3>
<p>✅ Works at the binary level.</p>
<p>md</p>

<table>
<thead>
<tr>
<th>Operator</th>
<th>Symbol</th>
<th>Example</th>
<th>Binary Equivalent</th>
<th>Result</th>
</tr>
</thead>
<tbody>
<tr>
<td>AND</td>
<td><code>&amp;</code></td>
<td><code>5 &amp; 1</code></td>
<td><code>101 &amp; 001</code></td>
<td><code>001 (1)</code></td>
</tr>
<tr>
<td>OR</td>
<td><code>|</code></td>
<td><code>5 | 1</code></td>
<td><code>101 | 001</code></td>
<td><code>101 (5)</code></td>
</tr>
<tr>
<td>XOR</td>
<td><code>^</code></td>
<td><code>5 ^ 1</code></td>
<td><code>101 ^ 001</code></td>
<td><code>100 (4)</code></td>
</tr>
<tr>
<td>NOT</td>
<td><code>~</code></td>
<td><code>~5</code></td>
<td><code>~00000101</code></td>
<td><code>11111010 (-6)</code></td>
</tr>
<tr>
<td>Left Shift</td>
<td><code>&lt;&lt;</code></td>
<td><code>5 &lt;&lt; 1</code></td>
<td><code>101 &lt;&lt; 1</code></td>
<td><code>1010 (10)</code></td>
</tr>
<tr>
<td>Right Shift</td>
<td><code>&gt;&gt;</code></td>
<td><code>5 &gt;&gt; 1</code></td>
<td><code>101 &gt;&gt; 1</code></td>
<td><code>10 (2)</code></td>
</tr>
</tbody>
</table><hr>
<h3 id="🔹-6.-string-operators">🔹 <strong>6. String Operators</strong></h3>
<p>✅ <code>+</code> is used for concatenation in strings.</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">let</span> firstName <span class="token operator">=</span> <span class="token string">"John"</span><span class="token punctuation">;</span> <span class="token keyword">let</span> lastName <span class="token operator">=</span> <span class="token string">"Doe"</span><span class="token punctuation">;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>firstName <span class="token operator">+</span> <span class="token string">" "</span> <span class="token operator">+</span> lastName<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// "John Doe"</span>
</code></pre>
<hr>
<h3 id="🔹-7.-ternary-operator--">🔹 <strong>7. Ternary Operator (<code>? :</code>)</strong></h3>
<p>✅ Shortened <code>if...else</code> statement.</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">let</span> age <span class="token operator">=</span> <span class="token number">18</span><span class="token punctuation">;</span> <span class="token keyword">let</span> result <span class="token operator">=</span> <span class="token punctuation">(</span>age <span class="token operator">&gt;=</span> <span class="token number">18</span><span class="token punctuation">)</span> <span class="token operator">?</span> <span class="token string">"Adult"</span> <span class="token punctuation">:</span> <span class="token string">"Minor"</span><span class="token punctuation">;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>result<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// "Adult"</span>
</code></pre>
<hr>
<h3 id="🔹-8.-type-operators">🔹 <strong>8. Type Operators</strong></h3>
<p>✅ Used to check or convert data types.</p>
<p>md</p>

<table>
<thead>
<tr>
<th>Operator</th>
<th>Symbol</th>
<th>Example</th>
<th>Result</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>typeof</code></td>
<td><code>typeof</code></td>
<td><code>typeof 42</code></td>
<td><code>"number"</code></td>
</tr>
<tr>
<td><code>instanceof</code></td>
<td><code>instanceof</code></td>
<td><code>arr instanceof Array</code></td>
<td><code>true</code></td>
</tr>
</tbody>
</table><p>js</p>
<pre class=" language-js"><code class="prism  language-js">console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token keyword">typeof</span>  <span class="token string">"Hello"</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// "string"  console.log([1,2,3] instanceof  Array); // true</span>
</code></pre>
<hr>
<h3 id="🏆-key-takeaways">🏆 <strong>Key Takeaways</strong></h3>
<p>✅ Arithmetic, Assignment, and Comparison operators are used in calculations and value manipulation.<br>
✅ Logical and Bitwise operators help in making complex decisions.<br>
✅ The Ternary Operator simplifies conditional checks.<br>
✅ <code>typeof</code> and <code>instanceof</code> help check and verify data types.</p>

