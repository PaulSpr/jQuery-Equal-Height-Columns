jQuery-Equal-Height-Columns
===========================

A simple jQuery plugin that makes the matched elements of equal height, based on the tallest element. Very useful if you have multiple horizontally aligned elements with a background that need to be of the same height. Every elements height is usually very unpredictable, especially if the page is responsive. Fixed heights are not the answer.

Usage of this plugin is simple. You just match the elements that need to be of the same height, and the plugin does the rest. If you make a responsive website that starts as a single column layout but changes into a multi column one from a certain viewport width, you can use the minWidth option to be sure that only than the plugin is applied.


Example call:
    $('.blocks li').equalHeightColumns({
      minWidth: 500,
    	maxWidth: 1000
    });


Exmaple HTML:
    <ul class="blocks">
      <li>
    		<h2>...</h2>
    		<p>....</p>
	    </li>

    	<li>
	    	<h2>...</h2>
	    	<p>...</p>
       <p>...</p>
       <p>...</p>
    	</li>

    	<li>
    		<li>
    		<h2>...</h2>
    		<p>...</p>
       <p>...</p>
    	</li>
    </ul>


Example CSS:
    .blocks{
      list-style: none;
      width: 50%;
    	margin: 0px auto;
    	overflow: hidden;
	    margin-bottom: 20px;
    }
    .blocks li{
	    background: #eee;
	    margin: 0 1%;
	    padding: 0 2%;
	    width: 27.33333%;
	    float: left;
  }
