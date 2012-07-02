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


See demo folder for a sample.