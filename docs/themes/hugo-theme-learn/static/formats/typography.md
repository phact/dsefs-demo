# Typography

This book includes some diagrams that are rendered 
on the client side from various graphical markup systems.

This page lets you verify that you can read the glyph and diagrams correctly. If
you do not see two of everything, then you will not be able to see some of the
diagrams in the book. In that case, please report the
[issue](https://github.com/virtualdataset/virtdata-docs/issues).

In each of the rendering checks below, the dynamically rendered element is shown
first, followed by a reference image.

### jsxgraph rendering

courtesy of [jsxgraph](http://jsxgraph.uni-bayreuth.de/wp/index.html)

<div title="dynamically rendered" align="middle">
<div id="jsxtest" class="jxgbox" style="width:250px; height:250px;"><br> </div> 
{{#jsxgraph
  var brd = JXG.JSXGraph.initBoard('jsxtest', 
   {
    boundingbox:[-10,10,10,-10], 
    keepaspectratio: true, 
    axis:true,
    showCopyright: false
   }
  ); 
  var axisx = brd.create('axis', [[0,0], [1,0]],    
  {
    firstArrow: true,
    lastArrow: true, 
    ticks: {
      drawZero: true,
      ticksDistance: 1,
      majorHeight: 30,
      tickEndings: [1,1],
      minorTicks: 0
    }  
  });
  var p = brd.create('glider', [2.2, 0, axisx], {});    
}}
</div>
<div title="reference image" align="middle">  
<img src="rendercheck/jsxgraph.png"></img> 
</div>

### Mermaid.js rendering  
 
courtesy of [mermaid.js](https://knsv.github.io/mermaid/) 

<div title="rendered dynamically" align="middle">
{{#mermaid
graph LR
A-->B
B-->C
C-->A
}} 
</div>

<div title="reference image" align="middle">
<img src="rendercheck/mermaid_abc.png"></img>
</div>

### nomnoml rendering

courtesy of [nomnoml.com](http://nomnoml.com/)

<div title="rendered dynamically" align="middle">
 {{#nomnoml
 #direction: right
 [A] -> [B]
 [B] ->  [C]
 [C] -> [A]
 }} 
</div>

<div title="reference image" align="middle">
<div><img src="rendercheck/nomnoml_abc.png"></img> 
</div>

### mathjax rendering

courtesy of [mathjax.org](https://mathjax.org)

An inline \\( \int x = \frac{x^2}{2} \\) equation, with a reference image: 
<img src="rendercheck/mathjax_inline.png"></img>. The images should match.

A block equation:

\\[ \mu = \frac{1}{N} \sum_{i=0} x_i \\]

The above equation should look like the reference image below:

<div align="middle">
<img src="rendercheck/mathjax_block.png"></img> 
</div> 