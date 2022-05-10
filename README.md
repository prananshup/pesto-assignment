# pesto-assignment

1. <strong>What is the main functionality of the browser?</strong>
<p>The primary function of a web browser is to render HTML, the code used to design or "mark up" webpages. Each time a browser loads a web page, it processes the HTML, which may include text, links, and references to images and other items, such as cascading style sheets and JavaScript functions. The browser processes these items, then renders them in the browser window.</p>

<img src="https://github.com/prananshup/pesto-assignment/blob/week1-exercise1.1/resource/images/how%20browser%20works.JPG">

2. <strong>High Level Components of a browser</strong>
<p>Primary components of a browser are</p>

<p>User Interface – This consists of forward and back button, bookmarks, address bar etc. along with the window that displays the requested page.</p>
<p>Browser engine – It commands action between rendering engine and the user interface.</p>
<p>Rendering engine – The main function of rendering engine is to display the content that is requested. For example, if an HTML content is requested, the engine parses CSS and HTML and when the content is parsed, it is displayed on the screen.</p>

3. <strong>Rendering engine and its use.</strong>
<p>When a web page is loaded, the browser first reads the HTML text and constructs DOM Tree from it. Then it processes the CSS whether that is inline, embedded, or external CSS and constructs the CSSOM Tree from it. After these trees are constructed, then it constructs the Render-Tree from it. Once the Render-Tree is constructed, then the browser starts the printing individual elements on the screen.</p>

4. <strong>Parsers (HTML, CSS, etc)</strong>
<p>HTML Parser - The job of the HTML parser is to parse the HTML markup into a parse tree.</p>
<p>Similar to HTML parsing, CSS parsing also starts by tokenizing the CSS source code into tokens, which are then parsed into CSS rules.</p>

5. <strong>Order of processing</strong>
<p>Scripts - The model of the web is synchronous. Authors expect scripts to be parsed and executed immediately when the parser reaches a <code>script</code> tag. The parsing of the document halts until the script has been executed. If the script is external then the resource must first be fetched from the network–this is also done synchronously, and parsing halts until the resource is fetched.</p>
<p>Speculative parsing - 
Both WebKit and Firefox do this optimization. While executing scripts, another thread parses the rest of the document and finds out what other resources need to be loaded from the network and loads them. In this way, resources can be loaded on parallel connections and overall speed is improved.</p>
<p>Style sheets - 
Style sheets on the other hand have a different model. Conceptually it seems that since style sheets don't change the DOM tree, there is no reason to wait for them and stop the document parsing.</p>

6. <strong>Layout and Painting</strong>
<p></p>