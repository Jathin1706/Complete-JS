---


---

<h2 id="🔹-1️⃣-what-are-arrays">🔹 1️⃣ <strong>What are Arrays?</strong></h2>
<p>✅ An <strong>array</strong> is a special variable that <strong>stores multiple values</strong> in a single variable.<br>
✅ Arrays can contain <strong>numbers, strings, objects, other arrays, or a mix of types</strong>.<br>
✅ Arrays are <strong>zero-indexed</strong> (first element is at index <code>0</code>).</p>
<hr>
<h2 id="🔹-2️⃣-creating-an-array">🔹 2️⃣ <strong>Creating an Array</strong></h2>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Using array literal (Recommended)  const fruits = ["Apple", "Banana", "Cherry"]; // Using new Array() constructor  const numbers = new  Array(1, 2, 3, 4, 5); console.log(fruits[0]); // "Apple"  console.log(numbers[2]); // 3</span>
</code></pre>
<hr>
<h2 id="🔹-3️⃣-array-properties--methods">🔹 3️⃣ <strong>Array Properties &amp; Methods</strong></h2>

<table>
<thead>
<tr>
<th>Property/Method</th>
<th>Description</th>
<th>Example</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>length</strong></td>
<td>Returns the number of elements in an array.</td>
<td><code>arr.length</code></td>
</tr>
<tr>
<td><strong>push()</strong></td>
<td>Adds an element <strong>to the end</strong>.</td>
<td><code>arr.push("item")</code></td>
</tr>
<tr>
<td><strong>pop()</strong></td>
<td>Removes <strong>last element</strong> and returns it.</td>
<td><code>arr.pop()</code></td>
</tr>
<tr>
<td><strong>unshift()</strong></td>
<td>Adds an element <strong>to the beginning</strong>.</td>
<td><code>arr.unshift("item")</code></td>
</tr>
<tr>
<td><strong>shift()</strong></td>
<td>Removes <strong>first element</strong> and returns it.</td>
<td><code>arr.shift()</code></td>
</tr>
<tr>
<td><strong>indexOf()</strong></td>
<td>Returns the <strong>index</strong> of an element.</td>
<td><code>arr.indexOf("item")</code></td>
</tr>
<tr>
<td><strong>includes()</strong></td>
<td>Checks if an array contains a value.</td>
<td><code>arr.includes("item")</code></td>
</tr>
<tr>
<td><strong>splice()</strong></td>
<td>Adds/removes elements from array.</td>
<td><code>arr.splice(1, 2, "New")</code></td>
</tr>
<tr>
<td><strong>slice()</strong></td>
<td>Returns a portion of an array.</td>
<td><code>arr.slice(1, 3)</code></td>
</tr>
<tr>
<td><strong>concat()</strong></td>
<td>Merges two arrays.</td>
<td><code>arr1.concat(arr2)</code></td>
</tr>
<tr>
<td><strong>join()</strong></td>
<td>Converts array to string.</td>
<td><code>arr.join(", ")</code></td>
</tr>
<tr>
<td><strong>reverse()</strong></td>
<td>Reverses the array order.</td>
<td><code>arr.reverse()</code></td>
</tr>
<tr>
<td><strong>sort()</strong></td>
<td>Sorts array (default is lexicographic).</td>
<td><code>arr.sort()</code></td>
</tr>
<tr>
<td><strong>map()</strong></td>
<td>Transforms each element.</td>
<td><code>arr.map(x =&gt; x * 2)</code></td>
</tr>
<tr>
<td><strong>filter()</strong></td>
<td>Filters elements based on condition.</td>
<td><code>arr.filter(x =&gt; x &gt; 10)</code></td>
</tr>
<tr>
<td><strong>reduce()</strong></td>
<td>Reduces array to single value.</td>
<td><code>arr.reduce((a, b) =&gt; a + b, 0)</code></td>
</tr>
<tr>
<td><strong>find()</strong></td>
<td>Finds first element matching condition.</td>
<td><code>arr.find(x =&gt; x &gt; 10)</code></td>
</tr>
</tbody>
</table><hr>
<h2 id="🔹-4️⃣-adding--removing-elements">🔹 4️⃣ <strong>Adding &amp; Removing Elements</strong></h2>
<p>✅ <strong>push() &amp; pop()</strong> → Modify the <strong>end</strong> of an array.</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> fruits <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token string">"Apple"</span><span class="token punctuation">,</span> <span class="token string">"Banana"</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
fruits<span class="token punctuation">.</span><span class="token function">push</span><span class="token punctuation">(</span><span class="token string">"Cherry"</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// ["Apple", "Banana", "Cherry"] fruits.pop(); // ["Apple", "Banana"]</span>
</code></pre>
<p>✅ <strong>unshift() &amp; shift()</strong> → Modify the <strong>start</strong> of an array.</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> fruits <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token string">"Banana"</span><span class="token punctuation">,</span> <span class="token string">"Cherry"</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
fruits<span class="token punctuation">.</span><span class="token function">unshift</span><span class="token punctuation">(</span><span class="token string">"Apple"</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// ["Apple", "Banana", "Cherry"] fruits.shift(); // ["Banana", "Cherry"]</span>
</code></pre>
<hr>
<h2 id="🔹-5️⃣-finding-elements-in-an-array">🔹 5️⃣ <strong>Finding Elements in an Array</strong></h2>
<p>✅ <strong>indexOf()</strong> → Returns the index of an element (or <code>-1</code> if not found).</p>
<p>js</p>
<p>CopyEdit</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> colors <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token string">"Red"</span><span class="token punctuation">,</span> <span class="token string">"Green"</span><span class="token punctuation">,</span> <span class="token string">"Blue"</span><span class="token punctuation">]</span><span class="token punctuation">;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>colors<span class="token punctuation">.</span><span class="token function">indexOf</span><span class="token punctuation">(</span><span class="token string">"Green"</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// 1  console.log(colors.indexOf("Yellow")); // -1</span>
</code></pre>
<p>✅ <strong>includes()</strong> → Checks if an element exists.</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js">console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>colors<span class="token punctuation">.</span><span class="token function">includes</span><span class="token punctuation">(</span><span class="token string">"Red"</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// true  console.log(colors.includes("Yellow")); // false</span>
</code></pre>
<p>✅ <strong>find()</strong> → Finds the <strong>first</strong> matching element.</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> numbers <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token number">10</span><span class="token punctuation">,</span> <span class="token number">20</span><span class="token punctuation">,</span> <span class="token number">30</span><span class="token punctuation">,</span> <span class="token number">40</span><span class="token punctuation">]</span><span class="token punctuation">;</span> <span class="token keyword">const</span> found <span class="token operator">=</span> numbers<span class="token punctuation">.</span><span class="token function">find</span><span class="token punctuation">(</span>num <span class="token operator">=&gt;</span> num <span class="token operator">&gt;</span> <span class="token number">25</span><span class="token punctuation">)</span><span class="token punctuation">;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>found<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// 30</span>
</code></pre>
<p>✅ <strong>filter()</strong> → Returns a <strong>new array</strong> with matching elements.</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> filtered <span class="token operator">=</span> numbers<span class="token punctuation">.</span><span class="token function">filter</span><span class="token punctuation">(</span>num <span class="token operator">=&gt;</span> num <span class="token operator">&gt;</span> <span class="token number">15</span><span class="token punctuation">)</span><span class="token punctuation">;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>filtered<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// [20, 30, 40]</span>
</code></pre>
<hr>
<h2 id="🔹-6️⃣-modifying-an-array">🔹 6️⃣ <strong>Modifying an Array</strong></h2>
<p>✅ <strong>splice(start, deleteCount, newItems…)</strong> → Modify elements in an array.</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> arr <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token string">"A"</span><span class="token punctuation">,</span> <span class="token string">"B"</span><span class="token punctuation">,</span> <span class="token string">"C"</span><span class="token punctuation">,</span> <span class="token string">"D"</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
arr<span class="token punctuation">.</span><span class="token function">splice</span><span class="token punctuation">(</span><span class="token number">1</span><span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">,</span> <span class="token string">"X"</span><span class="token punctuation">,</span> <span class="token string">"Y"</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Removes "B" and "C", adds "X" and "Y"  console.log(arr); // ["A", "X", "Y", "D"]</span>
</code></pre>
<p>✅ <strong>slice(start, end)</strong> → Returns a portion of an array <strong>without modifying it</strong>.</p>
<p>js</p>
<p>CopyEdit</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> arr <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token string">"A"</span><span class="token punctuation">,</span> <span class="token string">"B"</span><span class="token punctuation">,</span> <span class="token string">"C"</span><span class="token punctuation">,</span> <span class="token string">"D"</span><span class="token punctuation">]</span><span class="token punctuation">;</span> <span class="token keyword">const</span> sliced <span class="token operator">=</span> arr<span class="token punctuation">.</span><span class="token function">slice</span><span class="token punctuation">(</span><span class="token number">1</span><span class="token punctuation">,</span> <span class="token number">3</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// ["B", "C"]  console.log(sliced);</span>
</code></pre>
<hr>
<h2 id="🔹-7️⃣-sorting--reversing">🔹 7️⃣ <strong>Sorting &amp; Reversing</strong></h2>
<p>✅ <strong>sort()</strong> – Sorts array <strong>alphabetically</strong> (for strings)</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> names <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token string">"Charlie"</span><span class="token punctuation">,</span> <span class="token string">"Alice"</span><span class="token punctuation">,</span> <span class="token string">"Bob"</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
names<span class="token punctuation">.</span><span class="token function">sort</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>names<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// ["Alice", "Bob", "Charlie"]</span>
</code></pre>
<p>✅ <strong>sort() with compare function</strong> – Sorts numbers correctly.</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> numbers <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token number">40</span><span class="token punctuation">,</span> <span class="token number">100</span><span class="token punctuation">,</span> <span class="token number">1</span><span class="token punctuation">,</span> <span class="token number">5</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
numbers<span class="token punctuation">.</span><span class="token function">sort</span><span class="token punctuation">(</span><span class="token punctuation">(</span>a<span class="token punctuation">,</span> b<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> a <span class="token operator">-</span> b<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Ascending order  console.log(numbers); // [1, 5, 40, 100]</span>
</code></pre>
<p>✅ <strong>reverse()</strong> – Reverses the array.</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> letters <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token string">"A"</span><span class="token punctuation">,</span> <span class="token string">"B"</span><span class="token punctuation">,</span> <span class="token string">"C"</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
letters<span class="token punctuation">.</span><span class="token function">reverse</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>letters<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// ["C", "B", "A"]</span>
</code></pre>
<hr>
<h2 id="🔹-8️⃣-transforming-arrays">🔹 8️⃣ <strong>Transforming Arrays</strong></h2>
<p>✅ <strong>map()</strong> – Creates a new array by modifying each element.</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> numbers <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token number">1</span><span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">,</span> <span class="token number">3</span><span class="token punctuation">]</span><span class="token punctuation">;</span> <span class="token keyword">const</span> doubled <span class="token operator">=</span> numbers<span class="token punctuation">.</span><span class="token function">map</span><span class="token punctuation">(</span>num <span class="token operator">=&gt;</span> num <span class="token operator">*</span> <span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>doubled<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// [2, 4, 6]</span>
</code></pre>
<p>✅ <strong>reduce()</strong> – Reduces array to a single value.</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> numbers <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token number">1</span><span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">,</span> <span class="token number">3</span><span class="token punctuation">,</span> <span class="token number">4</span><span class="token punctuation">]</span><span class="token punctuation">;</span> <span class="token keyword">const</span> sum <span class="token operator">=</span> numbers<span class="token punctuation">.</span><span class="token function">reduce</span><span class="token punctuation">(</span><span class="token punctuation">(</span>acc<span class="token punctuation">,</span> num<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> acc <span class="token operator">+</span> num<span class="token punctuation">,</span> <span class="token number">0</span><span class="token punctuation">)</span><span class="token punctuation">;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>sum<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// 10</span>
</code></pre>
<hr>
<h2 id="🔥-javascript-arrays-summary-table">🔥 <strong>JavaScript Arrays Summary Table</strong></h2>

<table>
<thead>
<tr>
<th>Method</th>
<th>Action</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>push()</strong></td>
<td>Add to end</td>
</tr>
<tr>
<td><strong>pop()</strong></td>
<td>Remove from end</td>
</tr>
<tr>
<td><strong>unshift()</strong></td>
<td>Add to beginning</td>
</tr>
<tr>
<td><strong>shift()</strong></td>
<td>Remove from beginning</td>
</tr>
<tr>
<td><strong>indexOf()</strong></td>
<td>Find index of an element</td>
</tr>
<tr>
<td><strong>includes()</strong></td>
<td>Check if element exists</td>
</tr>
<tr>
<td><strong>splice()</strong></td>
<td>Modify elements in place</td>
</tr>
<tr>
<td><strong>slice()</strong></td>
<td>Extract part of array</td>
</tr>
<tr>
<td><strong>sort()</strong></td>
<td>Sorts array (lexicographic by default)</td>
</tr>
<tr>
<td><strong>reverse()</strong></td>
<td>Reverses array order</td>
</tr>
<tr>
<td><strong>map()</strong></td>
<td>Transforms elements and returns new array</td>
</tr>
<tr>
<td><strong>filter()</strong></td>
<td>Filters elements and returns new array</td>
</tr>
<tr>
<td><strong>reduce()</strong></td>
<td>Reduces to a single value</td>
</tr>
</tbody>
</table><hr>
<h2 id="🏆-key-takeaways">🏆 <strong>Key Takeaways</strong></h2>
<p>✅ Arrays store <strong>multiple values</strong> in a single variable.<br>
✅ Use <strong>push/pop</strong> to modify the <strong>end</strong>, and <strong>unshift/shift</strong> to modify the <strong>beginning</strong>.<br>
✅ <strong>map(), filter(), reduce()</strong> help in <strong>functional programming</strong>.<br>
✅ <strong>splice() modifies</strong>, while <strong>slice() creates a copy</strong>.<br>
✅ <strong>sort() and reverse()</strong> change array order.</p>

