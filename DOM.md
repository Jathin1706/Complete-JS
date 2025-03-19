---


---

<h2 id="🔹-1️⃣-what-is-the-dom">🔹 1️⃣ <strong>What is the DOM?</strong></h2>
<p>✅ <strong>DOM</strong> represents the <strong>structure of an HTML document</strong> as objects.<br>
✅ Each HTML element becomes a <strong>node</strong> in the DOM tree.<br>
✅ JavaScript can <strong>manipulate</strong> these nodes dynamically.</p>
<hr>
<h2 id="🔹-2️⃣-dom-tree-structure">🔹 2️⃣ <strong>DOM Tree Structure</strong></h2>
<p>Each HTML page is represented as a <strong>tree of nodes</strong>:</p>
<p>md</p>
<p>CopyEdit</p>
<p><code>📄 Document ├── 🏷️ &lt;html&gt; │ ├── &lt;head&gt; │ │ ├── &lt;title&gt; Title &lt;/title&gt; │ ├── &lt;body&gt; │ ├── &lt;h1&gt; Heading &lt;/h1&gt; │ ├── &lt;p&gt; Paragraph &lt;/p&gt; │ ├── &lt;button&gt; Click Me &lt;/button&gt;</code></p>
<hr>
<h2 id="🔹-3️⃣-selecting-elements-in-dom">🔹 3️⃣ <strong>Selecting Elements in DOM</strong></h2>
<p>md</p>
<p>CopyEdit</p>
<p><code>| Method | Description | Example | |--------|------------|---------| | **document.getElementById(id)** | Selects element by ID | `document.getElementById("myId")` | | **document.getElementsByClassName(className)** | Selects elements by class name | `document.getElementsByClassName("myClass")` | | **document.getElementsByTagName(tagName)** | Selects elements by tag name | `document.getElementsByTagName("p")` | | **document.querySelector(selector)** | Selects the **first** element matching the CSS selector | `document.querySelector(".myClass")` | | **document.querySelectorAll(selector)** | Selects **all** elements matching the CSS selector | `document.querySelectorAll("div p")` |</code></p>
<p>✅ <strong>Example: Selecting Elements</strong></p>
<p>js</p>
<p>CopyEdit</p>
<p><code>const heading = document.getElementById("title"); // Select by ID const buttons = document.getElementsByClassName("btn"); // Select by class const paragraphs = document.getElementsByTagName("p"); // Select by tag const firstDiv = document.querySelector("div"); // Select first &lt;div&gt; const allDivs = document.querySelectorAll("div"); // Select all &lt;div&gt;</code></p>
<hr>
<h2 id="🔹-4️⃣-changing-content--attributes">🔹 4️⃣ <strong>Changing Content &amp; Attributes</strong></h2>
<p>✅ <strong>Modify Text Content</strong></p>
<p>js</p>
<p>CopyEdit</p>
<p><code>const heading = document.getElementById("title"); heading.textContent = "New Heading"; // Changes text heading.innerHTML = "&lt;span&gt;Updated Text&lt;/span&gt;"; // Inserts HTML</code></p>
<p>✅ <strong>Modify Attributes</strong></p>
<p>js</p>
<p>CopyEdit</p>
<p><code>const image = document.querySelector("img"); image.src = "new-image.jpg"; // Change image source image.alt = "New Description"; // Change alt text</code></p>
<p>✅ <strong>Modify CSS Styles</strong></p>
<p>js</p>
<p>CopyEdit</p>
<p><code>const box = document.getElementById("box"); box.style.backgroundColor = "yellow"; box.style.fontSize = "20px"; box.style.border = "2px solid black";</code></p>
<hr>
<h2 id="🔹-5️⃣-adding--removing-elements">🔹 5️⃣ <strong>Adding &amp; Removing Elements</strong></h2>
<p>✅ <strong>Create &amp; Append Elements</strong></p>
<p>js</p>
<p>CopyEdit</p>
<p><code>const newPara = document.createElement("p"); newPara.textContent = "This is a new paragraph."; document.body.appendChild(newPara); // Adds paragraph to body</code></p>
<p>✅ <strong>Insert Before a Specific Element</strong></p>
<p>js</p>
<p>CopyEdit</p>
<p><code>const parent = document.getElementById("container"); const newDiv = document.createElement("div"); newDiv.textContent = "Inserted Div"; const reference = document.getElementById("existingElement"); parent.insertBefore(newDiv, reference);</code></p>
<p>✅ <strong>Remove an Element</strong></p>
<p>js</p>
<p>CopyEdit</p>
<p><code>const removeElement = document.getElementById("oldDiv"); removeElement.remove(); // Removes the element</code></p>
<p>✅ <strong>Replace an Element</strong></p>
<p>js</p>
<p>CopyEdit</p>
<p><code>const parent = document.getElementById("container"); const newHeading = document.createElement("h2"); newHeading.textContent = "New Heading"; const oldHeading = document.getElementById("title"); parent.replaceChild(newHeading, oldHeading);</code></p>
<hr>
<h2 id="🔹-6️⃣-event-handling-in-dom">🔹 6️⃣ <strong>Event Handling in DOM</strong></h2>
<p>✅ <strong>Adding an Event Listener</strong></p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> btn <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">"myButton"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
btn<span class="token punctuation">.</span><span class="token function">addEventListener</span><span class="token punctuation">(</span><span class="token string">"click"</span><span class="token punctuation">,</span> <span class="token keyword">function</span> <span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Button Clicked!"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<p>✅ <strong>Event Types</strong></p>

<table>
<thead>
<tr>
<th>Event Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>click</strong></td>
<td>Triggered when element is clicked</td>
</tr>
<tr>
<td><strong>mouseover</strong></td>
<td>Triggered when mouse hovers over element</td>
</tr>
<tr>
<td><strong>mouseout</strong></td>
<td>Triggered when mouse leaves element</td>
</tr>
<tr>
<td><strong>keydown</strong></td>
<td>Triggered when a key is pressed</td>
</tr>
<tr>
<td><strong>keyup</strong></td>
<td>Triggered when a key is released</td>
</tr>
<tr>
<td><strong>submit</strong></td>
<td>Triggered when a form is submitted</td>
</tr>
<tr>
<td><strong>change</strong></td>
<td>Triggered when input value changes</td>
</tr>
</tbody>
</table><p>✅ <strong>Example: Changing Text on Button Click</strong></p>
<p>js</p>
<p>CopyEdit</p>
<p>`const btn = document.getElementById(“changeText”); const text = document.getElementById(“text”);</p>
<p>btn.addEventListener(“click”, function () {<br>
text.textContent = “Text changed!”;<br>
});</p>
<hr>
<h2 id="🔹-7️⃣-traversing-the-dom">🔹 7️⃣ <strong>Traversing the DOM</strong></h2>

<table>
<thead>
<tr>
<th>Property</th>
<th>Description</th>
<th>Example</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>parentElement</strong></td>
<td>Get parent of an element</td>
<td><code>element.parentElement</code></td>
</tr>
<tr>
<td><strong>children</strong></td>
<td>Get all child elements</td>
<td><code>element.children</code></td>
</tr>
<tr>
<td><strong>firstElementChild</strong></td>
<td>Get first child element</td>
<td><code>element.firstElementChild</code></td>
</tr>
<tr>
<td><strong>lastElementChild</strong></td>
<td>Get last child element</td>
<td><code>element.lastElementChild</code></td>
</tr>
<tr>
<td><strong>nextElementSibling</strong></td>
<td>Get next sibling element</td>
<td><code>element.nextElementSibling</code></td>
</tr>
<tr>
<td><strong>previousElementSibling</strong></td>
<td>Get previous sibling element</td>
<td><code>element.previousElementSibling</code></td>
</tr>
</tbody>
</table><p>✅ <strong>Example: Traversing Elements</strong></p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> parent <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">"container"</span><span class="token punctuation">)</span><span class="token punctuation">;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>parent<span class="token punctuation">.</span>children<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Get all children  console.log(parent.firstElementChild); // Get first child  console.log(parent.lastElementChild); // Get last child</span>
</code></pre>
<hr>
<h2 id="🔹-8️⃣-form-handling-in-dom">🔹 8️⃣ <strong>Form Handling in DOM</strong></h2>
<p>✅ <strong>Getting User Input</strong></p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> inputField <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">"nameInput"</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token keyword">const</span> display <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">"output"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

inputField<span class="token punctuation">.</span><span class="token function">addEventListener</span><span class="token punctuation">(</span><span class="token string">"input"</span><span class="token punctuation">,</span> <span class="token keyword">function</span> <span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  display<span class="token punctuation">.</span>textContent <span class="token operator">=</span> inputField<span class="token punctuation">.</span>value<span class="token punctuation">;</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<p>✅ <strong>Prevent Default Form Submission</strong></p>
<p>js</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> form <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">"myForm"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

form<span class="token punctuation">.</span><span class="token function">addEventListener</span><span class="token punctuation">(</span><span class="token string">"submit"</span><span class="token punctuation">,</span> <span class="token keyword">function</span> <span class="token punctuation">(</span>event<span class="token punctuation">)</span> <span class="token punctuation">{</span>
  event<span class="token punctuation">.</span><span class="token function">preventDefault</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Prevents page reload  alert("Form Submitted Successfully!");</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<hr>
<h2 id="🔥-dom-summary-table">🔥 <strong>DOM Summary Table</strong></h2>

<table>
<thead>
<tr>
<th>Feature</th>
<th>Method/Property</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Selecting Elements</strong></td>
<td><code>getElementById()</code></td>
<td>Selects by ID</td>
</tr>
<tr>
<td></td>
<td><code>getElementsByClassName()</code></td>
<td>Selects by class</td>
</tr>
<tr>
<td></td>
<td><code>getElementsByTagName()</code></td>
<td>Selects by tag</td>
</tr>
<tr>
<td></td>
<td><code>querySelector()</code></td>
<td>Selects first match</td>
</tr>
<tr>
<td></td>
<td><code>querySelectorAll()</code></td>
<td>Selects all matches</td>
</tr>
<tr>
<td><strong>Modifying Elements</strong></td>
<td><code>textContent</code></td>
<td>Change text</td>
</tr>
<tr>
<td></td>
<td><code>innerHTML</code></td>
<td>Change HTML content</td>
</tr>
<tr>
<td></td>
<td><code>setAttribute()</code></td>
<td>Change attributes</td>
</tr>
<tr>
<td><strong>Styling</strong></td>
<td><code>style.property</code></td>
<td>Change CSS styles</td>
</tr>
<tr>
<td><strong>Creating Elements</strong></td>
<td><code>createElement()</code></td>
<td>Creates new element</td>
</tr>
<tr>
<td></td>
<td><code>appendChild()</code></td>
<td>Appends element to parent</td>
</tr>
<tr>
<td></td>
<td><code>insertBefore()</code></td>
<td>Inserts before specific element</td>
</tr>
<tr>
<td><strong>Removing Elements</strong></td>
<td><code>remove()</code></td>
<td>Removes element</td>
</tr>
<tr>
<td></td>
<td><code>removeChild()</code></td>
<td>Removes child element</td>
</tr>
<tr>
<td><strong>Event Handling</strong></td>
<td><code>addEventListener()</code></td>
<td>Attaches event handler</td>
</tr>
<tr>
<td></td>
<td><code>click</code>, <code>mouseover</code>, <code>keydown</code></td>
<td>Common events</td>
</tr>
<tr>
<td><strong>Traversing DOM</strong></td>
<td><code>parentElement</code></td>
<td>Gets parent node</td>
</tr>
<tr>
<td></td>
<td><code>children</code></td>
<td>Gets all child nodes</td>
</tr>
<tr>
<td></td>
<td><code>nextElementSibling</code></td>
<td>Gets next sibling</td>
</tr>
</tbody>
</table><hr>
<h2 id="🏆-key-takeaways">🏆 <strong>Key Takeaways</strong></h2>
<p>✅ DOM allows <strong>JavaScript to manipulate HTML dynamically</strong>.<br>
✅ Use <strong>selectors</strong> (<code>getElementById</code>, <code>querySelector</code>, etc.) to target elements.<br>
✅ Modify <strong>content, attributes, and styles</strong> dynamically.<br>
✅ Use <strong>event listeners</strong> (<code>click</code>, <code>keydown</code>, etc.) to handle user interactions.<br>
✅ Create, remove, and update elements using <strong>DOM methods</strong>.</p>

