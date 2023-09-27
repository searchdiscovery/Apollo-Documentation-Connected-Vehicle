# Apollo-Documentation-Connected-Vehicle

<h1 id="overview"><strong>Overview</strong></h1>
<p>This repository contains the necessary specifications to build an event driven data layer.</p>
<h2 id="adobe-launch-deployment">Adobe Launch Deployment</h2>
<p>The embed code is a <strong>script</strong> tag that you put on your web pages to load and execute the logic you build in Launch. If you load the library asynchronously, the browser continues to load the page, retrieves the Launch library, and executes it in parallel. In this case, there is only one embed code, which you put in the <code>&lt;head&gt;</code> (When Launch is deployed synchronously, there are two embed codes, one which you put in the <code>&lt;head&gt;</code> and another which you put before the <code>&lt;/body&gt;</code>).</p>
<!-- -->
<h3 id="implement-the-embed-code-in-the-of-the-sample-html-page">Implement the Embed Code in the of the Sample HTML Page</h3>
<p>The embed code should be implemented in the element of all HTML pages that will share the property. You might have one or several template files which control the globally across the site, making it a straightforward process to add Launch.</p>
<div class="code-block sc-cMjzQU dEWtyV"><span class="prismjs css-1xfvm4v" data-code-lang="" data-ds--code--code-block=""><code>&lt;script src="https://assets.adobedtm.com/b4c5c801023f/a766243d03d3/launch-cd46d47d77d3.min.js" async&gt;&lt;/script&gt;</code></span></div>
<p>Make sure you build a version of the library and then test that the JS file is correctly loading on the page.</p>
<p>For more information refer to the&nbsp;<a title="https://docs.adobe.com/content/help/en/core-services-learn/implementing-in-websites-with-launch/configure-launch/launch.html" href="https://docs.adobe.com/content/help/en/core-services-learn/implementing-in-websites-with-launch/configure-launch/launch.html" target="_blank" rel="noopener">official documentation</a>.</p>
<h2 id="data-layer">Data Layer</h2>
<p>Each file inside the events folder corresponds to a single use case or site event that needs to be implemented. These events are leveraged to trigger tracking rules in the tag management tool of choice and share data with the analytics reporting tool.</p>
<p>As the data layer is event-based, the order in which the events are fired is critical. In general, events should be pushed onto the data layer in the following sequence when a page load (virtual or otherwise) occurs:</p>
<p>Page Load Started &gt; <em>Other Page-level Events</em> &gt; Page Load Completed</p>
<p>If an Event is part of the page load sequence, it will be indicated in the corresponding event file.</p>
<p>Events that occur outside of the page load sequence should be pushed onto the data layer as they occur.</p>
<h2 id="questionscomments">Questions/Comments</h2>
<p>For any questions or comments, please contact mark.sawlor@searchdiscovery.com.</p>