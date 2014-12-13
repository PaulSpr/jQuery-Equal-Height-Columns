jQuery-Equal-Height-Columns
===========================

A simple jQuery plugin that makes the matched elements of equal height, based on the tallest element. Very useful if you have multiple horizontally aligned elements with a background that need to be of the same height. Every elements height is usually very unpredictable, especially if the page is responsive. Fixed heights are not the answer.

Usage of this plugin is simple. You just match the elements that need to be of the same height, and the plugin does the rest. If you make a responsive website that starts as a single column layout but changes into a multi column one from a certain viewport width, you can use the minWidth option to be sure that only than the plugin is applied.


Example call:

      $('.blocks li').equalHeightColumns({
        minWidth: 500,
        maxWidth: 1000
      });


Example HTML:

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


New 1.1 options
---------------

	afterLoading: 'iframe'

'afterLoading' attaches a load event to the selector in 'afterLoading' and fires the resize code.

	afterTimeout: 500
	
'afterTimeout' takes time in miliseconds and fires the resize code after that timeout.

If you set both 'afterTimeout' and 'afterLoading' the 'afterLoading' code will also be fired after the timeout. This way you can make sure that dynamically added content (like social media related iframes) are present in the DOM.

New 1.2 options
---------------

	equalizeRows: false
	
Set this option to 'true' to equalize every row individually. This way every colum is set to the tallest column in the row which can result in every row having a different height.

	checkHeight: 'height'
	
This option determines what method to use to determine a columns height. If you use box-sizing: border-box, it might be better to set this option to innerHeight. This might become the default in a future version since it seems to work well in most cases.