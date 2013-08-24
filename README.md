<h1>Jquery Keyword Highlight Plugin</h1>

<p>The Jquery Keyword Highlight Plugin is a simple Jquery Plugin that allows you to highlight a keyword in the contents of a targeted DOM element.  Useful to supplement dynamic search results that resulted from a keyword search, or for simply highlighting keywords in a simple and fast way. </p>

<h2>Requirements</h2>
<ul>
    <li>JQuery must be loaded.</li>
</ul>

<h2>Usage</h2>
<p>Add the plugin to your &#60;head&#62; tag or before the closing &#60;body&#62; tag:</p>
<pre><code>&#60;script type="text/javascript" src="/js/jquery-keyword-highlight.js"&#62;&#60;/script&#62;
</code></pre>
<p>Add a custom CSS class to the content that you want searched and highlighted:</p>
<pre><code>&#60;div <strong>class="highlight-content"</strong>&#62;Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.&#60;/div&#62;</code></pre>
<p>Initialize and bind to the CSS class you used above on page ready, if you are not using inline data attributes, you must initialize with at least the keyword to search for:</p>
<pre><code>$(document).ready(function() { 
  $(".highlight-content").keywordHighlight({
      keyword: 'ipsum'
  });
});
</code></pre>

<h2>Configuring</h2>
<p>There are two additional <i>optional</i> configurable options on initialization in addition to the required keyword :</p>
<pre><code>$(".highlight-content").keywordHighlight({
    keyword: 'keyword',
    caseSensitive: 'false',  
    highlightClass: 'highlight'
});</code></pre>
<ul>
    <li><strong>keyword</strong> :: the keyword you are searching and highlighting.  This is required.</li>
    <li><strong>caseSensitive</strong> :: indicates if keyword search should be case sensitive,  default = false</li>
    <li><strong>highlightClass</strong> :: the class of the span tag that will surround the found keyword, default = "highlight"</li>
</ul>

<h3>Inline Data Attributes</h3>
<p>The following data attributes may be used inline and will override any initialized or default settings for that instance of the targeted content:</p>
<ul>
    <li><strong>data-keyword</strong> :: overrides the keyword setting</li>
    <li><strong>data-caseSensitive</strong> :: overrides the case sensitivity setting</li>
    <li><strong>data-highlightClass</strong> :: overrides the highlightClass setting</li>
</ul>
<p>Example:</p>
<pre><code>&#60;div class="highlight-content" data-keyword="lorem" data-caseSensitive="false" data-highlightClass="highlight-circle" &#62;Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.&#60;/div&#62;</code></pre>
<p>With the above inline data attributes, you can simpl initialize the keyword highlight plugin like:  "  $('.highlight-content').keywordHighlight(); "  The above inline attributes will then allow the keyword highlight to search for the word "lorem" without case sensitivity and give it a highlight class of "highlight-circle".</p>

<p>That's it! See <a href="http://www.ampedupdesigns.com/blog/show?bid=57">example here</a> for usage.</p>

