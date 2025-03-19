---


---

<h4 id="️⃣-what-are-data-types">1️⃣ <strong>What are Data Types?</strong></h4>
<ul>
<li>Data types define the kind of values a variable can hold.</li>
<li>JavaScript has <strong>two main categories</strong>:
<ul>
<li><strong>Primitive Data Types</strong> (Stored by Value)</li>
<li><strong>Non-Primitive (Reference) Data Types</strong></li>
</ul>
</li>
</ul>
<hr>
<h3 id="🔹-primitive-data-types-immutable-stored-by-value">🔹 <strong>Primitive Data Types</strong> (Immutable, Stored by Value)</h3>
<p>✅ <strong>Stored directly in memory</strong> and copied by value when assigned to another variable.<br>
✅ <strong>7 Primitive Types</strong>:</p>
<p>md</p>

<table>
<thead>
<tr>
<th>Data Type</th>
<th>Example</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>String</strong></td>
<td><code>"Hello"</code>, <code>'World'</code></td>
<td>Text values enclosed in quotes.</td>
</tr>
<tr>
<td><strong>Number</strong></td>
<td><code>42</code>, <code>3.14</code>, <code>-7</code></td>
<td>Integers &amp; floating-point numbers.</td>
</tr>
<tr>
<td><strong>Boolean</strong></td>
<td><code>true</code>, <code>false</code></td>
<td>Represents logical values.</td>
</tr>
<tr>
<td><strong>Undefined</strong></td>
<td><code>let x;</code> (No value assigned)</td>
<td>A declared variable with no value.</td>
</tr>
<tr>
<td><strong>Null</strong></td>
<td><code>let y = null;</code></td>
<td>Represents an empty or unknown value.</td>
</tr>
<tr>
<td><strong>BigInt</strong></td>
<td><code>1234567890123456789n</code></td>
<td>Used for very large numbers beyond <code>Number</code> limits.</td>
</tr>
<tr>
<td><strong>Symbol</strong></td>
<td><code>Symbol('id')</code></td>
<td>Unique and immutable identifier.</td>
</tr>
</tbody>
</table><p>js</p>
<p>CopyEdit</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">let</span> name <span class="token operator">=</span> <span class="token string">"Alice"</span><span class="token punctuation">;</span> <span class="token comment">// String  let age = 25; // Number  let isStudent = true; // Boolean  let score; // Undefined  let emptyValue = null; // Null  let bigNumber = 1234567890123456789n; // BigInt  let uniqueId = Symbol("id"); // Symbol</span>
</code></pre>
<hr>
<h3 id="🔹-non-primitive-reference-data-types-mutable-stored-by-reference">🔹 <strong>Non-Primitive (Reference) Data Types</strong> (Mutable, Stored by Reference)</h3>
<p>✅ <strong>Stored as references in memory</strong> (objects, arrays, functions).<br>
✅ <strong>3 Key Types</strong>:</p>

<table>
<thead>
<tr>
<th>Data Type</th>
<th>Example</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Object</strong></td>
<td><code>{ name: "Alice", age: 25 }</code></td>
<td>Collection of key-value pairs.</td>
</tr>
<tr>
<td><strong>Array</strong></td>
<td><code>[1, 2, 3, 4]</code></td>
<td>Ordered list of values.</td>
</tr>
<tr>
<td><strong>Function</strong></td>
<td><code>function sayHello() {}</code></td>
<td>Block of reusable code.</td>
</tr>
</tbody>
</table><p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">let</span> person <span class="token operator">=</span> <span class="token punctuation">{</span> name<span class="token punctuation">:</span> <span class="token string">"Alice"</span><span class="token punctuation">,</span> age<span class="token punctuation">:</span> <span class="token number">25</span> <span class="token punctuation">}</span><span class="token punctuation">;</span> <span class="token comment">// Object  let numbers = [1, 2, 3, 4]; // Array  function  greet() { console.log("Hello!"); } // Function</span>
</code></pre>
<hr>
<h3 id="🔥-key-differences-primitive-vs-non-primitive">🔥 <strong>Key Differences: Primitive vs Non-Primitive</strong></h3>
<p>``</p>

<table>
<thead>
<tr>
<th>Feature</th>
<th>Primitive</th>
<th>Non-Primitive</th>
</tr>
</thead>
<tbody>
<tr>
<td>Stored in memory</td>
<td><strong>By Value</strong></td>
<td><strong>By Reference</strong></td>
</tr>
<tr>
<td>Mutable?</td>
<td>❌ No (Immutable)</td>
<td>✅ Yes (Mutable)</td>
</tr>
<tr>
<td>Copy Behavior</td>
<td>Creates <strong>copy</strong></td>
<td>Creates <strong>reference</strong></td>
</tr>
<tr>
<td>Example</td>
<td><code>let x = 10; let y = x;</code></td>
<td><code>let obj1 = {name: "Alice"}; let obj2 = obj1;</code></td>
</tr>
</tbody>
</table><p>``</p>
<p>js</p>
<p>CopyEdit</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Primitive (Copy Behavior)  let x = 10; let y = x; // y gets a copy of x y = 20; console.log(x); // 10 (unchanged)  // Non-Primitive (Reference Behavior)  let obj1 = { name: "Alice" }; let obj2 = obj1; // obj2 refers to obj1 obj2.name = "Bob"; console.log(obj1.name); // "Bob" (both changed)</span>
</code></pre>
<hr>
<h3 id="🏆-which-one-to-use">🏆 <strong>Which One to Use?</strong></h3>
<p>✅ <strong>Use Primitives</strong> when you need independent values.<br>
✅ <strong>Use Objects/Arrays</strong> when you need structured data.</p>

