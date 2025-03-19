---


---

<h2 id="🔹-1️⃣-what-are-functions">🔹 1️⃣ What are Functions?</h2>
<ul>
<li>A <strong>function</strong> is a reusable block of code that performs a specific task.</li>
<li>Functions make code <strong>modular, reusable, and maintainable</strong>.</li>
<li>Functions can take <strong>parameters (inputs)</strong> and return <strong>values (outputs)</strong>.</li>
</ul>
<hr>
<h2 id="🔹-2️⃣-types-of-functions-in-javascript">🔹 2️⃣ Types of Functions in JavaScript</h2>

<table>
<thead>
<tr>
<th>Function Type</th>
<th>Description</th>
<th>Example Syntax</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Function Declaration</strong></td>
<td>Named function, can be called before definition</td>
<td><code>function greet() {}</code></td>
</tr>
<tr>
<td><strong>Function Expression</strong></td>
<td>Anonymous function assigned to a variable</td>
<td><code>const greet = function() {};</code></td>
</tr>
<tr>
<td><strong>Arrow Function</strong></td>
<td>Shorter syntax, no <code>this</code> binding</td>
<td><code>const greet = () =&gt; {};</code></td>
</tr>
<tr>
<td><strong>Immediately Invoked Function Expression (IIFE)</strong></td>
<td>Runs immediately after definition</td>
<td><code>(function() { console.log("Hi"); })();</code></td>
</tr>
<tr>
<td><strong>Generator Function</strong></td>
<td>Returns an iterator for lazy evaluation</td>
<td><code>function* gen() { yield 1; }</code></td>
</tr>
</tbody>
</table><hr>
<h2 id="🔹-3️⃣-function-declarations-named-functions">🔹 3️⃣ Function Declarations (Named Functions)</h2>
<p>✅ Uses the <code>function</code> keyword.<br>
✅ Can be <strong>called before</strong> it’s defined (<strong>Hoisting</strong>).</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">function</span>  <span class="token function">greet</span><span class="token punctuation">(</span>name<span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token keyword">return</span>  <span class="token template-string"><span class="token string">`Hello, </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>name<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">!`</span></span><span class="token punctuation">;</span>
<span class="token punctuation">}</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token function">greet</span><span class="token punctuation">(</span><span class="token string">"Alice"</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// "Hello, Alice!"</span>
</code></pre>
<hr>
<h2 id="🔹-4️⃣-function-expressions-anonymous-functions">🔹 4️⃣ Function Expressions (Anonymous Functions)</h2>
<p>✅ A function assigned to a variable.<br>
✅ <strong>Not hoisted</strong> (cannot be called before its declaration).</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> <span class="token function-variable function">greet</span> <span class="token operator">=</span> <span class="token keyword">function</span><span class="token punctuation">(</span>name<span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token keyword">return</span>  <span class="token template-string"><span class="token string">`Hello, </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>name<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">!`</span></span><span class="token punctuation">;</span>
<span class="token punctuation">}</span><span class="token punctuation">;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token function">greet</span><span class="token punctuation">(</span><span class="token string">"Bob"</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// "Hello, Bob!"</span>
</code></pre>
<hr>
<h2 id="🔹-5️⃣-arrow-functions-es6">🔹 5️⃣ Arrow Functions (ES6)</h2>
<p>✅ Shorter syntax for functions.<br>
✅ <strong>No <code>this</code> binding</strong> (inherits <code>this</code> from the surrounding scope).<br>
✅ Implicit return if there’s only one statement.</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span>  <span class="token function-variable function">greet</span> <span class="token operator">=</span> <span class="token punctuation">(</span>name<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> <span class="token template-string"><span class="token string">`Hello, </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>name<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">!`</span></span><span class="token punctuation">;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token function">greet</span><span class="token punctuation">(</span><span class="token string">"Charlie"</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// "Hello, Charlie!"</span>
</code></pre>
<p>✅ <strong>If there is only one parameter, parentheses can be omitted</strong></p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span>  <span class="token function-variable function">square</span> <span class="token operator">=</span> num <span class="token operator">=&gt;</span> num <span class="token operator">*</span> num<span class="token punctuation">;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token function">square</span><span class="token punctuation">(</span><span class="token number">4</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// 16</span>
</code></pre>
<p>✅ <strong>If there are multiple parameters or no parameters, use parentheses</strong></p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span>  <span class="token function-variable function">add</span> <span class="token operator">=</span> <span class="token punctuation">(</span>a<span class="token punctuation">,</span> b<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> a <span class="token operator">+</span> b<span class="token punctuation">;</span> <span class="token keyword">const</span>  <span class="token function-variable function">sayHello</span> <span class="token operator">=</span> <span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">=&gt;</span> <span class="token string">"Hello, world!"</span><span class="token punctuation">;</span>
</code></pre>
<hr>
<h2 id="🔹-6️⃣-immediately-invoked-function-expressions-iife">🔹 6️⃣ Immediately Invoked Function Expressions (IIFE)</h2>
<p>✅ <strong>Runs immediately after definition</strong>.<br>
✅ <strong>Used to avoid polluting the global scope</strong>.</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token punctuation">(</span><span class="token keyword">function</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"I am an IIFE!"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Output: "I am an IIFE!"</span>
</code></pre>
<p>✅ <strong>Arrow Function IIFE</strong></p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token punctuation">(</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">=&gt;</span>  console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Arrow IIFE!"</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<hr>
<h2 id="🔹-7️⃣-using-arguments-keyword">🔹 7️⃣ Using <code>arguments</code> Keyword</h2>
<p>✅ <strong><code>arguments</code></strong> is an array-like object available in <strong>regular functions</strong> (not in arrow functions).<br>
✅ Used to access all passed arguments <strong>without defining parameters</strong>.</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">function</span>  <span class="token function">sum</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token keyword">let</span> total <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token keyword">for</span> <span class="token punctuation">(</span><span class="token keyword">let</span> i <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> i <span class="token operator">&lt;</span> arguments<span class="token punctuation">.</span>length<span class="token punctuation">;</span> i<span class="token operator">++</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
        total <span class="token operator">+=</span> arguments<span class="token punctuation">[</span>i<span class="token punctuation">]</span><span class="token punctuation">;</span>
    <span class="token punctuation">}</span> <span class="token keyword">return</span> total<span class="token punctuation">;</span>
<span class="token punctuation">}</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token function">sum</span><span class="token punctuation">(</span><span class="token number">1</span><span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">,</span> <span class="token number">3</span><span class="token punctuation">,</span> <span class="token number">4</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// 10</span>
</code></pre>
<p>🔴 <strong><code>arguments</code> does NOT work in arrow functions!</strong></p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span>  <span class="token function-variable function">sumArrow</span> <span class="token operator">=</span> <span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">=&gt;</span> <span class="token punctuation">{</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>arguments<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// ERROR: arguments is not defined };</span>
</code></pre>
<hr>
<h2 id="🔹-8️⃣-using-the-spread-...-operator">🔹 8️⃣ Using the Spread (<code>...</code>) Operator</h2>
<p>✅ The <strong>spread operator (<code>...</code>)</strong> allows functions to accept multiple arguments as an array.<br>
✅ Works in both <strong>function declarations</strong> and <strong>arrow functions</strong>.</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">function</span>  <span class="token function">sum</span><span class="token punctuation">(</span><span class="token operator">...</span>numbers<span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token keyword">return</span> numbers<span class="token punctuation">.</span><span class="token function">reduce</span><span class="token punctuation">(</span><span class="token punctuation">(</span>acc<span class="token punctuation">,</span> num<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> acc <span class="token operator">+</span> num<span class="token punctuation">,</span> <span class="token number">0</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token function">sum</span><span class="token punctuation">(</span><span class="token number">1</span><span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">,</span> <span class="token number">3</span><span class="token punctuation">,</span> <span class="token number">4</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// 10</span>
</code></pre>
<p>✅ <strong>Arrow Function with Spread</strong></p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span>  <span class="token function-variable function">multiply</span> <span class="token operator">=</span> <span class="token punctuation">(</span><span class="token operator">...</span>nums<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> nums<span class="token punctuation">.</span><span class="token function">reduce</span><span class="token punctuation">(</span><span class="token punctuation">(</span>acc<span class="token punctuation">,</span> num<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> acc <span class="token operator">*</span> num<span class="token punctuation">,</span> <span class="token number">1</span><span class="token punctuation">)</span><span class="token punctuation">;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token function">multiply</span><span class="token punctuation">(</span><span class="token number">2</span><span class="token punctuation">,</span> <span class="token number">3</span><span class="token punctuation">,</span> <span class="token number">4</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// 24</span>
</code></pre>
<hr>
<h2 id="🔥-function-types-summary-table">🔥 Function Types Summary Table</h2>
<p>md</p>

<table>
<thead>
<tr>
<th>Function Type</th>
<th>Syntax</th>
<th>Hoisted?</th>
<th><code>this</code> Binding</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Function Declaration</strong></td>
<td><code>function name() {}</code></td>
<td>✅ Yes</td>
<td>✅ Yes</td>
</tr>
<tr>
<td><strong>Function Expression</strong></td>
<td><code>const name = function() {};</code></td>
<td>❌ No</td>
<td>✅ Yes</td>
</tr>
<tr>
<td><strong>Arrow Function</strong></td>
<td><code>const name = () =&gt; {};</code></td>
<td>❌ No</td>
<td>❌ No (lexical <code>this</code>)</td>
</tr>
<tr>
<td><strong>IIFE</strong></td>
<td><code>(function() {})();</code></td>
<td>❌ No</td>
<td>✅ Yes</td>
</tr>
<tr>
<td><strong>Generator Function</strong></td>
<td><code>function* name() {}</code></td>
<td>✅ Yes</td>
<td>✅ Yes</td>
</tr>
</tbody>
</table><hr>
<h2 id="🏆-key-takeaways">🏆 Key Takeaways</h2>
<p>✅ <strong>Function declarations are hoisted</strong>, while function expressions are <strong>not</strong>.<br>
✅ <strong>Arrow functions have no <code>arguments</code> object and no <code>this</code> binding</strong>.<br>
✅ Use <strong>IIFE</strong> to execute code <strong>immediately</strong> and <strong>avoid global scope pollution</strong>.<br>
✅ The <strong>spread (<code>...</code>) operator</strong> is useful for handling multiple arguments dynamically.</p>

