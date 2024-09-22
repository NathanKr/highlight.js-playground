<h1>Experimenting with highlight.js for Browser Syntax Highlighting</h1>

<h2>Motivation</h2>
<p>This project demonstrates how to use <code>highlight.js</code> in the browser to achieve syntax highlighting similar to what is found in VS Code.</p>

<h2>Usage</h2>
<p>Simply open <code>index.html</code> in your browser.</p>

<h2>Installation</h2>
<p>No installation required. CDN links are already included in <code>index.html</code>.</p>

<h2>Ingredients of highlight.js</h2>
<p>To set up <code>highlight.js</code>, you need to include the following in your HTML file. In <code>index.html</code>, CDN paths are used, and the default CSS is replaced with the VS Code theme CSS. The key components are:</p>

<ol>
    <li>
        <strong>highlight.js CSS file</strong>
        <pre><code>&lt;link rel=&quot;stylesheet&quot; href=&quot;/path/to/styles/default.min.css&quot;&gt;</code></pre>
    </li>
    <li>
        <strong>highlight.js JS file</strong>
        <pre><code>&lt;script src=&quot;/path/to/highlight.min.js&quot;&gt;&lt;/script&gt;</code></pre>
    </li>
    <li>
        <strong>highlight.js Initialization</strong>
        <pre><code>&lt;script&gt;hljs.highlightAll();&lt;/script&gt;</code></pre>
    </li>
</ol>

<h2>Basic Idea</h2>
<ul>
    <li>Wrap the code block that you don't want the browser to interpret in <code>&lt;pre&gt;</code> and <code>&lt;code&gt;</code> elements.</li>
    <li>Add a class to the <code>&lt;code&gt;</code> element that starts with <code>language-</code>, such as <code>language-html</code>. This enables <code>hljs.highlightAll()</code> to recognize and style the code based on the selected theme, which is <code>vs.min.css</code> in this example.</li>
</ul>
<p>
    <img src="https://github.com/NathanKr/highlight.js-playground/blob/main/figs/post-processing.png" alt="Post-Processing Example">
</p>

<h2>HTML Example</h2>
<p>To display HTML code in a readable format, wrap it in the appropriate tags and escape <code>&lt;</code> and <code>&gt;</code>:</p>
<pre><code>&lt;pre&gt;&lt;code class=&quot;language-html&quot;&gt;
    &amp;lt;h1&amp;gt;Hello&amp;lt;/h1&amp;gt;
&lt;/code&gt;&lt;/pre&gt;</code></pre>

<h2>JavaScript Example</h2>
<p>Here is an example of how to display JavaScript code:</p>
<pre><code>&lt;pre&gt;&lt;code class=&quot;language-javascript&quot;&gt;
    function sum(num1, num2) {
        const s = num1 + num2; 
        return s;
    }
&lt;/code&gt;&lt;/pre&gt;</code></pre>

<h2>Result</h2>
<p>The syntax-highlighted code will be displayed similar to the image below:</p>
<p>
    <img src="https://github.com/NathanKr/highlight.js-playground/blob/main/figs/result_highlight.png" alt="Highlighted Result">
</p>
