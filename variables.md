---


---

<h4 id="️⃣-what-are-variables">1️⃣ <strong>What are Variables?</strong></h4>
<ul>
<li>Variables store data values in JavaScript.</li>
<li>Declared using <code>var</code>, <code>let</code>, or <code>const</code>.</li>
</ul>
<h4 id="️⃣-var-old-way---avoid-using">2️⃣ <strong><code>var</code> (Old Way - Avoid Using)</strong></h4>
<p>✅ Function-scoped (not block-scoped).<br>
✅ Can be re-declared &amp; updated.<br>
⚠️ Hoisted but <strong>initialized as <code>undefined</code></strong>.<br>
⚠️ Can cause unexpected bugs due to lack of block scoping.</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">var</span> name <span class="token operator">=</span> <span class="token string">"Alice"</span><span class="token punctuation">;</span> <span class="token keyword">var</span> name <span class="token operator">=</span> <span class="token string">"Bob"</span><span class="token punctuation">;</span> <span class="token comment">// ✅ Allowed (Re-declaration) name = "Charlie"; // ✅ Allowed (Re-assignment)</span>
</code></pre>
<h4 id="️⃣-let-modern--preferred-for-changeable-values">3️⃣ <strong><code>let</code> (Modern &amp; Preferred for Changeable Values)</strong></h4>
<p>✅ Block-scoped (only available inside <code>{}</code>).<br>
✅ Can be updated but <strong>not re-declared in the same scope</strong>.<br>
⚠️ Hoisted but <strong>not initialized</strong> (throws error if accessed before declaration).</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">let</span> age <span class="token operator">=</span> <span class="token number">25</span><span class="token punctuation">;</span>
age <span class="token operator">=</span> <span class="token number">30</span><span class="token punctuation">;</span> <span class="token comment">// ✅ Allowed (Re-assignment)  let age = 35; // ❌ Error (Cannot re-declare in the same scope)</span>
</code></pre>
<h4 id="️⃣-const-for-constants---preferred-for-fixed-values">4️⃣ <strong><code>const</code> (For Constants - Preferred for Fixed Values)</strong></h4>
<p>✅ Block-scoped.<br>
✅ Cannot be re-assigned or re-declared.<br>
✅ Must be initialized when declared.</p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span>  PI <span class="token operator">=</span> <span class="token number">3.14</span><span class="token punctuation">;</span> PI <span class="token operator">=</span> <span class="token number">3.1415</span><span class="token punctuation">;</span> <span class="token comment">// ❌ Error (Cannot re-assign a const variable)</span>
</code></pre>

