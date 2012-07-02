piSlideShow
===========

Jquery based Products Slideshow from all directions

#### Usage

Add jquery, jquery ui and piSlideShow.js to your html source:
  ```html
    <script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jquery/1.7.2/jquery.min.js"></script>
    <script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jqueryui/1.8.18/jquery-ui.min.js"></script>
    <script type="text/javascript" src="../js/piSlideshow.js"></script>
  ```

Your HTML may look like this:

  ```html
    <div id="pislideshow" class="slideshow">
      <ul>
	    <li>
	      <div class="main_img"><img src="myimage.jpg" width="100" height="100" /></div>
	      <div class="desc"><p> some descriptions comes here </p></div>
	    </li>
	    <li>
	      <div class="main_img"><img src="myimage.jpg" width="100" height="100" /></div>
	      <div class="desc"><p> some descriptions comes here </p></div>
	    </li>
      </ul>
    </div>
  ```
  Each `li` contains a div with class `.main_img`, this is mandatory. `.main_img` contains your product image which 
  you wish to slide. You may have as many `li`s based on the slides you wants. 
  
  Each `li` also contains description div with class name as `.desc`. This may contain any description you want to show 
  for the product. After the product sliding is over, description will automatically slide down. You must control
  positiion of desc div with your own custom style. To refer to each description div you can use class name as 
  `.slide1 .desc`, where slide1 refers to your first slide. Similarly you can have for all other slides too. 
  
When your Document is ready, call `piSlideShow` on main container of your slides. In this case it is `#pislideshow`
 ```javascript
 
 jQuery(document).ready(function(){
  var options = {
	'slideDirection' : ['right', 'bottom', 'left', 'top'],
	'slideTo' : [-200, 0, -70, -50],
  }
  $('#pislideshow').pislideshow(options);
});
 ```
### Options Explained

See demo folder for a sample.