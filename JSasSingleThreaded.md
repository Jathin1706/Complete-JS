---


---

<h4 id="q.-so-if-js-is-a-single-threaded--then-what-it-does-when-it-gets-a-async-function-">Q.) So if js is a single threaded , then what it does when it gets a async function ?</h4>
<p><strong>The Key Players:</strong></p>
<ul>
<li>
<p><strong>Call Stack:</strong></p>
<ul>
<li>This is where synchronous function calls are placed and executed. It operates on a “last-in, first-out” (LIFO) principle.</li>
</ul>
</li>
<li>
<p><strong>Web APIs:</strong></p>
<ul>
<li>These are provided by the browser (or Node.js) and handle tasks like timers (setTimeout), network requests (fetch), and DOM events. These are things that the Javascript engine itself does not handle.</li>
</ul>
</li>
<li>
<p><strong>Callback Queue (Task Queue):</strong></p>
<ul>
<li>When a Web API task completes, its callback function is placed in this queue.</li>
</ul>
</li>
<li>
<p><strong>Event Loop:</strong></p>
<ul>
<li>This is the orchestrator. It constantly monitors the call stack and the callback queue.  If the call stack is empty, it takes the first callback from the queue and pushes it onto the call stack for execution.</li>
</ul>
</li>
</ul>
<p><strong>How Asynchronous Functions Work:</strong></p>
<ol>
<li>
<p><strong>Initiation:</strong></p>
<ul>
<li>
<p>When an asynchronous function (like <code>setTimeout</code> or <code>fetch</code>) is called, it’s initially placed on the call stack.</p>
</li>
<li>
<p>The JavaScript engine then delegates the actual work to the Web APIs.</p>
</li>
<li>
<p>The asynchronous function itself is then popped off the call stack, allowing the engine to continue executing other code.</p>
</li>
</ul>
</li>
<li>
<p><strong>Web API Processing:</strong></p>
<ul>
<li>The Web APIs handle the long-running task (e.g., waiting for a timer to expire or a network response).</li>
</ul>
</li>
<li>
<p><strong>Callback Placement:</strong></p>
<ul>
<li>Once the task is complete, the Web API places the callback function (the code that should run after the asynchronous operation finishes) into the callback queue.</li>
</ul>
</li>
<li>
<p><strong>Event Loop’s Role:</strong></p>
<ul>
<li>The event loop continuously checks if the call stack is empty.</li>
<li>If the call stack is empty and there are callbacks in the queue, the event loop takes the first callback from the queue and pushes it onto the call stack.</li>
</ul>
</li>
<li>
<p><strong>Callback Execution:</strong></p>
<ul>
<li>The callback function is now executed on the call stack.</li>
</ul>
</li>
</ol>
<p><strong>In essence:</strong></p>
<ul>
<li>
<p>JavaScript doesn’t perform asynchronous tasks concurrently in separate threads.</p>
</li>
<li>
<p>Instead, it offloads those tasks to the Web APIs and uses the event loop to manage the execution of their callbacks.</p>
</li>
<li>
<p>This allows JavaScript to remain responsive while waiting for asynchronous operations to complete.</p>
</li>
</ul>
<p>Therefore, even with asynchronous code, Javascript is still running code in a single thread. The Web API’s allow for code to be ran outside of the main thread, and then the results of that code to be pushed back into the main thread when it is available.</p>

