---


---

<h4 id="️⃣-what-are-conditional-statements">1️⃣ <strong>What are Conditional Statements?</strong></h4>
<ul>
<li>Conditional statements allow code execution based on conditions.</li>
<li>Used to make decisions in JavaScript.</li>
<li>Main types:
<ul>
<li><code>if</code></li>
<li><code>if...else</code></li>
<li><code>if...else if...else</code></li>
<li><code>switch</code></li>
</ul>
</li>
</ul>
<hr>
<h3 id="🔹-1.-if-statement">🔹 <strong>1. <code>if</code> Statement</strong></h3>
<p>✅ Executes a block of code <strong>only if</strong> the condition is <code>true</code>.</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">let</span> age <span class="token operator">=</span> <span class="token number">18</span><span class="token punctuation">;</span> <span class="token keyword">if</span> <span class="token punctuation">(</span>age <span class="token operator">&gt;=</span> <span class="token number">18</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"You are eligible to vote."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span><span class="token template-string"><span class="token string">``</span></span><span class="token template-string"><span class="token string">` 

----------

### 🔹 **2. `</span></span><span class="token keyword">if</span><span class="token operator">...</span><span class="token keyword">else</span><span class="token template-string"><span class="token string">` Statement**

✅ Runs one block if `</span></span><span class="token boolean">true</span><span class="token template-string"><span class="token string">`, another if `</span></span><span class="token boolean">false</span><span class="token template-string"><span class="token string">`.

js

`</span></span><span class="token template-string"><span class="token string">``</span></span>js 
<span class="token keyword">let</span> num <span class="token operator">=</span> <span class="token number">10</span><span class="token punctuation">;</span> <span class="token keyword">if</span> <span class="token punctuation">(</span>num <span class="token operator">%</span> <span class="token number">2</span> <span class="token operator">===</span> <span class="token number">0</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Even number"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Odd number"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
<hr>
<h3 id="🔹-3.-if...else-if...else-statement">🔹 <strong>3. <code>if...else if...else</code> Statement</strong></h3>
<p>✅ Multiple conditions checked in sequence.</p>
<p>js</p>
<p>CopyEdit</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">let</span> marks <span class="token operator">=</span> <span class="token number">85</span><span class="token punctuation">;</span> <span class="token keyword">if</span> <span class="token punctuation">(</span>marks <span class="token operator">&gt;=</span> <span class="token number">90</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Grade: A"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span> <span class="token keyword">else</span>  <span class="token keyword">if</span> <span class="token punctuation">(</span>marks <span class="token operator">&gt;=</span> <span class="token number">80</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Grade: B"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span> <span class="token keyword">else</span>  <span class="token keyword">if</span> <span class="token punctuation">(</span>marks <span class="token operator">&gt;=</span> <span class="token number">70</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Grade: C"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Grade: F"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
<hr>
<h3 id="🔹-4.-ternary-operator--">🔹 <strong>4. Ternary Operator (<code>? :</code>)</strong></h3>
<p>✅ <strong>Shorter way</strong> to write <code>if...else</code>.</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">let</span> age <span class="token operator">=</span> <span class="token number">20</span><span class="token punctuation">;</span> <span class="token keyword">let</span> result <span class="token operator">=</span> <span class="token punctuation">(</span>age <span class="token operator">&gt;=</span> <span class="token number">18</span><span class="token punctuation">)</span> <span class="token operator">?</span> <span class="token string">"Adult"</span> <span class="token punctuation">:</span> <span class="token string">"Minor"</span><span class="token punctuation">;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>result<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// "Adult"</span>
</code></pre>
<hr>
<h3 id="🔹-5.-switch-statement">🔹 <strong>5. <code>switch</code> Statement</strong></h3>
<p>✅ Used when multiple conditions depend on a single value.<br>
✅ Uses <code>case</code> to match values and <code>break</code> to stop execution.<br>
✅ If no cases match, <code>default</code> executes.</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js">
<span class="token keyword">let</span> day <span class="token operator">=</span> <span class="token number">3</span><span class="token punctuation">;</span> <span class="token keyword">switch</span> <span class="token punctuation">(</span>day<span class="token punctuation">)</span> <span class="token punctuation">{</span>
 <span class="token keyword">case</span>  <span class="token number">1</span><span class="token punctuation">:</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Monday"</span><span class="token punctuation">)</span><span class="token punctuation">;</span> 
 <span class="token keyword">break</span><span class="token punctuation">;</span>
  <span class="token keyword">case</span>  <span class="token number">2</span><span class="token punctuation">:</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Tuesday"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
   <span class="token keyword">break</span><span class="token punctuation">;</span> 
   <span class="token keyword">case</span>  <span class="token number">3</span><span class="token punctuation">:</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Wednesday"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token keyword">break</span><span class="token punctuation">;</span>
    <span class="token keyword">case</span>  <span class="token number">4</span><span class="token punctuation">:</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Thursday"</span><span class="token punctuation">)</span><span class="token punctuation">;</span> 
   <span class="token keyword">break</span><span class="token punctuation">;</span>
    <span class="token keyword">case</span>  <span class="token number">5</span><span class="token punctuation">:</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Friday"</span><span class="token punctuation">)</span><span class="token punctuation">;</span> 
    <span class="token keyword">break</span><span class="token punctuation">;</span> 
    <span class="token keyword">default</span><span class="token punctuation">:</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Weekend"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
<hr>
<h3 id="🔥-key-differences-if-else-vs-switch">🔥 <strong>Key Differences: <code>if-else</code> vs <code>switch</code></strong></h3>
<p>md</p>

<table>
<thead>
<tr>
<th>Feature</th>
<th>if-else</th>
<th>switch</th>
</tr>
</thead>
<tbody>
<tr>
<td>Use Case</td>
<td>For complex, multiple conditions</td>
<td>For checking a single value against multiple cases</td>
</tr>
<tr>
<td>Readability</td>
<td>Can be harder to read with many conditions</td>
<td>More readable for value comparisons</td>
</tr>
<tr>
<td>Performance</td>
<td>Slower for multiple checks</td>
<td>Faster with many fixed cases</td>
</tr>
<tr>
<td>Example</td>
<td><code>if (x &gt; 10) {...}</code></td>
<td><code>switch(x) { case 10: ... }</code></td>
</tr>
</tbody>
</table><hr>
<h3 id="🏆-which-one-to-use">🏆 <strong>Which One to Use?</strong></h3>
<p>✅ <strong>Use <code>if-else</code></strong> when conditions involve different variables or complex expressions.<br>
✅ <strong>Use <code>switch</code></strong> when checking <strong>one variable</strong> against multiple fixed values.</p>

